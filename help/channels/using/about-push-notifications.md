---
title: About push notifications
seo-title: About push notifications
description: About push notifications
seo-description: Discover the main specificities of the push notification channel in Adobe Campaign.
page-status-flag: never-activated
uuid: 961aaeb5-6948-4fd2-b8d7-de4510c10566
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: push-notifications
discoiquuid: 23b4212e-e878-4922-be20-50fb7fa88ae8
context-tags: mobileApp,overview
internal: n
snippet: y
---

# About push notifications{#about-push-notifications}

>[!CAUTION]
>
>Push notification implementation has to be performed by expert users. If you need to be assisted, contact your Adobe Account executive or Professional services partner. Push notification is an optional feature. Please check your license agreement and contact your account executive to activate it.

Adobe Campaign allows you to send personalized and segmented push notifications to iOS and Android mobile devices.

These messages are received on mobile applications that you set up in Adobe Campaign by leveraging the Experience Cloud Mobile SDK V4 or Experience Platform SDK. For more information on this, refer to [Configuring a mobile application using SDK V4](https://helpx.adobe.com/campaign/kb/configuring-app-sdkv4.html) and [Configuring a mobile application using Adobe Experience Platform SDKs](https://helpx.adobe.com/campaign/kb/configuring-app-sdk.html).

In Adobe Campaign, mobile profile attributes data sent from mobile device are stored in **[!UICONTROL Subscriptions to an application (appSubscriptionRcp)]** resource which allows you to define the data that you want to collect from your applications' subscribers.

This resource needs to be extended to collect data you intend to send from the mobile device to Adobe Campaign. To do so, refer to this [page](../../developing/using/extending-the-subscriptions-to-an-application-resource.md) for the detailed steps.

Two types of push notification are available in Adobe Campaign:

* **[!UICONTROL Alert/Message/Badge]** type notifications enable you to send standard text-based messages with additional content (sound, badge, deeplink, etc.) that you can define in the **[!UICONTROL Advanced options]** section.

  This notification types allow you to add a title and a message in which you can use personalization fields. To be able to personalize your message, make sure you select the **[!UICONTROL Send push on profiles]** template.

* **[!UICONTROL Silent push]** type notifications are used to silently notify the application without any message or content for the end user. A typical use case for this type of message would be to make the application aware that there is content available on the server to be downloaded.

Some specific configurations can be set up to define notifications behavior. For more on this, refer to [this section](../../channels/using/customizing-a-push-notification.md).

As an expert user, to define these specific configurations, refer to the mobile app [technotes](https://helpx.adobe.com/campaign/kb/acs-article-list.html).

>[!NOTE]
>
>Laws concerning privacy differ by country. Some countries require that you inform users of the types of data collected by mobile applications. Please check the laws pertaining to mobile applications in your country. Make sure push notifications sent to mobile applications comply with the prerequisites and conditions specified by Apple (Apple Push Notification Service) and Google (Google Cloud Messaging or Firebase Cloud Messaging).

**Related content:**

* [Preparing and sending a push notification](../../channels/using/preparing-and-sending-a-push-notification.md)
* [Creating a multilingual push notification](../../channels/using/creating-a-multilingual-push-notification.md)
* [Push notification report](../../reporting/using/push-notification-report.md)
* [Push and In-App FAQ](https://helpx.adobe.com/campaign/kb/push_inapp_faq.html)

## Prerequisites {#prerequisites}

>[!NOTE]
>To leverage the push notification feature from Campaign, you need  to provide a valid push certificate in .pem format with no passwords.
If you have a valid p12 certificate, you can convert it easily into a .pem file using online resources.

First, to be able to start sending push notifications, you need to configure your mobile application using SDK V4. You can also configure your mobile application using Experience Platform SDKs. For more on this, refer to this [page](https://helpx.adobe.com/campaign/kb/configuring-app-sdk.html).

Before sending your push notifications, you should:

1. Make sure you can access the **[!UICONTROL Mobile app]** channel in Adobe Campaign.
1. Configure your mobile application in:

    * Adobe Campaign
    * The Adobe Mobile Services interface

1. Perform the mobile application's specific setup:

    * Package the configuration file downloaded from the Adobe Mobile Services interface with the mobile application.
    * Integrate the Experience Cloud Mobile SDK into your mobile application.

1. Define the data that you want to collect from your application's subscribers. The mobile application's subscribers who have a profile in the Adobe Campaign database are reconciled based on the criteria that you defined.

After configuring your mobile application, you can now start preparing and sending your In-app messages. For more on this, refer to [Preparing and sending a push notification](../../channels/using/preparing-and-sending-a-push-notification.md).
