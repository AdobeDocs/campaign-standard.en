---
title: Content design best practices
seo-title: Content design best practices
description: Content design best practices
seo-description: Read about these guidelines to ensure the editor's optimal operation.
uuid: 250e28e5-2037-473e-a261-1de17024a9e8
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: about-content-design
discoiquuid: ce3106f8-5893-4e0f-9e77-ca72bb0b11f1
index: y
internal: n
snippet: y
---

# Content design best practices{#content-design-best-practices}

To ensure the editor's optimal operation, we recommend observing the following guidelines:

* SCSS style sheets are not supported. Use regular CSS if you import ZIP files containing your HTML content.
* When editing **email content**:

  Preview your messages before sending them. Adobe Campaign offers a way to test email rendering using Litmus. For more on this, see [Email rendering](../../sending/using/email-rendering.md).

* When editing **landing page content**:

    * Before importing an HTML page template in Adobe Campaign, please make sure the template opens and displays correctly in the various browsers.
    * If the HTML page contains JavaScript scripts, they need to execute without errors outside of the editor. In general, avoid using scripts in message content to make sure it is correctly processed by email clients.
    * When building a template, we recommend adding a **'type'** attribute to  tags. This information will be processed by the editor and help the user to link a database field to the form field when configuring the web application.

      Example of HTML code in the template:

      ```    
      
      <input id="email" type="email" name="email"/>
         
      ```    
    
      The official list of 'type' attributes is available at the following address: [http://www.w3schools.com/tags/att_input_type.asp](http://www.w3schools.com/tags/att_input_type.asp)

More design and general best practices regarding messages are presented in the following Adobe Campaign step-by-step guide: [Delivery best practices with Adobe Campaign](https://docs.campaign.adobe.com/doc/standard/getting_started/en/ACS_DeliveryBestPractices.html ).
