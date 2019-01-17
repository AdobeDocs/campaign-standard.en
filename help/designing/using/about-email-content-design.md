---
title: About email content design
seo-title: About email content design
description: About email content design
seo-description: Discover the Email Designer that enables you to design content for your emails.
uuid: fa8a8eab-2d43-4e76-9c0f-6db51b43c83d
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: editing-email-content
discoiquuid: 43c71d7b-3816-4e06-add2-9342095be21e
isreadyforlocalization: false
index: y
internal: n
snippet: y
---

# About email content design{#about-email-content-design}

About email content design

Use the Email Designer drag-and-drop interface to create and modify the content of your emails in Adobe Campaign.

This section describes the specificities of the Email Designer:

* [About the Email Designer](../../designing/using/about-email-content-design.md#about-the-email-designer)
* [Defining the email structure](../../designing/using/defining-the-email-structure.md)
* [Editing email styles](../../designing/using/editing-email-styles.md)

To know more about actions that are common to one or more marketing activities, refer to the following sections:

* For more on personalizing an email content, see [Inserting a personalization field](../../designing/using/inserting-a-personalization-field.md) and [Adding a content block](../../designing/using/adding-a-content-block.md).
* For more on importing another email content, see [Selecting an existing content](../../designing/using/selecting-an-existing-content.md).
* For more on defining dynamic content in an email, see [Defining dynamic content in an email](../../designing/using/defining-dynamic-content-in-an-email.md).
* For more on inserting links in an email, see [Inserting a link](../../designing/using/inserting-a-link.md).
* For more on inserting images in an email, see [Inserting images](../../designing/using/inserting-images.md).

Also check the [general best practices for content design](../../designing/using/content-design-best-practices.md).

## About the Email Designer {#about-the-email-designer}

The Email Designer allows you to create email content and email content templates. It is compatible with simple emails, transactional emails, A/B test emails, multilingual emails, and recurring emails.

To learn how to design an email from scratch using the Email Designer, watch this [introduction video](https://video.tv.adobe.com/v/22771/?autoplay=true&hidetitle=true).

### Email Designer interface {#email-designer-interface}

The Email Designer provides many options that allow you to create, edit and customize every aspect of your content.

The interface is composed of several areas offering different functionalities:

![](assets/email_designer_overview.png)

From the elements available in the **Palette** (3), drag and drop structure components and content fragments in the main **Workspace** (1). Select a component or element in the **Workspace** (1) and customize its main styling and display characteristics from the **Settings** pane (2).

Access more general options and settings from the main **Toolbar** (4).

>[!NOTE]
>
>The **Settings** pane can move to the left according to your screen resolution and display.

The **Contextual toolbar** of the editor interface offers various functionalities depending on the zone selected. It contains action buttons and buttons that allow you to change the style of the text. The modifications carried out always apply to the zone selected.

### General recommendations for using the Email Designer {#general-recommendations-for-using-the-email-designer}

To make proper use of the Email Designer and create the best emails as simply as possible, we recommend applying the following principles:

* Use inline styling rather than a separate CSS and CSS in the &lt;head&gt; section of the HTML. By using inline styling, you can optimize content fragment save and reuse.

  See [Adding inline styling attributes](../../designing/using/editing-email-styles.md#adding-inline-styling-attributes).

* Settle your branding easily by creating and reusing content fragments to keep consistency across your marketing campaigns.

  See [Creating a content fragment](../../designing/using/defining-the-email-structure.md#creating-a-content-fragment).

Also check the [general best practices for content design](../../designing/using/content-design-best-practices.md).

### Email Designer compatibility mode {#email-designer-compatibility-mode}

When you upload a content, it must contain specific tagging to be fully compliant and editable with the WYSIWYG editor of the Email Designer. For more on this specific tagging, see [this section](../../designing/using/editing-existing-contents-with-the-email-designer.md#html-tagging-to-ensure-compatibility-with-the-email-designer).

If all or part of the uploaded HTML is not compliant with the expected tagging, the content is then loaded in 'compatibility mode', which limits the edition possibilities through the UI.

When a content is loaded in compatibility mode, you can still perform the following modifications through the interface (unavailable actions are hidden):

* Changing the text or changing an image
* Inserting links and personalization fields
* Edit some styling options on the selected HTML block
* Defining conditional content

![](assets/email_designer_compatibility.png)

Other modifications such as adding new sections to your email or advanced styling must be done directly in the source code of the email via the HTML mode.

## Designing an email content from scratch {#designing-an-email-content-from-scratch}

Here are the main steps to create and design an email content from scratch using the Email Designer:

1. Create an email and open its content.
1. Add structure components to shape the email. See [Editing the email structure](../../designing/using/defining-the-email-structure.md#editing-the-email-structure).
1. Insert content components and fragments in the structure components. See [Adding fragments and content components](../../designing/using/defining-the-email-structure.md#adding-fragments-and-content-components).
1. Add images and edit the text of the email. See [Inserting images](../../designing/using/inserting-images.md).
1. Personalize your email by adding personalization fields, links, and so on. See [Inserting a personalization field](../../designing/using/inserting-a-personalization-field.md), [Inserting a link](../../designing/using/inserting-a-link.md) and [Defining dynamic content in an email](../../designing/using/defining-dynamic-content-in-an-email.md).
1. Define the subject line of your email. See [Personalizing the subject line of an email](../../designing/using/personalizing-the-subject-line-of-an-email.md).
1. Preview your email.
1. Save your content, and proceed with your message after making sure that you have defined an audience and properly scheduled the sending.

You can also check out this [introduction video](https://video.tv.adobe.com/v/22771/?autoplay=true&hidetitle=true).

>[!NOTE]
>
>To avoid designing email content from scratch, you can use out-of-the-box content templates. For more on this, see [Content templates](../../start/using/about-templates.md#content-templates).

**Related topics**:

* [Creating an email](../../channels/using/creating-an-email.md)
* [Selecting an existing content](../../designing/using/selecting-an-existing-content.md)
* [Selecting an audience in a message](../../audiences/using/selecting-an-audience-in-a-message.md)
* [Scheduling messages](../../sending/using/about-scheduling-messages.md)
* [Previewing messages](../../sending/using/previewing-messages.md)
* [Email rendering](../../sending/using/email-rendering.md)

## Switching to mobile view {#switching-to-mobile-view}

You can fine-tune the responsive design of an email by separately editing all style options for mobile display. For example, you can adapt margins and padding, use smaller or bigger font sizes or apply different background colors that will be specific to the mobile version of your email.

All style options are available in mobile view. The Email Designer style settings are presented in the [Editing email styles](../../designing/using/editing-email-styles.md) section.

1. Create an email and start editing the content. For more on this, see [Designing an email content from scratch](../../designing/using/about-email-content-design.md#designing-an-email-content-from-scratch).
1. To access the dedicated mobile view, select the **[!UICONTROL Switch to mobile view]** button.

   ![](assets/email_designer_mobile_view_switch.png)

   The mobile version of the email is displayed. It contains all the components and styles that were defined in desktop view.

   ![](assets/email_designer_mobile_view.png)

1. You can edit independently all style settings such as background color, alignment, padding, margin, font family, text color, and so on.
1. When editing any style setting in mobile view, the modifications are only applied to the mobile display.

   For example, reduce the size of an image, add a green background and change the padding in mobile view.

   ![](assets/email_designer_mobile_view_change.png)

1. Click again the **[!UICONTROL Switch to mobile view]** button to go back to the standard desktop view. The style changes you just made are not reflected.

   ![](assets/email_designer_mobile_view_desktop_no-change.png)

   >[!NOTE]
   >
   >The only exception is the **[!UICONTROL Style inline]** settings. Any style inline setting change is also applied to the standard desktop view.

1. However, any other change to the structure or the content of the email such as text edits, uploading a new image, adding a new component, etc. is also applied to the standard view.

   For example, switch back to mobile view, edit some text and replace an image.

   ![](assets/email_designer_mobile_view_change_content.png)

   Click again the **[!UICONTROL Switch to mobile view]** button to go back to the standard desktop view. The changes are reflected.

   ![](assets/email_designer_mobile_view_desktop_content-change.png)

1. Removing a style in mobile view takes you back to the style that was applied in desktop mode.

   For example, in desktop view, apply a grey background color to a button.

   ![](assets/email_designer_mobile_view_background_desktop.png)

1. Switch to mobile view and apply a green background to the same button.

   ![](assets/email_designer_mobile_view_background_mobile.png)

1. While still in mobile view, now disable the **[!UICONTROL Background color]** setting.

   ![](assets/email_designer_mobile_view_background_mobile_disabled.png)

   The background color defined in desktop view is still applied: it turns grey (not blank).

   The only exception is the **[!UICONTROL Border color]** setting. When disabled in mobile view, no border is applied anymore, even if a border color is defined in desktop view.

## Plain text and HTML modes {#plain-text-and-html-modes}

### Generating a text version of the email {#generating-a-text-version-of-the-email}

By default, the **[!UICONTROL Plain text]** version of your email is automatically generated and synchronized with the **[!UICONTROL Edit]** version.

You can disable this synchronization by clicking the **[!UICONTROL Sync with HTML]** switch from the Plain text view of your email.

![](assets/email_designer_textversion.png)

Personalization fields added to the HTML version are also synchronized with the plain text version.

### Editing an email content source in HTML {#editing-an-email-content-source-in-html}

For the most advanced users and debugging, you can view and edit the email content directly in HTML.

You have two ways to edit the HTML version of the email:

* Select **[!UICONTROL Edit]** > **[!UICONTROL HTML]** to open the HTML version of the entire email.

  ![](assets/email_designer_html1.png)

* From the WYSIWYG interface, select an element and click the **[!UICONTROL Source code]** icon.

  Only the source of the selected element is displayed. You can edit the source code if the selected element is a **[!UICONTROL HTML]** content component. Other components are in read-only mode, but can still be edited in the full HTML version of the email.

  ![](assets/email_designer_html2.png)

If you modify the HTML the code, the responsiveness of the email could be broken. Make sure to test it using the **[!UICONTROL Preview]** button. See [Previewing messages with the Email Designer](../../sending/using/previewing-messages.md#previewing-messages-with-the-email-designer).

## Design through Adobe Campaign integrations {#design-through-adobe-campaign-integrations}

### Editing content in Dreamweaver {#editing-content-in-dreamweaver}

The Adobe Campaign Standard integration with Dreamweaver lets you edit an email's content in the Dreamweaver interface. You have access to the powerful interface of Dreamweaver to design and develop responsive email content.

This feature is detailed in the Dreamweaver Documentation accessible [here](https://helpx.adobe.com/dreamweaver/using/working-with-dreamweaver-and-campaign.html). A demonstration [video](https://docs.campaign.adobe.com/doc/standard/en/Videos/ACS_Dreamweaver.mp4) is also available.

### Editing content in Experience Manager {#editing-content-in-experience-manager}

Email content can be edited in Experience Manager and then used for one or several email messages in Adobe Campaign. Refer to [this document](../../integrating/using/integrating-with-experience-manager.md).
