---
title: About push notifications
seo-title: About push notifications
description: About push notifications
seo-description: Discover the main specificities of the push notification channel in Adobe Campaign.
uuid: 6b5fc2e9-ea69-408b-b153-ac2c8b0c258c
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/channels/using/about-push-notifications
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-30T04 53 54.893-0400
cq-lastreplicated: 2018-07-23T06 02 49.182-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: push-notifications
cq-template: /apps/help/templates/article-3
discoiquuid: 4768a77c-7aad-4346-856c-caa630595ad8
firstPublishExternalDate: 2018-07-23T06:02:49.153-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 01 19.896-0400
jcr-createdby: admin
jcr-description: About push notifications
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T06:02:49.153-0400
lochandoffdate: 2018-07-30T04 53 54.893-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: About push notifications
publishexternaldate: 2018-07-23T06 02 49.153-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/channels/using/about-push-notifications.html
sha1: a88e88e33dd5653b69bd3d362b3b3721c29d615a
topicBrowsingSortDate: 2018-07-23T06:02:49.153-0400
index: y
internal: n
snippet: y
---

# About push notifications

About push notifications

Adobe Campaign allows you to send personalized and segmented push notifications to iOS and Android mobile devices.

These messages are received on mobile applications that you set up in Adobe Campaign by leveraging the Experience Cloud Mobile SDK. See [Configuring mobile app channel](../../administration/using/configuring-mobile-app-channel.md).

The user process in Adobe Campaign is as follows:

1. [Creating and sending a push notification](../../channels/using/creating-and-sending-a-push-notification.md)
1. [Customizing a push notification](../../channels/using/customizing-a-push-notification.md)
1. [Sending the push notification](../../sending/using/confirming-send.md)

Two types of push notification are available in Adobe Campaign:

* **Alert/Message/Badge** type notifications enable you to send standard text-based messages with additional content (sound, badge, deeplink, etc.) that you can define in the **Advanced options** section.

  This notification types allow you to add a title and a message in which you can use personalization fields. To be able to personalize your message, make sure you select the **Send push on profiles** template.

* **Silent push** type notifications are used to download content from servers in the background. No message is actually sent to the application's users.

Some specific configurations can be set up to define notifications behavior. For more on this, refer to [this section](../../channels/using/customizing-a-push-notification.md).

As an expert user, to define these specific configurations, refer to the mobile app [technotes](https://helpx.adobe.com/campaign/kb/acs-article-list.html).

>[!NOTE]
>
>Laws concerning privacy differ by country. Some countries require that you inform users of the types of data collected by mobile applications. Please check the laws pertaining to mobile applications in your country. Make sure push notifications sent to mobile applications comply with the prerequisites and conditions specified by Apple (Apple Push Notification Service) and Google (Google Cloud Messaging).

