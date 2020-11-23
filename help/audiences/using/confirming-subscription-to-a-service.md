---
solution: Campaign Standard
product: campaign
title: Confirming subscription to a service
description: Follow these steps to set up a confirmation message for profiles subscribing to a service in Adobe Campaign.
audience: audiences
content-type: reference
topic-tags: managing-subscriptions

---

# Confirming subscription to a service{#confirming-subscription-to-a-service}

## About sending subscription confirmation {#sending-subscription-confirmation}

This section describes how to send an automatic custom confirmation email to the profiles who subscribe to a specific service.

When you want to send a confirmation message for a subscription (or unsubscription) to a service, you can use the default message or a custom message. The steps for selecting a confirmation message are presented in the [Creating a service](../../audiences/using/creating-a-service.md) section.

If you choose to use the default message, you can edit its content with the following limitations:
* You can only personalize the message content with limited fields from the event context.
* This message will be the same for all services that use the default mode.

To send a specific confirmation email for a given service, you can create a custom message, in which you will also be able to leverage personalization fields from other resources. To do this, you must create and configure a transactional message. This message can be referenced :
* From the service itself. For more on this, see [Configuring confirmation message from a service](#configuring-confirmation-message-from-service).
* From a subscription landing page. For more on this, see [Configuring confirmation message from a landing page](#configuring-confirmation-message-from-landing-page).

## Configuring confirmation message from a service {#configuring-confirmation-message-from-service}

For example, you want to automatically send a confirmation message to the visitors of your website when they subscribe to your brand newsletter.

You need to configure a transactional email and reference that message from the desired service (subscription to your brand newsletter in this case). In order to enrich the transactional message with service information, you can define a reconciliation when creating the event.

When configuring it from the service, the confirmation transactional message will be sent only the first time each visitor subscribes to that service. If a profile is already subscribed, no confirmation message will be sent again to that profile.

### Step 1: Create the confirmation email {#step-1--create-the-confirmation-email-1}

A confirmation email will be automatically sent to each profile subscribing to the newsletter (through a landing page or any other means). The subscription is considered as an event and the email is a [transactional message](../../channels/using/getting-started-with-transactional-msg.md) which will target each profile that subscribes to the service.

Steps to create the confirmation email are described below. As the transactional message will be referenced in the service, you need to create it first.

#### Create the event {#create-the-event-1}

The confirmation email is a transactional message as it reacts to an event: the subscription to a service. This message will be sent to confirm subscription to your newsletter.

1. Create an event from the **[!UICONTROL Marketing plans]** > **[!UICONTROL Transactional messages]** > **[!UICONTROL Event configuration]** menu, accessible from the Adobe Campaign logo.
1. Enter a label, select a targeting dimension and click **[!UICONTROL Create]**.

    The configuration steps are presented in the [Configuring transactional messaging](../../administration/using/configuring-transactional-messaging.md) section.

1. In the **[!UICONTROL Fields]** section, click **[!UICONTROL Create element]** and add **[!UICONTROL publicLabel]** to the data structure in order to enable reconciliation.

    ![](assets/confirmation_publicLabel-field.png)

    >[!NOTE]
    >
    >The **[!UICONTROL publicLabel]** field is mandatory. If you do not add it to the event data structure, Adobe Campaign will not be able to perform reconciliation with the service. When subscribing to a service, this field will be filled with the **[!UICONTROL Service label]** of the corresponding service.

1. In the **[!UICONTROL Enrichment]** section, click **[!UICONTROL Create element]** and select the **[!UICONTROL Service]** target resource.

    ![](assets/confirmation_enrichment-service.png)

1. In the **[!UICONTROL Join definition]** section, map the **[!UICONTROL publicLabel]** field of the **[!UICONTROL Service]** resource with the **[!UICONTROL publicLabel]** field of the event configuration.

   ![](assets/confirmation_publicLabel-join.png)

    >[!NOTE]
    >
    >This will enable you to use personalization fields from the **[!UICONTROL Service]** resource in the transactional message.

1. Save the event configuration and click **[!UICONTROL Publish]** to publish the event.

The event is ready. You can now design the transactional email message.

#### Design the confirmation message {#design-the-confirmation-message-1}

The confirmation email is a transactional message based on the event that you just published.

1. From the Adobe Campaign logo, select **[!UICONTROL Marketing plans]** > **[!UICONTROL Transactional messages]** and click **[!UICONTROL Transactional messages]**.
1. Select the transactional email corresponding to the event that you just published.

1. Click the **[!UICONTROL Content]** section and select an email template. For more on editing a transactional message content, see [Event transactional messages](../../channels/using/event-transactional-messages.md).
1. As you have direct access to all fields from the **[!UICONTROL Service]** resource, you can select any field from the **[!UICONTROL Context]** > **[!UICONTROL Real-time event (rtEvent)]** > **[!UICONTROL Event context (ctx)]** >**[!UICONTROL Service]** node to personalize your content.

    ![](assets/confirmation_personalization-service.png)

    For more on personalizing a transactional message, see [this section](../../channels/using/event-transactional-messages.md#personalizing-a-transactional-message).

1. Preview your message using a test profile. For more on this, see [Defining a test profile in a transactional message](../../channels/using/event-transactional-messages.md#defining-a-test-profile-in-a-transactional-message).

1. Click **[!UICONTROL Save & close]** to save your content.
1. Publish the transactional message. See [Publishing a transactional message](../../channels/using/event-transactional-messages.md#publishing-a-transactional-message).

### Step 2: Create and configure the service {#step-2--create-and-configure-the-service-1}

1. From the advanced menu **Profiles & audiences** > **Services** via the Adobe Campaign logo, create a service.
1. Go to the **[!UICONTROL Service properties]** section, accessed via the ![](assets/edit_darkgrey-24px.png) button in the service dashboard.
1. Fill in the **[!UICONTROL Service label]** field.

    ![](assets/confirmation_service-label.png)

    >[!NOTE]
    >
    >You must fill in this field to enable reconciliation with the transactional message.

1. In the **[!UICONTROL Confirmation messages]** section, select **[!UICONTROL Custom message]**: this mode allows you to reference a specific confirmation message for profiles subscribing to your service.
1. Select the **[!UICONTROL Custom subscription event configuration]** associated with the transactional message that you created.

    ![](assets/confirmation_service-confirmation-message.png)

1. Click **[!UICONTROL Confirm]** and save the service.

Now each time a profile subscribes to this service, he receives the transactional message that you defined, with personalized fields mapped to the selected service.

>[!NOTE]
>
>A message will be sent only the first time the user subscribes.

## Configuring confirmation message from a landing page {#configuring-confirmation-message-from-landing-page}

You can also reference the confirmation message from a subscription landing page by using the **[!UICONTROL Start sending messages]** option from the **[!UICONTROL Job]** section of the landing page.

When referencing the confirmation message from the landing page, a message will be sent each time the landing page is submitted (even if the profile is already subscribed).

### Step 1: Create the confirmation email {#step-1--create-the-confirmation-email-2}

A confirmation email will be automatically sent to each profile subscribing to the newsletter through a landing page. The subscription is considered as an event and the email is a is a [transactional message](../../channels/using/getting-started-with-transactional-msg.md) which will target each profile that subscribes to the service.

Steps to create these elements are described below. As the transactional message will be referenced in the landing page, you need to create it first.

#### Create the event {#create-the-event-2}

The confirmation email is a [transactional message](../../channels/using/getting-started-with-transactional-msg.md) as it reacts to an event: the subscription to a service. This message will be sent to confirm subscription to your newsletter.

1. Create an event from the **[!UICONTROL Marketing plans]** > **[!UICONTROL Transactional messages]** > **[!UICONTROL Event configuration]** menu, accessible from the Adobe Campaign logo.
1. Enter a label, select a targeting dimension and click **[!UICONTROL Create]**.

    The configuration steps are presented in the [Configuring transactional messaging](../../administration/using/configuring-transactional-messaging.md) section.

1. In the **[!UICONTROL Fields]** section, click **[!UICONTROL Create element]** and add **[!UICONTROL serviceName]** to the data structure in order to enable reconciliation.
    
   ![](assets/confirmation_serviceName-field.png)

    >[!NOTE]
    >
    >The **[!UICONTROL serviceName]** field is mandatory. If you do not add it to the event data structure, Adobe Campaign will not be able to perform reconciliation with the subscribed service.

1. In the **[!UICONTROL Enrichment]** section, click **[!UICONTROL Create element]** and select the **[!UICONTROL Service]** target resource.
1. In the **[!UICONTROL Join definition]** section, map the **[!UICONTROL serviceName]** field of the **[!UICONTROL Service]** resource with the **[!UICONTROL name]** field of the event configuration.

   ![](assets/confirmation_serviceName-join.png)

    >[!NOTE]
    >
    >This will enable you to use personalization fields from the [!UICONTROL Service]  resource in the transactional message.

#### Design the confirmation message {#design-the-confirmation-message-2}

The steps for designing the transactional message are presented in this [section](#design-the-confirmation-message-1).

### Step 2: Create and configure the service {#step-2--create-and-configure-the-service-2}

1. From the advanced menu **[!UICONTROL Profiles & audiences]** > **[!UICONTROL Services]** via the Adobe Campaign logo, create a service.
1. Go to the **[!UICONTROL Service properties]** section, accessed via the ![](assets/edit_darkgrey-24px.png) button in the service dashboard.
1. Fill in the **[!UICONTROL Service label]** field. This label will be displayed in the confirmation message and in the subscription landing page.
1. Click **[!UICONTROL Confirm]** and save the service.

### Step 3: Create and configure the landing page {#step-3--create-and-configure-the-landing-page}

Create a subscription landing page which will be published on your website.

To create and configure this landing page, follow the steps below:

1. Design a [new landing page](../../channels/using/getting-started-with-landing-pages.md) based on the **[!UICONTROL Subscription]** template.
1. Edit the landing page properties. In the **[!UICONTROL Job]** > **[!UICONTROL Specific actions]** section, select the **[!UICONTROL Specific service]** option and choose the service that you just created from the drop-down list.

    ![](assets/confirmation_lp-specific-service.png)

1. Select the **[!UICONTROL Start sending message]** option and choose the transactional message that you just created from the drop-down list.

   ![](assets/confirmation_lp-start-sending-message.png)

1. Customize the content of the landing page.

1. [Test and publish](../../channels/using/testing-publishing-landing-page.md) the landing page.

Now each time a profile subscribes to your newsletter by submitting the landing page, he receives the confirmation message that you defined with personalized fields mapped to the service.

>[!NOTE]
>
>A message will be sent each time the landing page is submitted, even if the profile is already subscribed.
