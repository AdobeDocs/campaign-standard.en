---
title: Personalizing URLs
seo-title: Personalizing URLs
description: Personalizing URLs
seo-description: Learn how to personalize URLs in a message by adding personalization fields, content blocks, or dynamic content.
page-status-flag: never-activated
uuid: c28a9783-a75e-4ebb-a8f4-72faaebb0ebc
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/designing/using/personalizing-urls
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: managing-links
discoiquuid: e6e66fe5-7911-45f5-9ad7-33aee9d54685
isreadyforlocalization: false
navTitle: Personalizing URLs
publishexternaldate: 2018-11-20
sha1: db2f03b566b9267b394af12aa35556ea46a4495a
index: y
internal: n
snippet: y
---

# Personalizing URLs{#personalizing-urls}

Personalizing URLs

Adobe Campaign allows you to personalize one or several URLs in your message by adding personalization fields, content blocks, or dynamic content to them. To do this:

* Insert an external URL and specify its parameters. See [Inserting a link](../../designing/using/inserting-a-link.md).
* If not displayed, click the pencil next to the selected URL in the side pane to access the personalization options.
* Add the personalization fields, content blocks, and dynamic contents that you want to use.

  ![](assets/des_personalize_links.png)

* Confirm your changes.

>[!NOTE]
>
>Personalizing URLs cannot be applied to the domain name, nor to the URL extension. An error message will be displayed during message analysis if personalization is incorrect. When selecting a content block, you are not allowed to select elements such as **Link to mirror page**. This type of blocks is forbidden inside a link.

To change a personalized URL, select it and use the **URL** button in the palette on the left-hand side.

In the [content editor](../../designing/using/about-personalization.md), the **Encoded value** option is checked by default. It allows for special characters to be encoded if they are present in the personalization field's value. We advise you to leave this option unchecked to avoid incorrect URL encoding.

![](assets/delivery_content_59.png)

**Related topics**:

* [Inserting a personalization field](../../designing/using/inserting-a-personalization-field.md)
* [Adding content blocks](../../designing/using/adding-a-content-block.md)
* [Defining dynamic content](../../designing/using/defining-dynamic-content-in-an-email.md)

