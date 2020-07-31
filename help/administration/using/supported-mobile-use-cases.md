---
title: Mobile use cases supported in Adobe Campaign Standard by using the Adobe Experience Platform SDKs
description: This document provides information about how to support mobile use cases.
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

# Mobile use cases supported in Adobe Campaign Standard {#mobile-use-cases}

In this page, you will find the list of every mobile use cases supported in [!DNL Adobe Campaign Standard] using the [!DNL Adobe Experience Platform SDKs]. Note supporting these use cases involve installing and configuring the [!DNL Adobe Experience Platform SDKs], [!DNL Adobe Experience Platform Launch], and [!DNL Adobe Campaign Standard]. For more information on this, refer to this [page](../administration/using/configuring-a-mobile-application.md).

Adobe Campaign Standard supports the following use cases:

* [Register a mobile profile in Campaign Standard](../administration/using/supported-mobile-use-cases.md#register-mobile-profile)
* [Send a push token to Campaign Standard](../administration/using/supported-mobile-use-cases.md#send-push-token)
* [Enrich a mobile profile with custom data from your application](../administration/using/supported-mobile-use-cases.md#enrich-mobile-profile-custom)
* Enrich a mobile profile with Lifecycle data from your application
* Track user interaction with Push notifications
* Implement a custom event in your mobile app to trigger In-App messages
* Track user interaction with In-App messages
* Set linkage fields for additional authentication for the profile template that is based In-App messages
* Send the user's location data to segment profiles that are based on the user's location history
* Leverage POI events as triggers in local notifications and In-App messages

To configure these use cases, you need the following extensions from Experience Platform Launch:

* **[!DNL Adobe Campaign Standard]** <br>To install and configure the Campaign Standard extension, see [Configure the Campaign Standard extension in Experience Platform Launch](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard#configure-the-campaign-standard-extension-in-experience-platform-launch).
* **[!DNL Mobile Core]**, which is automatically installed. <br>For more information about the Mobile Core extension, see [Mobile Core](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core).
* **[!DNL Profile]**, which is automatically installed. <br>For more information about the Profile extension, see [Profile](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/profile).

## Register a mobile profile in Campaign Standard {#register-mobile-profile}

### With iOS {#register-mobile-profile-ios}

In iOS, the following Experience Platform APIs are required:

* **[!UICONTROL Lifecycle Start]**, when the app is started and when the app is in the foreground.
* **[!UICONTROL Lifecycle Pause]**, when the app is in the background.

For more information, see [Lifecycle extension in iOS](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/lifecycle/lifecycle-extension-in-ios).

Here is a sample implementation of this use case with iOS:

```
 func application(_ application: UIApplication, didFinishLaunchingWithOptions launchOptions: [UIApplication.LaunchOptionsKey: Any]?) -> Bool {
  
  
 ACPCore.setLogLevel(.debug)
 appId = SettingsBundle.getLaunchAppId()
   
 //===== START Set up Adobe SDK =====
 ACPCore.configure(withAppId: appId)
   
 ACPCampaign.registerExtension()
 ACPIdentity.registerExtension()
 ACPLifecycle.registerExtension()
 ACPUserProfile.registerExtension()
 ACPSignal.registerExtension()
 ACPCore.start()
 ACPCore.lifecycleStart(nil)
   
 return true
 }
  
func applicationDidEnterBackground(_ application: UIApplication) {
 ACPCore.lifecyclePause()
 }
   
 func applicationDidBecomeActive(_ application: UIApplication) {
 // Workaround until jira AMSDK-7411 is fixed.
 sleep(2)
 ACPCore.lifecycleStart(nil)
 }

```

### With Android {#register-mobile-profile-android}

In Android, the following Experience Platform APIs are required:

* **[!UICONTROL OnResume]**
* **[!UICONTROL OnPause]**

For more information, see [Lifecycle extension in Android](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/lifecycle/lifecycle-extension-in-android).

Here is a sample implementation for this use case with Android:

```
@Override
  
public void onResume() {
 super.onResume();
 MobileCore.setApplication(getApplication());
 MobileCore.lifecycleStart(null);
 handleOpenTracking();
 }
  
 @Override
 public void onPause() {
 super.onPause();
 MobileCore.lifecyclePause();
 }
 ```

## Send a push token to Adobe Campaign Standard {#send-push-token}

### With iOS {#send-push-token-ios}

In iOS, the following Experience Platform SDK is required:

* **[!UICONTROL setPushIdentifier]** <br>For more information, see [setPushIdentifier](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard/adobe-campaign-standard-api-reference#setpushidentifier).

Here is the sample implementation for this use case with iOS:

```
func application(_ application: UIApplication, didRegisterForRemoteNotificationsWithDeviceToken deviceToken: Data) {
  
 // Register Device Token
 ACPCore.setPushIdentifier(deviceToken)
```

### With Android {#send-push-token-android}

In Android, the following Experience Platform SDK is required:

* **[!UICONTROL setPushIdentifier]** <br>For more information, see [setPushIdentifier](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard/adobe-campaign-standard-api-reference#setpushidentifier).

Here is the sample implementation for this use case with Android:

```
@Override
public void onNewToken(String token) {
    Log.d(TAG, "Refreshed token: " + token);
    MobileCore.setPushIdentifier(token);
}
```

## Enrich a mobile profile with custom data from your app {#enrich-mobile-profile-custom}

For this use case to work, you need to create rules for PII postbacks. For more information, see PII Postbacks.

### With iOS {#enrich-mobile-profile-custom-ios}

In iOS, the following Experience Platform API is required:

* collectPII <br> For more information, see collectPII.

Here is a sample implementation of this use case with iOS:

```
ACPCore.collectPii(["email":email, "firstName":firstName, "lastName":lastName])
```

### With Android {#enrich-mobile-profile-custom-android}

In Android, the following Experience Platform API is required:

* collectPII <br> For more information, see collectPII.

Here is a sample implementation for this use case with Android:

```
HashMap<String, String> data = new HashMap<>();
data.put("firstName", firstNameText);
data.put("lastName", lastNameText);
data.put("email", emailText);
MobileCore.collectPii(data);
```

