---
title: Push notification advanced options
seo-title: Push notification advanced options
description: Push notification advanced options
seo-description: Learn how to personalize your push notifications with various advanced options.
page-status-flag: never-activated
uuid: d23e7f0a-7036-4674-a749-983e72dc9599
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/channels/using/push-notification-advanced-options
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2017-11-28T11 31 12.756-0500
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: push-notifications
cq-template: /apps/help/templates/article-3
discoiquuid: a61c9232-58ae-4eb0-83d0-8ddaaf7efffa
firstPublishExternalDate: 2017-11-16T10:43:54.736-0500
herogradient: light
isreadyforlocalization: false
jcr-created: 2017-11-29T19 03 21.743-0500
jcr-createdby: admin
jcr-description: Push notification advanced options
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2017-11-16T10:43:54.736-0500
lochandoffdate: 2017-11-28T11 31 12.755-0500
lr-lastreplicatedby: wmyersta@adobe.com
navTitle: Push notification advanced options
publishexternaldate: 2017-11-16T10 43 54.736-0500
publishExternalURL: https://helpx.adobe.com/campaign/standard/channels/using/push-notification-advanced-options.html
sha1: 33c3744a051684d0a2ea66914fe67d89ed0701e3
topicBrowsingSortDate: 2017-11-16T10:43:54.736-0500
index: y
internal: n
snippet: y
---

# Push notification advanced options

Push notification advanced options

To personalize your push notification, Adobe Campaign allows you to access a set of advanced options while creating a push notification.

![](assets/push_notif_advanced.png)

From the **Content** section, you can access and define the following options:

* A sound file if included in the mobile application

  In the **Play a sound** field, enter the filename of the sound file (without extension) to be played by the mobile device when the notification is received.

  If a suitable sound file with the name you provided is found, that sound is played when delivering the notification. Otherwise, the device's default sound is played.

* A badge

  The badge value must be an integer.

  To refresh the badge, enter 0 in the **Value of the badge** field. If the field is empty or does not contain an integer, the badge value will not change.

* A deeplink

  A deeplink enables you to bring the users directly to content located inside the application (instead of opening a web browser page).

  A deeplink can include personalization data for a custom in-app experience. For example, recipients' first names are automatically filled in on the page that the application directs them to.

* A category ID if available in the mobile application

  Enter a predefined category name to display actionable buttons when the push notification is received.

  ![](assets/push_notif_actionable_buttons.png)

  The mobile application developer must define the category ID and the buttons' expected behavior in the application. For more on this, refer to the [Apple Developer documentation](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/SupportingNotificationsinYourApp.html) (**Configuring Categories and Actionable Notifications** section).

* A custom field such as a URL
* Rich media content

  Enter the URL of your files to add rich content to your notification. For example, if you include a video, it will be played in the notification itself. Your recipients do not have to open the application to watch it.

  For iOS 10 or higher, you can insert image, gif, audio and video files. For iOS earlier versions, the push notification will be displayed without rich content.

  For Android, you can only include image files.

