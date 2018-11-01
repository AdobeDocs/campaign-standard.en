---
title: Content editor interface
seo-title: Content editor interface
description: Content editor interface
seo-description: Learn how to use the different sections of the editor, such as the action bar, to modify your message content.
uuid: 871a6c74-471a-47f8-aeb1-562ed5b10d58
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/designing/using/content-editor-interface
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-06-25T08 45 01.138-0400
cq-lastreplicated: 2018-06-14T08 43 38.498-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: editing-message-and-landing-page-content
cq-template: /apps/help/templates/article-3
discoiquuid: a46eebda-49bc-4207-bf61-f37187731d64
firstPublishExternalDate: 2018-06-14T08:43:38.476-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 01 24.576-0400
jcr-createdby: admin
jcr-description: Content editor interface
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-06-14T08:43:38.476-0400
lochandoffdate: 2018-06-25T08 45 01.138-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Content editor interface
publishexternaldate: 2018-06-14T08 43 38.476-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/designing/using/content-editor-interface.html
sha1: 82a8fc492b5c147321babe360b3df4f4b2b86375
topicBrowsingSortDate: 2018-06-14T08:43:38.476-0400
index: y
internal: n
snippet: y
---

# Content editor interface

Content editor interface

The content editor is organized into three different sections. These sections allow you to view and edit the content.

![](assets/delivery_content_1.png)

1. The **palette** on the left-hand side of the screen allows you to modify the general options linked to a selected block. The options that can be modified are: background color, border, text alignment, visibility condition, etc. Refer to [HTML functionalities](../../designing/using/adding-a-personalization-field.md).
1. The **action bar** contains the general options for the page. You can select a template, change the display mode or preview the email from here. Refer to [Action bar](../../designing/using/content-editor-interface.md#action-bar).
1. The **editing zone** on the right-hand side of the screen allows you to directly interact with the content using the contextual toolbar: insert a link into an image, change the font, delete a field, etc. Refer to [Toolbar](../../designing/using/content-editor-interface.md#toolbar).

   >[!NOTE]
   >
   >Depending on the type of marketing activity being edited, some buttons or options may not be available. For example, the **From** and **Subject** fields, as well as the **Text** tab are only available for **Email** type marketing activities.

## <p>Action bar</p>

The action bar contains different buttons that allow you to interact with the content that is being created. Depending on the type of marketing activity, some buttons may not be available. 

![](assets/delivery_content_2.png) 

<table> 
 <thead> 
  <tr> 
   <th> Icon<br /> </th> 
   <th> Button name<br /> </th> 
   <th> Email<br /> </th> 
   <th> Landing page<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> </td> 
   <td> <strong>Change content</strong><br /> </td> 
   <td> </td> 
   <td> </td> 
   <td> Allows you to select out-of-the-box content or import your own HTML content. Refer to <a href="../../designing/using/importing-html-content.md">Importing HTML content</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> </td> 
   <td> <strong>Tracked URLs</strong><br /> </td> 
   <td> </td> 
   <td> </td> 
   <td> Displays the list of each URL. You can enable or disable the tracking separately for each URL in the message. <br /> </td> 
  </tr> 
  <tr> 
   <td> </td> 
   <td> <strong>Preview</strong><br /> </td> 
   <td> </td> 
   <td> </td> 
   <td> Allows you to view how the email is rendered for a recipient. Refer to <a href="../../sending/using/previewing-messages.md">Previewing messages</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> </td> 
   <td> <strong>Expand content editor</strong><br /> </td> 
   <td> </td> 
   <td> </td> 
   <td> Hides the palette and expands the content editor.<br /> </td> 
  </tr> 
  <tr> 
   <td> </td> 
   <td> <strong>Cancel</strong><br /> </td> 
   <td> </td> 
   <td> </td> 
   <td> Cancels the last action carried out.<br /> </td> 
  </tr> 
  <tr> 
   <td> </td> 
   <td> <strong>Redo</strong><br /> </td> 
   <td> </td> 
   <td> </td> 
   <td> Redoes the last action that you canceled.<br /> </td> 
  </tr> 
  <tr> 
   <td> </td> 
   <td> <strong>Show blocks</strong><br /> </td> 
   <td> </td> 
   <td> </td> 
   <td> Allows you to show the boxes around the content blocks (corresponds to the <strong>&lt;div&gt;</strong> HTML tag).<br /> </td> 
  </tr> 
  <tr> 
   <td> </td> 
   <td> <strong>Show source</strong><br /> </td> 
   <td> </td> 
   <td> </td> 
   <td> Allows you to show the HTML source code of the page.<br /> </td> 
  </tr> 
 </tbody> 
</table>

## <p>Toolbar</p>

The toolbar is a **contextual element** of the editor interface that offers various functionalities depending on the zone selected. It contains action buttons and buttons that allow you to change the style of the text. The modifications carried out always apply to the zone selected. Once you select a block, you can delete or duplicate it for example. After selecting the text inside a block, you can turn it into a link or make it bold. 

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
   <td> </td> 
   <td> <strong>Link to an external URL</strong><br /> </td> 
   <td> Any element<br /> </td> 
   <td> Allows you to add a link to a URL. Details of how to configure a link are presented in the <a href="../../designing/using/managing-links.md">Adding a link</a> section.<br /> </td> 
  </tr> 
  <tr> 
   <td> </td> 
   <td> <strong>Link that defines an action</strong><br /> </td> 
   <td> Any element (only for landing pages)<br /> </td> 
   <td> Allows you to define an action when an element in the landing page is clicked. Details of how to configure a link are presented in the <a href="../../designing/using/managing-links.md">Adding a link</a> section.<br /> </td> 
  </tr> 
  <tr> 
   <td> </td> 
   <td> <strong>Link to a landing page</strong><br /> </td> 
   <td> Any element<br /> </td> 
   <td> Allows access to an Adobe Campaign landing page. Details of how to configure a link are presented in the <a href="../../designing/using/managing-links.md">Adding a link</a> section.<br /> </td> 
  </tr> 
  <tr> 
   <td> </td> 
   <td> <strong>Subscription link</strong><br /> </td> 
   <td> Any element<br /> </td> 
   <td> Allows you to insert a service subscription link. Details of how to configure a link are presented in the <a href="../../designing/using/managing-links.md">Adding a link</a> section.<br /> </td> 
  </tr> 
  <tr> 
   <td> </td> 
   <td> <strong>Unsubscription link</strong><br /> </td> 
   <td> Any element<br /> </td> 
   <td> Allows you to insert a service unsubscription link. Details of how to configure a link are presented in the <a href="../../designing/using/managing-links.md">Adding a link</a> section.<br /> </td> 
  </tr> 
  <tr> 
   <td> </td> 
   <td> <strong>Remove link</strong><br /> </td> 
   <td> Link<br /> </td> 
   <td> Allows you to delete the link, as well as all the configurations linked to it, after confirming. <br /> </td> 
  </tr> 
  <tr> 
   <td> </td> 
   <td> <strong>Insert a personalization field</strong><br /> </td> 
   <td> Text element<br /> </td> 
   <td> Allows you to add a field from the database to the content. Refer to <a href="../../designing/using/adding-a-personalization-field.md">Adding a personalization field</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> </td> 
   <td> <strong>Insert a content block</strong><br /> </td> 
   <td> Text element<br /> </td> 
   <td> Allows you to add a personalization block to the content. Refer to <a href="../../designing/using/adding-a-content-block.md">Adding a content block</a>. <br /> </td> 
  </tr> 
  <tr> 
   <td> <br /> </td> 
   <td> <strong>Enable dynamic content</strong><br /> </td> 
   <td> Text element<br /> </td> 
   <td> Allows you to insert dynamic content in the content. Refer to <a href="../../designing/using/defining-dynamic-content.md">Defining dynamic content</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> <br /> </td> 
   <td> <strong>Disable dynamic content</strong><br /> </td> 
   <td> Text element<br /> </td> 
   <td> Allows you to delete dynamic content.<br /> </td> 
  </tr> 
  <tr> 
   <td> </td> 
   <td> <strong>Enlarge font</strong><br /> </td> 
   <td> Text element<br /> </td> 
   <td> Increases the size of the selected text (adds &lt;span style="font-size:"&gt;).<br /> </td> 
  </tr> 
  <tr> 
   <td> </td> 
   <td> <strong>Reduce font</strong><br /> </td> 
   <td> Text element<br /> </td> 
   <td> Reduces the size of the selected text (adds &lt;span style="font-size:"&gt;). <br /> </td> 
  </tr> 
  <tr> 
   <td> </td> 
   <td> <strong>Bold</strong><br /> </td> 
   <td> Text element<br /> </td> 
   <td> Adds the bold style to the selected text (wraps the text with the &lt;strong&gt;&lt;/strong&gt; tags). <br /> </td> 
  </tr> 
  <tr> 
   <td> </td> 
   <td> <strong>Italic</strong><br /> </td> 
   <td> Text element<br /> </td> 
   <td> Adds the italic style to the selected text (wraps the text with the &lt;em&gt;&lt;/em&gt; tags). <br /> </td> 
  </tr> 
  <tr> 
   <td> </td> 
   <td> <strong>Underline</strong><br /> </td> 
   <td> Text element<br /> </td> 
   <td> Underlines the selected text (wraps the selected text with the &lt;span style="text-decoration: underline;"&gt; tag). <br /> </td> 
  </tr> 
  <tr> 
   <td> </td> 
   <td> <strong>Change background color</strong><br /> </td> 
   <td> Text element<br /> </td> 
   <td> Allows you to change the background color of the block selected (adds style="background-color: rgba(170, 86, 255, 0.87)). <br /> </td> 
  </tr> 
  <tr> 
   <td> </td> 
   <td> <strong>Change font color</strong><br /> </td> 
   <td> Text element<br /> </td> 
   <td> Allows you to change the color of all the text in the block or just the text selected in the block (&lt;span style="color: #56ff56;"&gt;). <br /> </td> 
  </tr> 
  <tr> 
   <td> </td> 
   <td> <strong>Image</strong><br /> </td> 
   <td> Block containing an image<br /> </td> 
   <td> Allows you to insert an image from a file saved locally. <br /> </td> 
  </tr> 
  <tr> 
   <td> </td> 
   <td> <strong>Delete</strong><br /> </td> 
   <td> Any block<br /> </td> 
   <td> Deletes the block and its content. <br /> </td> 
  </tr> 
  <tr> 
   <td> </td> 
   <td> <strong>Duplicate</strong><br /> </td> 
   <td> Any block<br /> </td> 
   <td> Duplicates the block including any styles linked to it. <br /> </td> 
  </tr> 
 </tbody> 
</table>

