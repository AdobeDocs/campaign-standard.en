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

You can link database fields to input zone, radio button or checkbox type blocks. To do this, select the block and access the **[!UICONTROL Form data]** in the palette.

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

## Agreement checkbox {#agreement-checkbox}

It is now possible to add a mandatory checkbox that the profile needs to check before submitting the landing page.

This is particularly useful in the following case:

When a profile opens the landing page from an Outlook.com mailbox, Outlook checks whether the links on the landing page are suspicious. However, this Outlook security feature (called safelinks) has an unwanted effect: it automatically activates the buttons included on the landing page. Consequently, profiles are automatically subscribed or unsubscribed without confirmation when the landing page is displayed after clicking the email link, even if they do not submit the form.

![](assets/lp_submit_button.png)

To avoid this, Adobe recommends you always add to your landing page a checkbox which enables the profile to agree before proceeding with subscription or unsubscription.

>[!NOTE]
>
>Selecting this checkbox is mandatory for the user. If not selected, the profile will not be able to submit the form.

To do this:

1. When designing the landing page, click **[!UICONTROL Show source]**.

   ![](assets/lp_show_source.png)

1. Copy-paste the following code at the desired position in your content:

   ![](assets/lp_checkbox_code.png)

   ````
   <div id="HtmlPage_htmlPage.line3" data-nl-format="datetime"><input type="checkbox" class="nl-dce-todo" data-nl-bindto="agreement" data-nl-agreementmsg="Please tick the box to confirm" />I agree</div>
   ```

1. Click **[!UICONTROL Hide source]**.

1. The new checkbox is displayed. Select it.

   ![](assets/lp_select_checkbox.png)

1. The corresponding drop-down list is displayed in the **[!UICONTROL Form data]** section of the palette. Select the default value: **[!UICONTROL Agreement]**.

   ![](assets/lp_form_data_drop-down.png)

   >[!NOTE]
   >
   >This element from the list is not mapped to a field of the Campaign database.

1. Click the three dots next to **[!UICONTROL Form data]** and edit the message if needed. This text will display if the user does not select the checkbox before submitting the form.

   ![](assets/lp_agreement_message.png)

   >[!NOTE]
   >
   >This action is mandatory by default and cannot be changed.

1. Click **[!UICONTROL Confirm]**.

Now, each time a landing page is displayed, the profile will have to select this checkbox before submitting the form. If not, the designed message will display and the user will not be able to submit the form until the checkbox is activated.