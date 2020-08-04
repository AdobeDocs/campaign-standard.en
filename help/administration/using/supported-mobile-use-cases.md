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

In this page, you will find the list of every mobile use cases supported in [!DNL Adobe Campaign Standard] using the [!DNL Adobe Experience Platform SDKs]. Note that supporting these use cases involve installing and configuring the [!DNL Adobe Experience Platform SDKs], [!DNL Adobe Experience Platform Launch], and [!DNL Adobe Campaign Standard]. For more information on this, refer to this [page](../administration/using/configuring-a-mobile-application.md).

Adobe Campaign Standard supports the following use cases:

* [Register a mobile profile in Campaign Standard](../administration/using/supported-mobile-use-cases.md#register-mobile-profile)
* [Send a push token to Campaign Standard](../administration/using/supported-mobile-use-cases.md#send-push-token)
* [Enrich a mobile profile with custom data from your application](../administration/using/supported-mobile-use-cases.md#enrich-mobile-profile-custom)
* [Enrich a mobile profile with Lifecycle data from your application](../administration/using/supported-mobile-use-cases.md#enrich-mobile-profile-lifecycle)
* [Track user interaction with Push notifications](../administration/using/supported-mobile-use-cases.md#track-user-push)
* [Implement a custom event in your mobile app to trigger In-App messages](../administration/using/supported-mobile-use-cases.md#custom-event-inapp)
* [Set linkage fields for additional authentication for the profile template that is based In-App messages](../administration/using/supported-mobile-use-cases.md#linkage-fields-inapp)

To configure these use cases, you need the following extensions from [!DNL Experience Platform Launch]:

* **[!DNL Adobe Campaign Standard]** <br>To install and configure the Campaign Standard extension, see [Configure the Campaign Standard extension in Experience Platform Launch](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard#configure-the-campaign-standard-extension-in-experience-platform-launch).
* **[!DNL Mobile Core]**, which is automatically installed. <br>For more information about the Mobile Core extension, see [Mobile Core](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core).
* **[!DNL Profile]**, which is automatically installed. <br>For more information about the Profile extension, see [Profile](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/profile).

## Register a mobile profile in Campaign Standard {#register-mobile-profile}

### With iOS {#register-mobile-profile-ios}

In iOS, the following [!DNL Experience Platform APIs] are required:

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

In Android, the following [!DNL Experience Platform APIs] are required:

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

In iOS, the following [!DNL Experience Platform SDK] is required:

* **[!UICONTROL setPushIdentifier]** <br>For more information, see [setPushIdentifier](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard/adobe-campaign-standard-api-reference#setpushidentifier).

Here is the sample implementation for this use case with iOS:

```
func application(_ application: UIApplication, didRegisterForRemoteNotificationsWithDeviceToken deviceToken: Data) {
  
 // Register Device Token
 ACPCore.setPushIdentifier(deviceToken)
```

### With Android {#send-push-token-android}

In Android, the following [!DNL Experience Platform SDK] is required:

* **[!UICONTROL setPushIdentifier]** <br>For more information, see [setPushIdentifier](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard/adobe-campaign-standard-api-reference#setpushidentifier).

Here is the sample implementation for this use case with Android:

```
@Override
public void onNewToken(String token) {
    Log.d(TAG, "Refreshed token: " + token);
    MobileCore.setPushIdentifier(token);
}
```

## Enrich a mobile profile with custom data from your application {#enrich-mobile-profile-custom}

For this use case to work, you need to create rules for PII postbacks. For more information, see [PII Postbacks](../administration/using/configuring-rules-launch.md#pii-postback).

### With iOS {#enrich-mobile-profile-custom-ios}

In iOS, the following [!DNL Experience Platform API] is required:

* collectPII <br> For more information, see collectPII.

Here is a sample implementation of this use case with iOS:

```
ACPCore.collectPii(["email":email, "firstName":firstName, "lastName":lastName])
```

### With Android {#enrich-mobile-profile-custom-android}

In Android, the following [!DNL Experience Platform API] is required:

* collectPII <br> For more information, see collectPII.

Here is a sample implementation for this use case with Android:

```
HashMap<String, String> data = new HashMap<>();
data.put("firstName", firstNameText);
data.put("lastName", lastNameText);
data.put("email", emailText);
MobileCore.collectPii(data);
```

## Enrich a mobile profile with Lifecycle data from your application {#enrich-mobile-profile-lifecycle}

For this use case to work, you need to create rules for PII postbacks. For more information, see [PII Postbacks](../administration/using/configuring-rules-launch.md#pii-postback).

>[!NOTE]
>
>Adobe Campaign does not distinguish between custom data or lifecycle data from the mobile app. Both types of data can be sent to server using a collectPii postback rule in response to an event in the mobile app.

### With iOS {#enrich-mobile-profile-lifecycle-ios}

In iOS, the following [!DNL Experience Platform APIs] are required:

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

### With Android {#enrich-mobile-profile-lifecycle-android}

In Android, the following [!DNL Experience Platform APIs] are required:

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

## Track user interaction with Push notifications {#track-user-push}

You need to create rules for push notifications tracking postback. For more information, see [Push notifications tracking postback](../administration/using/configuring-rules-launch.md#push-tracking-postback).

### With iOS {#track-user-push-ios}

In iOS, the following [!DNL Experience Platform SDK] is required:

* **[!UICONTROL trackAction]**. For more information, see [Track app actions](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/mobile-core-api-reference#track-app-actions).

Here is a sample implementation of this use case with iOS:

```
let deliveryId = userInfo["_dId"] as? String
let broadlogId = userInfo["_mId"] as? String
if (deliveryId != nil && broadlogId != nil) {
    ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
}
 ```

### With Android {#track-user-push-android}

In Android, the following [!DNL Experience Platform SDK] is required:

* **[!UICONTROL trackAction]**
For more information, see [Track app actions](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/mobile-core-api-reference#track-app-actions).

Here is a sample implementation for this use case with Android:

```
contextData.put("deliveryId", deliveryId);
contextData.put("broadlogId", messageId);
contextData.put("action", "2");
MobileCore.trackAction("tracking", contextData);
```

## Implement a custom event in your application to trigger In-App messages {#custom-event-inapp}

### With iOS {#custom-event-inapp-ios}

In iOS, the following [!DNL Experience Platform SDK] is required:

* **[!UICONTROL trackAction]**. For more information, see [Track app actions](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/mobile-core-api-reference#track-app-actions).

Here is a sample implementation of this use case with iOS:

```
ACPCore.trackAction(mobileEventName, data: [:] )
 ```

### With Android {#custom-event-inapp-android}

In Android, the following [!DNL Experience Platform SDK] is required:

* **[!UICONTROL trackAction]**
For more information, see [Track app actions](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/mobile-core-api-reference#track-app-actions).

Here is a sample implementation for this use case with Android:

```
MobileCore.trackAction(mobileEventText, new HashMap<String,String>());
```

## Set linkage fields for additional authentication {#linkage-fields-inapp}

### With iOS {#linkage-fields-inapp-ios}

To set linkage fields for additional authentication for the profile template that is based on In-App messages in iOS, the following [!DNL Experience Platform SDK] is required:

* Set linkage fields <br>For more information, see [Set linkage fields](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard/adobe-campaign-standard-api-reference#set-linkage-fields).
* Reset linkage fields <br>For more information, see [Reset linkage fields](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard/adobe-campaign-standard-api-reference#reset-linkage-fields).

Here is are sample implementations of this use case with iOS.

To set linkage fields:

```
var linkageFields = [String: String]()
linkageFields["cusEmail"] = "john.doe@email.com"
ACPCampaign.setLinkageFields(linkageFields)
```

To reset linkage fields:

```
ACPCampaign.resetLinkageFields(linkageFields)
```

### With Android {#linkage-fields-inapp-android}

To set linkage fields for additional authentication for the profile template that is based on In-App messages in Android, the following Experience Platform SDK is required:

* Set linkage fields <br>For more information, see [Set linkage fields](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard/adobe-campaign-standard-api-reference#set-linkage-fields).
* Reset linkage fields <br>For more information, see [Reset linkage fields](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard/adobe-campaign-standard-api-reference#reset-linkage-fields).

Here is are sample implementations of this use case with Android.

To set linkage fields:

```
HashMap<String, String> linkageFields = new HashMap<String, String>();
linkageFields.put("cusEmail", "john.doe@email.com");
Campaign.setLinkageFields(linkageFields);
```

To reset linkage fields:

```
Campaign.resetLinkageFields()
```
