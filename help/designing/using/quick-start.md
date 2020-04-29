---
title: Get started with the Email Designer
description: Start building email content with the Email Designer.
page-status-flag: never-activated
uuid: 571ffc01-6e41-4501-9094-2f812b041a10
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: editing-email-content
discoiquuid: 39b86fda-7766-4e5f-ab48-bcc536ab66b3

internal: n
snippet: y
---
# Get started with the Email Designer {#quick-start}

The Email Designer provides four ways to create emails.

You can create an email [starting fresh in the Email Designer](#without-existing-content):

1. You can **create an email from a blank canvas** by easily adding structure and content components and personalize their content to send a delivery quickly. You can also fully manage style elements. For more information, [get started quickly](#from-scratch-email) or see the [complete documentation](../../designing/using/designing-from-scratch.md#designing-an-email-content-from-scratch).

1. You can **create an email from an out-of-the-box template** by selecting a template and building your new email content from here. [Learn more](#building-content-from-an-out-of-the-box-template)

You can also create an email [with existing content](#with-existing-content):

1. You can **convert an existing HTML content** (created externally or in the legacy editor). [Learn more](#converting-an-html-content)
1. You can **import an existing HTML content** straight away in compatibility mode. [Learn more](#compatibility-mode)

| Without content   | With content   |
|---|---|
| [Creating an email from scratch](#from-scratch-email)  | [Converting an existing HTML content](#converting-an-html-content)  |
| [Building content from an out-of-the-box template](#building-content-from-an-out-of-the-box-template)  | [Importing an existing HTML](#compatibility-mode) |

## Designing emails with the editor {#without-existing-content}

>[!NOTE]
>
>In both creation strategy, it is crucial to fill in the subject line before sending your email. Learn how to [Add a subject line](#add-a-subject-line).

### Creating an email from scratch {#from-scratch-email}

You can create an email easily, add components and personalize their content to send a delivery quickly. You can adapt the styling options to your content if needed. For more on managing style settings and inline attributes, see [Editing email styles](../../designing/using/styles.md).

1. Create an email.
1. Close homepage.

### Adding a subject line {#add-a-subject-line}

Subject lines are mandatory when sending an email. For more information, see [Defining the subject line of an email](../../designing/using/subject-line.md).

1. Go the **[!UICONTROL Properties]** tab of the Email Designer home page (accessible through the home icon) and fill in the **[!UICONTROL Subject]** section.

![](assets/subject-line-quick-start.png)

### Adding structure components {#add-structure-components}

Structure components will define the layout of your email. For more information, see [Defining the structure of an email](../../designing/using/designing-from-scratch.md#defining-the-email-structure).

In Structure components, drag and drop components for the layout you want to use.

>[!NOTE]
>
>You can select different content layouts that will add up in your email.

![](assets/structure-components-quick-start.png)

### Adding content components {#add-content-components}

You can add several content components to your email such as image, text and buttons. For more information, see [Content components](../../designing/using/designing-from-scratch.md#about-content-components).

* **Image**

1. In **Content Components**, drag and drop image into one of your structure components.
1. Click **Browse**.
1. Select your image file from your computer.

![](assets/browse-image-quick-start.png)

* **Text with personalization**

1. In **Content Components**, drag and drop text into one of your structure components.
1. Click on the component and enter your text. 
1. To add a personalization field, click **Insert personalization field** in the toolbar.
1. Select the field you need, such as First Name.

![](assets/edit-text-quick-start.png)

* **HTML**

1. In **Content Components**, drag and drop HTML into one of your structure components.
1. Click **Show the source code**.
1. Enter your HTML content.
1. Click **Save**.

![](assets/html-component-source-code.png)

If you are familiar with HTML, you can copy-paste the HTML code from the original footer using the **[!UICONTROL Html]** content component. For more on this, see [About content components](../../designing/using/designing-from-scratch.md#about-content-components).

![](assets/des_loading_compatible_fragment_9.png)

### Styling your email component

You can adjust your email styling, for example by changing the padding of a component. For more on managing style settings and inline attributes, see [Editing email styles](../../designing/using/styles.md). 

1. Click on your **Text component**. 
1. On the right, in the palette, go to **Padding**.
1. Click the lock icon to break synchronization between top and bottom or right and left parameters. 
1. Adjust **Padding** as you need. 
1. Click **Save**. 

![](assets/padding-quick-start.png)

You can now save and send your email.

### Building content from an out-of-the-box template {#building-content-from-an-out-of-the-box-template}

You can build an email from out-of-the-box templates such as customer welcome messages, newsletters and reengagement emails and personalize them.

1. Create an email and open its content. For more on this, see [Creating an email](../../channels/using/creating-an-email.md).
1. Click the home icon to access the **[!UICONTROL Email Designer]** home page.
1. Click the **[!UICONTROL Templates]** tab.
1. Choose an out-of-the-box HTML template.
    The different templates present various combinations of several types of elements. For example, 'Feather' templates have margins while 'Astro' templates do not have ones. For more on this, see [Content templates](../../designing/using/using-reusable-content.md#content-templates).
1. Go the **[!UICONTROL Properties]** tab of the Email Designer home page (accessible through the home icon) and fill in the **[!UICONTROL Subject]** section.
1. You can combine these elements to build a number of email variants. For example, you can duplicate an email section by selecting a structure component and clicking **[!UICONTROL Duplicate]** from the contextual toolbar.
1. You can move the elements around using the blue arrow on the left to drag a structure component below or above another. For more on this, see [Editing the email structure](../../designing/using/designing-from-scratch.md#defining-the-email-structure).
1. You can also move components around to change the organization of each structure element. For more on this, see [Adding fragments and components](../../designing/using/designing-from-scratch.md#defining-the-email-structure).
1. Modify the content of each element according to your needs: images, text, links.
1. Adapt the styling options to your content if needed. For more on this, see [Editing email styles](../../designing/using/styles.md).

## Using an existing email content {#with-existing-content}

If you want to build a framework of modular templates and fragments that can be combined to reuse in multiple emails, you should consider converting your email HTML into an Email Designer template.

### Converting HTML content {#converting-an-html-content}

This use case offers a quick way to convert HTML email into Email Designer components. For more on this topic, see [Converting HTML content](../../designing/using/using-existing-content.md#converting-an-html-content).

>[!CAUTION]
>
>This section is for users who are familiar with HTML code.

>[!NOTE]
>
>Like the compatibility mode, a HTML component is editable with limited options: you can only perform in-place edition.


### Importing and editing an HTML email {#compatibility-mode}

When you upload a content, it must contain specific tagging to be fully compliant and editable with the WYSIWYG editor of the Email Designer.

For more on converting an existing email into an Email Designer-compatible email, see [this section](../../designing/using/using-existing-content.md#compatibility-mode).
