---
title: Push Notification Channel upcoming changes
description: Push Notification Channel upcoming changes
audience: channels
feature: Push
role: Admin
level: Experienced
exl-id: e273b443-7c43-482b-8f86-60ada4b57cbf
---
# Push Notification Channel changes {#push-upgrade}

You can use Campaign to send push notifications on Android and iOS devices. To perform this, Campaign relies on specific subscription services.  Some important changes to the Android Firebase Cloud Messaging (FCM) service are released in 2024, and may impact your Adobe Campaign implementation. Your subscription services configuration for Android push messages may need to be updated to support this change.

In addition, Adobe highly recommends to move to the token-based connection to APNs rather than a certicate-based connection, which is more secure and scalable.

To ensure uninterrupted service, you must upgrade your mobile application(s) registered with Adobe Campaign to incorporate the latest authentication mechanisms for FCM (Android) and APNs (iOS).


[Learn more on how to configure your mobile application certificates in Adobe Campaign Standard](configuring-a-mobile-application.md#channel-specific-config)


## Google Android Firebase Cloud Messaging (FCM) service {#fcm-push-upgrade}

### What changed? {#fcm-changes}

As part of Google's continual effort to improve its services, the legacy FCM APIs will be discontinued on **June 20, 2024**. Learn more about Firebase Cloud Messaging HTTP protocol in [Google Firebase documentation](https://firebase.google.com/docs/cloud-messaging/http-server-ref){target="_blank"}.

Starting 24.2 release, Adobe Campaign Standard supports the HTTP v1 APIs to send Android Push Notification Messages. 

### Are you impacted? {#fcm-impact}

If you are already using Adobe Campaign Standard to send push notifications, your implementation must be updated.

Transition to the latest APIs is mandatory to avoid any service distruption. 

<!--To check if you are impacted, you can filter your **Services and Subscriptions** as per the filter below

* If any of your active push notification service uses the **HTTP (legacy)** API, your setup will be directly impacted by this change. You must review your current configurations and move to the newer APIs as described below.

* If your setup exclusively uses the **HTTP v1** API for Android push notifications, then you are already in compliance and no further action will be required on your part.-->

### How to update? {#fcm-transition-procedure}

#### Prerequisites {#fcm-transition-prerequisites}

* The support of **HTTP v1 APs** mode has been added in 24.1 release. If your environment is running on an older version, a prerequisite for this change is to upgrade your environment to the [latest Campaign Classic build](../../rn/using/release-notes.md).

* The Android Firebase Admin SDK service's account JSON file is needed to have the mobile application moved to HTTP v1. Learn how to get this file in [Google Firebase documentation](https://firebase.google.com/docs/admin/setup#initialize-sdk){target="_blank"}.

* If you are still using this legacy version of the SDK, you must update your implementation with Adobe Experience Platform SDK. Learn how to migrate to Adobe Experience Plaform SDK in [this article](sdkv4-migration.md).

* Make sure you have the **Mobile App Configuration** permission in Adobe Experience Platform Data Collection Mobile before performing the below steps. [Learn more](https://experienceleague.adobe.com/docs/experience-platform/collection/permissions.html?lang=en#adobe-experience-platform-data-collection-permissions){target="_blank"}.


#### Transition procedure {#fcm-transition-steps}

To move your environment to HTTP v1, follow these steps:

1. Browse to **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile app (AEP SDK)]**.
1. Select the specific mobile application that requires the certificate update.
1. Check the **[!UICONTROL Update app credentials]** checkbox. 
1. Provide the App ID (Android package name) from your Android project's `build.gradle` file. For example, `com.android.test.testApp`. Make sure to use different IDs for staging and production environments.
1. Upload your Android private key JSON key file.
1. Click the **Save** button.


>[!NOTE]
>
>Once these changes are applied, all new Push notification deliveries to Android devices use the HTTP v1 API. Existing push deliveries in retry, in progress, and in use, still use the HTTP (legacy) API.


## Apple iOS Push Notification service (APNs) {#apns-push-upgrade}

### What changed? {#ios-changes}

As recommended by Apple, you should secure your communications with Apple Push Notification service (APNs) by using stateless authentication tokens.

Token-based authentication offers a stateless way to communicate with APNs. Stateless communication is faster than certificate-based communication because it doesn't require APNs to look up the certificate, or other information, related to your provider server. There are other advantages to using token-based authentication:

* You can use the same token from multiple provider servers.

* You can use one token to distribute notifications for all of your company's apps.

Learn more about Token-based connections to APNs in [Apple Developer documentation](https://developer.apple.com/documentation/usernotifications/establishing-a-token-based-connection-to-apns){target="_blank"}.

Adobe Campaign Standard support both token-based and certificate-based connections. If your implementation relies on a certificate-based connection, Adobe highly recommends you to update it to a token-based connection.

### Are you impacted? {#ios-impact}

If your current implementation relies on certificate-based requests to connect to APNs, you are impacted. Transition to a token-based connection is recommended.

<!--To check if you are impacted, you can filter your **Services and Subscriptions** as per the filter below:

![](assets/filter-services-ios.png)


* If any of your active push notification service uses the **Certificate-based authentication** mode (.p12), your current implementations should be reviewed and moved to a **Token-based authentication** mode (.p8) as described below.

* If your setup exclusively uses the **Token-based authentication** mode for iOS push notifications, then your implementation is already up-to-date and no further action will be required on your part.-->

### How to update? {#ios-transition-procedure}

#### Prerequisites {#ios-transition-prerequisites}

* The support of **Token-based authentication** mode has been added in 24.1 release. If your environment is running on an older version, a prerequisite for this change is to upgrade your environment to the [latest Campaign Classic build](../../rn/using/release-notes.md).

* You need an APNs authentication token signing key to generate the tokens that your server uses. You request this key from your Apple developer account, as explained in [Apple Developer documentation](https://developer.apple.com/documentation/usernotifications/establishing-a-token-based-connection-to-apns){target="_blank"}.


#### Transition procedure {#ios-transition-steps}

To move your iOS mobile applications to the Token-based authentication mode, follow these steps:

1. Browse to **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile app (AEP SDK)]**.
1. Select the specific mobile application that requires the certificate update.
1. Check the **[!UICONTROL Update app credentials]** checkbox. 
1. Edit each of these mobile applications, and browse to the **Certificate/Private key** tab.
1. Provide the **App ID** (iOS Bundle ID). You can find the iOS Bundle ID (App ID) in your app's primary target in Xcode.
1. Fill in the APNs connection settings **[!UICONTROL Key Id]**, **[!UICONTROL Team Id]** and **[!UICONTROL Bundle Id]**. 
1. Upload your p8 certificate.
1. Click **[!UICONTROL Save]**. 

Your iOS application is now moved to the Token-based authentication mode.

## Frequently Asked Questions{#push-upgrade-faq}

+++Can we keep same appID on stage & prod instance?

For iOS mobile applications, you can use the same App ID, which is your iOS app bundle ID, for both staging and production environments. However, on Android, the App ID should be unique for each environment. Therefore, our suggestion is to append 'stage' to the App ID created on the staging environment

+++


+++Can we just migrate Android app only?

No, both Android and iOS apps need to be migrated according to the steps outlined above.

+++

+++What type of verification do we need to perform after migration?

Our recommendation is to conduct functional validation of all your push-related use cases.

+++

+++What to do when getting 'Not Authorized' error while saving the mobile app?

This appears to be a permission issue related to Adobe Experience Platform Data Collection. To solve this, you must add 'Mobile' and 'Mobile App Configuration' permissions in the Adobe Admin Console, as outlined in the Prerequisites section of this article.

+++

+++Are changes required in mobile app code?

No, only configuration-related changes in Firebase and the app developer account are required. Changes in the customer mobile app are not required.

+++

+++Do we need to update the iOS certificate every year?

No, after this migration, there is no need to update the iOS certificate every year.

+++

+++What happens if this migration is not done?

The Android push messages will start failing after June 20, 2024, as per the notification from Google. [Read more](https://firebase.google.com/docs/cloud-messaging/migrate-v1){target="_blank"}.

+++

+++Can customers migrate back to FCM after completing the FCMv1 migration?

Yes, customers will be able to migrate back to FCM until June 20, 2024. After this date, the migration option will no longer be available.

+++

+++Is HTTP v1 API migration supported on SDK V4 mobile app?

No, customers need to first migrate their mobile app to the V5 SDK and then proceed with the above migration. They need to do it as a priority, as their push service will begin to fail from June 2024, as per the notification from Google.

+++

+++Does change on stage instance will have any impact on the production instance?

No, there is no impact of any changes in the stage mobile app on the production instance.

+++