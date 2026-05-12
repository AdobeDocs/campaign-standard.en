---
title: Landing page templates
description: Learn more on landing page templates.
audience: channels
content-type: reference
topic-tags: landing-pages
context-tags: landingPage,wizard;landingPage,overview;landingPage,main
feature: Landing Pages
role: User
level: Intermediate
exl-id: 29d1badf-9ce3-470c-9bdc-169586d2e943
TQID: https://experienceleague.adobe.com/vJyIRO33IjK6o3--ekx-Iw9K-GcIZMViLz9wEr-kxY0
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
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
