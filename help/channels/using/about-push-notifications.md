---
title: About push notifications
description: Discover the main specificities of the push notification channel in Adobe Campaign.
audience: channels
content-type: reference
topic-tags: push-notifications
context-tags: mobileApp,overview
feature: Push
role: User
level: Intermediate
exl-id: e61daed6-a0ec-49d8-b1ad-77590fafb496
TQID: https://experienceleague.adobe.com/xwmywhEboE06iVgZJo2DTSqg2f1F1XHEAHGKjkKoqC4
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
feature_v2:
  - id: c5474392-5419-4296-9e41-f6f4ce4f6e9b
    internal-label: Administration
subfeature_v2:
  - id: e3988c18-3cfa-4f16-b812-ac2d2b1056fa
    internal-label: Permissions
  - id: e739ee2b-6228-412e-878f-45de0791417d
    internal-label: Use cases
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
---
# About push notifications{#about-push-notifications}

>[!CAUTION]
>
>Push notification implementation has to be performed by expert users. If you need to be assisted, contact your Adobe Account executive or Professional services partner. Push notification is an optional feature. Please check your license agreement and contact your account executive to activate it.

Adobe Campaign allows you to send personalized and segmented push notifications to iOS and Android mobile devices.

These messages are received on mobile applications that you set up in Adobe Campaign by leveraging the Experience Platform SDK. For more information on this, refer to [Configuring a mobile application using Adobe Experience Platform SDKs](../../administration/using/configuring-a-mobile-application.md).

In Adobe Campaign, mobile profile attributes data sent from mobile device are stored in **[!UICONTROL Subscriptions to an application (appSubscriptionRcp)]** resource which allows you to define the data that you want to collect from your applications' subscribers.

This resource needs to be extended to collect data you intend to send from the mobile device to Adobe Campaign. To do so, refer to this [page](../../developing/using/extending-the-subscriptions-to-an-application-resource.md) for the detailed steps.

Two types of push notification are available in Adobe Campaign:

* **[!UICONTROL Alert/Message/Badge]** type notifications enable you to send standard text-based messages with additional content (sound, badge, deeplink, etc.) that you can define in the **[!UICONTROL Advanced options]** section.

  This notification types allow you to add a title and a message in which you can use personalization fields. To be able to personalize your message, make sure you select the **[!UICONTROL Send push on profiles]** template.

* **[!UICONTROL Silent push]** type notifications are used to silently notify the application without any message or content for the end user. A typical use case for this type of message would be to make the application aware that there is content available on the server to be downloaded.

Some specific configurations can be set up to define notifications behavior. For more on this, refer to [this section](../../channels/using/customizing-a-push-notification.md).

>[!NOTE]
>
>Laws concerning privacy differ by country. Some countries require that you inform users of the types of data collected by mobile applications. Please check the laws pertaining to mobile applications in your country. Make sure push notifications sent to mobile applications comply with the prerequisites and conditions specified by Apple (Apple Push Notification Service) and Google (Google Cloud Messaging or Firebase Cloud Messaging).

**Related content:**

* [Preparing and sending a push notification](../../channels/using/preparing-and-sending-a-push-notification.md)
* [Creating a multilingual push notification](../../channels/using/creating-a-multilingual-push-notification.md)
* [Push notification report](../../reporting/using/push-notification-report.md)
* [Campaign Standard Mobile guide](../../channels/using/get-started-communication-channels.md)

## Prerequisites {#prerequisites}

>[!NOTE]
>To leverage the push notification feature from Campaign, you need  to provide a valid push certificate in .pem format with no passwords.
>
>If you have a valid p12 certificate, you can convert it easily into a .pem file using online resources.

Before sending your push notifications, you should:

1. In Adobe Campaign, make sure you can access the **[!UICONTROL Push notification]** channel. If you cannot access these channels, contact your account team.

1. Verify that your user has the necessary permissions in Adobe Campaign Standard and tags in Adobe Experience Platform.

1. In the Data Collection UI , create a mobile property. For more information, see [Set up a mobile property](https://developer.adobe.com/client-sdks/documentation/getting-started/create-a-mobile-property/).

1. In the Data Collection UI , install the **[!UICONTROL Adobe Campaign Standard]** extension.

1. In Adobe Campaign Standard, configure the mobile property that you created in the Data Collection UI. For more information, see [Setting up your tag application in Adobe Campaign](../../administration/using/configuring-a-mobile-application.md#set-up-campaign).

1. Add the channel-specific configuration to your mobile application set up. For more information, see [Channel-specific application configuration in Adobe Campaign](../../administration/using/configuring-a-mobile-application.md#channel-specific-config).

1. To support mobile use case implementations, see the detailed instructions about extensions, tag rules, and the SDK implementation in [Mobile use cases supported in Adobe Campaign Standard by using the Adobe Experience Platform SDKs](../../administration/using/configuring-rules-launch.md).

## Push notification FAQ {#push-faq}

### What would be some useful resource recommendations to learn more about Push channel? {#resource-push}

Check out the resources below:

* [Video Tutorials](https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/communication-channels/mobile/push/creating-a-push-notification.html)
* [Product Documentation](../../channels/using/about-push-notifications.md)
* Configure using AEP SDK [documentation](../../administration/using/configuring-a-mobile-application.md)
* [Community Page](https://experienceleaguecommunities.adobe.com/t5/adobe-campaign-standard/ct-p/adobe-campaign-standard-community)

### What do I have to do to acquire a Push token in Campaign? {#push-token-acquisition}

Ensure that the provisioning team has completed the provisioning of Push channel in Adobe Campaign Standard. Implement setPushIdentifier API from SDK. For more on this, refer to this [page](https://developer.adobe.com/client-sdks/documentation/adobe-campaign-standard/#set-up-push-messaging).

### Once I have Push token and ECID in Campaign, what else do I need to send a Push notification? {#sending-push}

Customers need to provide a valid Push certificate in .pem format in order to send a Push notification. You do not require a password for this certificate.

### What if I have a .p12 certificate instead of .pem certificate? {#certificates}

You can convert a .p12 certificate into a .pem certificate by running the below command in terminal. There are several online resources also available for conversion instructions.

```
openssl pkcs12 -in pushcert.p12 -out pushcert.pem -nodes -clcerts
```

### How do I know if the certificate upload is successful? {#certificate-upload}

You will see the following message.

![](assets/faq_2.png)

### Can I upload both Production and Sandbox certificates at the same time for iOS App (N/A for Android)? {#prod-sandbox-certificate}

No, apps will work in either sandbox or production mode and cannot be changed to the other (i.e. sandbox to production app) once set up. We recommend that you test your app in sandbox mode first and then transition to production mode.

To change to production mode, you will have to create another app. Also be sure to not check the sandbox checkbox and to upload a production certificate.

### Can I upload both iOS and Android credentials at the same time? {#ios-android-credentials}

Yes, Campaign supports both platforms at the same time and allows you to upload credentials for both platforms.

### I have uploaded Push certificates successfully, yet no Push messages are sent. {#push-certificates-upload}

Please make sure that your push certificates are valid by testing them [here](https://pushtry.com/).

### I am able to send Push notifications successfully from pushtry.com but not through Campaign. {#push-not-sending}

Please ensure that you are following the Push payload instructions provided [here](../../administration/using/push-payload.md).

Note that for Android, Campaign only supports Data payload not notification payload

### I have configured an app in the Administration section of Adobe Campaign Standard but the Mobile App is not available in the Delivery properties. {#mobile-app-unavailable}

An app has to have a valid Push certificate uploaded as well before it could be made available in the delivery properties.

### I have tried all the instructions on this page and yet I am not able to send Push from Campaign. {#push-troubleshoot}

Please open a customer care ticket.

### Push notifications are getting delivered from Campaign but the media file is not showing up.{#media-file-unavailable}

Mobile App developers need to handle the support for media files in the App. Sometimes network bandwidth may also prevent a media file from rendering. Refer to this [page](../../administration/using/image-push-notification.md) for additional pointers.

### What do I have to do to enable Push reporting in Campaign? {#push-reporting-enable}

Follow the steps below:

* Configure a Push tracking postback. Instructions can be found [here](../../administration/using/configuring-a-mobile-application.md).
* Implement trackAction API from Mobile Core. Refer to this [page](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/) for more information.

More detailed instructions can be found in this [page](../../administration/using/push-tracking.md).

### Which reports are available for Push channel? {#push-report-available}

An out-of-the-box report is available in Adobe Campaign for Push channel. Refer to this [documentation](../../reporting/using/push-notification-report.md).

See this [page](../../reporting/using/indicator-calculation.md#push-notification-delivery) to understand how each push metrics are calculated.

### Are deeplinks supported in Push and In-App messages? {#deeplink-push}

Yes, deeplinks are supported in Push messages. Deeplinks should include:

* Language that states that delivery tracking needs to be disabled in order for the deeplinks to work.
* Appsflyer with Branch as partners that can do the deeplink tracking. For more information on Branch and Adobe Campaign Standard integration, refer to this [page](https://help.branch.io/using-branch/docs/adobe-campaign-standard-1).
