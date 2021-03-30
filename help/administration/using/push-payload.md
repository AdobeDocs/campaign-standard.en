---
solution: Campaign Standard
product: campaign
title: Understanding Campaign Standard Push Notifications Payload Structure
description: This document is intended to describe the structure of the payload received in mobile applications.
audience: channels
content-type: reference
topic-tags: push-notifications
context-tags: mobileApp,overview
feature: Instance Settings
role: Administrator
level: Experienced
---

# Understanding push notifications payload structure {#push-payload}

Adobe Campaign allows you to send personalized and segmented push notifications on iOS and Android mobile devices to mobile applications (mobile app).

Every push notification that is received on a mobile app carries some information which is used by the app to display the push notification if an Alert push notification is sent, and most likely to also do some further computation, especially if a silent push notification is sent.

This information is received by the mobile app code in an event handler that indicates that a push notification was received. When sending push notifications from Adobe Campaign Standard, the information received in the mobile app may also contain Campaign Standard specific information which may be used to leverage some features provided by Campaign Standard. Additionally, the payload can contain custom data that can be consumed by the mobile app.

This document describes the structure of the payload received in a mobile app when a push notification is successfully sent to an app from Adobe Campaign Standard.

>[!NOTE]
>
>The payload structure varies depending on the type of mobile app (i.e. iOS app, FCM-enabled Android app).

## Push payload structure {#push-payload-structure}

This section details a structure of a sample payload for various mobile platforms and describes major attributes that are contained in it. This is the structure of the payload received in the mobile app code in the event handler that indicates that a push notification has been received. 

The payload attributes and their values will vary based on the configurations provided in Push notification advanced options. This section also provides a mapping between these configurations in Campaign Standard UI and the attributes in the payload in order to clarify how the payload will change on configuring an option in Campaign Standard.

### For iOS Mobile App {#payload-structure-ios}

**Sample Payload sent from Adobe Campaign to iOS app:**

```
{

    "aps":{

            "alert":{

                    "body":"This is the content of my push notification",

                    "title":"Push Notification Title"

            },

            "content-available":1,

            "category":"NEW_MESSAGE_CATEGORY",

            "badge":2,

            "mutable-content":1,

            "sound":"default"

        },

    "custom_field1":"custom_value1",

    "custom_field2":"custom_value2",

    "media-attachment-url":"https://2.img-dpreview.com/files/p/articles/9440145363/Creative_Cloud.jpeg",

    "uri":"https://mydeeplinkurl.com",

    "_dId":"56c4",

    "_mId":"h138a"} 
```

**JSON sample payload to use with [iOS APNS Tester](https://pushtry.com/)**

```
{

  "aps": {

    "alert": {

      "title": "Push Notification Title",

      "body": "body of push"

    },

    "badge": 33,

    "sound": "default"

  },

  "custom_field1": "custom_value1",

  "uri": "https://mydeeplinkurl.com"

}
```

The most important section of the payload is the aps dictionary, which contains Apple-defined keys and is used to determine how the system receiving the notification should alert the user, if at all. This section contains pre-defined keys that are used by the mobile app to formulate the behavior of the push notification.

In-depth details on the attributes within aps can be found in Apple developer docs: [Creating the Remote Notification Payload](https://developer.apple.com/library/archive/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CreatingtheNotificationPayload.html#//apple_ref/doc/uid/TP40008194-CH10-SW1).

### For Android App {#payload-structure-android}

**Sample Payload send from Adobe Campaign to Android app**

```
{

  "collapseKey": "1476005",

  "priority": "high",

  "data": {

    "_dId": "d57fd6",

    "_mId": "h1685a5",

    "body": "adobe body 123",

    "category": "adobe category 123",

    "custom key 1": "value 1",

    "custom key 2": "test value 2",

    "custom key 3": "foo bar android",

    "media-attachment-url": "http://adobegiphy.com?test=123",

    "sound": "http://testcampaign.instance.com/r/?id=s1685a5,d57fd6,d57ff5",

    "title": "adobe title 123",

    "uri": "http://testcampaign.instance.com/r/?id=d1685a5,d57fd6,d57ff6",

    "badge": 1817

  }

}
```

**JSON sample payload to use [Google FCM tester](https://pushtry.com/)**

```
{

  "to": "<==========ENTER your device token==============>",

  "collapseKey": "1476005",

  "priority": "high",

  "data": {

    "_dId": "d57fd6",

    "_mId": "h1685a5",

    "title": "adobe title 123",

    "body": "adobe body 123",

    "category": "adobe category 123",

    "custom key 1": "value 1",

    "custom key 2": "test value 2",

    "custom key 3": "foo bar android",

    "media-attachment-url": "http://adobegiphy.com?test=123",

    "sound": "http://testcampaign.instance.com/r/?id=s1685a5,d57fd6,d57ff5",

    "uri": "http://testcampaign.instance.com/r/?id=d1685a5,d57fd6,d57ff6",

    "badge": 1817

  }

}
```

The payload contains data message which includes all the push notification delivery content including the custom key/value pairs, and the client app must handle the message to build and show push notification, if required or else to add any other business logic. 

To understand aspects of an android payload refer to [Messaging Concepts and Options (fcm)](https://firebase.google.com/docs/cloud-messaging/concept-options).

>[!NOTE]
>
>Support for Notification messages in Android payload was removed as of January 2018 to enable waking up of the App and passing control to the mobile App without needing user to interact with the App.

### Mapping between Campaign Standard Configurations and Payload Attributes {#mapping-payload}

|  Campaign Configuration | Impacted Attribute in iOS  |  Impacted Attribute in Android |  Description |
|:-:|:-:|:-:|:-:|
|  Message title <br>Message body | alert → title <br> alert → body  | title <br>body  | This data contains specifics of the alert message.<br>The title and body keys provide the contents of the alert.  |
|  Play a sound | sound  |  sound |  A custom sound to play with the alert. |
| Value of the badge | badge  |  badge |  An integer value to be used to badge the app’s icon. |
| Add a deeplink |  uri |  NA |  A deeplink enables you to bring the users directly to content located inside the application (instead of opening a web browser page). |
| Category  |  category |  category |  To display custom actions with a remote notification. <br>The category key helps the system display the actions for that category as buttons in the alert interface. |
|  Custom fields |  custom_field1, custom_field2 ... |  custom_field1, custom_field2 ... | Any custom data that you want to send to your app.  |
| Rich media content URL (image, gif, audio and video files)<br>(Only applicable for iOS 10 or higher)  |  media-attachment-url |  NA | URL of your media files to add rich content to your notification. <br>On providing a value for this URL, the mutable-content flag is automatically sent into the payload. <br> (Only applicable for iOS 10 or higher)  |
|  Mutable Content <br> (Only applicable for iOS 10 or higher) | mutable-content  | NA  | The Notification Service Extension in your app will "intercept" all remote notifications with the mutable-content key and will allow you to handle/manipulate the contents of the request payload, which can then be used to customize the notification. Use cases of this feature include downloading and displaying multiple media, decrypting any encrypted data present in the push payload. More information can be found in [Modify the payload of a Remote Notification](https://developer.apple.com/library/archive/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/ModifyingNotifications.html). <br>(Only applicable for iOS 10 or higher)  |
|   Content Available |   content-available |  NA | Selecting this option enables waking up of an iOS app while it is in background/suspended state. Waking up implies that the app runs in the background and the appropriate event handler responsible for receiving the push notification data payload gets a control and can use the data to do any computation, including but not limited to building custom push notification and displaying the same. More information can be found in [Wake up App with Notification delivery](https://developer.apple.com/library/archive/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CreatingtheNotificationPayload.html).  |
| Rich media content URL (image files)<br>(Only applicable forAndroid)  | NA | media-attachment-url  |  URL of your image files to add rich content to your notification. |
|  NA |  _mId<br>_dId |  _mId <br>_dId | Values of broadlogId and deliveryId.<br>These attributes are required if your app wishes to call a tracking postback to track when the push notification was clicked/opened. This information is computed and sent internally by the app server without user intervention.<br>Information on postbacks can be found in this [page](https://helpx.adobe.com/campaign/kb/config-app-in-launch.html#PIIpostback). |

### How to retrieve payload information in mobile app code {#payload-information}

The payload information that is sent by the app server is received by the mobile app code in an event handler that indicates that a push notification was received. This event would vary based on the mobile platform being worked upon and also based on whether the app is running in foreground or background. The following documentation will help you identify the event handler you wish to handle based on your use case.

* iOS applications: **Handling Remote Notifications** section in [Remote Notifications](https://developer.apple.com/library/archive/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/HandlingRemoteNotifications.html).
* Android applications: [Receiving Messages on an Android Client App](https://firebase.google.com/docs/cloud-messaging/android/receive)

**Sample for iOS Mobile App**

```
 - (void)application:(UIApplication *)application

didReceiveRemoteNotification:(NSDictionary *)userInfo {

    

    NSDictionary *apsDict = [userInfo objectForKey:@"aps"];

    NSDictionary *alertDict = [apsDict objectForKey:@"alert"];

    NSString *title = [alertDict objectForKey:@"title"];

    NSString *body = [alertDict objectForKey:@"body"];

    NSString *category = [apsDict objectForKey:@"category"];

    NSString *deliveryId = userInfo[@"_dId"];

    NSString *broadlogId = userInfo[@"_mId"];

    NSString *mediaAttachmentURL = userInfo[@"media-attachment-url"];

    NSString *deeplinkURL = userInfo[@"uri"];

    NSString *customValue1 = userInfo[@"custom_field1"];   

}
```

**Sample for Android Mobile FCM App**

```
public void onMessageReceived(RemoteMessage message) {

    Map<String, String> dataMap = message.getData();

     

    String title = dataMap.get("title");

    String body = dataMap.get("body");

    String category = dataMap.get("category");

    String deliveryId = dataMap.get("_dId");

    String broadlogId = dataMap.get("_mId");

    String mediaAttachmentURL = dataMap.get("media-attachment-url");

    String deeplinkURL = dataMap.get("uri");

    String customValue1 = dataMap.get("custom_field1");

}
```