---
title: Push notification report
description: With the Push notification out-of-the-box report, learn about the success of your push notifications.
audience: reporting
content-type: reference
topic-tags: list-of-reports
feature: Reporting
role: Leader
level: Intermediate
exl-id: acfe0b9c-77a4-46ad-8151-7bf9c21fa4b0
TQID: https://experienceleague.adobe.com/Z7fXMSiDxpF6LXWMV2aYc71UvOYWlUzyOv8TS6ogS7k
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
role_v2:
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
---
# Push notification report{#push-notification-report}

>[!CAUTION]
>
>Please note that you have to drag and drop the **[!UICONTROL Message type]** metrics to your tables to split your data depending on your delivery types, in this case push notification deliveries.

The **Push notification** report provides details of marketing performance of push notifications in Adobe Campaign. This out-of-the-box report helps you understand how users interact with push notifications, mobile applications and deliveries.

Some configuration is required in the mobile application to implement push tracking, refer to this [page](../../administration/using/push-tracking.md) for the detailed steps.

![](assets/dynamic_report_push.png)

Each table is represented by summary numbers and charts. You can change how the details are shown in their respective visualization settings.

The first table **Push notification Engagement Summary** is split into three categories: by day, by mobile app and by delivery. It contains the available data for recipient reactivity to the delivery:

* **[!UICONTROL Processed/sent]**: Total number of push notifications sent.
* **[!UICONTROL Delivered]**: Number of push notifications successfully sent, in relation to the total number of sent push notifications.
* **[!UICONTROL Impressions]**: Number of times a push notification has been delivered to the device and left untouched in the notification center. In most cases, impressions number should be similar to the delivered number. This ensures that the device got the message and relayed that information back to the server.
* **[!UICONTROL Unique impressions]**: Number of impressions by recipient.
* **[!UICONTROL Click through rate]**: Percentage of users who interacted with the push notification.
* **[!UICONTROL Open rate]**: Percentage of opened push notifications.

![](assets/dynamic_report_push_2.png)

The second table **Push notification Clicks & opens** is split into three categories: by day, by mobile app and by delivery. It contains the available data for recipient behavior per delivery:

* **[!UICONTROL Impressions]**: Total of push notifications seen by recipients. 
* **[!UICONTROL Unique impressions]**: Number of impressions by recipient.
* **[!UICONTROL Click]**: Number of times a push notification has been delivered to the device and clicked by the user. The user either wanted to view the notification, which will then be moved to Push Open tracking, or dismiss it.
* **[!UICONTROL Unique clicks]**: Number of times a unique user interacts with the push notification, e.g. clicks on the notification or button.
* **[!UICONTROL Open]**: Total number of push notifications delivered to the device and clicked on by users thus opening the app. This is similar to the Push Click except a Push Open will not be triggered if the notification was dismissed.
* **[!UICONTROL Unique Opens]**: Number of recipients who opened the delivery.
