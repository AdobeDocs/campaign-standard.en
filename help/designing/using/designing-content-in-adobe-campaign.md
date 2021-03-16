---
solution: Campaign Standard
product: campaign
title: Designing content in Adobe Campaign
description: Create email content starting from scratch, importing HTML or leveraging existing templates.
audience: designing
content-type: reference
topic-tags: about-content-design

feature: Email Design
role: Business Practitioner
level: Beginner
---

# Campaign Email Designer{#designing-content-in-adobe-campaign}

Once you have created an email in Adobe Campaign, you need to define its content.

The Email Designer enables you to create captivating, individually tailored emails through a drag and drop
interface. Whether you're starting from a blank slate, or leveraging existing content fragments or templates, design and refine all content for every email, whether promotional or transactional.

Built to deliver HTML optimized for responsive design, the Email Designer allows you to easily define and apply visibility conditions and dynamic content to an email, template, or fragment directly through the user interface. You can seamlessly switch betwing the drag and drop interface and HTML code at the click of a button.

The Email Designer allows you to create email content and email content templates. It is compatible with simple emails, transactional emails, A/B test emails, multilingual emails, and recurring emails.

<!--The Email Designer has more features than the Legacy Editor and is backward compatible.-->

![](assets/do-not-localize/how-to-video.png) [Discover the Email Designer in video](#video)

* To discover how to create email content, see [Get started with the Email Designer](../../designing/using/quick-start.md).
* For an overview of the Email Designer, see [Using the Email Designer](../../designing/using/designing-content-in-adobe-campaign.md).
* For more on building content:
  * From scratch, see [Designing emails from scratch](../../designing/using/designing-from-scratch.md).
  * Using existing content, see [Designing using existing content](../../designing/using/using-existing-content.md).
  * Using Creative Cloud integrations, see [Multi-solution email design](../../designing/using/using-integrations.md).
* For more on Personalization, see [Personalization](../../designing/using/personalization.md).

When creating an email, you can choose to use a predefined template or to load an existing content from another source. See [Selecting an existing content](../../designing/using/using-existing-content.md#selecting-an-existing-content).

To increase the efficiency of your marketing campaigns, personalize your content. See [Inserting a personalization field](../../designing/using/personalization.md#inserting-a-personalization-field) and [Adding a content block](../../designing/using/personalization.md#adding-a-content-block).

You can also define dynamic content that varies depending on each profile. See [Defining dynamic content in an email](../../designing/using/personalization.md#defining-dynamic-content-in-an-email) and [Defining dynamic content in a landing page](../../channels/using/designing-a-landing-page.md#defining-dynamic-content-in-a-landing-page).

Enhance your messages and landing pages with links and images. See [Inserting a link](../../designing/using/links.md#inserting-a-link) and [Inserting images](../../designing/using/images.md#inserting-images).

## Email Designer interface {#email-designer-interface}

The Email Designer provides many options that allow you to create, edit and customize every aspect of your content.

The interface is composed of several areas offering different functionalities:

![](assets/email_designer_overview.png)

From the elements available in the **Palette** (1), drag and drop structure components and content fragments into the main **Workspace** (2). Select a component or element in the **Workspace** (2) and customize its main styling and display characteristics from the **Settings** pane (3).

Access more general options and settings from the main **Toolbar** (4).

>[!NOTE]
>
>The **Settings** pane can move to the left according to your screen resolution and display.

![](assets/email_designer_toolbar.png)

The **Contextual toolbar** of the editor interface offers various functionalities depending on the zone selected. It contains action buttons and buttons that allow you to change the style of the text. The modifications carried out always apply to the zone selected.

### Email Designer home page {#email-designer-home-page}

When [creating an email](../../channels/using/creating-an-email.md), the **[!UICONTROL Email Designer]** home page automatically displays upon selecting the email content.

![](assets/email_designer_home_page.png)

The **[!UICONTROL Properties]** tab enables you to edit the email details such as the label, the sender's address and name, or the email subject. You can also access this tab by clicking the email label on top of the screen.

![](assets/email_designer_home_properties.png)

The **[!UICONTROL Templates]** tab enables you to choose from the out-of-the-box HTML contents or the templates that you already created to quickly start designing your email. See [Content templates](../../designing/using/using-reusable-content.md#content-templates).

![](assets/email_designer_home_templates.png)

The **[!UICONTROL Learn & support]** tab gives you easy access to the related documentation and tutorials.

![](assets/email_designer_home_support.png)

If you do not select a template, the Email Designer home page also enables you to choose how you want to start designing your content:

* Click the **[!UICONTROL Create]** button to start a new content from scratch. See [Designing an email content from scratch](../../designing/using/designing-from-scratch.md#designing-an-email-content-from-scratch).
* Click the **[!UICONTROL Upload]** button to upload a file from your computer. See [Importing content from a file](../../designing/using/using-existing-content.md#importing-content-from-a-file).
* Click the **[!UICONTROL Import from URL]** button to retrieve existing content form a URL. See [Importing content from a URL](../../designing/using/using-existing-content.md#importing-content-from-a-url).

## Terminology {#terminology}

**Templates**: Templates are structures of email you can build and reuse for several deliveries.

**Fragments**: A fragment is a reusable component that can be referenced in one or more emails.

**Structure components**: Structural elements defining the layout of the email.

**Content components**: Content components are raw, empty components that you can edit once placed in an email.

## Content design best practices {#content-design-best-practices}

To make proper use of the Email Designer and create the best emails as simply as possible, we recommend applying the following principles:

* Use inline styling rather than a separate CSS and CSS in the &lt;head&gt; section of the HTML. By using inline styling, you can optimize content fragment save and reuse.

  See [Adding inline styling attributes](../../designing/using/styles.md#adding-inline-styling-attributes).

* If you import ZIP files containing your HTML content, use regular CSS. SCSS style sheets are not supported.

* Settle your branding easily by creating and reusing content fragments to keep consistency across your marketing campaigns.

  See [Creating a content fragment](../../designing/using/using-reusable-content.md#creating-a-content-fragment).

* When editing **email content**:

  Preview your messages before sending them. Adobe Campaign offers a way to test email rendering using Litmus. For more on this, see [Email rendering](../../sending/using/email-rendering.md).

* Referrer meta tag is not supported in the Email designer.

More design and general best practices regarding messages are presented in the following Adobe Campaign step-by-step guide: [Delivery best practices with Adobe Campaign](https://docs.campaign.adobe.com/doc/standard/getting_started/en/ACS_DeliveryBestPractices.html).

### Updating fragments {#email-designer-updates}

The Email Designer is under continuous improvement. If you created an email content from scratch, from an out-of-the-box template or if you created fragments, you may get the following update message the next time you open your content:

![](assets/email_designer_fragment_patch_message.png)

Adobe recommends updating your content to the latest version to avoid problems such as CSS collision issues. Click **[!UICONTROL Update now]**.

If an error occurs during the content update, check your HTML and fix it before running this update again.

When it comes to fragments, please note the following:

* If you want to add a fragment to a new email or template and if you get this message, you need to update this fragment first.

* If you have multiple fragments, you have to update each fragment that you want to use in an email content.

* To avoid impact on the current email messages that are not prepared yet, you can choose not to update some fragments.

* You can still send emails where a fragment that is not updated is already used, but that fragment is not editable.

* Updating fragments used in emails that are already prepared has no impact on those emails.

## Email Designer limitations {#email-designer-limitations}

* You cannot use personalization fields in a fragment. For more on fragments, see [this section](../../designing/using/using-reusable-content.md#about-fragments).

<!--* You cannot save directly as a fragment some content of an email that you are editing within the Email Designer. You need to copy-paste the HTML corresponding to that content into a new fragment. For more on this, see [Saving content as a fragment](../../designing/using/using-reusable-content.md#saving-content-as-a-fragment).-->

* When editing styles, only the web fonts officially supported by most email clients are available.
* Styles cannot be saved as a theme for future reuse. However, the CSS style can be saved in a content template or in an email. For more on styles, see [this section](../../designing/using/styles.md).
* Referrer meta tag is not supported in the Email designer.
* Surrogate pairs, characters not included in the Basic Multilingual Plane of the Unicode character set, cannot be stored in 2 bytes (16bits) and need to get encoded into 2 UTF-16 characters. These characters include some CJK ideographs, most emojis and some languages.<br>These characters can cause some incompatibility issues in dynamic text. You need to perform strong tests before sending your messages.

**Related topics**

* [Creating an email](../../channels/using/creating-an-email.md)
* [Designing a landing page](../../channels/using/designing-a-landing-page.md)
* [Creating an SMS message](../../channels/using/creating-an-sms-message.md)
* [Creating and sending a push notification](../../channels/using/preparing-and-sending-a-push-notification.md)

## Tutorial video {#video}

This video provides an overview of the Email Designer.

>[!VIDEO](https://video.tv.adobe.com/v/22771?quality=12)

To get started with the Email Designer, watch this [set of videos](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/designing-content/email-designer/email-designer-overview.html#GettingStarted) that explain the general functionality of the Email Designer and how to design an email from scratch or using templates
