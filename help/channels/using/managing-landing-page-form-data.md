---
title: Managing landing page form data
seo-title: Managing landing page form data
description: Managing landing page form data
seo-description: Learn how to manage landing page form data.
page-status-flag: never-activated
uuid: 5b222ea2-6628-457f-a618-bfc0e5eb93dd
contentOwner: lemaitre
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: landing-pages
discoiquuid: 899c7152-f415-4df9-b4b4-5ff3470a4e32
context-tags: landingPage,main
internal: n
snippet: y
---

# Managing landing page form data{#managing-landing-page-form-data}

## Changing a landing page form data properties{#changing-a-landing-page-form-data-properties}

You can link database fields to input zone, radio button or checkbox type blocks. To do this, select the block and enter the **[!UICONTROL Form data]** in the palette.

![](assets/delivery_content_9.png)

* The **Field** input zone lets you select a database field to link with the form field.
* The **Mandatory** option lets you only authorize the page's submission if the user has filled in the field. If a mandatory field is not filled in, an error message will appear.

## Mapping form fields {#mapping-form-fields}

Input fields are used to store or update data in Campaign database. For this, you need to link database fields with input zone, radio button, or checkbox type blocks. To do this:

1. Select a block in the landing page.
1. Complete the **[!UICONTROL Form data]** part in the palette.

   ![](assets/editing_lp_content_4.png)

1. Choose a database field to link with the form field in the **[!UICONTROL Field]** selection zone.

   When the **[!UICONTROL Mandatory]** option is checked, the page can only be submitted if the user has completed this field. If a mandatory field is not completed, an error message will appear when the user validates the page.

   >[!NOTE]
   >
   >Landing pages can only be mapped with **Profiles**.

1. Define the field type by choosing, for example **[!UICONTROL Text]**, **[!UICONTROL Number]**, or **[!UICONTROL Date]** in the **[!UICONTROL HTML type of the field]** selection area.

>[!NOTE]
>
>The default fields of the built-in landing pages are preconfigured. You can modify them as needed.

## Linking a form to a service {#linking-a-form-to-a-service}

You can link a form to a service so that profiles can subscribe to a specific service when validating the landing pages.

The parameters for linking a landing page allow you to specify the performed action type and whether the landing page is specifically linked to a single service or whether it is generic.

In order to select the service to link, you need to:

1. Edit the landing page properties accessed via the ![](assets/edit_darkgrey-24px.png) icon in the landing page dashboard, and display the **[!UICONTROL Job]** parameters.

   ![](assets/lp_edit_properties_button.png)

1. Choose **[!UICONTROL Subscription]** in the **[!UICONTROL Specific actions]** drop-down list.

   ![](assets/lp_parameters_5.png)

1. Select **[!UICONTROL Specific service]** to link the landing page to a single service. Do not select this option if you would like to use several services with the landing page.

   Use the **[!UICONTROL Specified service in the URL]** option to allow the landing page to be used for several services. You therefore must reference the landing page when configuring the service.

## Data storage and reconciliation{#data-storage-and-reconciliation}

Data reconciliation parameters allow you to define how the data entered in the landing page is managed once it has been submitted by a user.

To do this:

1. Edit the landing page properties accessed via the ![](assets/edit_darkgrey-24px.png) icon in the landing page dashboard, and display the **[!UICONTROL Job]** parameters.

   ![](assets/lp_parameters_4.png)

1. Select the **[!UICONTROL Reconciliation key]**: these database fields (for example: email, first name, last name) are used to determine whether the visitor has a profile that is already known in the Adobe Campaign database. This allows you to update or create a profile, according to the update strategy parameters defined.
1. Define the **[!UICONTROL Form parameter mapping]**: this section allows you to map the landing page field parameters and those used in the reconciliation key.
1. Select the **[!UICONTROL Update strategy]**: if the reconciliation key recovers an existing database profile, you can choose for this profile to be updated with the data entered in the form or instead prevent this update.
