---
title: About Adobe Experience Platform Data Connector
description: Manage XDM schemas to make your Campaign Standard data available on Adobe Experience Platform.
audience: administration
content-type: reference
topic-tags: configuring-channels
feature: Microsoft CRM Integration
role: Data Architect
level: Experienced
exl-id: f4fcf256-e030-4d7b-b4b7-2448acc2ae1c
hide: yes
hidefromtoc: yes
---
# About Adobe Experience Platform Data Connector {#about-aep-data-connector}

>[!IMPORTANT]
>
>Adobe Experience Platform Data Connector is currently in beta, which may be subject to frequent updates without notice. Customers are required to be hosted on Azure (currently in beta for North America only) to access these capabilities. Please reach out to Adobe Customer Care if you would like access.

Adobe Experience Platform Data Connector helps existing customers to make their data available on Adobe Experience Platform by mapping XTK data (data ingested in Campaign) to Experience Data Model (XDM) data on Adobe Experience Platform.

Note that the connector is **uni-directional** and sends the data from Adobe Campaign Standard to Adobe Experience Platform. The data are never sent from the Adobe Experience Platform to Adobe Campaign Standard.

Adobe Experience Platform Data Connector is intended for **data engineers** who understand Adobe Campaign Standard custom resources and have an understanding of how customer's overall data schema should be inside Adobe Experience Platform.

The following sections describe the key-steps to perform a data mapping between Campaign Standard and Adobe Experience Platform. This starts with the creation of an XDM schema and a dataset.

![](assets/do-not-localize/how-to-video.png) [Discover this feature in video](#video)

>[!NOTE]
>Once Adobe Experience Platform Data Connector is configured and data is successfully ingested into Adobe Experience Platform, you need to enable the dataset so that the data is included in the Real-time Customer Profile.
>
>This can be performed either through the APIs or the Adobe Experience Platform interface. For more information, refer to the dedicated documentations:
>
>* [Enable a dataset for Real-time Customer Profile](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/datasets/dataset.html)
>* [Configure a dataset for Real-time Customer Profile and Identity Service using APIs](https://experienceleague.adobe.com/docs/experience-platform/catalog/api/getting-started.html)

## Key concepts {#key-concepts}

* Out of the Box Mapping is only available for fields which are provided in Campaign Standard by default. For ingesting all custom fields and resources, each customer needs to define their own mapping.

* Adobe Experience Platform Data Connector will push profile data through the platform at regular intervals.​ The interval duration is 15 minutes. This value can be modified using [Adobe Experience Platform APIs](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html).

* Data engineer can publish, modify and pause the mapping from Campaign to Adobe Experience Platform.

* Any targeting dimension can be mapped. The recommendation is to have one single mapping for all fields in a single targeting dimension.

* All profile updates including channel opt-ins / opt-outs are part of the batch update.

* Any Adobe Campaign Standard or XDM schema changes needs to be manually remapped.​

* Tracking log and Broadlog data are ingested automatically to Adobe Experience Platform as Experience Events. This ingestion is streamed in real-time to Adobe Experience Platform.

* Experience Cloud ID Service (ECID) is a device identifier which is sent by default with Experience Events.

    It is a unique and persistent ID assigned to a visitor, that can be used by the Platform Identity Service to identify the same visitor and their data in different Experience Cloud solutions. For more on this, refer to the [Experience Cloud Identity Service Help](https://experienceleague.adobe.com/docs/id-service/using/home.html).

    >[!NOTE]
    >
    >Be aware that, if two or more profiles share a same device, the ECID would be the same for these two profiles in the Unified Identity service.

## Limitations {#limitations}

* The out-of-the-box transfer of subscription events is not supported. To transfer subscription events, you can create corresponding XDM and dataset on Adobe Experience Platform, then configure a custom data mapping for these data.

* Regarding privacy requests (both Access and Delete actions), customers need to place separate requests via the [Privacy Core Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html#how-to-use-privacy-service-to-manage-privacy-job-requests): one for Campaign and one for Adobe Experience Platform. For more on this, see [About Privacy Requests](https://helpx.adobe.com/campaign/kb/acs-privacy.html#righttoaccess) and [Managing Privacy Requests](https://helpx.adobe.com/campaign/kb/acs-privacy.html#ManagingPrivacyRequests) in Campaign.

* For each XDM field, the DULE labeling needs to be done in Adobe Experience Platform. This is customer responsibility to apply DULE labels.

* Restrictions on marketing actions become applicable only after DULE labels are applied in Adobe Experience Platform. Before that, all data are available for all types of marketing actions.

* Every 15 minutes, the batch job is running and it identifies the records which have changed since the latest batch. If all records change at the same timestamp, a performance bottleneck could appear to manage ingestion of all profiles

## Tutorial video {#video}

This video provides an overview over the Adobe Experience Platform Data Connector.

>[!VIDEO](https://video.tv.adobe.com/v/27304?quality=12&captions=eng)

Additional videos related the Adobe Experience Platform Data Connector are available [here](https://experienceleague.adobe.com/docs/campaign-learn/campaign-standard-tutorials/administrating/adobe-experience-platform-data-connector/understanding-the-adobe-experience-platform-data-connector.html).
