---
title: Setting up a double opt-in process
seo-title: Setting up a double opt-in process
description: Setting up a double opt-in process
seo-description: Follow these steps to set up a double opt-in process using landing pages in Adobe Campaign.
page-status-flag: never-activated
uuid: 23e6c4c2-e2c7-472f-b616-36a95225ac1d
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: landing-pages
discoiquuid: 1a24504e-7f9d-4297-b39e-c5f085b0f388

internal: n
snippet: y
---

# Setting up a double opt-in process{#setting-up-a-double-opt-in-process}

## About double opt-in {#about-double-opt-in}

Double opt-in mechanism is a best practice when sending emails. It protects the platform from wrong or invalid email addresses, spambots, and prevents possible spam complaints.

The principle is to send an email to confirm the visitor's agreement before storing them as ‘profiles' into your Campaign database: the visitor fills out an online landing page, then receives an email and has to click in the confirmation link to finalize its subscription.

![](assets/optin_mechanism.png)

To set this up, you need to:

1. Create and publish a landing page so that the visitors can register and subscribe. This landing page will be available from a website. Visitors who fill in and submit this landing page will be stored in the database but ‘blacklisted', in order not to receive any communication before the final validation (see [Managing blacklisting in Campaign](../../audiences/using/about-opt-in-and-opt-out-in-campaign.md)). 
1. Create and send automatically the opt-in email, with a confirmation link. This email will target population who submitted the landing page. It will be based on an email template which allows to target ‘opt-out’ profiles. 
1. Redirect to a confirmation landing page. This final landing page will propose a confirmation button: the visitors has to click it. You can design a welcome email to be sent as confirmation is done, and for example add a special offer in the email for new recipients.

These steps have to be set up in Adobe Campaign in a specific order to have all parameters enabled properly.

## Step 1: Create the confirmation landing page {#step-1--create-the-confirmation-landing-page}

The process to setup double opt-in mechanism starts with the creation of the confirmation landing page: this page will be displayed when the visitors clicked on the confirmation email in order to register.

To create and configure this landing page, you need to:

1. Design a [new landing page](../../channels/using/about-landing-pages.md) based on the **[!UICONTROL Profile acquisition (acquisition)]** template. Enter the label '**CONFIRMATION**'.

   If you need to use [services](../../audiences/using/about-subscriptions.md), you can also use the **[!UICONTROL Subscription (sub)]** template.

1. Edit the landing page properties and under the **[!UICONTROL Access and loading]** section, unselect the option **[!UICONTROL Authorize unidentified visitors]**, select **[!UICONTROL Preload visitor data]** (this one is not mandatory).

   ![](assets/optin_confirmlp_param.png)

1. In the **[!UICONTROL Job]** > **[!UICONTROL Additional data]** section, click **[!UICONTROL Add an element]** and enter the following context path:

   /context/profile/blackList

   Set the value to **false** and click **[!UICONTROL Add]**.

   ![](assets/optin_confirmlp_newelement.png)

   This context removes the blacklist field, in order to be able to send emails. We will see later that the first landing page was setting this field to **true** before confirmation, to prevent from sending emails to non-confirmed profiles. For more on this, see [Step 3: Create the acquisition landing page](../../channels/using/setting-up-a-double-opt-in-process.md#step-3--create-the-acquisition-landing-page).

1. Customize the content of the landing page: you can display personalized data and change the label of the confirmation button to ‘Click here to confirm my subscription’ for example.

   ![](assets/optin_confirmlp_design.png)

1. Adapt the content of the confirmation page to inform your subscribers that they are now registered.

   ![](assets/optin_confimlp_page2.png)

1. [Test and publish](../../channels/using/sharing-a-landing-page.md) the landing page.

## Step 2: Create the confirmation email {#step-2--create-the-confirmation-email}

Once the confirmation landing page is created, you can design the confirmation email: this email will be automatically sent to every visitor who validates the acquisition landing page. This validation is considered as an event and the email is a transactional message, linked to a specific typology rule which allows to target opt-out populations.

Steps to create these elements are described below. You need to follow them before creating the acquisition landing page itself as this email template will be referenced in it.

### Create the event {#create-the-event}

The confirmation email is a [transactional message](../../channels/using/about-transactional-messaging.md) as it reacts to an event: the validation of the form. You must first create the event and then create the template of the transactional message.

1. Create an event, from the **[!UICONTROL Marketing plans]** > **[!UICONTROL Transactional messages]** > **[!UICONTROL Event configuration]** menu, accessible from the Adobe Campaign logo, and enter the label '**CONFIRM**'.
1. Select the **[!UICONTROL Profile]** targeting dimension and click **[!UICONTROL Create]**.

   ![](assets/optin_eventcreate.png)

1. In the **[!UICONTROL Fields]** section, click **[!UICONTROL Create element]** and add the **[!UICONTROL email]** in the data structure to enable reconciliation.
1. In the **[!UICONTROL Enrichment]** section, click **[!UICONTROL Create element]** and select the **[!UICONTROL Profile]** target resource. You can then map on the **[!UICONTROL email]** field in the **[!UICONTROL Join definition]** section, or any other composite reconciliation key, depending on your needs.

   ![](assets/optin_eventcreate_join.png)

   If you need to use services, add the **[!UICONTROL Service]** target resource and map on the **[!UICONTROL serviceName]** field. For more on this, see .

1. Select **[!UICONTROL Profile]** as the **[!UICONTROL Targeting enrichment]** in the dropdown list.
1. Click **[!UICONTROL Publish]** to publish the event.

The event is ready. You can now design the email template. This template must include a link to the **CONFIRMATION** landing page created before. For more on this, see [Design the confirmation message](../../channels/using/setting-up-a-double-opt-in-process.md#design-the-confirmation-message).

### Create the typology rule {#create-the-typology-rule}

You need to create a specific [typology rule](../../administration/using/about-typology-rules.md), by duplicating an out-of-box one. This rule will allow to send messages to profiles who did not confirm their agreement yet and are still blacklisted. By default, typology rules exclude opt-out (i.e. blacklisted) profiles. To create this typology rule, follow these steps:

1. From the Adobe Campaign logo, select **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Typologies]** and click **[!UICONTROL Typologies]**.
1. Duplicate the out-of-box typology **[!UICONTROL Transactional message on profile (mcTypologyProfile)]**.
1. Once duplication confirmed, edit the new typology and enter the label **TYPOLOGY_PROFILE**.
1. Remove the **blacklisted address** rule.
1. Click **[!UICONTROL Save]**.

This typology can now be associated to the confirmation email.

### Design the confirmation message {#design-the-confirmation-message}

The confirmation email is a transactional message based on the event created before. Follow the steps below to create this message:

1. From the Adobe Campaign logo, select **[!UICONTROL Marketing plans]** > **[!UICONTROL Transactional messages]** and click **[!UICONTROL Transactional messages]**.
1. Edit the **CONFIRM** email template and personalize it. You can upload an existing content or use an out-of-box template.
1. Add a link to the **CONFIRMATION** landing page, and click **[!UICONTROL Confirm]** to save modifications.

   ![](assets/optin_email_selectlp.png)

1. Edit the email template properties. In the **[!UICONTROL Advanced parameters]** > **[!UICONTROL Preparation]** section, select the **TYPOLOGY_PROFILE** typology created before.
1. Save and publish the transactional message.

## Step 3: Create the acquisition landing page {#step-3--create-the-acquisition-landing-page}

You have to create the initial acquisition landing page: this opt-in form will be published on your website.

To create and configure this landing page, you need to:

1. Design a [new landing page](../../channels/using/about-landing-pages.md) based on the **[!UICONTROL Profile acquisition (acquisition)]** template. Enter the label '**ACQUISITION**'.
1. Edit the landing page properties: in the **[!UICONTROL Job]** > **[!UICONTROL Additional data]** section, click **[!UICONTROL Add an element]** and enter the following context path:

   /context/profile/blackList

   and set the value to **true**.

   This is mandatory to force blacklist and avoid sending messages to visitors who did not confirm their agreement. The validation of the CONFIRMATION landing page will set this field to **false** after confirmation. For more on this, see [Step 1: Create the confirmation landing page](../../channels/using/setting-up-a-double-opt-in-process.md#step-1--create-the-confirmation-landing-page).

1. In the **[!UICONTROL Job]** > **[!UICONTROL Specific actions]** section, select the option **[!UICONTROL Start sending messages]**.
1. In the associated drop-down list, choose the **CONFIRM** transactional message template you created.

   ![](assets/optin_acquisition_startoption.png)

1. Customize the content of the landing page, depending on your brand and on data you need to acquire. You can display personalized data and change the label of the confirmation button to **Confirm my subscription** for example.

   ![](assets/optin_acquisition_page1.png)

1. Customize the confirmation page to inform the new subscriber that he needs to validate his subscription.

   ![](assets/optin_acquisition_page2.png)

1. [Test and publish](../../channels/using/sharing-a-landing-page.md) the landing page.

Double opt-in mechanism is now configured. You can run and test the procedure from end to end, starting from the public URL of this **[!UICONTROL ACQUISITION]** landing page. This URL is displayed in the landing page dashboard.
