---
title: Enriching the database
seo-title: Enriching the database
description: Enriching the database
seo-description: Learn about the various methods to enrich the database.
page-status-flag: never-activated
uuid: 71f53808-0309-49f6-a4ee-3446eac9758a
contentOwner: lemaitre
products: SG_CAMPAIGN/STANDARD
audience: start
content-type: reference
topic-tags: about-adobe-campaign
discoiquuid: d8c8a318-9433-4aec-b378-fd0beb50e9fb

internal: n
snippet: y
---

# Enriching the database{#enriching-the-database}

Campaign Standard offers several tools to help you grow your marketing database. This section details the different methods that you can use to inject data into Campaign, with references to the dedicated documentations.

## Importing data through workflows {#importing-data-through-workflows}

Workflows allow you to collect data and import it into Campaign database through the use of [**[!UICONTROL Data management]**](../../automating/using/about-data-management-activities.md) activities.

Generic information and best practices when importing data through workflows are presented in [this section](../../automating/using/importing-data.md).

Additionally, you can set up templates to import data. Using import templates is a best practice if you need to import files with the same structure on a regular basis.

You can set up two types of templates:

* **Workflow templates**: these are pre-configured workflows that you can set up once according to your needs, and reuse each time you want to import data and udpate the database.

    An example of workflow template to import data is detailed in [this section](../../automating/using/importing-data.md#example--import-workflow-template).

* **Import data templates**: like workflow templates, these are templates based on workflows, that are set up to upload files to update the database. Once configured, they are made available to users with a simplified view under the **[!UICONTROL Profile & audiences]** / **[!UICONTROL Imports]** menu.

    For more on import data templates, refer to the [dedicated documentation](../../automating/using/importing-data-with-import-templates.md).

## Collecting data from landing pages {#collecting-data-from-landing-pages}

Landing pages are web forms that can be used to collect data and create or update existing information in your database.

The principle is as follows:

* Create and design your landing page by adding input fields to collect data (first name, last name, email, etc.).
* Map each input field with the corresponding field from the database.
* Make the landing page available online via a website or through a direct link into a message.

For more on landing pages, refer to the [dedicated documentation](../../channels/using/about-landing-pages.md).

## Synchronizing profiles from Microsoft Dynamics 365

Campaign Standard integration with Microsoft Dynamics 365 allows you to pass on contact data from Microsoft Dynamics 365 to Campaign database.
These contacts are then visible in the Profiles list and can be targeted in marketing campaigns.

For more on this integration, refer to the [dedicated documentation](https://helpx.adobe.com/campaign/kb/acs-ms-dynamics.html).

>[!NOTE]
>
>Please note that Campaign Standard-Microsoft Dynamics 365 connector is currently in Limited Availability, and that it is subject to several limitations, detailed in the documentation.

## Importing data through API calls

Campaign Standard APIs allow you to perform operations to update the database like profiles or services' creation, update or deletion.

For more on how to use the APIs, refer to the [dedicated documentation](https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html).

>[!CAUTION]
>
>Before performing profiles mass creation or update via API calls, please check the scale limitations corresponding to your license agreement. For more on this, refer to [this page](https://helpx.adobe.com/legal/product-descriptions/campaign-standard.html#ITInfrastructureResourcesbyActiveProfilesTiers).
