---
title: Creating a service
description: Learn how to create your first service and configure it to send email confirmations to your subscribers.
page-status-flag: never-activated
uuid: 0d95d852-0f22-4b7b-b301-8fb4844c3ca2
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: audiences
content-type: reference
topic-tags: managing-subscriptions
discoiquuid: 6b7788fe-fa6c-472a-97db-765595ce1589
context-tags: service,wizard;service,main
internal: n
snippet: y
---

# Creating a service{#creating-a-service}

In order to be able to manage subscriptions, you first need to create a service and configure it. Configuring a new service allows you to specify the email confirmations that the profiles will receive when they subscribe to or unsubscribe from the service. You will also define the subscription and unsubscription landing pages linked to the service. For example, a service subscription link inserted into an email will automatically direct the profile to the subscription landing page that is specified in the service.

To configure a service:

1. From the advanced menu **[!UICONTROL Profiles & audiences]** > **[!UICONTROL Services]** via the Adobe Campaign logo, add a new service or select an existing service. If you create a new service, simply follow the steps shown on the screen.

   A default service template is available. This template is pre-configured with default landing pages and confirmation emails. You can create other templates to define specific configurations. For more on this, refer to the [Managing templates](../../start/using/about-templates.md) section.

1. In the **[!UICONTROL Service properties]** section, accessed via the ![](assets/edit_darkgrey-24px.png) button in the service dashboard, configure the confirmation messages for subscriptions and unsubscriptions.

   ![](assets/lp_service_parameters.png)

1. Fill in the **[!UICONTROL Service label]** field. The service label is mandatory when using a custom confirmation message.

1. Select a confirmation message template for subscriptions and unsubscriptions. Three modes are available:

    * **[!UICONTROL No message]**: this mode allows you to create a service without a confirmation message.
    * **[!UICONTROL Default message]**: this mode will use the default subscription or unsubscription confirmation transactional message. The default confirmation messages are generic and will be the same for all services that use the default mode.

        >[!NOTE]
        >
        >You can modify a default message by clicking its label in the **[!UICONTROL Service properties]** section or by selecting it from the Adobe Campaign transactional message list, after checking the **[!UICONTROL Show internal transactional messages]** box.

    * **[!UICONTROL Custom message]**: this mode allows you to handle custom confirmation messages, specific for each service. You then select the **[!UICONTROL Custom subscription event configuration]** which is associated with a specific [transactional message](../../channels/using/about-transactional-messaging.md) template. For more on this, see [Confirming subscription to a service](../../audiences/using/confirming-subscription-to-a-service.md).

1. Save the service. It is now ready to be used.

Once a service has been created, you can start promoting it.

**Related topics:**

* [Managing a service and subscriptions](https://helpx.adobe.com/campaign/kt/acs/using/acs-services-and-subscriptions-feature-video-use.html) video
* [Promoting a service](../../audiences/using/promoting-a-service.md)
* [Creating an audience made of subscribers](../../audiences/using/creating-audiences.md#creating-list-audiences)
* [Linking a landing page to a service](../../channels/using/configuring-landing-page.md#linking-a-landing-page-to-a-service)
