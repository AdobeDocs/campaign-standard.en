---
title: Get started with Sources and Destinations
description: Learn more about Adobe Experience Platform Sources and Destinations.
audience: integrating
content-type: reference
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: ba6205fa-dbcf-497a-882f-f15c00f12e68
TQID: https://experienceleague.adobe.com/r1rASYXuo-xeKH80eZVYG-jUhxy93GuTa8CIDyouSNY
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
feature_v2:
  - id: a075b2c1-7748-4328-b7f6-343aa314616a
    internal-label: Campaigns
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
---
# Get started with Sources and Destinations {#rtcdp}

## About Sources and Destinations

With Adobe Experience Platform, you can share data between Campaign Standard and Adobe Real-time Customer Data Platform (RTCDP). This allows you to target Adobe Experience Platform audiences in your Campaign workflows, then send back to Adobe Real-time Customer Data Platform data related to these audiences like sends, opens, and clicks.

* With **Destinations**, ingest audiences from Adobe Experience Platform into Campaign Standard. This allows you to activate your known and unknown data for your marketing campaigns.
* With **Sources**, export Campaign Standard data (e.g. sends, opens, clicks) into Adobe Experience Platform. This allows you to centralize data you collect from disparate sources into one single place, and use the insights gained from it to do more.


>[!IMPORTANT]
>
>Please keep in mind the SFTP storage limits, database storage limits, and active profile limits as per your Adobe Campaign contract while performing this integration.

For a more detailed overview of Adobe Real-time Customer Data Platform, Destinations and Sources, refer to these pages:

* [Adobe Real-time Customer Data Platform](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html)
* [Destinations documentation](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html)
* [Sources documentation](https://experienceleague.adobe.com/docs/experience-platform/sources/home.html)

## Connect Campaign Standard with Adobe Experience Platform

To be able to share data between Adobe Experience Platform and Campaign Standard, you first need to connect Adobe Campaign as a **Destination**, and connect your AWS S3 or Azure blob storage location as a **Source** in Adobe experience Platform.

Once the connectors have been configured, you can set up a data import or export into Campaign Standard using workflows.

![](assets/rtcdp-schema.png) 

For more details on how to setup these import and export processes, refer to these sections:

* [Ingest Adobe Experience Platform audiences into Campaign](../../integrating/using/ingest-aep-data.md)
* [Export data from Campaign to Adobe Experience Platform](../../integrating/using/export-campaign-data.md)
