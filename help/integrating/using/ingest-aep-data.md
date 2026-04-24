---
title: Ingest Adobe Experience Platform audiences into Campaign
description: Learn how to ingest Adobe Experience Platform audiences into Campaign Standard.
audience: integrating
content-type: reference
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: 5c266c44-535b-4954-862d-74c83a6f6406
TQID: https://experienceleague.adobe.com/LdVWEXa90p4yOKgPGG5LUOGRk3xWE8kJ8SkKM7ODBXk
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
feature_v2:
  - id: a658c786-869b-4194-a780-2594d663adda
    internal-label: Data management
subfeature_v2:
  - id: b70f632b-2cfd-43d0-9266-284281100d70
    internal-label: Data import and export
  - id: fcb46c0f-76e1-48bc-9dd0-fcf9d97526cf
    internal-label: Workflows
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
    internal-label: Data management
---
# Ingest Adobe Experience Platform audiences into Campaign {#destinations}

To ingest Adobe Experience Platform audiences into Campaign and use them in your workflows, you first need to connect Adobe Campaign as an Adobe Experience Platform **Destination** and configure it with the segment to export.

Once the Destination has been configured, data will be exported to your storage location, and you will need to build a dedicated workflow in Campaign Standard to ingest it.

## Connect Adobe Campaign as a Destination

In Adobe Experience platform, configure a connection with Adobe Campaign by selecting a storage location for the exported segments. This steps also allows you to select the segments to export and specify additional XDM fields to include.

For more on this, refer to the [Destinations documentation](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/email-marketing/adobe-campaign.html).

After the Destination has been configured, Adobe Experience Platform creates a tab-delimited .txt or .csv file in the storage location that you provided. This operation is scheduled and performed once per 24h.

You can now configure a Campaign Standard workflow to ingest the segment into Campaign.

## Create an import workflow in Campaign Standard

Once Campaign Standard has been configured as a Destination, you need to build a dedicated workflow to import the file that has been exported by Adobe Experience Platform.

To do this, you need to add and configure a **[!UICONTROL Transfer file]** activity. For more on how to configure this activity, refer to [this section](../../automating/using/transfer-file.md).

   ![](assets/rtcdp-transfer-file.png)

You can then build your workflow according to your needs (update the database using the segment data, send a cross-channel deliveries to the segment, etc.)

As an example, the workflow below downloads the file from your storage location on a daily basis, then updates Campaign database with the segment data.

   ![](assets/rtcdp-workflow.png)

Examples of data management workflows are available in the [workflows use cases](../../automating/using/about-workflow-use-cases.md#management) section.

Related topics:

* [Data management activities](../../automating/using/about-data-management-activities.md)
* [About data import and export](../../automating/using/about-data-import-and-export.md)
