---
solution: Campaign Standard
product: campaign
title: Managing landing page form data
description: Learn how to manage landing page form data.
audience: channels
content-type: reference
topic-tags: landing-pages
context-tags: landingPage,main
feature: Landing Pages
role: Business Practitioner
level: Intermediate
exl-id: 7083447c-4cac-41cb-8453-369819e0c7c1
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

1. Choose a database field to link with the form field in the **[!UICONTROL Field]** selection zone. Landing pages can only be mapped with **Profiles**.

1. Check the **[!UICONTROL Mandatory]** option if needed. The page can only be submitted if the user has completed this field. If a mandatory field is not completed, an error message will appear when the user validates the page.

1. Define the field type by choosing, for example **[!UICONTROL Text]**, **[!UICONTROL Number]**, or **[!UICONTROL Date]** in the **[!UICONTROL HTML type of the field]** selection area.
   If you choose a mandatory **[!UICONTROL Checkbox]**, make sure that it is of **[!UICONTROL Field]** type.

>[!NOTE]
>
>The default fields of the built-in landing pages are preconfigured. You can modify them as needed.

## Data storage and reconciliation{#data-storage-and-reconciliation}

Data reconciliation parameters allow you to define how the data entered in the landing page is managed once it has been submitted by a user.

To do this:

1. Edit the landing page properties accessed via the ![](assets/edit_darkgrey-24px.png) icon in the landing page dashboard, and display the **[!UICONTROL Job]** parameters.

   ![](assets/lp_parameters_4.png)

1. Select the **[!UICONTROL Reconciliation key]**: these database fields (for example: email, first name, last name) are used to determine whether the visitor has a profile that is already known in the Adobe Campaign database. This allows you to update or create a profile, according to the update strategy parameters defined.
1. Define the **[!UICONTROL Form parameter mapping]**: this section allows you to map the landing page field parameters and those used in the reconciliation key.
1. Select the **[!UICONTROL Update strategy]**: if the reconciliation key recovers an existing database profile, you can choose for this profile to be updated with the data entered in the form or instead prevent this update.

## Workaround to Safelink issue

It is now possible to add a checkbox corresponding to a drop-down list where an element from the list is not mapped to a field of the Campaign database, and this element is "mandatory" by default (and you cannot change this).

Thanks to this new feature, this mandatory checkbox enables the user to agree before before proceeding with subscription or unsubscription. Otherwise the user is automatically subscribed or unsubscribed (without confirmation) when the landing page is displayed after clicking the email link, even if they do not click the Submit button. This is to support a new behaviour introduced by Outlook security rules when clicking a safelink.

To do this when designing the landing page:
1. Click Show source.
1. Copy-paste the following code:

   ````
   <div id="HtmlPage_htmlPage.line3" data-nl-format="datetime"><input type="checkbox" class="nl-dce-todo" data-nl-bindto="agreement" data-nl-agreementmsg="Please tick the box to confirm" />I agree</div>
   ```

1. Click Hide source.
1. Click the checkbox.
1. Click the dots next to Form data and edit the message if needed. This text will display if the user doesn't select the checkbox beform clicking the Submit button.
1. Click Confirm.
