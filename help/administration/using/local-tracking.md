---
solution: Campaign Standard
product: campaign
title: Implementing Push tracking
description: This document allows you to ensure that push notification tracking has been implemented correctly on iOS and Android.
audience: channels
content-type: reference
topic-tags: push-notifications
context-tags: mobileApp,overview
feature: Instance Settings
role: Admin
level: Experienced
exl-id: b983d0a3-c345-44d4-bc82-202bf6ed26ab
---
# Implementing local tracking {#local-tracking}

## About local tracking {#about-local-tracking}

In this page, learn how to ensure that local notification tracking has been implemented correctly. Note that this implies that local notification has already been configured.

Local notification tracking can be split into three types:

* **Local impressions** - When a local notification has been delivered to the device and is sitting on the notification center, but has not been touched at all. In most cases, impressions number should be similar if not the same as the delivered number. It ensures that the device did get the message and relays that information back to the server.

* **Local click** - When a local notification has been delivered to the device and the user has clicked on the notification. The user either wanted to view the notification (which will in turn move to local open tracking) or to dismiss the notification.

* **Local open** - When a local notification has been delivered to the device and the user has clicked on the notification causing the application the open. This is similar to the local click except a local open will not be triggered if the notification was dismissed.

To implement tracking for Adobe Campaign Standard, the mobile application needs to include Mobile SDK in the application. These SDKs are available in [!DNL Adobe Mobile Services].

To send tracking information, there are three variables that must be sent: two are part of the data received from Adobe Campaign and the other is an action variable that dictates whether it is an impression, click or open.

| Variable | Value |
| :-: | :-: |
| deliveryId | `deliveryId` from incoming data (similar to push tracking where `_dld` is used) |
| broadlogId | `broadlogId` from incoming data (similar to push tracking where `_mld` is used) |
| action | "1" for Open, "2" for Click and "7" for Impression |

## Implement local impression tracking {#implement-local-impression-tracking}

The Adobe Experience Platform Mobile SDK will automatically send the impression event for both Android and iOS without any additional configuration.

## Implement click tracking {#implementing-click-tracking}

For click tracking, you must send value "2" for action when calling `collectMessageInfo()` or `trackAction()` functions.

### For Android {#implement-click-tracking-android}

To track clicks, two scenarios must be implemented:

* The user sees the notification but clears it.
    
    To track click in case of dismissal scenario, add the broadcast receiver `NotificationDismissalHandler` in your application module's AndroidManifest file.

    ```
    <receiver
    android:name="com.adobe.marketing.mobile.NotificationDismissalHandler">
    </receiver>
    ```

* The user sees the notification and clicks on it, this will turn to a open tracking.
    
    This scenario should produce a click and an open. Tracking this click will be a part of the implementation needed to track the open. See [Implementing open tracking](#implement-open-tracking).

### For iOS {#implement-click-tracking-ios}

To send the click tracking information, you must add the following:

```
class NotificationDelegate: NSObject, UNUserNotificationCenterDelegate {

   func userNotificationCenter(_ center: UNUserNotificationCenter, didReceive response: UNNotificationResponse, withCompletionHandler completionHandler: @escaping () -> Void) {
        let userInfo = response.notification.request.content.userInfo
        switch response.actionIdentifier {
        case UNNotificationDismissActionIdentifier:
            print("Dismiss Action")
            let deliveryId = userInfo["deliveryId"] as? String
            let broadlogId = userInfo["broadlogId"] as? String
            if (deliveryId != nil && broadlogId != nil) {
                
                //If you are using ACPCore v2.3.0 or later, use the next line.
                
                ACPCore.collectMessageInfo(["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
                
                //Else comment out the above line and uncomment the line below
                
                // ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
            }
        default:
            
            ////MORE CODE
        }
        completionHandler()
    }
}
```

## Implement open tracking {#implement-open-tracking}

You must send "1" and "2" since user must click on the notification to open the application. If the application is not launched/opened through local notification, then no tracking events occur.

### For Android {#implement-open-tracking-android}

To track open, we must create intent. Intent objects allow Android OS to call your method when certain actions are done, in this case clicking the notification to open the app.

This code is based on the implementation of the click impression tracking. With intent set, you now must send tracking information back to Adobe Campaign. In this case, Android View([!DNL Activity]) which triggered the notification will be opened or brought to foreground as a result of the click by user. The intent object in [!DNL Activity] contains the notification data which can be used to track open.

MainActivity.java (extends [!DNL Activity])

```

@Override
protected void onResume() {
    super.onResume();
    handleTracking();
}
 
 
private void handleTracking() {

    //Check to see if this view was opened based on a notification

    Intent intent = getIntent();
    Bundle data = intent.getExtras();
 
    if (data != null) {

        //Opened based on the notification, you must get the tracking that was passed on.

        Map<String, String> notificationData = (Map<String, Object>)data.getSerializableExtra("NOTIFICATION_USER_INFO");
        String deliveryId = (String)notificationData.get("deliveryId");
        String messageId = (String)notificationData.get("broadlogId");

        if (deliveryId != null && messageId != null) {
            HashMap<String, String> contextData = new HashMap<>();
            contextData.put("deliveryId", deliveryId);
            contextData.put("broadlogId", messageId);
 
            //Send click tracking since the user did click on the notification

            contextData.put("action", "2");

            //If you are using ACPCore v1.4.0 or later, use the next line.
    
            MobileCore.collectMessageInfo(contextData);

            //Else comment out the above line and uncomment the line below

            // MobileCore.trackAction("tracking", contextData);
 
            //Send open tracking since the user opened the app

            contextData.put("action", "1");

            //If you are using  ACPCore v1.4.0 or later, use the next line.

            MobileCore.collectMessageInfo(contextData);

            //Else comment out the above line and uncomment the line below

            // MobileCore.trackAction("tracking", contextData);
        }
    }
}
```

### For iOS {#implement-open-tracking-ios}

```
import os.log
import Foundation
import UserNotifications
import UserNotificationsUI
import ACPCore
 
class NotificationDelegate: NSObject, UNUserNotificationCenterDelegate {
 
    //Called when user clicks the local notification or also called from willPresent()

    func userNotificationCenter(_ center: UNUserNotificationCenter, didReceive response: UNNotificationResponse, withCompletionHandler completionHandler: @escaping () -> Void) {
 
        let userInfo = response.notification.request.content.userInfo
        os_log("App push data %{public}@, in userNotificationCenter:didReceive()", type: .debug, userInfo)
        switch response.actionIdentifier {
        case UNNotificationDismissActionIdentifier:

            //This is to handle the Dismiss action

            let deliveryId = userInfo["deliveryId"] as? String
            let broadlogId = userInfo["broadlogId"] as? String
            if (deliveryId != nil && broadlogId != nil) {

                //If you are using ACPCore v2.3.0 or later, use the next line.

                ACPCore.collectMessageInfo(["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])

                //Else comment out the above line and uncomment the line below

                // ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
            }
        default:
            //This is to handle the tracking when the app opens
            let deliveryId = userInfo["deliveryId"] as? String
            let broadlogId = userInfo["broadlogId"] as? String
            if (deliveryId != nil && broadlogId != nil) {

               //If you are using ACPCore v2.3.0 or later, use the next line.

               ACPCore.collectMessageInfo(["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
               ACPCore.collectMessageInfo(["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"1"])

               //Else comment out the above line and uncomment the line below

               // ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
               // ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"1"])
            }
        }
        completionHandler()
    }
}
```
