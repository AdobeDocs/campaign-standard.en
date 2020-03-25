---
title: "Working with Campaign Standard and Microsoft Dynamics 365: Notices and recommendations"
description: Learn notices and recommendations for how to Work with Campaign Standard and Microsoft Dynamics 365
page-status-flag: never-activated
uuid: ed6c1b76-87f7-4d23-b5e2-0765297a905c
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-experience-manager
discoiquuid: 6c0c3c5b-b596-459e-87dd-a06bb7d633d2

internal: n
snippet: y
---

# Working with Campaign Standard and Microsoft Dynamics 365: Notices and recommendations

## Region support

This integration is available in the North America, EMEA and APAC regions.

If you are located in EMEA or APAC regions, some of your data will be processed in the US as part of this integration. For more information, refer to [this section](../../reporting/using/about-dynamic-reports.md#dynamic-reporting-usage-agreement).

## Source of truth for one-way contact sync

For Contact and custom entity synchronization, this integration treats Dynamics 365 as the source of truth.  Any changes to  synchronized  attributes should be done in Microsoft Dynamics 365, not Adobe Campaign Standard.  If changes are made in Campaign, they can eventually get overwritten in Campaign during synchronization, as synchronization is in one direction.  In addition, the Contacts Synchronization is designed to pull all Contact records, whether they are marked as active or inactive in Microsoft Dynamics 365.

## Managing Privacy Requests

This integration is designed to transfer end user data (including, but not limited to, personal information, if it is contained in your end user data), between Microsoft Dynamics 365 and Adobe Campaign Standard.  As a data controller, your company is responsible for complying with any privacy laws and regulations applicable to your collection and use of personal data.

For this integration, you must process each data subject request in each system independently in order for the change to be reflected in both databases. The change should first be executed in Microsoft Dynamics 365 and then in Adobe Campaign Standard. The only exception to this is that a privacy related delete request will be added to the Privacy Tools queue in Campaign Standard when a contact is deleted in Dynamics 365.

Below are links to help guide you in implementing access and/or delete privacy related requests in each system:

* [Microsoft Dynamics 365](https://docs.microsoft.com/en-us/microsoft-365/compliance/gdpr-dsr-dynamics365?toc=/microsoft-365/enterprise/toc.json)

* [Adobe Campaign Standard](https://www.adobe.io/apis/experiencecloud/gdpr/docs.html)

## Contact deletion

As Dynamics 365 is the source of truth, Contact deletions in Dynamics 365 will be reflected in Campaign.  

When a Contact is deleted in Dynamics 365, the integration queues up a privacy related delete request in the Campaign Privacy request/tools screen.  If you have disabled the 2-step process for privacy related delete requests, Campaign will take care of the deletion for you.  

However, if the 2-step process is enabled, you will need to go into the Privacy request/tools screen, after the privacy technical workflows have run, and confirm if the records are ok to be deleted.  Only then will Campaign take care of the deletion.

For more details, refer to [How to execute privacy related delete requests in Adobe Campaign Standard](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/privacy/execute-privacy-requests.html)

>[!CAUTION]
>
>If you have the 2-step process enabled for privacy requests in Campaign, your deletes in Dynamics 365 will not automatically be reflected in Campaign.  You will need to go into the Campaign Privacy request screen to confirm the deletions.

>[!NOTE]
>
>This integration creates a request using the External Id (i.e., the Dynamics 365 Contact Id) as the record/profile identifier.

## Opt-out

Due to the differences in opt-out attributes between Dynamics 365 and Campaign, and to the differences in business requirements of each customer, opt-out mapping has been left  as an exercise for the customer to complete.  It is important to ensure opt-outs are properly mapped between systems so that end user opt-out preferences are maintained, and they don’t get a communication via a channel that they have opted out of.  

Please be aware that only Campaign attributes with the “blackList” prefix (e.g., blackListEmail) or the specific attribute for CCPA opt-out can be used in opt-out mappings.  In Dynamics 365, most opt-out fields have the “doNot” prefix; however, you can also utilize custom attributes you have created for opt-out purposes if the data-types are compatible.

When provisioning the integration, you will have the opportunity to specify which opt-out configuration you require for your business:

* Dynamics 365 is source of truth for opt-outs: opt-out attributes will be synchronized in one direction from Dynamics 365 to Campaign Standard
* Campaign Standard is the source of truth for opt-outs: opt-out attributes will be synchronized in one direction from Campaign Standard to Dynamics 365
* Dynamics 365 AND Campaign Standard are both sources of truth: opt-out attributes will be synchronized bidirectionally between Campaign Standard and Dynamics 365

Follow post-provisioning instructions in the [Unifi user guide](https://drive.google.com/drive/folders/16seHF45e6bFxHX15zWLqFLEXymCuA_wn) to properly map these values.

The bidirectional opt-out configuration uses logic determine which value to write to both systems.  The logic compares timestamps between the two systems (record-level change in Dynamics 365, attribute-level change in Campaign) to determine which system prevails.  If Campaign contains the more recent timestamp, then the Campaign value prevails.  If Dynamics 365 contains the more recent timestamp or if they are equal, then opt-out=TRUE will win (assuming one of the values is TRUE).

**Opt-outs under the California Consumer Protection Act (CCPA) and similar legislation.** 

The bidirectional opt-out configuration feature is currently not able to support compliance with certain statutory requirements under the CCPA and/or other data privacy laws out of the box.. Customers who must comply with the CCPA or similar legal requirements pertaining to opt-outs are responsible for implementing their own third party solution to perform bi-directional syncs.

>[!NOTE]
>
>It is recommended that, if your company doesn’t require bidirectional opt-out support, that you select a one-direction opt-out option.

>[!NOTE]
>
>Please review and, if appropriate, update the default and specific typology rules in Adobe Campaign before making changes here to ensure that such changes are correctly applied to all outgoing communications. For example, please be sure that any mappings to opt-out preferences accurately reflect the intent/communication choices of the recipient and do not inadvertently discontinue the delivery of relationship or transactional messages such as customer order confirmations.

## Existing Campaign data

This integration will synchronize Contacts and custom entities from Dynamics 365 to Campaign. Campaign records created outside of the integration (i.e., not created by the sync job) will not be touched by the integration, including Campaign records existing at time of integration configuration.

Because this integration uses the **[!UICONTROL externalId]** field in Campaign Standard to sync Campaign profile records with Dynamics 365 Contact records, this Campaign field (**[!UICONTROL externalId]** ) must be populated with the Dynamics 365 **[!UICONTROL contactId]** for the records you wish to be synced from Dynamics 365.  Custom entities will also need to have this field present and populated correctly to maintain the sync.  Keep in mind, however, that Dynamics 365 will still be the source of truth, and that the Campaign profile data can get overwritten as the integration detects updates on the Dynamics 365 side.  There may also be other steps required to enable the integration, depending on your existing deployment; therefore, it is recommended that you work closely with your Adobe technical contact.

>[!NOTE]
>
>Due to the complexity of existing customer deployments, it is recommended that you work with your Adobe technical contact when planning and setting up the integration.
