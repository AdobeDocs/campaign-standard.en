---
solution: Campaign Standard
product: campaign
title: Implementing Push tracking
description: This document allows you to ensure that push notification tracking has been implemented correctly on iOS and Android.
audience: channels
content-type: reference
topic-tags: push-notifications
context-tags: mobileApp,overview
---

# Implementing local tracking {#local-tracking}

## About local tracking {#about-local-tracking}

In this page, learn how to ensure that local notification tracking has been implemented correctly. Note that this implies that local notification has already been configured.

Local notification tracking can be split into three types:

* **Local impressions** - When a local notification has been delivered to the device and is sitting on the notification center, but has not been touched at all. In most cases, impressions number should be similar if not the same as the delivered number. It ensures that the device did get the message and relays that information back to the server.

* **Local click** - When a local notification has been delivered to the device and the user has clicked on the device. The user either wanted to view the notification (which will in turn move to local open tracking) or to dismiss the notification.

* **Local open** - When a local notification has been delivered to the device and the user has clicked on the notification causing the application the open. This is similar to the local click except a local open will not be triggered if the notification was dismissed.

To implement tracking for Adobe Campaign Standard, the mobile application needs to include Mobile SDK in the application. These SDKs are available in [!DNL Adobe Mobile Services].

To send tracking information, there are three variables that need to be sent: two are part of the data received from Adobe Campaign and the other is an action variable that dictates whether it is an impression, click or open.

| Variable | Value |
| :-: | :-: |
| deliveryId |  "deliveryId" from incoming data (similar to push tracking where"_dld" is used) |
| broadlogId | "broadlogId" from incoming data (similar to push tracking where "_mld" is used) |
| action | "1" for Open, "2" for Click and "7" for Impression |

## Implementing local impression tracking {#implement-local-impression-tracking}

For impression tracking, you need to send value "7" for action when calling collectMessageInfo() or trackAction() functions.

### For Android {#implement-local-impression-tracking-android}

The Adobe Experience Platform Mobile SDK starts the impression tracking for local notification when triggering it.

### For iOS {#implement-local-impression-tracking-ios}

To explain how to implement impression tracking, we need to understand the three states of an application:

* **Foreground**: when the application is currently active and on screen in the foreground.

* **Background**: when the application is not on screen but the process is not closed either. When double-clicking the home button, it usually showcases all the applications in the background.

* **Off/Closed**: when the application's process has been killed. If an application is closed, Apple will not call it until the application has been relaunched. This means that you can never truly know when the notification has been received on iOS.

To have impression tracking still working while the application is in the background, we need to send "Content-Available" to let the application know that tracking needs to be done.

The Adobe Experience Platform Mobile SDK starts the impression tracking for local notification when triggering it.

>[!CAUTION]
>
>iOS impression tracking is not accurate and should not be looked at reliably.

## Implementing click tracking {#implementing-click-tracking}

For click tracking, you need to send value "2" for action when calling collectMessageInfo() or trackAction() functions.

### For Android {#implement-click-tracking-android}

To track click, two scenarios need to be handled:

* The user sees the notification but clears it.

* The user sees the notification and clicks on it, this will turn to a open tracking.

First scenario of click is tracked by Adobe Experience Platform Mobile SDK.

### For iOS {#implement-click-tracking-ios}

```
// AppDelegate.swift
...
import os.log
import UserNotifications
...
  
func registerForPushNotifications() {
        let center = UNUserNotificationCenter.current()
        center.delegate = notificationDelegate
        //Here we are creating a new Category that allows us to handle Dismiss Actions
        let defaultCategory = UNNotificationCategory(identifier: "DEFAULT", actions: [], intentIdentifiers: [], options: .customDismissAction)
        //Add it to our array of Category, in this case we only have one
        center.setNotificationCategories([defaultCategory])
        center.requestAuthorization(options: [.alert, .sound, .badge]) {
            (granted, error) in
            os_log("Permission granted: %{public}@", type:. debug, granted.description)
            if error != nil {
                return
            }
            if granted {
                os_log("Notifications allowed", type: .debug)
            }
            else {
                os_log("Notifications denied", type: .debug)
            }
  
            // 2. Attempt registration for remote notifications on the main thread
            DispatchQueue.main.async {
                UIApplication.shared.registerForRemoteNotifications()
            }
        }
    }
```

Then to handle the dismiss and send a tracking information, you need to add the following:

```
func userNotificationCenter(_ center: UNUserNotificationCenter, didReceive response: UNNotificationResponse, withCompletionHandler completionHandler: @escaping () -> Void) {
        let userInfo = response.notification.request.content.userInfo
        switch response.actionIdentifier {
        case UNNotificationDismissActionIdentifier:
            print("Dismiss Action")
            let deliveryId = userInfo["deliveryId"] as? String
            let broadlogId = userInfo["broadlogId"] as? String
            if (deliveryId != nil && broadlogId != nil) {
                // If you're using  ACPCore v2.3.0 or later, use the line below.
                ACPCore.collectMessageInfo(["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
                // Else comment out the above line and uncomment the line below
                // ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
            }
        default:
            ////MORE CODE
        }
        completionHandler()
    }
```

## Implementing open tracking {#implement-open-tracking}

You need to send "1" and "2" since user must click on the notification to open the application. If the application is not launched/opened through local notification, then no tracking events occur.

### For Android {#implement-open-tracking-android}

To track open, we need to create intent. Intent objects allow Android OS to call your method when certain actions are done, in this case clicking the notification to open the app.

This code is based on the implementation of the click impression tracking. With intent set, you now need to send tracking information back to Adobe Campaign. In this case, Android View([!DNL Activity]) which triggered the notification will be opened or brought to foreground as a result of the click by user. The intent object in [!DNL Activity] contains the notification data which can be used to track open.

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
        //Looks it was opened based on the notification, lets get the tracking we passed on.
        Map<String, String> notificationData = (Map<String, Object>)data.getSerializableExtra("NOTIFICATION_USER_INFO");
        String deliveryId = (String)notificationData.get("deliveryId");
        String messageId = (String)notificationData.get("broadlogId");
  
  
  
        if (deliveryId != null && messageId != null) {
            HashMap<String, String> contextData = new HashMap<>();
            contextData.put("deliveryId", deliveryId);
            contextData.put("broadlogId", messageId);
  
            //Send Click Tracking since the user did click on the notification
            contextData.put("action", "2");
            // If you're using  ACPCore v1.4.0 or later, use the next line.
            MobileCore.collectMessageInfo(contextData);
            // Else comment out the above line and uncomment the line below
            // MobileCore.trackAction("tracking", contextData);
  
            //Send Open Tracking since the user opened the app
            contextData.put("action", "1");
            // If you're using  ACPCore v1.4.0 or later, use the next line.
            MobileCore.collectMessageInfo(contextData);
            // Else comment out the above line and uncomment the line below
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
  
    // Called when user clicks the local notification or also called from willPresent()
    func userNotificationCenter(_ center: UNUserNotificationCenter, didReceive response: UNNotificationResponse, withCompletionHandler completionHandler: @escaping () -> Void) {
  
        let userInfo = response.notification.request.content.userInfo
        os_log("App push data %{public}@, in userNotificationCenter:didReceive()", type: .debug, userInfo)
        switch response.actionIdentifier {
        case UNNotificationDismissActionIdentifier:
            //This is to handle the Dismiss Action
            let deliveryId = userInfo["deliveryId"] as? String
            let broadlogId = userInfo["broadlogId"] as? String
            if (deliveryId != nil && broadlogId != nil) {
            // If you're using  ACPCore v2.3.0 or later, use the line below.
                ACPCore.collectMessageInfo(["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
            // Else comment out the above line and uncomment the line below
            // ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
            }
        default:
            //This is to handle the tracking when the app opens
            let deliveryId = userInfo["deliveryId"] as? String
            let broadlogId = userInfo["broadlogId"] as? String
            if (deliveryId != nil && broadlogId != nil) {
               // If you're using  ACPCore v2.3.0 or later, use the line below.
               ACPCore.collectMessageInfo(["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
               ACPCore.collectMessageInfo(["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"1"])
               // Else comment out the above line and uncomment the line below
               // ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
               // ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"1"])
            }
        }
        completionHandler()
    }
}
```
