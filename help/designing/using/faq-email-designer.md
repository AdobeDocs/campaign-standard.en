---
title: Email Designer Frequently Asked Questions 
description: Frequently asked questions about Email Designer.
audience: designing
content-type: reference
topic-tags: working-with-campaign-and-analytics

feature: Email Design
role: User
level: Intermediate
exl-id: f3208380-a4cf-4944-aa24-883995d1075d
---
# Email Designer Frequently Asked Questions 

## What is the difference between Content blocks and content fragments? 

 Content blocks and content fragments are pieces of reusable contents that are common across multiple emails. These are used to ensure consistency across emails and also to optimize/standardize email creation. The differences between content blocks and content fragments are the level of customization possible.

* Content blocks are pure HTML where HTML code is inserted manually (not user-friendly UI, it is direct source code). Although it’s really oriented to people with HTML knowledge, it allows level of personalization not available in content fragments.

* Content Fragments are visual piece of content created via the Email Designer, using its user-friendly UI. However, it is not possible to personalize the content. If personalization is required, it can only be done via content blocks.

## How can I add padding to an element from the HTML structure?

You can add padding by using the HTML breadcrumb.

1. On the bottom left of the screen, click the HTML breadcrumb.

   ![](assets/do-not-localize/breadcrumb.png)

1. Click on the element you want to add a padding.
1. Click on the parent tag in the HTML breadcrumb.
You can now add a padding to this element.

## Can I import HTML content in the Email Designer?

You can upload your own HTML content to the Email Designer. If it hasn’t been created through Email Designer, it will load in compatibility mode which is designed to keep your original HTML but limits certain edition capabilities through the UI.

For more information, refer to [Compatibility mode](../../designing/using/using-existing-content.md#compatibility-mode)

## How do I create my first email content?

First of all, create an email from the home page. 
Then to add content to an email, you need to add a structure component, and insert a content component in it.

For more information, refer to [Creating an email from scratch](../../designing/using/quick-start.md#from-scratch-email)

## Why do I need to update fragments? 

The Email Designer is under continuous improvement. If you created an email content from scratch, from an out-of-the-box template or if you created fragments, you may need to update your content to the latest version to avoid problems such as CSS collision issues.

For more information, refer to [Updating fragments](../../designing/using/designing-content-in-adobe-campaign.md#email-designer-updates)

## Can I save a styles in a theme? 

Styles cannot be saved as a theme for future reuse. However, the CSS style can be saved in a content template or in an email.

For more information, refer to [Styles](../../designing/using/styles.md)

## Which fonts are available? 

When editing styles, only the web fonts officially supported by most email clients are availableby default through the UI. Using custom fonts requires to update the HTML code.
