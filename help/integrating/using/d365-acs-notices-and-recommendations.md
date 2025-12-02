---
title: Campaign and Microsoft Dynamics 365 data management
description: Learn how Campaign Standard and Microsoft Dynamics 365 manage common data
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-ms-dynamics

feature: Microsoft CRM Integration
old-role: Data Architect
role: Developer
level: Experienced
exl-id: aab6f005-f3da-4c0b-b856-da8504e611dc
---
# Best practices and limitations {#acs-msdyn-best-practices}

## Manage data {#acs-msdyn-manage-data}

For contact and custom entity synchronization, this integration treats **Microsoft Dynamics 365 as the source of truth**.  Any changes to synchronized attributes should be done in Dynamics 365 and not in Adobe Campaign Standard).  If changes are made in Campaign, they can eventually get overwritten in Campaign during synchronization, as synchronization is in one direction. 

The integration can be optionally configured to issue profile delete calls to Campaign when a contact is deleted in Dynamics 365 to help maintain data integrity. However, a profile delete is different than a privacy delete. A privacy delete in Campaign will remove the Campaign profile record and associated log entries; whereas, a regular profile delete will only delete the Campaign profile record, leaving remnants behind in Campaign logs. If the profile delete feature is enabled in the integration, additional steps will need to be followed to properly process data subject privacy requests. Refer to the steps in the [Privacy section below](#manage-privacy-requests).

## Privacy{#acs-msdyn-manage-privacy}

This integration is designed to transfer end user data between Microsoft Dynamics 365 and Adobe Campaign Standard. This data includes personal information if it is contained in your end user data.  As a data controller, your company is responsible for complying with any privacy laws and regulations applicable to your collection and use of personal data.

This integration is designed to transfer end user data (including, but not limited to, personal information, if it is contained in your end user data), between Microsoft Dynamics 365 and Adobe Campaign Standard. As a data controller, your company is responsible for complying with any privacy laws and regulations applicable to your collection and use of personal data.

The integration does not issue any data subject privacy (e.g., GDPR) deletes or handle any other privacy requests (with the exception of opt-out). When processing privacy requests, you should do so in both Microsoft Dynamics 365 and Campaign (via the Adobe Experience Platform Privacy Service), independently.

If you have configured the integration to issue regular profile delete calls to Campaign when a contact is deleted in Dynamics 365, the steps below should be followed. Ensure no updates are made to the record in question during this process.

1. Issue privacy delete request to [Adobe Experience Platform Privacy Service](https://developer.adobe.com/experience-platform-apis/references/privacy-service)

1. Monitor request until it has completed successfully

1. Verify record is no longer in your Campaign instance

1. (Soon afterward) Issue privacy delete within Dynamics 365

1. Verify record has been removed from both systems


>[!IMPORTANT]
>
>If any Campaign custom resource record contains personal information, applicable to a customer’s use of Campaign, such record should be linked to a corresponding Campaign profile record (either directly or through another custom resource) so that a privacy related delete on the profile record can also delete the linked custom resource record containing personal information; the linking and deletion options between the entities must be configured to enable this cascade-like removal of the linked records. Personal information should not be entered into a custom resource that is not linked to the profile.

## Opt-out {#opt-out}

Due to the differences in opt-out attributes between Microsoft Dynamics 365 and Campaign, and to the differences in business requirements of each customer, opt-out mapping has been left as an exercise for the customer to complete.  It is important to ensure opt-outs are properly mapped between systems so that end user opt-out preferences are maintained, and they don't receive a communication via a channel that they have opted out of.  

Please be aware that only the following can be used in opt-out mappings:

* Campaign attributes with the 'No longer contact by' prefix (e.g., No longer contact by email), or 

* the specific attribute for CCPA 

More information regarding Profile entity fields can be found [here](../../developing/using/datamodel-profile.md).

In Dynamics 365, most opt-out fields have the "donot" prefix, however, you can also utilize other attributes for opt-out purposes if the data-types are compatible.

When provisioning the integration, you will have the opportunity to specify which opt-out configuration you require for your business:

* **Unidirectional (Microsoft Dynamics 365 to Campaign)**: Dynamics 365 is source of truth for opt-outs. Opt-out attributes will be synchronized in one direction from Dynamics 365 to Campaign Standard
* **Unidirectional (Campaign to Microsoft Dynamics 365)**: Campaign Standard is the source of truth for opt-outs. Opt-out attributes will be synchronized in one direction from Campaign Standard to Dynamics 365
* **Bidirectional**: Dynamics 365 AND Campaign Standard are both sources of truth. Opt-out attributes will be synchronized bi-directionally between Campaign Standard and Dynamics 365

Alternatively, if you have a separate process to manage opt-out synchronization between the systems, the integration's opt-out data flow can be disabled.

The bidirectional opt-out configuration uses logic to determine which value to write to both systems. The logic compares timestamps between the two systems (record-level change in Dynamics 365, attribute-level change in Campaign) to determine which system prevails. If Campaign contains the more recent timestamp, then the Campaign value prevails. If Dynamics 365 contains the more recent timestamp or if they are equal, then opt-out=TRUE will win (assuming one of the values is TRUE).

Learn how to select opt-in/out options in [this section](../../integrating/using/d365-acs-self-service-app-data-sync.md#opt-in-out-wf).

>[!NOTE]
>
>Please review and, if appropriate, update the default and specific typology rules in Adobe Campaign before making changes here to ensure that such changes are correctly applied to all outgoing communications. For example, please be sure that any mappings to opt-out preferences accurately reflect the intent/communication choices of the recipient and do not inadvertently discontinue the delivery of relationship or transactional messages such as customer order confirmations.

If you selected the **Bidirectional** or **Unidirectional (Campaign to Microsoft Dynamics 365)** opt-out configuration, Campaign opt-out data will be periodically exported via workflow to your Campaign SFTP storage area (see "Campaign SFTP Usage below"). In the event that your Campaign opt-out workflows stops running, you will need to manually restart as soon as possible to reduce the possibility of missed opt-out syncs.

>[!IMPORTANT]
>
>If you require the **Bidirectional** or **Unidirectional (Campaign to Microsoft Dynamics 365)** opt-out configuration, you will need to make the request to your Adobe technical contact for the opt-out workflows to be set up on your Campaign instance

## Campaign SFTP Usage

Your Campaign SFTP storage will need to be utilized by the integration in the use cases below.  You will need to ensure that your SFTP account has adequate storage capacity to accommodate these use cases. Exceeding the licensed SFTP storage capacity may severely impair the functional use of Campaign, the integration and/or the SFTP account.

| Use case | Description |
|---|---|
| Bidirectional and Unidirectional (Campaign to Microsoft Dynamics 365) | Bidirectional and Unidirectional (Campaign to Microsoft Dynamics 365) opt-out data flows will utilize the Campaign SFTP storage. A Campaign workflow will export incremental changes to the SFTP folder. From there, the integration will pick up the records and process. |
| Opt-out logs | Output logs from the connector will be helpful when troubleshooting the integration. Output logs can be toggled on/off. |


>[!IMPORTANT]
>
>You are responsible for the information you access and download from the SFTP folders. If the information contains personal data, you are responsible for complying with any applicable privacy laws and regulations. [Learn more](#acs-msdyn-manage-privacy).

## Data management

### Existing Campaign data

This integration will synchronize contacts and custom entities from Microsoft Dynamics 365 to Campaign. Campaign records created outside of the integration (i.e., not created by the sync job) will not be modified by the integration, including Campaign records existing at time of integration configuration.

Because this integration uses the **[!UICONTROL externalId]** field in Campaign to sync Campaign profile records with Dynamics 365 contact records, this Campaign field (**[!UICONTROL externalId]** ) must be populated with the Microsoft Dynamics 365 **[!UICONTROL contactId]** for the records you wish to be synced from Microsoft Dynamics 365.  Custom entities are also synchronized using a Microsoft Dynamics 365 unique ID. The Campaign custom entity will need to include this ID attribute as a table column. The externalId column can be used to store this attribute value, but it isn't required for Campaign custom entities.

Keep in mind, that Microsoft Dynamics 365 is still the source of truth, and that the Campaign profile data can be overwritten as the integration detects updates on the Dynamics 365 side.  There may also be other steps required to enable the integration, depending on your existing deployment; therefore, it is recommended that you work closely with your Adobe technical contact.

>[!NOTE]
>
>Due to the complexity of existing customer deployments, it is recommended that you work with your Adobe technical contact when planning and setting up the integration.

### Data Sync Frequency

The integration utilizes an architecture that allows updates to be detected and added to the processing "queue" shortly after they occur in Microsoft Dynamics 365 (i.e., streaming, not batch processing). For this reason, there is no need to specify data flow run frequencies or schedules.

The exception to this is the bidirectional and Campaign to Dynamics 365 opt-out data flows. For these opt-out configurations, updated Campaign records are exported to SFTP via a Campaign workflow once per day, after which the integration tool reads the file and processes the record.

### Data usage agreement

If you are located in EMEA or APAC regions, some of your data will be processed in the US as part of this integration. For more information, refer to [this section](../../reporting/using/about-dynamic-reports.md#dynamic-reporting-usage-agreement).

## Guardrails and limitations

>[!IMPORTANT]
>
>Certain actions on your part (e.g., initial ingest of records, replaying of record data, etc.) could result in a large load of records being ingested from Microsoft Dynamics 365 to your Adobe Campaign instance. To reduce the risk of performance issues, it is recommended you stop all Campaign processes (e.g., no marketing activity, no running of workflows, etc.) until after the large load of records has been ingested into Campaign.

### Custom entities

The [Microsoft Dynamics 365-Adobe Campaign Standard integration](../../integrating/using/d365-acs-get-started.md) supports custom entities, enabling custom entities in Dynamics 365 to be synchronized to corresponding custom resources in Campaign.

The integration supports both linked and non-linked tables.

When configuring custom entity data flows, it is important to be aware of the following:

* Creating and modifying Campaign custom resources are sensitive operations which must be performed by expert users only.
* For custom entity data flows, change tracking must be enabled within Dynamics 365 for synchronized custom entities.
* If a parent and linked child record are created close to the same time in Dynamics 365, due to the parallel processing of the integration, there is a slight chance that a new child record could be written to Campaign before its parent record.

* If the parent and child are linked on the Campaign side using the **1 cardinality simple link** option, the child record will remain hidden and inaccessible (via UI or API) until the parent record arrives in Campaign.

* (Assuming **1 cardinality simple link** in Campaign) If the child record is updated or deleted in Dynamics 365, and that change is written to Campaign before the parent record shows up in Campaign (not likely, but a remote possibility), that update or delete will not be processed in Campaign and an error will be thrown. In the case of update, the record in question will need to be updated in Dynamics 365 again in order to sync the updated record. In the case of delete, the record in question will need to be taken care of separately on the Campaign side since there is no longer a record in Dynamics 365 to delete or update.

* If you run into a situation where you believe you have hidden child records and no way to access them, you can temporarily change the cardinality link type to **0 or 1 cardinality simple link** to access those records.

A more comprehensive overview of Campaign custom resources can be found [in this section](../../developing/using/key-steps-to-add-a-resource.md).

### Integration Guardrails

The following guardrails should be taken into consideration when planning to use this integration. Consult with your Adobe technical representative if you believe you exceed these guardrails.

* You will need to license the proper Campaign package to support the engine call volume generated by the integration. Exceeding the licensed engine call volume could cause a degradation in Campaign performance.

    Use the following to help estimate the engine call volume from the integration:

    * Record inserts (i.e., new record): 1 engine call
    * Record deletes: 1 engine call
    * Record updates: 2 engine calls (only 1 call if the destination record is identical to the source record – i.e., if no change to the Campaign record)

    When estimating overall Campaign engine call volume, it is important to factor in other sources of engine calls, including landing pages, WebApps, JSSP, APIs, mobile app registrations, etc.
    
    View Adobe Campaign Standard package information here: [https://helpx.adobe.com/legal/product-descriptions/campaign-standard.html](https://helpx.adobe.com/legal/product-descriptions/campaign-standard.html)
    
* The integration supports a maximum of 15 million total records for the initial sync to resources in Campaign. Incremental sync is limited by the Adobe Campaign Standard package.

* The standard integration offering includes support for up to twenty custom entities, each with a max of 50 columns in size.

* You will need to create and publish your custom resources before implementing the integration.

* The maximum table depth when linking tables is two (i.e., table1->table2->table3)

* The integration supports up to 5 linked columns per custom resource. Linking multiple columns between custom resources can have dramatic performance impacts. **0 or 1 cardinality simple link** is preferred over **1 cardinality simple link**.

* The integration supports transformation between primitive Microsoft Dynamics 365 data types (Boolean, Integer, Decimal, Double, String, DateTime, Date) and Adobe Campaign Standard data types (integer, boolean, float, double, date, datetime, string). More advanced data types are interpreted as strings and are synced as is.

* Onboarding maintenance windows may need to be established between Adobe and the customer.

* Be aware that significant increases or “spikes” in usage of the integration (e.g., sharp increase in new or updated records) may cause slowdowns in data syncing.

* As part of the integration, you will be expected to complete the pre-integration configuration steps in Microsoft Azure and Dynamics 365. See the configuration steps [on this page](../../integrating/using/d365-acs-configure-d365.md)

* It is expected that you will bring your Dynamics 365 and Campaign data models to the integration and will maintain them.

### Integration boundaries

The integration was designed to solve the general use case of common data movement between Microsoft Dynamics 365 and Campaign, but it is not intended to address every use case specific to each customer:

* The integration does not issue any privacy (e.g., GDPR) deletes. The responsibility of fulfilling end-user privacy requests rests with the customer; such requests should be made in both Campaign (via the Adobe Experience Platform Privacy Service) and Dynamics 365 independently. The integration can issue regular deletes to help with data synchronization, if desired.   Review [the Privacy section](#manage-privacy-requests) for more information.

* No profile or custom entity data will be synchronized from Campaign to Dynamics 365, with the exception of opt-out information (if configured by the customer).

* Campaign subscription management (i.e., subscribes/unsubscribes) is not natively supported.

* Composing and triggering Campaign email campaigns from within Dynamics 365 is not supported.

* The integration does **not** support the remodeling of data between the Dynamics 365 and Campaign Standard data models. It is expected that the integration will be syncing one Dynamics 365 table to one Campaign table.
