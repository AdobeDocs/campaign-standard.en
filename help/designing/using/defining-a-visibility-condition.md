---
title: Defining a visibility condition
seo-title: Defining a visibility condition
description: Defining a visibility condition
seo-description: Make a web page element visible only if a certain condition is respected.
uuid: 6d878a56-d3ef-4caa-9444-37237b509614
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: defining-conditional-content
discoiquuid: df09f9fb-a1c8-45eb-8905-788c86328d1a
index: y
internal: n
snippet: y
---

# Defining a visibility condition{#defining-a-visibility-condition}

Defining a visibility condition

You can specify a visibility condition on any element. It will only be visible if the condition is respected.

To add a visibility condition, select a block and enter the condition to be respected in the **[!UICONTROL Visibility condition]** field of its settings.

![](assets/delivery_content_5.png)

This option is only available for the following elements: ADDRESS, BLOCKQUOTE, CENTER, DIR, DIV, DL, FIELDSET, FORM, H1, H2, H3, H4, H5, H6, NOSCRIPT, OL, P, PRE, UL, TR, TD.

The expression editor is presented in the [Advanced expression editing](../../automating/using/editing-queries.md#about-query-editor) section.

These conditions adopt the XTK expression syntax (e.g. **context.profile.email !=''** or **context.profile.status='0'**). By default, all fields are visible.

>[!NOTE]
>
>A condition cannot be defined for a block that already contains a sub-element with a dynamic content or a block that already makes up a dynamic content. Non-visible dynamic blocks like drop-down lists cannot be edited.

