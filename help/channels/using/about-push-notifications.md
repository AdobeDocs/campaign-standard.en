---
title: About push notifications
seo-title: About push notifications
description: About push notifications
seo-description: Discover the main specificities of the push notification channel in Adobe Campaign.
page-status-flag: never-activated
uuid: 72f67b0d-7ece-4667-bc6f-b7a94ba3734a
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: push-notifications
discoiquuid: a97021cf-b100-4dea-bc10-ffbd5d3308e4
isreadyforlocalization: true
index: y
internal: n
snippet: y
---

# About push notifications{#about-push-notifications}

About push notifications

Adobe Campaign allows you to send personalized and segmented push notifications to iOS and Android mobile devices.

These messages are received on mobile applications that you set up in Adobe Campaign by leveraging the Experience Cloud Mobile SDK. See [Configuring mobile app channel](../../administration/using/configuring-a-mobile-application-using-sdk-v4.md).

The user process in Adobe Campaign is as follows:

1. [Creating and sending a push notification](../../channels/using/creating-and-sending-a-push-notification.md)
1. [Customizing a push notification](../../channels/using/customizing-a-push-notification.md)
1. [Sending the push notification](../../sending/using/confirming-the-send.md)

Two types of push notification are available in Adobe Campaign:

* **Alert/Message/Badge** type notifications enable you to send standard text-based messages with additional content (sound, badge, deeplink, etc.) that you can define in the **Advanced options** section.

  This notification types allow you to add a title and a message in which you can use personalization fields. To be able to personalize your message, make sure you select the **Send push on profiles** template.

* **Silent push** type notifications are used to download content from servers in the background. No message is actually sent to the application's users.

Some specific configurations can be set up to define notifications behavior. For more on this, refer to [this section](../../channels/using/customizing-a-push-notification.md).

As an expert user, to define these specific configurations, refer to the mobile app [technotes](https://helpx.adobe.com/campaign/kb/acs-article-list.html).

>[!NOTE]
>
>Laws concerning privacy differ by country. Some countries require that you inform users of the types of data collected by mobile applications. Please check the laws pertaining to mobile applications in your country. Make sure push notifications sent to mobile applications comply with the prerequisites and conditions specified by Apple (Apple Push Notification Service) and Google (Google Cloud Messaging).

