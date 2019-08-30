---
title: About landing page content design
seo-title: About landing page content design
description: About landing page content design
seo-description: Learn about the specificities of the landing page content editor.
page-status-flag: never-activated
uuid: 8b230690-8a63-44da-b4ed-8e9d8fd84262
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: editing-landing-page-content
discoiquuid: 212720d2-5d57-4e7a-bb72-10512050e78c

internal: n
snippet: y
---
# About landing page content design{#about-landing-page-content-design}

Use the standard content editor to create and modify the content of your landing pages in Adobe Campaign.

This section describes the specificities of the landing page content editor:

* [Landing page content editor interface](../../channels/using/landing-page-content-editor-interface.md)
* [Managing landing page structure and style](../../channels/using/managing-landing-page-structure-and-style.md)
* [Changing a landing page form data properties](../../channels/using/changing-a-landing-page-form-data-properties.md)

To know more about actions that are common to one or more marketing activities, refer to the following sections:

* For more on personalizing a landing page content, see [Inserting a personalization field](../../designing/using/inserting-a-personalization-field.md) and [Adding a content block](../../designing/using/adding-a-content-block.md).
* For more on importing another landing page content, see [Selecting an existing content](../../designing/using/selecting-an-existing-content.md).
* For more on defining dynamic content in a landing page, see [Defining dynamic content in a landing page](../../channels/using/defining-dynamic-content-in-a-landing-page.md).
* For more on inserting links in a landing page, see [Inserting a link](../../designing/using/inserting-a-link.md).
* For more on inserting images in a landing page, see [Inserting images](../../designing/using/inserting-images.md).

Also check the [general best practices for content design](../../designing/using/content-design-best-practices.md).

>[!NOTE]
>
>If your instance was installed before the Adobe Campaign Standard 19.0 release, you still have access to the legacy email content editor. The interface, principles of use and configuration are mostly the same as described below for landing pages. However, all features may not be available or maintained in the legacy email content editor, which is deprecated starting 19.0 release. To quickly edit your email content through a drag and drop interface with extended functionalities, use the [Email Designer](../../designing/using/overview.md).

## Landing page design best practices {#landing-pages-best-practices-design}

* When editing **landing page content**:

  * Before importing an HTML page template in Adobe Campaign, please make sure the template opens and displays correctly in the various browsers.
  * If the HTML page contains JavaScript scripts, they need to execute without errors outside of the editor. In general, avoid using scripts in message content to make sure it is correctly processed by email clients.
  * When building a template, we recommend adding a **'type'** attribute to  tags. This information will be processed by the editor and help the user to link a database field to the form field when configuring the web application.

  Example of HTML code in the template:

  ```    
  
  <input id="email" type="email" name="email"/>
  
  ```

  The official list of 'type' attributes is available at the following address: [http://www.w3schools.com/tags/att_input_type.asp](http://www.w3schools.com/tags/att_input_type.asp)