---
title: Personalizing URLs
seo-title: Personalizing URLs
description: Personalizing URLs
seo-description: Learn how to personalize URLs in a delivery by adding personalization fields, content blocks, or dynamic content.
page-status-flag: never-activated
uuid: 46643c47-6cad-45b3-941d-b779738d57b4
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: managing-links
discoiquuid: 73b0b048-849f-4bdf-a353-11b6bc59c2f1
isreadyforlocalization: true
index: y
internal: n
snippet: y
---

# Personalizing URLs{#personalizing-urls}

Personalizing URLs

Adobe Campaign allows you to personalize one or several URLs in your delivery by adding personalization fields, content blocks, or dynamic content to them. To do this:

* Insert an external URL and specify its parameters. See [Inserting a link](../../designing/using/inserting-a-link.md).
* If not displayed, click the pencil next to the selected URL in the side pane to access the personalization options.
* Add the personalization fields, content blocks, and dynamic contents that you want to use.

  ![](assets/des_personalize_links.png)

* Confirm your changes.

>[!NOTE]
>
>Personalizing URLs cannot be applied to the domain name, nor to the URL extension. An error message will be displayed during delivery analysis if personalization is incorrect. When selecting a content block, you are not allowed to select elements such as **Link to mirror page**. This type of blocks is forbidden inside a link.

To change a personalized URL, select it and use the **URL** button in the palette on the left-hand side.

In the [content editor](../../designing/using/about-email-content-design.md#using-the-email-content-editor), the **Encoded value** option is checked by default. It allows for special characters to be encoded if they are present in the personalization field's value. We advise you to leave this option unchecked to avoid incorrect URL encoding.

![](assets/delivery_content_59.png)

**Related topics**:

* [Inserting a personalization field](../../designing/using/inserting-a-personalization-field.md)
* [Adding content blocks](../../designing/using/adding-a-content-block.md)
* [Defining dynamic content](../../designing/using/defining-dynamic-content-in-an-email.md)

