---
title: Push configuration
seo-title: Push configuration
description: Push configuration
seo-description: Discover how to configure Adobe Campaign to send push notifications.
page-status-flag: never-activated
uuid: 141631ae-b957-4630-aeb5-714d9aae7139
content-encoding: UTF-8
aemsrcnodepath: /content/help/en/campaign/standard/administration/using/push-configuration
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2017-11-28T11 03 16.305-0500
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: configuring-channels
cq-template: /apps/help/templates/article-3
discoiquuid: 49896600-72df-4fe7-a752-f00f3994fc5e
firstPublishExternalDate: 2017-11-16T10:49:17.792-0500
herogradient: light
isreadyforlocalization: false
jcr-created: 2017-11-29T19 03 16.117-0500
jcr-createdby: admin
jcr-description: Push configuration
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2017-11-16T10:49:17.792-0500
lochandoffdate: 2017-11-28T11 03 16.303-0500
lr-lastreplicatedby: wmyersta@adobe.com
navTitle: Push configuration
publishexternaldate: 2017-11-16T10 49 17.792-0500
publishExternalURL: https://helpx.adobe.com/campaign/standard/administration/using/push-configuration.html
sha1: 7829c0dfc978fcb188e926b4b59c282c0aa298e4
topicBrowsingSortDate: 2017-11-16T10:49:17.792-0500
index: y
internal: n
snippet: y
---

# Push configuration

Push configuration

The mobile applications receiving push notifications must be configured by an **administrator** in the Adobe Campaign interface.

By configuring both Adobe Campaign and Adobe Mobile Services, you will be able to use your mobile application's data for your campaigns.

>[!CAUTION]
>
>Push notification implementation has to be performed by expert users. If you need to be assisted, contact your Adobe Account executive or Professional services partner.

For more information on using push notifications, see [Push notifications](../../channels/using/about-push-notifications.md).

>[!NOTE]
>
>This document details the process for integrating your mobile application with Adobe Campaign. It does not provide information on how to create the mobile application or how to configure it for managing notifications. If you would like further information on this, refer to the official [Apple](https://developer.apple.com/) and [Android](http://developer.android.com/) documentations.

To be able to send push notifications, you need to:

1. Make sure you can access the **Mobile app** channel in Adobe Campaign.
1. Configure your mobile application in:

    * Adobe Campaign. See [Setting up a mobile application in Adobe Campaign](../../administration/using/push-configuration.md#setting-up-a-mobile-application-in-adobe-campaign).
    * The Adobe Mobile Services interface. See [Configuring a mobile application in Adobe Mobile Services](../../administration/using/push-configuration.md#configuring-a-mobile-application-in-adobe-mobile-services).

1. Perform the mobile application's specific setup:

    * Package the configuration file downloaded from the Adobe Mobile Services interface with the mobile application.
    * Integrate the Marketing Cloud Mobile SDK into your mobile application. See [Integrating the SDK into a mobile application](../../administration/using/push-configuration.md#integrating-the-sdk-into-a-mobile-application).

1. Define the data that you want to collect from your application's subscribers. The mobile application's subscribers who have a profile in the Adobe Campaign database are reconciled based on the criteria that you defined. See [Collecting subscribers' data from a mobile application](../../administration/using/push-configuration.md#collecting-subscribers--data-from-a-mobile-application).
1. Make sure that the setup has been completed successfully by launching your mobile application on your device and signing in. Make sure you opt in to receive notifications.
1. Then, in Adobe Campaign's advanced menu, select **Administration** > **Channels** > **Mobile app**.
1. Select your mobile application from the list to display its properties. Your subscription information is displayed under the subscribers list.

   ![](assets/push_notif_mobile_app.png)

1. To check the mobile applications a profile has subscribed to, in the **Profiles & Audiences > Profiles** menu, select a profile and click the **Edit profile properties** button on the right. The mobile applications are listed in the **Mobile App Subscriptions** tab.

   ![](assets/push_notif_subscriptions.png)

You can now send push notifications to your recipients.

## <p>Setting up a mobile application in Adobe Campaign</p>

To be able to send push notifications with Adobe Campaign, you must configure the mobile application that will receive them.

1. Click the **Adobe Campaign** logo, in the top left corner, then select **Administration** > **Channels** > **Mobile app**.
1. Click **Create** to set up an application.
1. Enter a name.
1. In the **Device-specific settings** section of a mobile application dashboard, for each device, provide the application details, including the certificate for iOS and the server key for Android.

   >[!NOTE]
   >
   >For iOS devices, you can create an application that uses the sandbox mode for tests and approvals. For more on this, refer to the documentation on the [Apple notifications service](http://developer.apple.com/notifications/).

   ![](assets/push_notif_create_mobile_app.png)

1. Click **Create**.

   ![](assets/push_notif_created_mobile_app.png)

In the **Mobile application properties** section, two URLs are listed: **Collect PII Endpoint** and **Campaign Tracking Endpoint**. They will be used in the Adobe Mobile Services interface. See [Configuring a mobile application in Adobe Mobile Services](../../administration/using/push-configuration.md#configuring-a-mobile-application-in-adobe-mobile-services).

* The **Collect PII endpoint** URL is used to collect the users' Marketing Cloud IDs and registration tokens from the mobile application when it is launched. When a user logs into the application using credentials such as email, first name, last name etc., this data is also collected and used to reconcile the user's registration token with an Adobe Campaign profile.
* The **Campaign Tracking Endpoint** URL is used to track push notification opening.

You can now use these values in Adobe Mobile Services to finish the configuration, as explained in the [Configuring a mobile application in Adobe Mobile Services](../../administration/using/push-configuration.md#configuring-a-mobile-application-in-adobe-mobile-services) section.

## <p>Configuring a mobile application in Adobe Mobile Services</p>

To send the data collected by Adobe Mobile Services to Adobe Campaign, you must configure postbacks in the Mobile Services interface.

You will need specific information that you can find in the mobile application parameters set in Adobe Campaign (see [Setting up a mobile application in Adobe Campaign](../../administration/using/push-configuration.md#setting-up-a-mobile-application-in-adobe-campaign)):

* **IMS Organization ID**
* **Collect PII Endpoint**
* **Campaign Tracking Endpoint**

You must have access to Adobe Analytics to do the following configuration. If you are not an Adobe Analytics user, contact your Adobe Campaign administrator.

1. Log into [mobilemarketing.adobe.com](http://mobilemarketing.adobe.com/).
1. Create the application or select an existing one.
1. Go to the **Manage App Settings** page.
1. In the **Visitor ID Service ** section, check **Enable** and select your organization from the drop-down list. Click **Save**.

   >[!NOTE]
   >
   >This organization must be the same as the one you use on the Adobe Campaign instance.

1. Click **Manage Postbacks**.
1. Create a postback.

    * Select **Postback** as the **Postback Type**.
    * In the **URL** field, copy the **Campaign Tracking Endpoint** URL from the mobile application that you configured in the Adobe Campaign interface, preceded by the server name. See [Setting up a mobile application in Adobe Campaign](../../administration/using/push-configuration.md#setting-up-a-mobile-application-in-adobe-campaign).
    * Fill in the **Post Body** field as follows:

      For iOS:

      ```    
      {
      "pushPlatform":"apns",
      "marketingCloudId":"{%mcid%}"
      }
      ```    
    
      For Android:

      ```    
      {
      "pushPlatform":"gcm",
      "marketingCloudId":"{%mcid%}"
      }
      ```

    * Set **Content Type** as **application/json**.
    * In the **Which Data Tags Trigger the Postback?**, select any event, typically **Launched** and **does not exist**.
    * Click **Save & Activate**.

1. Create a second postback.

    * Select **Postback** as the **Postback Type**.
    * In the **URL** field, copy the **Collect PII Endpoint** URL from the mobile application that you configured in the Adobe Campaign interface, preceded by the server name. See [Setting up a mobile application in Adobe Campaign](../../administration/using/push-configuration.md#setting-up-a-mobile-application-in-adobe-campaign).
    * Fill in the **Post Body** field as follows:

      For iOS:

      ```    
      {
      "pushPlatform":"apns",
      "marketingCloudId":"{%mcid%}"
      }
      ```    
    
      For Android:

      ```    
      {
      "pushPlatform":"gcm",
      "marketingCloudId":"{%mcid%}"
      }
      ```

    * Set **Content Type** as **application/json**.
    * In the **Which Data Tags Trigger the Postback?**, select any event, typically **Launched** and **does not exist**.
    * Click **Save & Activate**.

1. Create a third postback.

    * Select **PII** as the **Postback Type**.
    * In the **URL** field, copy the **Collect PII Endpoint** URL from the mobile application that you configured in the Adobe Campaign interface, preceded by the server name. See [Setting up a mobile application in Adobe Campaign](../../administration/using/push-configuration.md#setting-up-a-mobile-application-in-adobe-campaign).
    * Fill in the **Post Body** field as follows:

      For iOS:

      ```    
      {
      "userKey": "{userKey}",
      "pushPlatform":"apns",
      "marketingCloudId":"{%mcid%}",
      "cusEmail":"{email}",
      "cusFirstName":"{firstName}",
      "cusLastName":"{lastName}"
      }
      
      ```    
    
      For Android:

      ```    
      {
      "userKey": "{userKey}",
      "pushPlatform":"gcm",
      "marketingCloudId":"{%mcid%}",
      "cusEmail":"{email}",
      "cusFirstName":"{firstName}",
      "cusLastName":"{lastName}"
      }
      
      ```

    * Set **Content Type** as **application/json**.
    * In the **Which Data Tags Trigger the Postback?**, select any event, typically **Launched** and **does not exist**.
    * Click **Save & Activate**.

## <p>Integrating the SDK into a mobile application</p>

The Mobile core service’s software development kit (SDK) facilitates the integration of a mobile application into Adobe Campaign.

The SDK also enables the mobile application to:

* Register the subscribers to Adobe Campaign.
* Collect and send data to Adobe Campaign.
* Track the notification clicks in Adobe Campaign.

To integrate a mobile application with the SDK:

1. Go to [https://marketing.adobe.com/developer/gallery/marketing-cloud-mobile-libraries](https://marketing.adobe.com/developer/gallery/marketing-cloud-mobile-libraries) to download the Mobile core service’s SDK.
1. Integrate the SDK with your application by following these steps:

   iOS: [https://marketing.adobe.com/resources/help/en_US/mobile/ios/push_messaging.html](https://marketing.adobe.com/resources/help/en_US/mobile/ios/push_messaging.html)

   Android: [https://marketing.adobe.com/resources/help/en_US/mobile/android/push_messaging.html](https://marketing.adobe.com/resources/help/en_US/mobile/android/push_messaging.html)

The detailed steps are described in the [Integrating the Adobe Mobile SDK with your mobile app](https://docs.campaign.adobe.com/doc/AC6.1/en/Technotes/AdobeCampaign-IntegratingtheAdobeMobileSDKwithyourmobileapp.pdf) technote.

## <p>Collecting subscribers' data from a mobile application</p>

A specific custom resource enables you to define the data that you want to collect from your applications' subscribers.

1. Click the **Adobe Campaign** logo, in the top left corner, select **Administration** > **Development**, then **Custom resources** in the navigation pane.

   >[!CAUTION]
   >
   >Only users assigned with **administration rights** can extend resources. For more on this, refer to the [Custom resources](../../developing/using/data-model-concepts.md) section.

1. Select the **Subscriptions to an application** resource to extend it.

   ![](assets/POI_subscriptions_cusResource.png)

1. In the **Fields** section, define the customer data that you want to retrieve from your mobile applications, such as email, first name, last name, etc.

   >[!NOTE]
   >
   >If you are managing several mobile applications, all fields used by all of your applications must be listed. The iOS or Android collect PII call defines which fields are captured by each application.

1. In the **Link to profiles** section, set the reconciliation key used to link the profiles from the Adobe Campaign database to your applications' subscribers, such as the email.

   >[!NOTE]
   >
   >You can only define one reconciliation key for all of your mobile applications.

1. Publish the custom resource.

You are now able to collect subscribers' data in Adobe Campaign.
