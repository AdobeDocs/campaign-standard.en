---
title: About Data Mapping
description: Manage XDM schemas to make your Campaign Standard data available on Adobe Experience Platform.
page-status-flag: never-activated
uuid: 867b1c4b-4c79-4c52-9d0a-ef71993e50a2
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: configuring-channels
discoiquuid: 406c955a-b2d2-4099-9918-95f5fa966067

internal: n
snippet: y
---

# About Data Mapping {#about-data-mapping}

>[!IMPORTANT]
>
>Campaign Standard Data service is currently in beta, which may be subject to frequent updates without notice. Customers are required to be hosted on Azure (currently in beta for North America only) to access these capabilities. Please reach out to Adobe Customer Care if you would like access.

Adobe Campaign Standard is available on Adobe Experience Platform - Data Mapping for all customers with an access to Adobe Experience Platform. The Data Mapping features help existing customers to make their data available on Adobe Experience Platform by mapping XTK data (data ingested in Campaign) to Experience Data Model (XDM) data on Adobe Experience Platform.

The mapping feature is intended for data engineers who understand Adobe Campaign Standard custom resources and have an understanding of how customer's overall data schema should be inside Adobe Experience Platform.

The following sections describe the key-steps to perform a data mapping between Campaign Standard and Adobe Experience Platform. This starts with the creation of an XDM schema and a dataset.

>[!NOTE]
>Once data mapping is configured and data is successfullly ingested into Adobe Experience Platform, you need to enable the dataset so that the data is included in the Real-time Customer Profile.
>
>This can be performed either through the APIs or the Adobe Experience Platform interface. For more information, refer to the dedicated documentations:
>
>* [Enable a dataset for Real-time Customer Profile](https://www.adobe.io/apis/experienceplatform/home/tutorials/alltutorials.html#!api-specification/markdown/narrative/tutorials/data_ingestion_tutorial/data_ingestion_tutorial.md)
>* [Configure a dataset for Real-time Customer Profile and Identity Service using APIs](https://www.adobe.io/apis/experienceplatform/home/tutorials/alltutorials.html#!api-specification/markdown/narrative/tutorials/unified_profile_dataset_tutorial/unified_profile_dataset_api_tutorial.md)

## Key concepts {#key-concepts}

* Out of the Box Mapping is only available for fields which are provided in Campaign Standard by default. For ingesting all custom fields and resources, each customer needs to define his own mapping.

* This process is single tenant and it needs to be deployed on each Adobe Campaign Standard instance​.

* The service will push profile data through the platform at regular intervals.​ The interval duration is 15 mn. This value is not modifiable.

* Data engineer can publish, modify and pause the mapping from Campaign to Adobe Experience Platform.
* *Any targeting dimension can be mapped. The recommendation is to have one single mapping for all fields in a single targeting dimension.

* All profile updates including channel opt-ins / opt-outs are part of the batch update.
The service is uni-directional and sends the data from Adobe Campaign Standard to Adobe Experience Platform. The data are never sent from the Adobe Experience Platform to Adobe Campaign Standard.

* Any Adobe Campaign Standard or XDM schema changes needs to be manually remapped.​

* Tracking log and Broadlog data are ingested automatically to Adobe Experience Platform as Experience Events. This ingestion is streamed real-time to Adobe Experience Platform.

## Limitations {#limitations}

* The out-of-the-box transfer of subscription events is not supported. To transfer subscription events, you can create corresponding XDM and dataset on Adobe Experience Platform, then configure a custom data mapping for these data.

* Existing experience events cannot be ingested into Adobe Experience Platform, but ongoing generated experience events will be streamed to Adobe Experience Platform.Data engineer cannot manually stop/pause ingestion of tracking log and broadlog data to Adobe Experience Platform.

* Regarding GDPR Requests, customers need to place separate requests for Campaign Standard and Adobe Experience Platform for both access and delete actions.

* For each XDM field, the DULE labeling needs to be done in Adobe Experience Platform. This is customer responsibility to apply DULE labels. 

* Restrictions on marketing actions become applicable only after DULE labels are applied in Adobe Experience Platform. Before that, all data are available for all types of marketing actions.

* Every 15 minutes, the batch job is running and it identifies the records which have changed since the latest batch. If all records change at the same timestamp, a performance bottleneck could appear to manage ingestion of all profiles
