---
title: About push notifications
description: Discover the main specificities of the push notification channel in Adobe Campaign.
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

These messages are received on mobile applications that you set up in Adobe Campaign by leveraging the Experience Platform SDK. For more information on this, refer to [Configuring a mobile application using Adobe Experience Platform SDKs](https://helpx.adobe.com/campaign/kb/configuring-app-sdk.html).

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
* [Campaign Standard Mobile guide](https://helpx.adobe.com/campaign/kb/acs-mobile.html)

## Prerequisites {#prerequisites}

>[!NOTE]
>To leverage the push notification feature from Campaign, you need  to provide a valid push certificate in .pem format with no passwords.
If you have a valid p12 certificate, you can convert it easily into a .pem file using online resources.

Before sending your push notifications, you should:

1. In Adobe Campaign, make sure you can access the **[!UICONTROL Push notification]** channel. If you cannot access these channels, contact your account team.

1. Verify that your user has the necessary permissions in Adobe Campaign Standard and Experience Platform Launch.

1. In Experience Platform Launch, create a mobile property. For more information, see [Set up a mobile property](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property).

1. In Experience Platform Launch, install the **[!UICONTROL Adobe Campaign Standard]** extension.

1. In Adobe Campaign Standard, configure the mobile property that you created in Experience Platform Launch. For more information, see [Setting up your Experience Platform Launch application in Adobe Campaign](https://helpx.adobe.com/campaign/kb/configuring-app-sdk.html#SettingupyourAdobeExperiencePlatformLaunchapplicationinAdobeCampaign).

1. Add the channel-specific configuration to your mobile application set up. For more information, see [Channel-specific application configuration in Adobe Campaign](https://helpx.adobe.com/campaign/kb/configuring-app-sdk.html#ChannelspecificapplicationconfigurationinAdobeCampaign).

1. To support mobile use case implementations, see the detailed instructions about extensions, Experience Platform Launch rules, and the SDK implementation in [Mobile use cases supported in Adobe Campaign Standard by using the Adobe Experience Platform SDKs](https://helpx.adobe.com/campaign/kb/configure-launch-rules-acs-use-cases.html).