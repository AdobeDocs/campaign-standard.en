---
title: Personalizing emails 
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

# Inserting a personalization field{#inserting-a-personalization-field}

Adobe Campaign allows you to insert a field from the database into your page such as the profile's first name.

>[!NOTE]
>
>The images below show how to insert a personalization field using the [Email Designer](../../designing/using/about-email-content-design.md#about-the-email-designer) for an email.

To add a personalization field to the content:

1. Click inside a text block, click the **[!UICONTROL Personalize]** icon from the contextual toolbar and select **[!UICONTROL Insert personalization field]**. For more on the Email Designer interface, see [this section](../../designing/using/about-email-content-design.md#email-designer-interface).

   ![](assets/email_perso_field_1.png)

1. Select the field that you would like to insert into your page content.

   ![](assets/email_perso_field_2.png)

1. Click **[!UICONTROL Confirm]**.

The field name appears in the editor and it is highlighted.

![](assets/email_perso_field_3.png)

Once personalization is generated (when previewing and preparing the email for example), this field will be replaced by the value corresponding to the targeted profile.

>[!NOTE]
>
>If the email is created from a workflow, the additional data computed in the workflow is also available in the personalization fields. For more information about adding additional data from a workflow, refer to the [Enriching data](../../automating/using/targeting-data.md#enriching-data) section.

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

# Personalizing the sender{#personalizing-the-sender}

## Email sender {#email-sender}

To define the name of the sender which will appear in the header of messages sent, go the **[!UICONTROL Properties]** tab of the Email Designer home page (accessible through the home icon).

![](assets/delivery_content_edition16.png)

* The **[!UICONTROL From: name]** field allows you to enter the sender name. By default, the default **Sender name** block is automatically entered in the field. Adobe Campaign refers to the email channel configuration (from the advanced menu **[!UICONTROL Administration > Channels > Email > Email accounts]** via the Adobe Campaign logo) to designate this sender.

  You can change the sender name by clicking the **Sender name** block. The field then becomes editable and you can enter the name you would like to use.

  This field can be personalized. To do this, you can add personalization fields, content blocks and dynamic content by clicking the icons below the sender name.

* The **[!UICONTROL From: email address]** field cannot be edited from this section. You can change it by editing the properties of the email from its dashboard. For more on this, see [List of email advanced parameters](../../administration/using/configuring-email-channel.md#advanced-parameters).

>[!NOTE]
>
>The header parameters must not be empty. The sender's address is mandatory to allow an email to be sent (RFC standard). Adobe Campaign checks the syntax of email addresses entered.

**Related topics:**

* [Inserting a personalization field](../../designing/using/inserting-a-personalization-field.md)
* [Adding a content block](../../designing/using/adding-a-content-block.md)
* [Defining dynamic content in an email](../../designing/using/defining-dynamic-content-in-an-email.md)

## SMS sender {#sms-sender}

You can personalize the name of the SMS sender. For more on this, refer to the [SMS configuration](../../administration/using/configuring-sms-channel.md#configuring-sms-properties) section.

# Personalizing the subject line of an email{#personalizing-the-subject-line-of-an-email}

## Personalizing an email subject {#personalizing-an-email-subject}

The message subject is mandatory to prepare and send the message.

>[!NOTE]
>
>If the subject line is empty, a warning is displayed in the message dashboard and in the Email Designer.

To configure the email subject, go the **[!UICONTROL Properties]** tab of the Email Designer home page (accessible through the home icon) and fill in the **[!UICONTROL Subject]** section.

![](assets/email_designer_subject.png)

You can also add personalization fields, content blocks and dynamic content to the subject line by clicking the corresponding icons.

**Related topics:**

* [Inserting a personalization field](../../designing/using/inserting-a-personalization-field.md)
* [Adding a content block](../../designing/using/adding-a-content-block.md)
* [Defining dynamic content in an email](../../designing/using/defining-dynamic-content-in-an-email.md)

## Predictive subject line {#predictive-subject-line}

When editing an email, you can try out different subject lines and get an estimation of its open rate before you send it.

This feature is disabled by default. It is enabled when the first model is imported. A model is the result of training data sets specific to a given industry. Models allow the system to predict the open rate of the email when a new subject line is submitted.

>[!NOTE]
>
>This feature is available for email messages and for databases that contain English contents only. The trained model will be inconsistent and will lead to erroneous results if your instance contains emails in other languages. The option that allows you to test a subject is only visible if a model is already available on your instance.

### Testing a subject {#testing-a-subject}

To test your subject line:

1. Create or open your email.
1. Open the content and enter the subject of the email in the corresponding input field.
1. Click the **[!UICONTROL Test subject]** button to access the **[!UICONTROL Test your subject line]** window. You can still edit the subject from this window.
1. Select the correct model to be taken into account for the open rate prediction. Several models are available, each corresponding to a specific industry.
1. Click **[!UICONTROL Test]**.

Your subject is then analyzed.

>[!NOTE]
>
>If the subject line is too short, it cannot be analyzed and an error message is displayed.

Several indicators are calculated and a set of tools are displayed to help you:

* **Predicted open rate**: This chart gives you an idea of the open rate you can expect for the email with its current subject.
* **Subject length**: This indicator lets you see if the current length of the subject is correct or whether it would need to be longer or shorter.
* **Colored words**: When testing the subject, words highlighted in green are the words that contribute the most to increasing the open rate prediction. Words highlighted in red are the words that contribute the least to increasing the open rate prediction. If you add or remove words in the subject, highlighted words will change.
* **Categories and word suggestions**: Towards the lower part of the window, a number of relevant categories for the selected model are displayed. These categories are sorted by order of importance and they allow you to see whether your subject contains words that are associated with it via a check symbol. Each category contains a set of suggested words that could be used in your subject to make it more relevant and increase the open rate. These words are the words that are used the most often in a given category.

>[!NOTE]
>
>Personalization fields and punctuation marks are stripped from the subject analysis. In the case of dynamic/conditional text, all variants are considered as one subject line.

![](assets/predictive_subject_line_example.png)

### Importing models {#importing-models}

By default, there is no model running on your Adobe Campaign server. There are two ways to get a model and activate the feature:

* You can train a local model from the data of your previous email messages:

    * If you are already using Adobe Campaign, the local model will be automatically trained on the messages that you have already sent.
    * If you are new to Adobe Campaign, you can extract a CSV file from your previous system/ESP that contains 4 columns: date, subject, sent, opens. To do that, go to **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Email]** > **[!UICONTROL Subject Line Import]** and follow the instructions provided on the successive screens. When the subject upload is complete, import a local model as described below. The local model is automatically trained with the data you uploaded.
    * If you are new to Adobe Campaign and cannot get a CSV file as described above, you can use a pre-trained model or wait until you have enough delivery data in your system to train a local model. The system will automatically determine whether your current data set contains enough data to recognize patterns and to train the model.

      >[!NOTE]
      >
      >There is no defined number of subject lines needed to train your own model. To be able to train it, the subject lines need to be varied and to have no duplicates. If there is not enough data to process, the system will not be able to train the model. You can only have one trained model on your instance.

  To train a local model, download the subjectLineTraining.xml from [here](https://support.neolane.net/webApp/downloadCenter?__userConfig=psaDownloadCenter) and use the [package import](../../automating/using/managing-packages.md) feature to upload it to your Adobe Campaign instance. A technical workflow will automatically do the training for you.

  The first time you want to train a model, an administrator can force the **[!UICONTROL SubjectLine Training workflow]** to start from the **[!UICONTROL Administration]** > **[!UICONTROL Application settings]** > **[!UICONTROL Workflows]** menu.

  Once a model has been uploaded and trained, the feature is automatically activated and a new option appears next to the subject line field of your messages.

  Then, the technical workflow will automatically continue to train your model every week.

* You can import pre-trained models that are specific to certain industries (medical, etc.) using the [package import](../../automating/using/managing-packages.md) feature. These models are available [here](https://support.neolane.net/webApp/downloadCenter?__userConfig=psaDownloadCenter) and cannot be trained.

  Once a model has been uploaded, the feature is automatically activated and a new option appears next to the subject line field of your messages.

>[!NOTE]
>
>Importing and generating trained models can only be performed by an administrator.

The models that are available for use are:

* Cosmetic industry: subjectInsightCosmetic.xml
* Supermarket industry: subjectInsightSupermarket.xml
* Medical industry: subjectInsightMedical.xml
* Model to train: subjectlineTraining.xml.
