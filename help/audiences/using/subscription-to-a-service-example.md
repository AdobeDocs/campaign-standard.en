---
title: Subscription to a service example
seo-title: Subscription to a service example
description: Subscription to a service example
seo-description: Follow these steps to set up a subscription process to a service in Adobe Campaign.
page-status-flag: never-activated
uuid: 23e6c4c2-e2c7-472f-b616-36a95225ac1d
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: audiences
content-type: reference
topic-tags: managing-subscriptions
discoiquuid: 1a24504e-7f9d-4297-b39e-c5f085b0f388

internal: n
snippet: y
---

# Subscription to a service example{#subscription-to-a-service-example}

## About subscription to a service {#about-subscription-to-a-service}

This section describes how to send an email to the profiles/visitors who subscribe to a specific service.

If you want to send an automatic custom confirmation message to users who subscribed to a service, you can:
* Do it from the subscription landing page.
* Do it from the service message confirmation.

To set this up, you need to:

1. Create a transactional message that will be sent to confirm subscription to the service. Declare a field "publicLabel" in the event configuration. (When subscribing to a service this field will be filled with the "service label" of the corresponding service.)
1. Configure the service and define a Service label (publicLabel). If a "service label" is set in the service settings, this information can now be used to reconcile the event configuration to this service.
1. To be able to personalize the confirmation transactional message, enrich the event configuration on Service using the publicLabel field.
1. Define the confirmation transactional email content. This email will target the population who subscribed to the designated service. Personalize your message with fields from the Service resource.


You can also use the "Start sending message" from the "Job" section of the landing page you should be able to do what you want.

If you want to use this feature, you MUST use a "serviceName" field in your rtEvent which will be reconciled to the "@name" attribute of the service.

The main difference between these two approaches are that configured from the service, a message will be sent only once the user subscribes. From the landing page, a message will be sent each time the landing page is submitted (even if the user is already subscribed).

(These steps have to be set up in Adobe Campaign in a specific order to have all parameters enabled properly.)



## Step 1: Create the confirmation email {#step-2--create-the-confirmation-email}

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