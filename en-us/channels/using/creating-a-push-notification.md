---
title: Creating a push notification
seo-title: Creating a push notification
description: Creating a push notification
seo-description: Follow these steps to create a single-send push notification in Adobe Campaign.
page-status-flag: never-activated
uuid: 1b228263-8b8b-48af-800c-d9a426ffb6a7
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/channels/using/creating-a-push-notification
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2017-11-28T11 30 56.339-0500
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: push-notifications
cq-template: /apps/help/templates/article-3
discoiquuid: f11bc624-2d4c-481f-b763-ec80196cb2a2
firstPublishExternalDate: 2017-11-16T11:00:16.898-0500
herogradient: light
isreadyforlocalization: false
jcr-created: 2017-11-29T19 01 10.560-0500
jcr-createdby: admin
jcr-description: Creating a push notification
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2017-11-16T11:00:16.898-0500
lochandoffdate: 2017-11-28T11 30 56.338-0500
lr-lastreplicatedby: wmyersta@adobe.com
navTitle: Creating a push notification
publishexternaldate: 2017-11-16T11 00 16.898-0500
publishExternalURL: https://helpx.adobe.com/campaign/standard/channels/using/creating-a-push-notification.html
sha1: 79df6f7e625f28743e817fef3e181d341bd2b746
topicBrowsingSortDate: 2017-11-16T11:00:16.898-0500
index: y
internal: n
snippet: y
---

# Creating a push notification

Creating a push notification

A single push notification can be created from a [campaign](../../start/using/marketing-activities.md#creating-a-marketing-activity), from the Adobe Campaign [home page](../../start/using/interface-description.md#home-page), or in the [marketing activity list](../../start/using/programs-and-campaigns.md#creating-a-campaign).

Creating a marketing activity is detailed in the [Creating marketing activities](../../start/using/marketing-activities.md#creating-a-marketing-activity) section.

The steps for creating a push notification with Adobe Campaign are:

1. From the **Marketing activities** window, create a new marketing activity.

   You can also use a mobile app delivery activity in a workflow. This activity is presented in the [Mobile app delivery](../../automating/using/mobile-app-delivery.md) section.

1. Select **Mobile app message**.
1. Select a template. See [Managing templates](../../start/using/about-templates.md).

   ![](assets/push_notif_type.png)

   By default, you can select one of the following two templates:

    * **Send push to Campaign profiles**: use this template to target the Adobe Campaign profiles who have subscribed to your mobile application. You can insert [personalization](../../designing/using/example--email-personalization.md) fields into your push notification, such as the recipient's first name.
    * **Send push to app subscribers**: use this template to send an anonymous push notification to all users who have opted in to receive notifications from your application. You cannot leverage data from Adobe Campaign, but only data collected from your mobile application.

   >[!NOTE]
   >
   >If you choose to send notifications to profiles, they will be compatible with multi-channel fatigue rules. If you're sending messages to app subscribers, the fatigue rule will be limited to the mobile application channel only. See [Fatigue rules](../../administration/using/typologies.md#choosing-the-channel).

1. Enter the push notification's general properties.

   ![](assets/push_notif_properties.png)

   A push notification can also be created within a parent campaign. Select it from the campaigns that have already been created.

   ![](assets/push_notif_campaign.png)

1. In the following screen, you can specify an audience, for example all of your VIP customers who subscribed to a specific mobile application. For more on this, see [Creating audiences](../../audiences/using/creating-audiences.md).

   Options for selecting an audience vary depending on the template used. In this example, you can target a mobile application because you selected the **Send push to Campaign profiles** template.

   ![](assets/push_notif_audience.png)

1. Choose the message type. The push notification types are described in the [About push notifications](../../channels/using/about-push-notifications.md) section.

   ![](assets/push_notif_content.png)

1. Edit the content of your push notification and define the advanced options. See [Push notification advanced options](../../channels/using/push-notification-advanced-options.md).

   The push notification content and options configured here are passed to your mobile app in the form of a payload. The detailed structure of the payload is described in the [Understanding ACS push notifications payload structure](https://docs.campaign.adobe.com/doc/AC6.1/en/Technotes/AdobeCampaign-UnderstandingACSPushNotificationsPayloadStructure.pdf) technote. 

   ![](assets/push_notif_content_personalization.png)

1. Once the notification is configured and before sending it, you can click the **Preview** button to display the message using a test profile.

   ![](assets/push_notif_preview.png)

   The **Estimated Payload Size** is a directional estimate based on test profile data. Actual payload size may vary. The limit of the message is 4KB.

   >[!NOTE]
   >
   >If you exceed the 4KB limit, the message will not be delivered. Personalization can have an impact on the message size.

1. Send the push notification. You can check its delivery through the message dashboard and logs. See [Sending messages](../../sending/using/confirming-send.md) and [Delivery logs](../../sending/using/monitoring-a-delivery.md#delivery-logs).

   >[!NOTE]
   >
   >You can set global cross-channel fatigue rules that will automatically exclude oversollicited profiles from campaigns. See [Fatigue rules](../../administration/using/typologies.md#fatigue-rules).

Your push notification is now sent. You can measure its impact with delivery reports. See [Push notification report](../../reporting/using/push-notification-report.md).
