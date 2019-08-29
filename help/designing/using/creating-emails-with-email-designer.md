---
title: Creating emails using the Email Designer
seo-title: About email designer
description: About email designer
seo-description: Discover the Email Designer that enables you to design content for your emails.
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

## Designing an email content from scratch {#designing-an-email-content-from-scratch}

Here are the main steps to create and design an email content from scratch using the Email Designer:

1. Create an email and open its content.
1. Add structure components to shape the email. See [Editing the email structure](../../designing/using/defining-the-email-structure.md#editing-the-email-structure).
1. Insert content components and fragments in the structure components. See [Adding fragments and content components](../../designing/using/designing-from-scratch.md#editing-the-email-structure).
1. Add images and edit the text of the email. See [Inserting images](../../designing/using/inserting-images.md).
1. Personalize your email by adding personalization fields, links, and so on. See [Inserting a personalization field](../../designing/using/inserting-a-personalization-field.md), [Inserting a link](../../designing/using/inserting-a-link.md) and [Defining dynamic content in an email](../../designing/using/defining-dynamic-content-in-an-email.md).
1. Define the subject line of your email. See [Personalizing the subject line of an email](../../designing/using/personalizing-the-subject-line-of-an-email.md).
1. Preview your email.
1. Save your content, and proceed with your message after making sure that you have defined an audience and properly scheduled the sending.

You can also check out this [introduction video](https://video.tv.adobe.com/v/22771/?autoplay=true&hidetitle=true).

>[!NOTE]
>
>To avoid designing email content from scratch, you can use out-of-the-box content templates. For more on this, see [Content templates](../../start/using/about-templates.md#content-templates).

## Editing the email structure {#editing-the-email-structure}

The Email Designer allows you to easily define the structure of your email. By adding and moving structural elements with simple drag-and-drop actions, you can design the shape of your email within seconds.

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

## Adding fragments and content components {#adding-fragments-and-content-components}

With the Email Designer, after adding structure components to your email, you can define their content. To do that, you need to add elements inside each structure component.

There are two categories of content elements that you can use: **fragments** and **content components**.

### About content components {#about-content-components}

Content components are raw, empty components that you can edit once placed in an email.

You can add as many content components as you want in a structure component. You can also move them inside the structure component or to another structure component.

Here is the list of the available components in the Email Designer:

* **[!UICONTROL Button]**

  If you need to use multiple buttons, rather than editing each button from scratch, you can duplicate the **[!UICONTROL Button]** component using the contextual toolbar.

  You can also save buttons into fragments that can be reused. For more on this, see [Creating a content fragment](../../designing/using/designing-from-scratch.md#creating-a-content-fragment) and [Saving content as a fragment](../../designing/using/designing-from-scratch.md#saving-content-as-a-fragment).

* **[!UICONTROL Carousel]**

  For more on this, see [Using the carousel component](../../designing/using/designing-from-scratch.md#using-the-carousel-component).

* **[!UICONTROL Divider]** 
* **[!UICONTROL Html]**

  Use this component to copy-past the different parts of your existing HTML. This enables you to create free modular HTML components.

  >[!NOTE]
  >
  >A free HTML component is editable with limited options. If all styles are not inlined, make sure to add the proper CSS in the **head** section of the HTML code, otherwise the email will not be responsive. Use the **[!UICONTROL Preview]** button to test the responsiveness of your content (see [Previewing messages](../../sending/using/previewing-messages.md)).

* **[!UICONTROL Image]** 
* **[!UICONTROL Social]** 
* **[!UICONTROL Text]**

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

**Related topics**:

* [Creating an email](../../channels/using/creating-an-email.md)
* [Selecting an existing content](../../designing/using/selecting-an-existing-content.md)
* [Selecting an audience in a message](../../audiences/using/selecting-an-audience-in-a-message.md)
* [Scheduling messages](../../sending/using/about-scheduling-messages.md)
* [Previewing messages](../../sending/using/previewing-messages.md)
* [Email rendering](../../sending/using/email-rendering.md)


## Designing and using reusable content

### Designing reusable content 

#### About fragments {#about-fragments}

A fragment is a reusable component that can be referenced in one or more emails.

To make the best use of fragments in the Email Designer:

* Create your own fragments. See [Creating a content fragment](../../designing/using/designing-from-scratch.md#creating-a-content-fragment) and [Saving content as a fragment](../../designing/using/designing-from-scratch.md#saving-content-as-a-fragment).
* Use them as many times as needed in your emails. See [Inserting elements into an email](../../designing/using/designing-from-scratch.md#inserting-elements-into-an-email).
* When you edit a fragment, the changes are synchronized: they are automatically propagated to all emails (provided they have not been prepared or sent yet) containing that fragment.

When added to an email, fragments are locked by default. If you want to modify a fragment for a specific email, you can break the synchronization with the original fragment by unlocking it in the email where it is used. The changes will not be synchronized anymore.

To unlock a fragment inside an email, select it and click the lock icon from the contextual toolbar.

![](assets/des_unlocking_fragment.png)

That fragment becomes a standalone component that is not linked anymore to the original fragment. It can then be edited as any other content component. See [About content components](../../designing/using/designing-from-scratch.md#about-content-components).

#### Inserting elements into an email {#inserting-elements-into-an-email}

To define the content of your email, you can add content elements in the structure components you have placed beforehand. See [Editing the email structure](../../designing/using/defining-the-email-structure.md#editing-the-email-structure).

1. Access the content elements by selecting the **+** icon on the left. Select [Fragments](../../designing/using/designing-from-scratch.md#about-fragments) or [Content components](../../designing/using/designing-from-scratch.md#about-content-components).
1. If you already know the label or part of the label of the fragment you want to add, you can search for it.

   ![](assets/email_designer_fragmentsearch.png)

1. Drag and drop a fragment or content component from the palette to a structure component of the email.

   ![](assets/email_designer_addfragment.png)

   Once an element is added to the email, it can be moved inside the structure component or to another structure component in the email.

   ![](assets/email_designer_movefragment.png)

1. Edit the element to match the exact needs of this email. You can add text, links, images, and so on.

   >[!NOTE]
   >
   >Fragments are locked by default when added to an email. You can break the synchronization with the original fragment if you want to modify the fragment for a specific email, or make your change directly in the fragment. See [About fragments](../../designing/using/designing-from-scratch.md#about-fragments).

1. Repeat this procedure for all elements you need to add to your email.
1. Save your email.

Now that your email structure is populated, you can edit the style of each content element. See [Editing an element](../../designing/using/styles.md#editing-an-element).

>[!NOTE]
>
>If a fragment is modified, the changes are automatically propagated in the emails where it is used. For more on this, see [About fragments](../../designing/using/designing-from-scratch.md#about-fragments).

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
>You cannot insert personalization fields inside a fragment unless it is used in an email. To do this, you need to unlock this fragment. See [About fragments](../../designing/using/designing-from-scratch.md#about-fragments).

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


## Designing an email using existing contents {#designing-an-email-using-existing-contents}

This section explains how to convert an existing email into an Email Designer-compatible email.

By default, if you just upload any HTML (see [Importing content from a file](../../designing/using/importing-content-from-a-file.md)), the content is loaded in '[compatibility mode](../../designing/using/using-existing-content.md#compatibility-mode)', which limits the edition possibilities through the UI (only in-place edition, no drag-and-drop).

However, if you want to build a framework of modular templates and fragments that can be combined to reuse in multiple emails, you should consider converting your email HTML into an Email Designer template.

When designing content with the Email Designer, you have three options:

* [Building content from an out-of-the-box template](../../designing/using/quick-start.md#building-content-from-an-out-of-the-box-template )
* [Using fragments and components](../../designing/using/designing-from-scratch.md), start from scratch and recreate an HTML design
* [Converting an HTML content](../../designing/using/using-existing-content.md#converting-an-html-content) email into a modular Email Designer content

### Building content from an out-of-the-box template {#building-content-from-an-out-of-the-box-template}

1. Create an email and open its content. For more on this, see [Creating an email](../../channels/using/creating-an-email.md).
1. Click the home icon to access the **[!UICONTROL Email Designer]** home page.
1. Click the **[!UICONTROL Templates]** tab.
1. Choose an out-of-the-box HTML template.

   The different templates present various combinations of several types of elements. For example, 'Feather' templates have margins while 'Astro' templates do not have ones. For more on this, see [Content templates](../../start/using/about-templates.md#content-templates).

1. You can combine these elements to build a number of email variants. For example, you can duplicate an email section by selecting a structure component and clicking **[!UICONTROL Duplicate]** from the contextual toolbar.
1. You can move the elements around using the blue arrow on the left to drag a structure component below or above another. For more on this, see [Editing the email structure](../../designing/using/defining-the-email-structure.md#editing-the-email-structure).
1. You can also move components around to change the organization of each structure element. For more on this, see [Adding fragments and components](../../designing/using/designing-from-scratch.md#editing-the-email-structure).
1. Modify the content of each element according to your needs: images, text, links.
1. Adapt the styling options to your content if needed. For more on this, see [Editing email styles](../../designing/using/editing-email-styles.md).

### Using fragments and components {#using-fragments-and-components}

To simply make an external content compliant with the Email Designer, Adobe recommends creating a message from scratch and copy the content from your existing email into fragments and components.

When you have a content that cannot be recreated, you can copy-paste the HTML code from the original email using the **[!UICONTROL Html]** content component. Make sure you are familiar with HTML before proceeding.

A full example is presented below.

>[!NOTE]
>
>The new content will not be the exact copy of your original email, but the steps below will guide you through the creation of a message that will be as close as possible.

Let's say that you want to use an existing newsletter that was created outside of Adobe Campaign.

You want to have the same header and footer in all the emails that you will send with Adobe Campaign. The body of the email will change according to the content that you intend to display in each newsletter.

**Prerequisites**

1. In your original email, identify the reusable sections from the sections that will be unique to each email that you will send.
1. Save all the images and assets that you want to use.
1. If you are familiar with HTML, split your original HTML content into different parts.

**Creating fragments for your reusable content**

Using the Email Designer, create a fragment for each reusable section. In this example, you will create two fragments: one for the header and one for the footer. You can then copy the relevant parts from your existing content into these fragments.

To do this, follow the steps below:

1. In Adobe Campaign, go to **[!UICONTROL Resources]** > **[!UICONTROL Content templates & fragments]** and create a fragment for your header. For more on this, see [Creating a content fragment](../../designing/using/designing-from-scratch.md#creating-a-content-fragment).
1. Add as many structure components as you need to your fragment.

   ![](assets/des_loading_compatible_fragment_1.png)

1. Insert image and text components into your structure.

   ![](assets/des_loading_compatible_fragment_2.png)

1. Upload the corresponding image, enter your text and adjust the settings.

   For more on managing style settings and inline attributes, see [Editing email styles](../../designing/using/editing-email-styles.md).

   ![](assets/des_loading_compatible_fragment_3.png)

1. Save your fragment.
1. Proceed similarly to create your footer and save it.

   ![](assets/des_loading_compatible_fragment_4.png)

   If you are familiar with HTML, you can copy-paste the HTML code from the original footer using the **[!UICONTROL Html]** content component. For more on this, see [About content components](../../designing/using/designing-from-scratch.md#about-content-components).

   ![](assets/des_loading_compatible_fragment_9.png)

Your fragments are now ready to be used in a template.

**Inserting fragments and components into your template**

You can now create an email template with the Email Designer. Use content components to reflect the different sections of your email and adjust the settings to make them as close as possible to your original newsletter. Finally, insert the fragments that you just created.

1. Using the Email Designer, create a template. For more on this, see [Content templates](../../start/using/about-templates.md#content-templates).
1. Insert several structure components into your template - corresponding to the header, footer and body of your email. For more on adding structure components, see [Editing the email structure with the Email Designer](../../designing/using/defining-the-email-structure.md#editing-the-email-structure).
1. Insert as many content components as needed to create the body of your newsletter. This will be the editable content of your email that you will update every month.

   ![](assets/des_loading_compatible_fragment_5.png)

   If you are familiar with HTML code, Adobe recommends leveraging **[!UICONTROL Html]** components where you can copy-paste the more complex elements of the original email. Use other components such as **[!UICONTROL Button]**, **[!UICONTROL Image]** or **[!UICONTROL Text]** for the rest of the content. For more on this, see [About content components](../../designing/using/designing-from-scratch.md#about-content-components).

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

**Related topic**:

* [Creating an email](../../channels/using/creating-an-email.md)
* [Introduction video to the Email Designer](https://video.tv.adobe.com/v/22771/?autoplay=true&hidetitle=true)
* [Designing an email content from scratch](../../designing/using/designing-from-scratch.md#designing-an-email-content-from-scratch)

## Importing 

### Importing content from a file{#importing-content-from-a-file}

From the Email Designer home page, click the **[!UICONTROL Upload]** button to upload a file from your computer, then confirm.

There are no constraints on the zip file structure. However, referencing HTML files has to be relative and respect the tree structure of the zip folder.

The following formats are supported for import:

* An HTML file with an incorporated style sheet
* A .zip folder containing the HTML file, the style sheet (.CSS) and the images

>[!NOTE]
>
>For email content, we recommend that you import single HTML files with an incorporated style sheet.

# Importing content from a URL{#importing-content-from-a-url}

Before importing content from a URL, make sure it follows the requirements below:

* The content needs to be publicly available via this URL.
* For security reasons, only URLs beginning with **[!UICONTROL https]** are allowed.
* Make sure that all resources (images, CSS) are set in absolute links and in HTTPS. Otherwise, after sending the email, the mirror page would be displayed without its resources. Here is an example of an absolute link definition:

  ```
  <a href="https://www.mywebsite.com/images/myimage.png">
  ```

>[!NOTE]
>
>Loading content from a URL is available for the email channel only.

To retrieve existing content form a URL, follow the steps below:

1. From the Email Designer home page, select the **[!UICONTROL Import from URL]** button.

   ![](assets/email_designer_importfromurl.png)

1. Define the URL from which the content will be retrieved.
1. Click **[!UICONTROL Confirm]**.

**Related topic:**

[Importing content from a URL](https://helpx.adobe.com/campaign/kt/acs/using/acs-email-designer-tutorial.html#Workingwithexistingcontent) video

## Retrieving content from a URL automatically at preparation time {#retrieving-content-from-a-url-automatically-at-preparation-time}

Importing content from a URL during message preparation enables you to retrieve the latest HTML content each time the email is prepared. This way, the content of recurring emails is always up-to-date at the time of their sending. This feature also enables you to create a message scheduled at a specific date, even if the content is not ready yet.

To retrieve content at preparation time, follow the steps below:

1. Select the **[!UICONTROL Content imported during preparation]** option.

   ![](assets/email_designer_importfromurl2.png)

1. The URL content displays in the editor as read-only.

   >[!CAUTION]
   >
   >At this step, the HTML display in the content editor should not be taken into account. It will be retrieved at the preparation phase.

1. To preview the URL content that has been retrieved, open the message once it is created then click the **[!UICONTROL Preview]** button.

It is possible to personalize the remote URL from which the content will be retrieved. To do this, follow the steps below:

1. Click the email label on top of the screen to acces the Email Designer **[!UICONTROL Properties]** tab.
1. Find the **[!UICONTROL Remote URL]** field.

   ![](assets/email_designer_importfromurl4.png)

1. Insert the desired personalization field, content block or dynamic text.

   The **[!UICONTROL Current date - YYYYMMDD]** content block, for example, enables you to insert the date of the day.

   >[!NOTE]
   >
   >The available personalization fields are linked to **Delivery** attributes only (email creation date, status, campaign label...).

   ## Design through Adobe Campaign integrations {#design-through-adobe-campaign-integrations}

### Editing content in Dreamweaver {#editing-content-in-dreamweaver}

The Adobe Campaign Standard integration with Dreamweaver lets you edit an email's content in the Dreamweaver interface. You have access to the powerful interface of Dreamweaver to design and develop responsive email content.

* **Bidirectional syncing**

  Whenever an edit is made in one product, it is updated in real time in the other. If you want to change the color of text in Dreamweaver, as soon as you make that edit, the color of the text is live in Campaign. Additionally, when you select code in either Dreamweaver or Campaign, since the line numbers are the same, the selection remains between the two products, which is very useful when looking for something specific in the code.

* **Upload local images to AC through Dreamweaver**

  When creating or editing an email within Dreamweaver, you can simply select an image from your desktop or local machine. While Dreamweaver has always allowed you to do this, when Dreamweaver and Campaign are connected, the local file is immediately uploaded to the Adobe Campaign server: no need to manually upload images as content changes. Additionally, it ensures that the latest images are always live in Campaign.

* **Add Campaign personalization in Dreamweaver**

  For the email developer there is no longer a need to add text like [[FIRSTNAME_PLACEHOLDER]] nor to look up the syntax of your data model’s tables. The Campaign toolbar in Dreamweaver connects directly to your Campaign instance's data model. That means you can pull in any data you want for personalization from something like First Name to Address. If you’ve created Content Blocks within Campaign, you can also pull those directly into Dreamweaver.

This capability is detailed in the Dreamweaver Documentation accessible [here](https://helpx.adobe.com/dreamweaver/using/working-with-dreamweaver-and-campaign.html). A demonstration [video](https://helpx.adobe.com/campaign/kt/acs/using/acs-dreamweaver-integration-feature-video-use.html) is also available.

### Editing content in Experience Manager {#editing-content-in-experience-manager}

Email content can be edited in Experience Manager and then used for one or several email messages in Adobe Campaign Standard. Refer to [this document](../../integrating/using/integrating-with-experience-manager.md).

### Email design options comparison {#email-design-options-comparison}

Adobe Campaign offers several email authoring options. The table below shows the main possibilities, benefits and limitations for each of them.

<table> 
 <thead> 
  <tr> 
   <th> </th> 
   <th> Email Designer<br /> </th> 
   <th> Experience Manager<br /> </th> 
   <th> Dreamweaver<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <strong>Start blank email</strong><br /> </td> 
   <td> Supported<br /> </td> 
   <td> Supported<br /> </td> 
   <td> Supported<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Write HTML</strong><br /> </td> 
   <td> Supported<br /> </td> 
   <td> Not supported<br /> </td> 
   <td> Supported<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Update HTML</strong><br /> </td> 
   <td> Only inside an HTML component<br /> </td> 
   <td> Not supported<br /> </td> 
   <td> Supported<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Basic personalization</strong><br /> </td> 
   <td> Supported<br /> </td> 
   <td> Supported<br /> </td> 
   <td> Supported<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Advanced personalization</strong><br /> </td> 
   <td> Supported<br /> </td> 
   <td> Not supported<br /> </td> 
   <td> Not supported<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Proof/Preview</strong><br /> </td> 
   <td> Supported<br /> </td> 
   <td> Preview in AEM<br /> Proof in Campaign<br /> </td> 
   <td> Preview and proof in Campaign<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Product listings</strong><br /> </td> 
   <td> Supported in email transactional messages<br /> </td> 
   <td> Not supported<br /> </td> 
   <td> Not supported<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Benefits</strong><br /> </td> 
   <td> 
     - Easy email building through drag-and-drop experience<br/>
     - Functionalities similar to legacy content editor<br/>
     - Reusable content with fragments
  </td> 
   <td> 
     - Reusing assets from website in emails<br/>
     - Leveraging the power of Experience Manager in email contents
    </td> 
   <td> 
    - Capability for a developer to directly code an email<br/>
    - Bi-directional synchronization<br/>
    - Editing offline in Dreamweaver and synchronizing later<br/>
    - Uploading images to Adobe Campaign through Dreamweaver
  </td> 
  </tr> 
  <tr> 
   <td> <strong>Limitations</strong><br /> </td> 
   <td> 
     - No conditional content within fragments<br/>
     - Using Experience Manager fragments not possible
  </td> 
   <td> 
     - Advanced personalization difficult to implement<br/>
     - Need to send tests in Adobe Campaign
  </td> 
   <td> Dynamic content not supported<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Audience</strong><br /> </td> 
   <td> Marketers who want to keep the flexibility to use HTML components in combination with drag-and-drop features<br /> </td> 
   <td> Marketers already using Experience Manager who want to use standard email templates with little personalization<br /> </td> 
   <td> Developers who want to code email contents and integrate directly with Adobe Campaign<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>To learn more</strong><br /> </td> 
   <td> See <a href="../../designing/using/about-email-content-design.md#about-the-email-designer">About the Email Designer</a><br /> </td> 
   <td> See <a href="../../integrating/using/integrating-with-experience-manager.md">Integrating with Experience Manager</a><br /> </td> 
   <td> See <a href="https://helpx.adobe.com/dreamweaver/using/working-with-dreamweaver-and-campaign.html">Dreamweaver and Campaign</a> and watch this <a href="https://helpx.adobe.com/campaign/kt/acs/using/acs-dreamweaver-integration-feature-video-use.html">video</a><br /> </td> 
  </tr> 
 </tbody> 
</table>

## Plain text and HTML modes {#plain-text-and-html-modes}

### Generating a text version of the email {#generating-a-text-version-of-the-email}

By default, the **[!UICONTROL Plain text]** version of your email is automatically generated and synchronized with the **[!UICONTROL Edit]** version.

Personalization fields and content blocks added to the HTML version are also synchronized with the plain text version.

>[!NOTE]
>
>To use content blocks in plain text version, make sure they do not contain HTML code.

To have a plain text version different from the HTML version, you can disable this synchronization by clicking the **[!UICONTROL Sync with HTML]** switch from the **[!UICONTROL Plain text]** view of your email.

![](assets/email_designer_textversion.png)

You can then edit the plain text version as desired.

>[!NOTE]
>
>If you edit the **[!UICONTROL Plain text]** version while synchronization is disabled, the next time you enable the **[!UICONTROL Sync with HTML]** option, all the changes you made in the plain text version will be replaced with the HTML version. The changes made in **[!UICONTROL Plain text]** view cannot be reflected in **[!UICONTROL HTML]** view.

### Editing an email content source in HTML {#editing-an-email-content-source-in-html}

For the most advanced users and debugging, you can view and edit the email content directly in HTML.

You have two ways to edit the HTML version of the email:

* Select **[!UICONTROL Edit]** > **[!UICONTROL HTML]** to open the HTML version of the entire email.

  ![](assets/email_designer_html1.png)

* From the WYSIWYG interface, select an element and click the **[!UICONTROL Source code]** icon.

  Only the source of the selected element is displayed. You can edit the source code if the selected element is a **[!UICONTROL HTML]** content component. Other components are in read-only mode, but can still be edited in the full HTML version of the email.

  ![](assets/email_designer_html2.png)

If you modify the HTML the code, the responsiveness of the email could be broken. Make sure to test it using the **[!UICONTROL Preview]** button. See [Previewing messages](../../sending/using/previewing-messages.md).