---
title: About In-App messaging
seo-title: About In-App messaging
description: About In-App messaging
seo-description: Display message or alert within the mobile application with In-App messaging.
uuid: e4b3f9b4-9054-4337-b845-7bd952e9910b
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: in-app-messaging
discoiquuid: ada166c6-2593-4a7e-bdd2-556f392c2050
isreadyforlocalization: false
index: y
internal: n
snippet: y
---

# About In-App messaging{#about-in-app-messaging}

About In-App messaging

>[!NOTE]
>
>This feature is optional and currently a Beta feature which can be subject to future changes. Please check your license agreement and contact your account executive to activate it. In-App Messaging enables Campaign Customers to serve personalized messages to enhance a user’s In-App experience. Adobe’s Mobile SDK utilizes Marketing Cloud IDs to retrieve data for from Adobe Servers for personalization which may include personal information as directed by Customer. Customer is responsible for securing the mobile application where In-App messaging will be used and to prevent any unauthorized access of user’s data by a third party.

In-App messaging allows you to display a message when the user is active within the mobile application. This message type is complimentary to push notifications which are delivered to the notification center of users' phone. For more information on the push notification channel, refer to this [section](../../channels/using/about-push-notifications.md).

Three types of In-App message are available in Adobe Campaign:

* **[!UICONTROL Target users based on their Campaign profile (inAppProfile)]** : This message type enables you to target Adobe Campaign profiles (CRM profiles) who have subscribed to your mobile application and to personalize In-App messages with all available profile attributes in Campaign.
* **[!UICONTROL Target all users of a Mobile app (inAppBroadcast)]** : This message type enables you to send messages to all users of your mobile application even if they don't have an existing profile in Campaign.
* **[!UICONTROL Target users based on their Mobile profile (inApp)]** : This message type enables you to target all known or anonymous users of a mobile app that have a mobile profile in Campaign and to personalize In-App messages with any profile attributes that have been obtained from mobile device.

## Prerequisites {#prerequisites}

First, to be able to start sending In-app message, you need to configure your mobile application using Experience Platform SDKs:

1. Make sure you can access the **[!UICONTROL In-App]** channel in Adobe Campaign. If you cannot access these channels, contact your account team.
1. In Launch, create the mobile application by creating a mobile property.

   For more information, refer to the [Set up a mobile property](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property) section in Adobe Launch documentation.

1. Install the **[!UICONTROL Adobe Campaign Standard]** extension for your mobile application in Adobe Launch:

   For more information on extensions, refer to the [Configure Campaign Standard Extension in Launch](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard-beta) in Adobe Launch documentation.

1. Configure rules for your application in Adobe Launch.
1. Configure your Adobe Launch application in Adobe Campaign Standard.
1. Add channel specific configuration to your Mobile Application set-up.

For more information on how to configure Experience Platform SDKs, refer to this [page](https://helpx.adobe.com/campaign/kb/configuring-app-sdk.html).

After configuring your mobile application, you can now start preparing and sending your In-app messages.
