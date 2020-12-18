---
solution: Campaign Standard
product: campaign
title: Campaign and Microsoft Dynamics 365 data management
description: Learn how Campaign Standard and Microsoft Dynamics 365 manage common data
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-ms-dynamics

---

# Manage data between Campaign and Microsoft Dynamics 365

## Source of truth for one-way sync

For contact and custom entity synchronization, this integration treats Microsoft Dynamics 365 as the source of truth.  Any changes to synchronized attributes should be done in Dynamics 365 and not in Adobe Campaign Standard).  If changes are made in Campaign, they can eventually get overwritten in Campaign during synchronization, as synchronization is in one direction. 

## Contact deletion

The integration can be optionally configured to issue profile delete calls to Campaign when a contact is deleted in Dynamics 365 to help maintain data integrity.

However, a profile delete is different than a privacy delete. A privacy delete in Campaign will remove the Campaign profile record and associated log entries; whereas, a regular profile delete will only delete the ACS profile record, leaving remnants behind in Campaign logs.

If the profile delete feature is enabled in the integration, additional steps will need to be followed to properly process data subject privacy requests. Refer to the steps in the [section below](#manage-privacy-requests).

## Privacy

### Manage privacy requests {#manage-privacy-requests}

This integration is designed to transfer end user data between Microsoft Dynamics 365 and Adobe Campaign Standard. This data includes personal information if it is contained in your end user data.  As a data controller, your company is responsible for complying with any privacy laws and regulations applicable to your collection and use of personal data.

The integration does not issue any data subject privacy (e.g., GDPR) deletes or handle any other privacy requests (with the exception of opt-out). When privacy requests, you will need to perform these independently in both Dynamics 365 and Campaign Standard.

If you have configured the integration to issue regular profile delete calls to Campaign when a contact is deleted in Dynamics 365, the steps below should be followed. Ensure no updates are made to the record in question during this process.

1. Issue privacy delete request to [Adobe Experience Platform Privacy Service](https://www.adobe.io/apis/experiencecloud/gdpr.html)

1. Monitor request until it has completed successfully

1. Verify record is no longer in your Campaign instance

1. (Soon afterward) Issue privacy delete within Dynamics 365

1. Verify record has been removed from both systems

Below are links to help guide you in implementing access and/or delete privacy related requests in each system:

* [Microsoft Dynamics 365](https://docs.microsoft.com/en-us/microsoft-365/compliance/gdpr-dsr-dynamics365?toc=/microsoft-365/enterprise/toc.json)

* [Adobe Campaign Standard](https://www.adobe.io/apis/experiencecloud/gdpr/docs.html)

### Privacy and linked resources {#privacy-linked-resources}

>[!CAUTION]
>
>If any Campaign custom resource record contains personal information, applicable to a customer’s use of Campaign, such record should be linked to a corresponding Campaign profile record (either directly or through another custom resource) so that a privacy related delete on the profile record can also delete the linked custom resource record containing personal information; the linking and deletion options between the entities must be configured to enable this cascade-like removal of the linked records. Personal information should not be entered into a custom resource that is not linked to the profile.

## Opt-out {#opt-out}

Due to the differences in opt-out attributes between Dynamics 365 and Campaign, and to the differences in business requirements of each customer, opt-out mapping has been left as an exercise for the customer to complete.  It is important to ensure opt-outs are properly mapped between systems so that end user opt-out preferences are maintained, and they don't receive a communication via a channel that they have opted out of.  

Please be aware that only the following can be used in opt-out mappings:

* Campaign attributes with the 'No longer contact by' prefix (e.g., No longer contact by email), or 

* the specific attribute for CCPA 

More information regarding Profile entity fields can be found [here](../../developing/using/datamodel-profile.md).

In Dynamics 365, most opt-out fields have the "donot" prefix, however, you can also utilize other attributes for opt-out purposes if the data-types are compatible.

When provisioning the integration, you will have the opportunity to specify which opt-out configuration you require for your business:

* Dynamics 365 is source of truth for opt-outs: opt-out attributes will be synchronized in one direction from Dynamics 365 to Campaign
* Campaign is the source of truth for opt-outs: opt-out attributes will be synchronized in one direction from Campaign to Dynamics 365
* Dynamics 365 AND Campaign are both sources of truth: opt-out attributes will be synchronized **bidirectionally** between Campaign and Dynamics 365

Alternatively, if you have a separate process to manage opt-out synchronization between the systems, the integration's opt-out data flow can be disabled.

The bidirectional opt-out configuration uses logic to determine which value to write to both systems. The logic compares timestamps between the two systems (record-level change in Dynamics 365, attribute-level change in Campaign) to determine which system prevails. If Campaign contains the more recent timestamp, then the Campaign value prevails. If Dynamics 365 contains the more recent timestamp or if they are equal, then opt-out=TRUE will win (assuming one of the values is TRUE).

>[!NOTE]
>
>Please review and, if appropriate, update the default and specific typology rules in Adobe Campaign before making changes here to ensure that such changes are correctly applied to all outgoing communications. For example, please be sure that any mappings to opt-out preferences accurately reflect the intent/communication choices of the recipient and do not inadvertently discontinue the delivery of relationship or transactional messages such as customer order confirmations.

If your selected the bidirectional or Campaign to Dynamics 365 opt-out configuration, Campaign opt-out data will be periodically exported via workflow to your Campaign SFTP storage area (see "Campaign SFTP Usage below"). In the event that your Campaign opt-out workflows stops running, you will need to manually restart as soon as possible to reduce the possibility of missed opt-out syncs.

## Campaign SFTP Usage

Your Campaign SFTP storage will need to be utilized by the integration in the opt-out use case below.  You will need to ensure that your SFTP account has adequate storage capacity to accommodate these use cases. Exceeding the licensed SFTP storage capacity may severely impair the functional use of Campaign, the integration and/or the SFTP account.

| Use case | Description |
|---|---|
| Bi-directional opt-out and Campaign to Dynamics 365 uni-directional opt-out | Bi-directional opt-out and Campaign to Dynamics 365 uni-directional opt-out data flows will utilize the Campaign SFTP storage. An ACS workflow will export incremental changes to the SFTP folder. From there, the integration will pick up the records and process. |

## Existing Campaign data

This integration will synchronize contacts and custom entities from Dynamics 365 to Campaign. Campaign records created outside of the integration (i.e., not created by the sync job) will not be modified by the integration, including Campaign records existing at time of integration configuration.

Because this integration uses the **[!UICONTROL externalId]** field in Campaign to sync Campaign profile records with Dynamics 365 contact records, this Campaign field (**[!UICONTROL externalId]** ) must be populated with the Dynamics 365 **[!UICONTROL contactId]** for the records you wish to be synced from Dynamics 365.  Custom entities are also synchronized using a Dynamics 365 unique ID. The Campaign custom entity will need to include this ID attribute as a table column. The externalId column can be used to store this attribute value, but it isn't required for Campaign custom entities.

Keep in mind, that Dynamics 365 is still the source of truth, and that the Campaign profile data can be overwritten as the integration detects updates on the Dynamics 365 side.  There may also be other steps required to enable the integration, depending on your existing deployment; therefore, it is recommended that you work closely with your Adobe technical contact.

>[!NOTE]
>
>Due to the complexity of existing customer deployments, it is recommended that you work with your Adobe technical contact when planning and setting up the integration.

## Data Sync Frequency

The integration utilizes an architecture that allows updates to be detected and added to the processing "queue" shortly after they occur in Dynamics 365 (i.e., streaming, not batch processing). For this reason, there is no need to specify data flow run frequencies or schedules.

The exception to this is the bidirectional and Campaign to Dynamics 365 opt-out data flows. For these opt-out configurations, updated ACS records are exported to SFTP via ACS workflow once per day, after which the integration tool reads the file and processes the record.

## Data usage agreement

If you are located in EMEA or APAC regions, some of your data will be processed in the US as part of this integration. For more information, refer to [this section](../../reporting/using/about-dynamic-reports.md#dynamic-reporting-usage-agreement).

## Impact on ACS Performance

>[!WARNING]
>
>Certain actions on your part (e.g., initial ingest of records, replaying of record data, etc.) could result in a large load of records being ingested from Microsoft Dynamics 365 to your Adobe Campaign Standard (ACS) instance. To reduce the risk of performance issues which may adversely impact your ACS instance, it is recommended you stop all ACS processes (e.g., no marketing activity, no running of workflows, etc.) until after the large load of records has been ingested into ACS.

## Custom entities

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