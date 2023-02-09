---
title: Customizing lists
description: "Learn how to customize display and act on list screens in Adobe Campaign Standard:sorting, filtering, deleting or duplicating elements. Lists screens display elements of one or several given resources."
audience: start
content-type: reference
topic-tags: discovering-the-interface
---

# Working with profiles & audiences

<table>
<tr>
    <td valign="top">
        <a href="../../start/using/work-with-audiences.md"><img width="60px" alt="conditions" src="assets/icon_profile.svg"/></a>
    </td>
    <td valign="top">
        <a href="../../api/using/creating-a-service.md"><img width="60px" alt="conditions" src="assets/icon_profile.svg"/></a>
    </td>
    <td valign="top">
        <a href="../../api/using/interacting-with-custom-resources.md"><img width="60px" alt="conditions" src="assets/icon_profile.svg"/></a>
    </td>
    <td valign="top">
        <a href="../../api/using/interacting-with-marketing-history.md"><img width="60px" alt="conditions" src="assets/icon_profile.svg"/></a>
    </td>
</tr>
<tr>
<td>Customer profiles</td>
<td>Enriching your database</td>
<td>Organize your audiences</td>
<td>Privacy management</td>
</tr>
</table>

## Customer profiles {#customer-profiles}

<img width="60px" alt="conditions" src="assets/icon_profile.svg"/>

Adobe Campaign profiles represent all of the contacts stored in the database. Each profile corresponds to one entry in the database which contains the necessary information for that profile to be targeted, qualified and individually tracked. This means that a profile can be: a client, a prospect, an individual subscribed to a newsletter, a recipient, a user, or any other denomination depending on the organization.

**Read more**

* [About profiles](../../audiences/using/about-profiles.md)
* [Accessing the number of Active Profiles in your organization](../../audiences/using/active-profiles.md)

## Enriching your database {#populating-database}

<img width="60px" alt="conditions" src="assets/icon_populate.svg"/>

Campaign Standard offers several tools to help you grow your marketing database. This section details the different methods that you can use to inject data into Campaign, with references to the dedicated documentations.

### Importing data through workflows {#importing-data-through-workflows}

Workflows allow you to collect data and import it into Campaign database through the use of [**[!UICONTROL Data management]**](../../automating/using/about-data-management-activities.md) activities. Generic information and best practices when importing data through workflows are presented in [this section](../../automating/using/about-data-import-and-export.md).

Additionally, you can set up templates to import data. Using import templates is a best practice to import files with the same structure on a regular basis. You can set up two types of templates:

* **Workflow templates**: these are pre-configured workflows that you can set up once according to your needs, and reuse each time you want to import data and udpate the database. An example of workflow template to import data is detailed in [this section](../../automating/using/creating-import-workflow-templates.md).

* **Import data templates**: like workflow templates, these are templates based on workflows, that are set up to upload files to update the database. Once configured, they are made available to users with a simplified view under the **[!UICONTROL Profile & audiences]** / **[!UICONTROL Imports]** menu. For more on import data templates, refer to the [dedicated documentation](../../automating/using/importing-data-with-import-templates.md).

### Collecting data from landing pages {#collecting-data-from-landing-pages}

Landing pages are web forms that can be used to collect data and create or update existing information in your database. The principle is as follows:

* Create and design your landing page by adding input fields to collect data (first name, last name, email, etc.).
* Map each input field with the corresponding field from the database.
* Make the landing page available online via a website or through a direct link into a message.

For more on landing pages, refer to the [dedicated documentation](../../channels/using/getting-started-with-landing-pages.md).

**Read more**

* xxxx
* xxxx

### Synchronizing profiles from Microsoft Dynamics 365

Campaign Standard integration with Microsoft Dynamics 365 allows you to pass on contact data from Microsoft Dynamics 365 to Campaign database.
These contacts are then visible in the Profiles list and can be targeted in marketing campaigns. For more on this integration, refer to the [dedicated documentation](../../integrating/using/d365-acs-get-started.md).

>[!NOTE]
>
>Please note that Campaign Standard-Microsoft Dynamics 365 connector is currently in Limited Availability, and that it is subject to several limitations, detailed in the documentation.

**Read more**

* xxxx
* xxxx

### Importing data through API calls

Campaign Standard APIs allow you to perform operations to update the database like profiles or services' creation, update or deletion. For more on how to use the APIs, refer to the [dedicated documentation](../../api/using/get-started-apis.md).

>[!CAUTION]
>
>Before performing profiles mass creation or update via API calls, please check the scale limitations corresponding to your license agreement. For more on this, refer to [this page](https://helpx.adobe.com/legal/product-descriptions/campaign-standard.html#ITInfrastructureResourcesbyActiveProfilesTiers).

**Read more**

* xxxx
* xxxx

## Organizing your audiences {#organizing-audiences}

<img width="60px" alt="conditions" src="assets/icon_audience.svg"/>

To enable you to deliver relevant and effective messages, and engage your customers effectively, Adobe Campaign integrates advanced analysis and targeting functionalities.

Thanks to the workflows and the query editor, you can build audiences that will be targeted by your different campaigns, depending on the information that you have on them, their activities, their language, their preferences or their marketing history. This allows you to filter subscribed profiles for example, or create target audiences on an unlimited number of criteria.

**Read more**

* [About audiences](../../audiences/using/about-audiences.md)
* [Creating audiences](../../audiences/using/creating-audiences.md)

## Privacy management {#privacy-management}

<img width="60px" alt="conditions" src="assets/icon_privacy.svg"/>

GDPR is the European Union’s (EU) new privacy law that harmonizes and modernizes data protection requirements. GDPR applies to Adobe Campaign customers who hold data for Data Subjects residing in the EU. In addition to the privacy capabilities already available in Adobe Campaign (including consent management, data retention settings, and user roles), we are taking this opportunity in our role as a Data Processor to include additional capabilities, to help facilitate your readiness as a Data Controller for certain GDPR requests.

Refer to [this section](../../start/using/privacy.md) to learn more about the tools and functionalities that Adobe Campaign provides to help you become GDPR compliant.

**Read more**

* xxxx
* xxxx