---
title: Preparing and sending a push notification
seo-title: Preparing and sending a push notification
description: Preparing and sending a push notification
seo-description: Follow these steps to create a single-send push notification in Adobe Campaign.
page-status-flag: never-activated
uuid: 77d5e407-9b97-41d2-b6e4-421a746ca113
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/channels/using/preparing-and-sending-a-push-notification
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: push-notifications
discoiquuid: 11c85ffa-b224-4cdf-b54b-d4b0505e8e1b
isreadyforlocalization: false
navTitle: Preparing and sending a push notification
publishexternaldate: 2018-11-20
sha1: f7ec216f32e12fdff85ef2fe083281e70cb75aa0
index: y
internal: n
snippet: y
---

# Preparing and sending a push notification{#preparing-and-sending-a-push-notification}

Preparing and sending a push notification

## Preparing the notification {#preparing-the-notification}

The steps for creating a push notification with Adobe Campaign are:

1. From the **Marketing activities** window, [create a new marketing activity](../../start/using/marketing-activities.md#creating-a-marketing-activity).

   Note that a single push notification can also be created from a [campaign](../../start/using/marketing-activities.md#creating-a-marketing-activity) or from the Adobe Campaign [home page](../../start/using/interface-description.md#home-page).

   You can also use a push notification delivery activity in a workflow. This activity is presented in the [Push notification delivery](../../automating/using/push-notification-delivery.md) section.

1. Select **Push notification**.
1. Select a template. 

   ![](assets/push_notif_type.png)

   By default, you can select one of the following two templates:

    * **Send push to Campaign profiles**: use this template to target the Adobe Campaign profiles who have subscribed to your mobile application. You can insert [personalization](../../designing/using/inserting-a-personalization-field.md) fields into your push notification, such as the recipient's first name.
    * **Send push to app subscribers**: use this template to send an anonymous push notification to all users who have opted in to receive notifications from your application. You cannot leverage data from Adobe Campaign, but only data collected from your mobile application.

   You can also select multilingual templates. For more information, refer to [Creating a multilingual push notification](../../channels/using/creating-a-multilingual-push-notification.md).

   For more on templates, refer to the [Managing templates](../../start/using/about-templates.md) section.

1. Enter your push notification properties and select your mobile app in the **Associate a Mobile App to a delivery** field.

   ![](assets/push_notif_properties.png)

   You can link the push notification to a campaign. To do this, select it from the campaigns that have already been created.

1. In the following screen, you can specify an audience, for example all of your VIP customers who subscribed to a specific mobile application. For more on this, see [Creating audiences](../../audiences/using/creating-audiences.md).

   Options for selecting an audience vary depending on the template used. In this example, you can target a mobile application because you selected the **Send push to Campaign profiles** template.

   Your audience will be automatically filtered according to the chosen application.

   ![](assets/push_notif_audience.png)

1. Choose the message style: **Alert/Message/Badge** or **Silent push**. The push notification types are described in the [About push notifications](../../channels/using/about-push-notifications.md) section.

   Edit the content of your push notification and define the advanced options. See [Customizing a push notification](../../channels/using/customizing-a-push-notification.md).

   ![](assets/push_notif_content.png)

   The push notification content and options configured here are passed to your mobile app in the form of a payload. The detailed structure of the payload is described in the [Understanding ACS push notifications payload structure](https://helpx.adobe.com/campaign/kb/understanding-campaign-standard-push-notifications-payload-struc.html) technote. 

1. Click **Create**. 
1. Before sending the notification, you can test it with test profiles and then see exactly what your recipients will see before sending the delivery. Select **Audiences** from your delivery summary and click the **Test profiles** tab.

   For more on sending tests, refer to [Test profiles](../../sending/using/managing-test-profiles-and-sending-proofs.md).

1. Select your test profiles and click **Preview** to display the notification: content is personalized with the test profile data.
1. Check the push notification layout on different devices: select iPhone, Android phone, iPad or Android tablet to preview rendering.

   ![](assets/push_notif_preview.png)

1. The **Estimated Payload Size** is an estimate based on test profile data. Actual payload size may vary. The limit of the message is 4KB.

   >[!CAUTION]
   >
   >If the payload size exceeds 4KB limit, the message will not be delivered. Personalization data impacts the size of message.

**Related topic:**

[About SMS and push content edition](JMA_sect1_ndh_dg4_h2b)

## Sending the notification {#sending-the-notification}

Push notifications can be sent to a selected audience in Adobe Campaign by defining the audience criteria. For the example below, our selected audience consists of 4 targeted mobile app subscribers.

1. Click **Prepare** to compute the target and generate the notifications.

   ![](assets/push_send_1.png)

1. Once the preparation has finished successfully, the **Deployment** window presents the following KPIs: **Target** and **To deliver**. Note that the **To deliver** count is lower than the **Targeted** one due to exclusions which can be viewed by clicking  ![](assets/lp_link_properties.png) button at the bottom of the **Deployment** window. 

   ![](assets/push_send_2.png)

1. In the **Exclusion logs** tab, you can find the list of all the messages excluded from the target sent and the reason behind this exclusion.

   Here, we can see that one of our mobile app subscribers was excluded because the address was blacklisted and the other subscribers because the profile was a duplicate.

   ![](assets/push_send_5.png)

1. Click the **Exclusion causes** tab to display the volume of excluded messages.

   ![](assets/push_send_7.png)

1. You can now click **Confirm** to start sending push notifications.
1. Check the status of your delivery through the message dashboard and logs. For more on this, see [Sending messages](../../sending/using/confirming-the-send.md) and [Delivery logs](../../sending/using/monitoring-a-delivery.md#delivery-logs).

   In this example, the message dashboard displays that Adobe Campaign attempted to send two push notifications: one was delivered successfully to the device and another one failed. To know why the delivery has errors, click the  ![](assets/lp_link_properties.png) button at the bottom of the **Deployment** window.

   ![](assets/push_send_4.png)

1. From the **Deployment** window, click the **Sending logs** tab to access the list of sent push notifications and their statuses. For this delivery, one push notification was successfully sent whereas the other failed due to a bad device token. This subscriber will then be blacklisted from further deliveries.

   >[!NOTE]
   >
   >Reasons can be any failure downstream to Adobe Campaign. In case of failures from providers like apns and fcm, the reason will reflect that as well. For more information on provider failures, you can refer to the [Apple](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CommunicatingwithAPNs.html) and [Android](https://firebase.google.com/docs/cloud-messaging/http-server-ref  ) documentation.

   ![](assets/push_send_6.png)

You can now measure the impact of your push notification delivery with dynamic reports. See [Push notification report](../../reporting/using/push-notification-report.md).

>[!NOTE]
>
>You can set global cross-channel fatigue rules that will automatically exclude oversollicited profiles from campaigns. See [Fatigue rules](../../administration/using/fatigue-rules.md).

