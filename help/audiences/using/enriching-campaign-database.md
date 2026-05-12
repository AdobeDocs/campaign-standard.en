---
title: Enriching the database
description: Learn about the various methods to enrich the database.
audience: start
content-type: reference
topic-tags: about-adobe-campaign
feature: Profiles
role: User
level: Intermediate
exl-id: 9c55a8b3-034e-4319-8a88-7b59e83fa458
TQID: https://experienceleague.adobe.com/LROFX17EE6zvJRbH4P--NjtiJLwanqeudAKzwnQj0BI
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
feature_v2:
  - id: a075b2c1-7748-4328-b7f6-343aa314616a
    internal-label: Campaigns
  - id: b12f6872-9271-4369-85e5-86969a0b99a2
    internal-label: APIs
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
    internal-label: Data management
---
# Enriching the database{#enriching-the-database}

Campaign Standard offers several tools to help you grow your marketing database. This section details the different methods that you can use to inject data into Campaign, with references to the dedicated documentations.

## Importing data through workflows {#importing-data-through-workflows}

Workflows allow you to collect data and import it into Campaign database through the use of [[!UICONTROL Data management]](../../automating/using/about-data-management-activities.md) activities.

Generic information and best practices when importing data through workflows are presented in [this section](../../automating/using/about-data-import-and-export.md).

Additionally, you can set up templates to import data. Using import templates is a best practice if you need to import files with the same structure on a regular basis.

You can set up two types of templates:

* **Workflow templates**: these are pre-configured workflows that you can set up once according to your needs, and reuse each time you want to import data and update the database.

    An example of workflow template to import data is detailed in [this section](../../automating/using/creating-import-workflow-templates.md).

* **Import data templates**: like workflow templates, these are templates based on workflows, that are set up to upload files to update the database. Once configured, they are made available to users with a simplified view under the **[!UICONTROL Profile & audiences]** / **[!UICONTROL Imports]** menu.

    For more on import data templates, refer to the [dedicated documentation](../../automating/using/importing-data-with-import-templates.md).

## Collecting data from landing pages {#collecting-data-from-landing-pages}

Landing pages are web forms that can be used to collect data and create or update existing information in your database.

The principle is as follows:

* Create and design your landing page by adding input fields to collect data (first name, last name, email, etc.).
* Map each input field with the corresponding field from the database.
* Make the landing page available online via a website or through a direct link into a message.

For more on landing pages, refer to the [dedicated documentation](../../channels/using/getting-started-with-landing-pages.md).

## Synchronizing profiles from Microsoft Dynamics 365

Campaign Standard integration with Microsoft Dynamics 365 allows you to pass on contact data from Microsoft Dynamics 365 to Campaign database.
These contacts are then visible in the Profiles list and can be targeted in marketing campaigns.

For more on this integration, refer to the [dedicated documentation](../../integrating/using/d365-acs-get-started.md).

>[!NOTE]
>
>Please note that Campaign Standard-Microsoft Dynamics 365 connector is currently in Limited Availability, and that it is subject to several limitations, detailed in the documentation.

## Importing data through API calls

Campaign Standard APIs allow you to perform operations to update the database like profiles or services' creation, update or deletion.

For more on how to use the APIs, refer to the [dedicated documentation](../../api/using/get-started-apis.md).

>[!IMPORTANT]
>
>Before performing profiles mass creation or update via API calls, please check the scale limitations corresponding to your license agreement. For more on this, refer to [this page](https://helpx.adobe.com/legal/product-descriptions/campaign-standard.html#ITInfrastructureResourcesbyActiveProfilesTiers).
