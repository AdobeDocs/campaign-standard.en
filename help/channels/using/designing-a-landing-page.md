---
title: Designing a landing page
seo-title: Designing a landing page
description: Designing a landing page
seo-description: Follow these steps to design the content of a landing page and link it to a service.
page-status-flag: never-activated
uuid: de6fe190-835c-40fd-8101-a809b430b423
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: landing-pages
discoiquuid: bd77d6f0-3143-4030-a91b-988a2bebc534
context-tags: landingPage,main
internal: n
snippet: y
---

# Designing a landing page{#designing-a-landing-page}

## About landing page content design content design {#about-content-design}

Landing pages are created as any [marketing activity](../../start/using/marketing-activities.md#about-marketing-activities).

When designing a landing page, you need to define the content of the page itself, the confirmation page, and the error page. Use the switcher under the action bar to display and configure each of these pages.

The content of landing pages is designed through Campaign content editor.

>[!NOTE]
>
>If your instance was installed before the Adobe Campaign Standard 19.0 release, you still have access to the legacy email content editor. The interface, principles of use and configuration are mostly the same as described below for landing pages. However, all features may not be available or maintained in the legacy email content editor, which is deprecated starting 19.0 release. To quickly edit your email content through a drag and drop interface with extended functionalities, use the [Email Designer](../../designing/using/overview.md).

This page describes the specificities of the landing page content editor. For more on the actions that are common to one or more marketing activities, refer to these sections form the **Designing email content** guide:

* [Inserting a personalization field](../../designing/using/personalization.md#inserting-a-personalization-field)
* [Adding a content block](../../designing/using/personalization.md#adding-a-content-block).
* [Inserting a link](../../designing/using/links.md#inserting-a-link).
* [Inserting images](../../designing/using/images.md).
* [General best practices for content design](../../designing/using/overview.md#content-design-best-practices).

>[!NOTE]
>If you have a landing page that is already predefined in HTML format, you can import it directly using the **[!UICONTROL Change content]** button.
>
>Before importing an HTML page in Adobe Campaign, make sure it opens and displays correctly in the various browsers. If the HTML page contains JavaScript scripts, they need to execute without errors outside of the editor. In general, avoid using scripts in message content to make sure it is correctly processed by email clients.

## Landing page content editor interface{#landing-page-content-editor-interface}

The landing page content editor allows you to easily define, modify, and personalize content in Adobe Campaign. To access it, click the **[!UICONTROL Content]** block in a landing page dashboard.

The content editor is organized into three different sections. These sections allow you to view and edit the content.

![](assets/des_lp_content_8.png)

1. The **palette** on the left-hand side of the screen allows you to modify the general options linked to a selected block. The options that can be modified are: background color, border, text alignment, visibility condition, etc. See [Inserting a personalization field](../../designing/using/personalization.md#inserting-a-personalization-field).
1. The **action bar** contains the general options for the page. You can select a template and change the display mode.
1. The main **editing zone** allows you to directly interact with the content using the contextual toolbar: insert a link into an image, change the font, delete a field, etc.

The **action bar** contains different buttons that allow you to interact with the content that is being created.

![](assets/des_lp_content_9.png)

<table> 
 <thead> 
  <tr> 
   <th> Icon<br /> </th> 
   <th> Button name<br /> </th> 
   <th> Channel<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <img height="21px" src="assets/download_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Change content</span> <br /> </td> 
   <td> Landing page and email<br /> </td> 
   <td> Allows you to select out-of-the-box content or import your own HTML content. Refer to <a href="../../designing/using/using-existing-content.md">Loading an existing content</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/undo_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Undo</span> <br /> </td> 
   <td> All<br /> </td> 
   <td> Cancels the last action carried out.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/redo_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Redo</span> <br /> </td> 
   <td> All<br /> </td> 
   <td> Redoes the last action that you canceled.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/display_block_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Show blocks</span> <br /> </td> 
   <td> Landing page and email<br /> </td> 
   <td> Allows you to show the boxes around the content blocks (corresponds to the <strong>&lt;div&gt;</strong> HTML tag).<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/code_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Show source</span> <br /> </td> 
   <td> Landing page and email<br /> </td> 
   <td> Allows you to show the HTML source code of the page.<br /> </td> 
  </tr> 
 </tbody> 
</table>

The **toolbar** is a contextual element of the editor interface that offers various functionalities depending on the zone selected. It contains action buttons and buttons that allow you to change the style of the text. The modifications carried out always apply to the zone selected. Once you select a block, you can delete or duplicate it for example. After selecting the text inside a block, you can turn it into a link or make it bold.

![](assets/delivery_content_17.png)

>[!CAUTION]
>
>Certain toolbar functions let you format the HTML content. However, if the page contains a CSS style sheet, the **instructions** from the style sheet may prove to take **priority** over the instructions specified via the toolbar.

<table> 
 <thead> 
  <tr> 
   <th> Icon<br /> </th> 
   <th> Button name<br /> </th> 
   <th> Context<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <img height="21px" src="assets/link_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Link to an external URL</span> <br /> </td> 
   <td> Any element<br /> </td> 
   <td> Allows you to add a link to a URL. Details of how to configure a link are presented in the <a href="../../designing/using/links.md#inserting-a-link">Inserting a link</a> section.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/linkpage_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Link to a landing page</span> <br /> </td> 
   <td> Any element<br /> </td> 
   <td> Allows access to an Adobe Campaign landing page. Details of how to configure a link are presented in the <a href="../../designing/using/links.md#inserting-a-link">Inserting a link</a> section.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/link_subscribe_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Subscription link</span> <br /> </td> 
   <td> Any element<br /> </td> 
   <td> Allows you to insert a service subscription link. Details of how to configure a link are presented in the <a href="../../designing/using/links.md#inserting-a-link">Inserting a link</a> section.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/link_unsubscribe_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Unsubscription link</span> <br /> </td> 
   <td> Any element<br /> </td> 
   <td> Allows you to insert a service unsubscription link. Details of how to configure a link are presented in the <a href="../../designing/using/links.md#inserting-a-link">Inserting a link</a> section.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/linkoff_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Remove link</span> <br /> </td> 
   <td> Link<br /> </td> 
   <td> Allows you to delete the link, as well as all the configurations linked to it, after confirming.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/personalization_field_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Insert a personalization field</span> <br /> </td> 
   <td> Text element<br /> </td> 
   <td> Allows you to add a field from the database to the content. Refer to <a href="../../designing/using/personalization.md#inserting-a-personalization-field">Inserting a personalization field</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/personalization_block_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Insert a content block</span> <br /> </td> 
   <td> Text element<br /> </td> 
   <td> Allows you to add a personalization block to the content. Refer to <a href="../../designing/using/personalization.md#adding-a-content-block">Adding a content block</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/dynamiccontent_24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Enable dynamic content</span> <br /> </td> 
   <td> Text element<br /> </td> 
   <td> Allows you to insert dynamic content in the content. Refer to <a href="../../channels/using/designing-a-landing-page.md#defining-dynamic-content-in-a-landing-page">Defining dynamic content</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/dynamiccontentdisable_24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Disable dynamic content</span> <br /> </td> 
   <td> Text element<br /> </td> 
   <td> Allows you to delete dynamic content.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/increase_fontsize_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Enlarge font</span> <br /> </td> 
   <td> Text element<br /> </td> 
   <td> Increases the size of the selected text (adds <strong>&lt;span style="font-size:"&gt;</strong>).<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/decrease_fontsize_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Reduce font</span> <br /> </td> 
   <td> Text element<br /> </td> 
   <td> Reduces the size of the selected text (adds <strong>&lt;span style="font-size:"&gt;</strong>).<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/textbold_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Bold</span> <br /> </td> 
   <td> Text element<br /> </td> 
   <td> Adds the bold style to the selected text (wraps the text with the <strong>&lt;strong&gt;</strong><strong>&lt;/strong&gt;</strong> tags).<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/textitalic_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Italic</span> <br /> </td> 
   <td> Text element<br /> </td> 
   <td> Adds the italic style to the selected text (wraps the text with the <strong>&lt;em&gt;</strong><strong>&lt;/em&gt;</strong> tags).<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/textunderline_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Underline</span> <br /> </td> 
   <td> Text element<br /> </td> 
   <td> Underlines the selected text (wraps the selected text with the <strong>&lt;span style="text-decoration: underline;"&gt;</strong> tag).<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/colorselector_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Change background color</span> <br /> </td> 
   <td> Text element<br /> </td> 
   <td> Allows you to change the background color of the block selected (adds style="background-color: rgba(170, 86, 255, 0.87)).<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/textcolor_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Change font color</span> <br /> </td> 
   <td> Text element<br /> </td> 
   <td> Allows you to change the color of all the text in the block or just the text selected in the block (<strong>&lt;span style="color: #56ff56;"&gt;</strong>).<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/image_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Image</span> <br /> </td> 
   <td> Block containing an image<br /> </td> 
   <td> Allows you to insert an image from a file saved locally.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/delete_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Delete</span> <br /> </td> 
   <td> Any block<br /> </td> 
   <td> Deletes the block and its content.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/duplicate_fontsize_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Duplicate</span> <br /> </td> 
   <td> Any block<br /> </td> 
   <td> Duplicates the block including any styles linked to it.<br /> </td> 
  </tr> 
 </tbody> 
</table>

## Managing landing page structure and style{#managing-landing-page-structure-and-style}

### Managing blocks in the content editor {#managing-blocks-in-the-content-editor}

The different HTML content elements are displayed in the landing page as blocks, corresponding to the **&lt;div&gt;** **&lt;/div&gt;** tag. Select a block to interact with it. It will then be surrounded by a blue box.

![](assets/des_lp_content_1.png)

If a block is selected, the parent objects of the corresponding HTML element will show in a breadcrumb located at the bottom of the editing zone.

When the mouse hovers over one of the breadcrumb elements, the element concerned is highlighted. You can therefore navigate easily between the different blocks and select exactly the HTML element you would like to modify.

![](assets/des_lp_content_2.png)

Use the options from the palette and the contextual toolbar to modify, delete, or duplicate the block. 

For the blocks containing text, click again in the block to enable text editing mode. The frame around the block turns green. You can then select or enter text. Use the options from the palette and the contextual toolbar to add a link or modify the text formatting.

![](assets/des_lp_content_3.png)

The parameters defined for an element in a block (links, personalization fields, content blocks, etc.) can be modified at any time from the palette.

![](assets/des_lp_content_4.png)

### Adding a border and a background in the content editor {#adding-a-border-and-a-background-in-the-content-editor}

You can also define a **background color** by selecting a color from the chart. This color is applied to the selected block.

![](assets/des_lp_content_5.png)

You can add a **border** to the selected block.

![](assets/des_lp_content_6.png)

### Changing the text style in the content editor {#changing-the-text-style-in-the-content-editor}

To change the style of the text, you have to click inside a text block.

To change the text alignment, select one of the following three icons in the palette on the left:

![](assets/des_lp_content_7.png)

* **Align left**: aligns the text to the left of the selected block (adds style="text-align: left;"). 
* **Center**: centers the text in the block selected (adds style="text-align: center;"). 
* **Align right**: aligns the text to the right of the selected block (adds style="text-align: right;").

You can also use the toolbar to change the font attributes: adapt the font size, make the text bold or italic, underline or change the color of the text. Refer to [this section](../../channels/using/designing-a-landing-page.md#landing-page-content-editor-interface).

### Inserting images in a landing page {#inserting-images-in-a-landing-page}

1. In a landing page content, select a block containing an image.
1. Select the **[!UICONTROL Insert]** button.

   ![](assets/des_insert_images_lp_1.png)

1. Choose **[!UICONTROL Local image]** from the contextual toolbar.

   ![](assets/des_insert_images_lp_2.png)

1. Select a file.

   ![](assets/des_insert_images_lp_3.png)

1. Adjust the image properties as needed.

   ![](assets/des_insert_images_lp_4.png)

## Defining dynamic content in a landing page{#defining-dynamic-content-in-a-landing-page}

To define dynamic content in a landing page, select a block using the breadcrumb or by directly clicking an element.

![](assets/dynamic_content_lp_1.png)

Certain blocks, such as images, cannot be directly selected. In this case, select the parent block using the breadcrumb. You can then modify all of the elements included in this parent element, including images. The condition will be applied to all child elements within the parent block.

The breadcrumb is presented in the [Managing blocks](../../channels/using/designing-a-landing-page#managing-landing-page-structure-and-style) section.

The next steps for defining dynamic content in a landing page are similar to the steps to follow for an email. See [this section](../../designing/using/personalization.md#defining-dynamic-content-in-an-email).

>[!NOTE]
>
>If a variant element is outlined in red, this means that an expression has not yet been defined.

You can navigate between the different dynamic contents of a block. To do this:

1. Select the block.

   Arrows appear on the right- and left-hand sides of the image.

1. Click the right arrow to browse through the available dynamic contents.

   ![](assets/dynamic_content_lp_2.png)

   The arrows on each side dim according to whether you have reached the last or first available dynamic contents.

   ![](assets/dynamic_content_lp_3.png)

1. To delete all the conditions applied to a block, select that block and click the **[!UICONTROL Disable dynamic content]** icon.
1. Select the dynamic content that you would like to keep.

   ![](assets/dynamic_content_lp_5.png)

In the palette:

* The contents which have an expression entered are no longer outlined in red, they are shown in gray.
* The content that is currently selected appears in blue.

![](assets/dynamic_content_lp_4.png)

## Confirm a landing page submission {#confirm-a-landing-page-submission}

When a landing page is submitted by a visitor, you can configure the actions triggered. To do this:

1. Edit the landing page properties accessed via the ![](assets/edit_darkgrey-24px.png) icon in the landing page dashboard, and display the **[!UICONTROL Job]** parameters.

   ![](assets/lp_edit_properties_button.png)

1. Under the **[!UICONTROL Specific actions]** section, select **[!UICONTROL Start sending message]** to determine the sending of an automatic message, for example to confirm subscription to a service. You need then to select an email delivery template.

   Note that if a confirmation message is already configured at the service level, you should not select one in this screen to avoid sending multiple confirmation messages. Refer to [Configure a service](../../audiences/using/creating-a-service.md). 

1. Create **[!UICONTROL Additional data]** to enable storing additional data when the landing page is being submitted. This data is not visible to people who visit the page. Only constant values are taken into account.

   ![](assets/lp_parameters_6.png)

## Setting permissions and pre-loading data {#setting-permissions-and-pre-loading-data}

Access to a landing page can be restricted to identified visitors, who come from a link in a message sent by Campaign for example. In this case, you can preload their data in the landing page. To do this:

1. Edit the landing page properties accessed via the ![](assets/edit_darkgrey-24px.png) icon in the landing page dashboard, and display the **[!UICONTROL Access & loading]** parameters. 

   ![](assets/lp_edit_properties_button.png)

1. Select **[!UICONTROL Preload visitor data]**.

   If a visitor to the page corresponds to a profile in the database, their data is displayed in the form's fields that are mapped with the database data and the landing page's personalization elements are taken into account.

   ![](assets/lp_parameters_3.png)

You can also:

* Use the URL parameters to identify the visitors, using the **[!UICONTROL Authorize visitor identification via URL parameters]** option: then you must choose the loading key and map the filter parameters with the parameters of the corresponding URL.
* Authorize any visitor to access the landing page, using the **[!UICONTROL Authorize unidentified visitors]** option.

## Setting Google reCAPTCHA {#setting-google-recaptcha}

You can set up Google reCAPTCHA V3 with your landing page to protect it from spam and abuse caused by bots. To be able to use it with your landing page, you first need to create an external account. For more information on how to configure it, refer to this [section](../../administration/using/external-accounts.md#google-recaptcha-external-account).

Once your Google reCAPTCHA V3 external account has been set up, you can add it to your landing page:

1. Before publishing your landing page, access the page properties accessed via the ![](assets/edit_darkgrey-24px.png) icon from you landing page dashboard.

   ![](assets/lp_parameters_google3.png)

1. Unfold the **[!UICONTROL Access & loading]** menu.
1. Check the **[!UICONTROL Use reCAPTCHA to protect your site from spam and abuse]** option.
1. Select your previously created Google reCAPTCHA external account.

   ![](assets/lp_parameters_google.png)

1. Click **[!UICONTROL Confirm]**.

Your landing page is now set up with Google reCAPTCHA which can be seen at the bottom of your page.

![](assets/lp_parameters_google2.png)

Google reCAPTCHA will then return a score based on users' interactions with your page. To check your score, connect to your [Google admin console](https://g.co/recaptcha/admin).
