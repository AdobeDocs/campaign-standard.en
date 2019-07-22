---
title: Adding a content block
seo-title: Adding a content block
description: Adding a content block
seo-description: Discover the various out-of-the-box dynamic content blocks you can use to personalize your messages and learn how to create custom content blocks.
page-status-flag: never-activated
uuid: 08153ea0-42fb-4c0b-8d4b-9407540748d6
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: personalizing-content
discoiquuid: 3ffda143-f42a-4cf9-b43c-e53d24549025

internal: n
snippet: y
---

# Adding a content block{#adding-a-content-block}

Adobe Campaign offers a list of pre-configured content blocks. These content blocks are dynamic, personalized and have a specific rendering. For example, you can add a greeting or a link to the mirror page.

>[!NOTE]
>
>The images below show how to insert a content block using the [Email Designer](../../designing/using/about-email-content-design.md#about-the-email-designer) for an email.

To add a content block:

1. Click inside a text block, click the **[!UICONTROL Personalize]** icon from the contextual toolbar and select **[!UICONTROL Insert content block]**. For more on the Email Designer interface, see [this section](../../designing/using/about-email-content-design.md#email-designer-interface).

   ![](assets/email_content_block_1.png)

1. Select the content block that you would like to insert. The blocks available vary depending on the context (email or landing page).

   ![](assets/email_content_block_2.png)

1. Click **[!UICONTROL Save]**.

The name of the content block appears in the editor and it is highlighted in yellow. It will automatically adapt to the profile when the personalization is generated.

![](assets/email_content_block_3.png)

The out-of-the-box content blocks are:

* **[!UICONTROL Database URL in emails (EmailUrlBase)]**: This content block can only be used in a **delivery**.
* **[!UICONTROL Mirror page URL (MirrorPageUrl)]**: This content block can only be used in a **delivery**.
* **[!UICONTROL Link to mirror page (MirrorPage)]**: This content block can only be used in a **delivery**.
* **[!UICONTROL Greetings (Greetings)]** 
* **[!UICONTROL Unsubscription link (UnsubscriptionLink)]**: This content block can only be used in a **delivery**.
* **[!UICONTROL Social network sharing links (LandingPageViralLinks)]**: This content block can only be used in a **landing page**.
* **[!UICONTROL Default sender name (DefaultSenderName)]**: This content block can only be used in a **delivery**.
* **[!UICONTROL Name of default reply-to email address (DefaultReplyName)]**: This content block can only be used in a **delivery**.
* **[!UICONTROL Email address of default sender (DefaultSenderAddress)]**: This content block can only be used in a **delivery**.
* **[!UICONTROL Default error email address (DefaultErrorAddress)]**: This content block can only be used in a **delivery**.
* **[!UICONTROL Default reply-to email address (DefaultReplyAddress)]**: This content block can only be used in a **delivery**.
* **[!UICONTROL Brand name (BrandingUsualName)]** 
* **[!UICONTROL Link to the brand website (BrandingWebSiteLink)]** 
* **[!UICONTROL Brand logo (BrandingLogo)]** 
* **[!UICONTROL Notification style (notificationStyle)]**

## Creating custom content blocks {#creating-custom-content-blocks}

You can define new content blocks that will be inserted into a message or landing page.

To create a content block, follow these steps:

1. Click **[!UICONTROL Resources > Content blocks]** from the advanced menu to access the list of content blocks.
1. Click the **[!UICONTROL Create]** button or duplicate a pre-existing content block.

   ![](assets/content_bloc_01.png)

1. Enter a label.
1. Select the block's **[!UICONTROL Content type]**. There are three options available:

    * **[!UICONTROL Shared]**: The content block can be used in a delivery or a landing page.
    * **[!UICONTROL Delivery]**: The content block can only be used in a delivery.
    * **[!UICONTROL Landing page]**: The content block can only be used in a landing page.

   ![](assets/content_bloc_02.png)

1. You can select a **[!UICONTROL Targeting dimension]**. For more on this, see [About targeting dimension](../../designing/using/adding-a-content-block.md#about-targeting-dimension).

   ![](assets/content_bloc_04.png)

1. You can select the **[!UICONTROL Depends on format]** option to define two different blocks: one for HTML emails, and one for emails in text format. Two tabs will then be displayed in the editor (HTML and Text) to define the corresponding contents.

   ![](assets/content_bloc_03.png)

1. Enter the content of the content block(s), and click the **[!UICONTROL Create]** button.

Your content block can now be used in the content editor of a message or a landing page.

>[!CAUTION]
>
>When editing the content of a block, make sure there are no extra white spaces between the beginning and the end of your *if* statements. In HTML the white spaces are displayed on screen and they will therefore impact your content layout.

## About targeting dimension {#about-targeting-dimension}

The targeting dimension enables you to define in which type of message you can use the content block. This is to prevent using inappropriate blocks in a message, which may lead to errors.

Indeed, when editing a message, you can only select content blocks with a targeting dimension that is compatible with that message's targeting dimension.

For example, the **[!UICONTROL Unsubscription link]** block's targeting dimension is **[!UICONTROL Profiles]** because it contains personalization fields specific to the **[!UICONTROL Profiles]** resource. Therefore, you cannot use an **[!UICONTROL Unsubscription link]** block in an [event transactional message](../../channels/using/event-transactional-messages.md), because the targeting dimension of that type of message is **[!UICONTROL Real-time events]**. However, you can use the **Unsubscription link** block in a [profile transactional message](../../channels/using/profile-transactional-messages.md), because the targeting dimension of that type of message is **Profiles**. Finally, the **[!UICONTROL Link to mirror page]** block does not have a targeting dimension, so you can use it in any message.

If you leave this field empty, the content block will be compatible with all messages, no matter what the targeting dimension is. If you set a targeting dimension, that block will only be compatible with messages that have the same targeting dimension.

For more on this, refer to [Targeting dimensions and resources](../../automating/using/query.md#targeting-dimensions-and-resources).
