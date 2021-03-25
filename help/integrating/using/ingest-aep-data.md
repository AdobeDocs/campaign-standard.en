---
solution: Campaign Standard
product campaign
title: Ingest Adobe Experience Platform segments into Campaign
description: Learn how to ingest Adobe Experience Platform segments into Campaign Standard.
audience: integrating
content-type: reference

feature: Triggers
role: Data Architect
level: Intermediate
---

# Ingest Adobe Experience Platform segments into Campaign {#destinations}

To ingest Adobe Experience Platform into Campaign and use them in your workflows, you first need to connect a **Destination** to Adobe Campaign and configure it with the segment to export.

>[!NOTE]
>
>When ingesting the segment, you are exporting all its members, together with the XDM schema fields specified when configuring the Destination.

Once the Destination has been configured and the segment to export selected, you need to build a dedicated workflow in Campaign Standard to ingest the segment.

## Connect and configure a Destination to Adobe Campaign

The main steps to connect and configure a Destination to Adobe Campaign are listed below. Detailed information on each of these steps is available in the [Destinations documentation](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/email-marketing/adobe-campaign.html).

1. In Adobe Experience platform **[!UICONTROL Destinations]** menu, configure a connection with Adobe Campaign by authenticating and selecting a storage location for the exported segments.

    >[!NOTE]
    >
    >The storage location can be Amazon S3, SFTP with Password, SFTP with SSH Key, or Azure Blob connections. The preferred method to send data to Adobe Campaign is through Amazon S3 or Azure Blob.

1. Activate the segments to export with the Destination. This steps allows you to configure the segment to export. You can also specify additional XDM fields to include.

1. Once the Destination is configured, Adobe Experience Platform creates a tab-delimited .txt or .csv file in the storage location that you provided. You can now configure a Campaign Standard workflow to ingest the segment into Campaign.

## Create an import workflow in Campaign Standard


