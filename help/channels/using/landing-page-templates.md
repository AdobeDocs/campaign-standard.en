---
title: Landing page templates
description: Learn more on landing page templates.
page-status-flag: never-activated
uuid: b316bf47-7d98-46fa-ab4f-67ff50de8095
contentOwner: lemaitre
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: landing-pages
discoiquuid: ca8d1698-6e8a-4f5a-b017-74a152e14286
context-tags: landingPage,wizard;landingPage,overview;landingPage,main
---

# About landing page templates {#landing-page-templates}

Campaign comes with a set of built-in landing page templates:

* **[!UICONTROL Acquisition]**: this is the default template for landing pages, which enables you to capture and update data in Campaign database.
* **[!UICONTROL Subscription]**: this template should be used to offer subscriptions to a service.
* **[!UICONTROL Unsubscription]**: this template can be linked from an email sent to subscribers to a service, to allow them to unsubscribe this service.
* **[!UICONTROL Denylist]**: this template should be used when a profile no longer wants to be contacted by Campaign. For more about denylist management, refer to [About opt-in and opt-out in Campaign](../../audiences/using/about-opt-in-and-opt-out-in-campaign.md).

These templates are proposed by default when creating a new landing page.

![](assets/lp_creation_1.png)

To access landing page templates, click the Adobe Campaign logo on the upper left corner and select **[!UICONTROL Resources]** > **[!UICONTROL Templates]** > **[!UICONTROL Landing page templates]**.

>[!NOTE]
>
>Adobe recommends creating your own templates by duplicating a built-in template. Some parameters can only be set in landing page templates, and cannot be modified in landing pages directly.

When building a template, we recommend adding a **'type'** attribute to tags. This information will be processed by the editor and help the user to link a database field to the form field when configuring the web application.

  Example of HTML code in the template:

  ```
  <input id="email" type="email" name="email"/>
  ```

  The official list of 'type' attributes is available at the following address: [https://www.w3schools.com/tags/att_input_type.asp](https://www.w3schools.com/tags/att_input_type.asp)
  