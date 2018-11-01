---
title: Sending at the recipient's time zone
seo-title: Sending at the recipient's time zone
description: Sending at the recipient's time zone
seo-description: Learn how to send the message at the recipient's time zone.
page-status-flag: never-activated
uuid: 9c6d278b-c5fd-4043-a630-7e63718ae59e
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/sending/using/sending-at-the-recipient-s-time-zone
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-01-10T15 31 17.261-0500
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: sheduling-messages
cq-template: /apps/help/templates/article-3
discoiquuid: 6cfc3f7e-8e64-4fce-8fa5-eef91c7eedee
firstPublishExternalDate: 2018-01-10T15:31:17.252-0500
herogradient: light
jcr-created: 2018-01-11T19 02 04.811-0500
jcr-createdby: admin
jcr-description: Sending at the recipient's time zone
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-01-10T15:31:17.252-0500
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Sending at the recipient's time zone
publishexternaldate: 2018-01-10T15 31 17.252-0500
publishExternalURL: https://helpx.adobe.com/campaign/standard/sending/using/sending-at-the-recipient-s-time-zone.html
sha1: 13a823130921883b21c536a93bc4913ec6d4c3db
topicBrowsingSortDate: 2018-01-10T15:31:17.252-0500
index: y
internal: n
snippet: y
---

# Sending at the recipient's time zone

Sending at the recipient's time zone

When managing a campaign in which the date and time are important, you can schedule a delivery that takes each recipient's local time into account.

To use this functionality, make sure that all profiles targeted by your delivery have a time zone specified in the **Address** section of their properties. If a profile's **Time zone** is not specified, the message will be sent to the corresponding recipient as soon as the send is confirmed (not at the scheduled time). For more information on accessing profile properties, see [Editing profiles](../../audiences/using/editing-profiles.md).

**Example**

You want to send a promotional code that is only valid on Valentine's Day to all your customers around the world. To provide sufficient time to use it during the day, all customers must receive your message on February 14th at 8:00 AM.

1. In the delivery's **Schedule** window, select **Messages to be sent automatically on the date specified below**.
1. Set the contact date (February 14th at 8:00 AM) in the **Start sending from** field.

   ![](assets/send-time_opt_valentine.png)

1. From the send time optimization drop-down menu, choose **Send at the recipient's time zone**.
1. **Prepare** and **Confirm** your delivery.

   >[!NOTE]
   >
   >Make sure to confirm the send at least 24 hours in advance. Otherwise, depending on their locations, some recipients might receive the message as soon as the delivery is confirmed and not at the scheduled time.

No matter where they are located, all recipients will receive the message on February 14th at 8:00 AM their local time.
