---
title: Design best practices
seo-title: Design best practices
description: Design best practices
seo-description: Read about these guidelines to ensure the editor's optimal operation.
uuid: 26326c2d-85a3-4665-b885-d0f322af4d3c
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/designing/using/design-best-practices
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-06-25T08 45 00.832-0400
cq-lastreplicated: 2018-06-14T08 43 37.939-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: about-content-design
cq-template: /apps/help/templates/article-3
discoiquuid: e38d77c3-3c47-48f6-84f0-8ca388191fe7
firstPublishExternalDate: 2018-06-14T08:43:37.917-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 01 47.498-0400
jcr-createdby: admin
jcr-description: Design best practices
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-06-14T08:43:37.917-0400
lochandoffdate: 2018-06-25T08 45 00.832-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Design best practices
publishexternaldate: 2018-06-14T08 43 37.917-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/designing/using/design-best-practices.html
sha1: 5051ccd65a03852b81ca95c238634e907c944fe7
topicBrowsingSortDate: 2018-06-14T08:43:37.917-0400
index: y
internal: n
snippet: y
---

# Design best practices

Design best practices

To ensure the editor's optimal operation, we recommend observing the following guidelines:

* Before **importing an HTML page template** in Adobe Campaign, please make sure the template opens and displays correctly in the various browsers.
* If the HTML page contains **JavaScript scripts**, they need to execute **without errors** outside of the editor. In general, avoid using scripts in message content to make sure it is correctly processed by email clients.
* When building a template, we recommend adding a **'type'** attribute to &lt;input&gt; tags. This information will be processed by the editor and help the user to link a database field to the form field when configuring the web application.

  Example of HTML code in the template:

  ```
  
  <input id="email" type="email" name="email"/>
     
  ```

  The official list of 'type' attributes is available at the following address: [http://www.w3schools.com/tags/att_input_type.asp](http://www.w3schools.com/tags/att_input_type.asp)

* Preview your messages before sending them. Adobe Campaign offers a way to test email rendering using Litmus. For more on this, see [Email rendering](../../sending/using/email-rendering.md).
* SCSS style sheets are not supported. Use regular CSS if you import ZIP files containing your HTML content.

More design and general best practices regarding messages are presented in the following Adobe Campaign step-by-step guide: [Delivery best practices with Adobe Campaign](https://docs.campaign.adobe.com/doc/standard/getting_started/en/ACS_DeliveryBestPractices.html ).
