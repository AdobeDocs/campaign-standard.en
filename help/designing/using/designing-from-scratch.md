---
title: Designing emails from scratch 
seo-title: Designing emails from scratch 
description: Designing emails from scratch 
seo-description: Discover how to design emails from scratch email content in the Email Designer.
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

# Designing emails from scratch {#designing-an-email-content-from-scratch}

Learn how to master email content edition. With Email Designer, you can create emails and templates starting with or without your own predefined content. 

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

## Designing using templates {#designing-templates}

### Content templates {#content-templates}

You can manage HTML contents that will be offered in the **[!UICONTROL Templates]** tab of the [Email Designer](../../designing/using/about-email-content-design.md#about-the-email-designer) home page. The different templates present various combinations of several types of elements. For example, 'Feather' templates have margins while 'Astro' templates do not have ones. For more on this, see [Content templates](../../start/using/about-templates.md#content-templates).

![](assets/template_content.png)

To learn how to build an email from an out-of-the-box-template, see [Email Designer](../../designing/using/quick-start.md#building-content-from-an-out-of-the-box-template).

### Creating a template with fragments and components {#template-fragments-components}

You can now create an email template with the Email Designer. Use content components to reflect the different sections of your email and adjust the settings to make them as close as possible to your original newsletter. Finally, insert the fragments that you just created.

1. Using the Email Designer, create a template. For more on this, see [Content templates](../../start/using/about-templates.md#content-templates).
1. Insert several structure components into your template - corresponding to the header, footer and body of your email. For more on adding structure components, see [Editing the email structure with the Email Designer](../../designing/using/defining-the-email-structure.md#editing-the-email-structure).
1. Insert as many content components as needed to create the body of your newsletter. This will be the editable content of your email that you will update every month.

   ![](assets/des_loading_compatible_fragment_5.png)

   If you are familiar with HTML code, Adobe recommends leveraging **[!UICONTROL Html]** components where you can copy-paste the more complex elements of the original email. Use other components such as **[!UICONTROL Button]**, **[!UICONTROL Image]** or **[!UICONTROL Text]** for the rest of the content. For more on this, see [About content components](../../designing/using/defining-the-email-structure.md#about-content-components).

   >[!NOTE]
   >
   >Using the **[!UICONTROL Html]** component results in creating components that are editable with limited options. Make sure you know how to handle HTML code before selecting this component.

1. Adjust the content components to match your original email as much as you can.

   ![](assets/des_loading_compatible_fragment_6.png)

   For more on managing style settings and inline attributes, see [Editing email styles](../../designing/using/editing-email-styles.md).

1. Insert the two fragments (header and footer) that you previously created into the desired structure components.

   ![](assets/des_loading_compatible_fragment_10.png)

1. Save your template.

You can now fully manage this template within the Email Designer to create and update the newsletter that you will send every month to your recipients.

To use it, create an email and select the content template that you just created.

- Save as templates

## Editing the email structure {#editing-the-email-structure}

The Email Designer allows you to easily define the structure of your email. By adding and moving structural elements with simple drag-and-drop actions, you can design the shape of your email within seconds.

### Defining Email Structure {#defining-the-email-structure}

To edit the structure of an email:

1. Open an existing content or create a new email content.
1. Access the **[!UICONTROL Structure components]** by selecting the **+** icon on the left.

   ![](assets/email_designer_structure.png)

1. Drag and drop the structure components that you need to shape your email.

   ![](assets/email_designer_structure_components.png)

   A blue line materializes the exact location of the structure components before you drop it. You can drop it above, between or below any other component, but not inside.

   >[!NOTE]
   >
   >Once placed in the email, you cannot move nor remove your components unless there is already a content component or a fragment placed inside.

1. Several structure components composed of one or more columns are available.

   Select the **[!UICONTROL n:n column]** component to define the number of columns of your choice (between 3 and 10). You can also define the width of each column by moving the arrows at the bottom of each column.

   ![](assets/email_designer_n-n-column.png)

   >[!NOTE]
   >
   >Each column size cannot be under 10% of the total width of the structure component. You cannot remove a column that is not empty.

Once the structure is defined, you are able to add content fragments and components to your email.

### About content components {#about-content-components}

Content components are raw, empty components that you can edit once placed in an email.

You can add as many content components as you want in a structure component. You can also move them inside the structure component or to another structure component.

Here is the list of the available components in the Email Designer:

* **[!UICONTROL Button]**

  If you need to use multiple buttons, rather than editing each button from scratch, you can duplicate the **[!UICONTROL Button]** component using the contextual toolbar.

  You can also save buttons into fragments that can be reused. For more on this, see [Creating a content fragment](../../designing/using/defining-the-email-structure.md#creating-a-content-fragment) and [Saving content as a fragment](../../designing/using/defining-the-email-structure.md#saving-content-as-a-fragment).

* **[!UICONTROL Carousel]**

  For more on this, see [Using the carousel component](../../designing/using/defining-the-email-structure.md#using-the-carousel-component).

* **[!UICONTROL Divider]** 
* **[!UICONTROL Html]**

  Use this component to copy-past the different parts of your existing HTML. This enables you to create free modular HTML components.

  >[!NOTE]
  >
  >A free HTML component is editable with limited options. If all styles are not inlined, make sure to add the proper CSS in the **head** section of the HTML code, otherwise the email will not be responsive. Use the **[!UICONTROL Preview]** button to test the responsiveness of your content (see [Previewing messages](../../sending/using/previewing-messages.md)).

* **[!UICONTROL Image]** 
* **[!UICONTROL Social]** 
* **[!UICONTROL Text]**

#### Using the HTML component {#using-html-component}

To simply make an external content compliant with the Email Designer, Adobe recommends creating a message from scratch and copy the content from your existing email into fragments and components.

When you have a content that cannot be recreated, you can copy-paste the HTML code from the original email using the **[!UICONTROL Html]** content component. Make sure you are familiar with HTML before proceeding.

<!-- A full example is presented below. -->

>[!NOTE]
>
>The new content will not be the exact copy of your original email, but the steps below will guide you through the creation of a message that will be as close as possible.

**Before copying your content**

1. In your original email, identify the reusable sections from the sections that will be unique to each email that you will send.
1. Save all the images and assets that you want to use.
1. If you are familiar with HTML, split your original HTML content into different parts.

#### Using the carousel component {#using-the-carousel-component}

1. Drag and drop the **[!UICONTROL Carousel]** component inside a structure component.
1. Browse to select images from your computer.

   ![](assets/des_carousel_browse.png)

1. From the **[!UICONTROL Settings]** pane, set the number of thumbnails that you want in the carousel.
1. Select a fallback image from your computer.

   ![](assets/des_carousel_fallback.png)

   The carousel component is not compatible with all email programs. Upload a fallback to display an image instead when the carousel is not supported in the email.

   >[!NOTE]
   >
   >The carousel component is compatible with the following email platforms: Apple Mail 7, Apple Mail 8, Outlook 2011 for Mac, Outlook 2016 for Mac, Mozilla Thunderbird, iPad and iPad mini iOS, iPhone iOS, Android, AOL (Chrome, Firefox and Safari).

1. Select **[!UICONTROL Fallback view]** to display the fallback image in the Email Designer.

### About fragments {#about-fragments}

A fragment is a reusable component that can be referenced in one or more emails.
They can be found in the interface under **Resources** > **Content fragments and templates**. 

To make the best use of fragments in the Email Designer:

* Create your own fragments. See [Creating a content fragment](../../designing/using/defining-the-email-structure.md#creating-a-content-fragment) and [Saving content as a fragment](../../designing/using/defining-the-email-structure.md#saving-content-as-a-fragment).
* Use them as many times as needed in your emails. See [Inserting elements into an email](../../designing/using/defining-the-email-structure.md#inserting-elements-into-an-email).
* When you edit a fragment, the changes are synchronized: they are automatically propagated to all emails (provided they have not been prepared or sent yet) containing that fragment.

When added to an email, fragments are locked by default. If you want to modify a fragment for a specific email, you can break the synchronization with the original fragment by unlocking it in the email where it is used. The changes will not be synchronized anymore.

To unlock a fragment inside an email, select it and click the lock icon from the contextual toolbar.

![](assets/des_unlocking_fragment.png)

That fragment becomes a standalone component that is not linked anymore to the original fragment. It can then be edited as any other content component. See [About content components](../../designing/using/defining-the-email-structure.md#about-content-components).

#### Inserting fragments into an email {#inserting-elements-into-an-email}

To define the content of your email, you can add content elements in the structure components you have placed beforehand. See [Editing the email structure](../../designing/using/defining-the-email-structure.md#editing-the-email-structure).

1. Access the content elements by selecting the **+** icon on the left. Select [Fragments](../../designing/using/defining-the-email-structure.md#about-fragments) or [Content components](../../designing/using/defining-the-email-structure.md#about-content-components).
1. If you already know the label or part of the label of the fragment you want to add, you can search for it.

   ![](assets/email_designer_fragmentsearch.png)

1. Drag and drop a fragment or content component from the palette to a structure component of the email.

   ![](assets/email_designer_addfragment.png)

   Once an element is added to the email, it can be moved inside the structure component or to another structure component in the email.

   ![](assets/email_designer_movefragment.png)

1. Edit the element to match the exact needs of this email. You can add text, links, images, and so on.

   >[!NOTE]
   >
   >Fragments are locked by default when added to an email. You can break the synchronization with the original fragment if you want to modify the fragment for a specific email, or make your change directly in the fragment. See [About fragments](../../designing/using/defining-the-email-structure.md#about-fragments).

1. Repeat this procedure for all elements you need to add to your email.
1. Save your email.

Now that your email structure is populated, you can edit the style of each content element. See [Editing an element](../../designing/using/editing-email-styles.md#editing-an-element).

>[!NOTE]
>
>If a fragment is modified, the changes are automatically propagated in the emails where it is used. For more on this, see [About fragments](../../designing/using/defining-the-email-structure.md#about-fragments).

#### Creating a content fragment {#creating-a-content-fragment}

You can create your own content fragments to use them as needed in one or more emails.

1. Go to **[!UICONTROL Resources]** > **[!UICONTROL Content templates & fragments]** and click **[!UICONTROL Create]**.
1. Click the email label to access the **[!UICONTROL Properties]** tab of the Email Designer.
1. Specify a recognizable label and select the following parameters to find the fragment later in new emails:

    * Because fragments are only compatible with emails, select **[!UICONTROL Delivery]** from the **[!UICONTROL Content type]** drop-down list.
    * Select **[!UICONTROL Fragment]** from the **[!UICONTROL HTML type]** drop-down list to be able to use this content as a fragment in your emails.

   ![](assets/email_designer_createfragment.png)

1. If needed, you can set an image that will be used as a thumbnail for the fragment. Select it from the **[!UICONTROL Thumbnail]** tab of the template properties.

   ![](assets/email_designer_createfragment_thumbnail.png)

   This thumbnail will be displayed next to the fragment's label when editing an email.

1. Save your changes to return to the main workspace.
1. Add a structure component and a content component that you can customize as needed.
1. Once edited, save your fragment.

The fragment can now be used in any email built with the Email Designer. It appears under the **[!UICONTROL Fragments]** section of the Palette.

>[!NOTE]
>
>You cannot insert personalization fields inside a fragment unless it is used in an email. To do this, you need to unlock this fragment. See [About fragments](../../designing/using/defining-the-email-structure.md#about-fragments).

#### Saving content as a fragment {#saving-content-as-a-fragment}

When editing an email with the Email Designer, you can directly save part of that email as a fragment.

>[!CAUTION]
>
>You cannot save as fragment a structure containing personalization fields, dynamic content or another fragment.

1. When editing an email in the Email Designer, select **[!UICONTROL Save as fragment]** from the main toolbar.

   ![](assets/email_designer_save-as-fragment.png)

1. From the workspace, select the structures that will compose the fragment.

    ![](assets/email_designer_save-as-fragment_select.png)

    >[!NOTE]
    >
    >You can only select structures that are adjacent to each other.

1. Click **[!UICONTROL Create]**.

1. Add a label and a description if needed, then click **[!UICONTROL Save]**.

    ![](assets/email_designer_save-as-fragment_popup.png)

1. To find the fragment that you just created, go to **[!UICONTROL Resources]** > **[!UICONTROL Content templates & fragments]**.

    ![](assets/email_designer_save-as-fragment_list.png)

1. To use your new fragment, open any email content and select it from the fragment list.

![](assets/email_designer_save-as-fragment_in-new-email.png)

**Related topics**:

* [Creating an email](../../channels/using/creating-an-email.md)
* [Selecting an existing content](../../designing/using/selecting-an-existing-content.md)
* [Selecting an audience in a message](../../audiences/using/selecting-an-audience-in-a-message.md)
* [Scheduling messages](../../sending/using/about-scheduling-messages.md)
* [Previewing messages](../../sending/using/previewing-messages.md)
* [Email rendering](../../sending/using/email-rendering.md)
