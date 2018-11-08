---
title: Adding a content block
seo-title: Adding a content block
description: Adding a content block
seo-description: Discover the various out-of-the-box dynamic content blocks you can use to personalize your messages and learn how to create custom content blocks.
uuid: 9db80292-1380-422a-bdda-5214257a3f70
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/designing/using/adding-a-content-block
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-10T07 25 12.302-0400
cq-lastreplicated: 2018-09-07T15 00 25.826-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: personalizing-content
cq-template: /apps/help/templates/article-3
discoiquuid: 0a012935-6b4a-41b0-8f4c-11d86a323bcc
firstPublishExternalDate: 2018-09-07T15:00:22.317-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 42.371-0400
jcr-createdby: admin
jcr-description: Adding a content block
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T15:00:22.317-0400
lochandoffdate: 2018-09-10T07 25 12.300-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Adding a content block
publishexternaldate: 2018-09-07T15 00 22.317-0400
publishExternalURL: "https://helpx.adobe.com/campaign/standard/designing/using/adding-a-content-block.html"
sha1: b137e4d0411f7e67a92037b79d6f18af0e525400
topicBrowsingSortDate: 2018-09-07T15:00:22.317-0400
index: y
internal: n
snippet: y
---

# Adding a content block{#adding-a-content-block}

Adding a content block

Adobe Campaign offers a list of pre-configured content blocks. These content blocks are dynamic, personalized and have a specific rendering. For example, you can add a greeting or a link to the mirror page.

>[!NOTE]
>
>The images below show how to insert a content block using the [content editor](../../designing/using/about-email-content-design.md#using-the-email-content-editor).

To add a content block, click inside a text block and click the **Insert content block** button in the toolbar (refer to [Email content editor toolbar](../../designing/using/about-email-content-design.md#email-content-editor-toolbar)).

Select the content block that you would like to insert. The blocks available vary depending on the context (email or landing page).

![](assets/delivery_content_23.png)

The name of the content block appears in the editor and it is highlighted in yellow. It will automatically adapt to the recipient profile when the personalization is generated.

![](assets/delivery_content_24.png)

The out-of-the-box content blocks are:

* Database URL in emails (EmailUrlBase): This content block can only be used in a **delivery**.
* Mirror page URL (MirrorPageUrl): This content block can only be used in a **delivery**.
* Link to mirror page (MirrorPage): This content block can only be used in a **delivery**.
* Greetings
* Unsubscription link (UnsubscriptionLink): This content block can only be used in a **delivery**.
* Social network sharing links (LandingPageViralLinks): This content block can only be used in a **landing page**.
* Default sender name (DefaultSenderName): This content block can only be used in a **delivery**.
* Name of default reply-to email address (DefaultReplyName): This content block can only be used in a **delivery**.
* Email address of default sender (DefaultSenderAddress): This content block can only be used in a **delivery**.
* Default error email address (DefaultErrorAddress): This content block can only be used in a **delivery**.
* Default reply-to email address (DefaultReplyAddress): This content block can only be used in a **delivery**.
* Brand name (BrandingUsualName)
* Link to the brand website (BrandingWebSiteLink)
* Brand logo (BrandingLogo)
* Notification style (notificationStyle)

## Creating custom content blocks {#creating-custom-content-blocks}

You can define new content blocks that will be inserted into a delivery or landing page.

To create a content block, follow these steps:

1. Click **Resources > Content blocks** from the advanced menu to access the list of content blocks.
1. Click the **Create** button or duplicate a pre-existing content block.

   ![](assets/content_bloc_01.png)

1. Enter the block label.
1. Select the block's **Content type**. There are three options available:

    * Shared: The content block can be used in a delivery or a landing page.
    * Delivery: The content block can only be used in a delivery.
    * Landing page: The content block can only be used in a landing page.

   ![](assets/content_bloc_02.png)

1. You can select the **Depends on format** option to define two different blocks for HTML emails and those that are in text format. Two tabs will then be displayed in the editor (HTML and Text) to define the corresponding contents.

   ![](assets/content_bloc_03.png)

1. Enter the content of the content block(s), and click the **Create** button.

   Your content block can now be used in the content editor of a delivery or a landing page.

