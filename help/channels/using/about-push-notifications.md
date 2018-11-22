---
title: About push notifications
seo-title: About push notifications
description: About push notifications
seo-description: Discover the main specificities of the push notification channel in Adobe Campaign.
page-status-flag: never-activated
uuid: 5b43bada-3e9f-4736-9b4e-eff488a2ce06
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/channels/using/about-push-notifications
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: push-notifications
discoiquuid: 03a139ab-48d2-4713-b584-ce7f84c3bc7c
isreadyforlocalization: false
navTitle: About push notifications
publishexternaldate: 2018-11-20
sha1: 88409c108369a3d617a59a2e92a082acce6489b9
index: y
internal: n
snippet: y
---

# About push notifications{#about-push-notifications}

About push notifications

>[!CAUTION]
>
>Push notification implementation has to be performed by expert users. If you need to be assisted, contact your Adobe Account executive or Professional services partner. Push notification is an optional feature. Please check your license agreement and contact your account executive to activate it.

Adobe Campaign allows you to send personalized and segmented push notifications to iOS and Android mobile devices.

These messages are received on mobile applications that you set up in Adobe Campaign by leveraging the Experience Cloud Mobile SDK V4 and V5. For more information on this, refer to [Configuring a mobile application using SDK V4](../../administration/using/configuring-a-mobile-application-using-sdk-v4.md) and [Configuring a mobile application using SDK V5](../../administration/using/configuring-a-mobile-application-using-sdk-v5.md).

Two types of push notification are available in Adobe Campaign:

* **Alert/Message/Badge** type notifications enable you to send standard text-based messages with additional content (sound, badge, deeplink, etc.) that you can define in the **Advanced options** section.

  This notification types allow you to add a title and a message in which you can use personalization fields. To be able to personalize your message, make sure you select the **Send push on profiles** template.

* **Silent push** type notifications are used to download content from servers in the background. No message is actually sent to the application's users.

Some specific configurations can be set up to define notifications behavior. For more on this, refer to [this section](../../channels/using/customizing-a-push-notification.md).

As an expert user, to define these specific configurations, refer to the mobile app [technotes](https://helpx.adobe.com/campaign/kb/acs-article-list.html).

>[!NOTE]
>
>Laws concerning privacy differ by country. Some countries require that you inform users of the types of data collected by mobile applications. Please check the laws pertaining to mobile applications in your country. Make sure push notifications sent to mobile applications comply with the prerequisites and conditions specified by Apple (Apple Push Notification Service) and Google (Google Cloud Messaging).

