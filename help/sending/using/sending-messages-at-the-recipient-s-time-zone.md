---
title: Sending messages at the recipient's time zone
seo-title: Sending messages at the recipient's time zone
description: Sending messages at the recipient's time zone
seo-description: Learn how to send messages at the recipient's time zone.
uuid: 90e61d78-2de3-451b-a94c-35449a93b4e7
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/sending/using/sending-messages-at-the-recipient-s-time-zone
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-08T08 23 05.533-0400
cq-lastreplicated: 2018-09-07T15 11 22.010-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: sheduling-messages
cq-template: /apps/help/templates/article-3
discoiquuid: c8538eeb-9884-4d7b-8807-b63a2ac93182
firstPublishExternalDate: 2018-09-07T15:11:21.952-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 01 59.928-0400
jcr-createdby: admin
jcr-description: Sending messages at the recipient's time zone
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T15:11:21.952-0400
lochandoffdate: 2018-09-08T08 23 05.533-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Sending messages at the recipient's time zone
publishexternaldate: 2018-09-07T15 11 21.952-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/sending/using/sending-messages-at-the-recipient-s-time-zone.html
sha1: 169d74daf2939b121d89b84d4ffabd212b04fc21
topicBrowsingSortDate: 2018-09-07T15:11:21.952-0400
index: y
internal: n
snippet: y
---

# Sending messages at the recipient's time zone

Sending messages at the recipient's time zone

When managing a campaign in which the date and time are important, you can schedule a delivery that takes each recipient's local time into account.

To use this functionality, make sure that all profiles targeted by your delivery have a time zone specified in the **Address** section of their properties. For more information on accessing profile properties, refer to this [section](../../audiences/using/editing-profiles.md).

To send a delivery at the recipient's time zone, you can also use the **Scheduler** activity in a workflow. For more on this, refer to this [page](../../automating/using/scheduler.md).

In the following example, we want to send a promotional code that is only valid on Valentine's Day to all customers around the world. To provide sufficient time to use it during the day, all customers must receive your message on February 14th at 8:00 AM depending on their time zones.

1. In the **Marketing activities** tab, start creating your delivery, in our case an email. To learn more on delivery creation, refer to this [section](../../channels/using/creating-an-email.md).
1. After designing your Valentine's Day email, click **Create** to access the delivery dashboard. For more on email designing, refer to this [page](../../designing/using/example--email-personalization.md).

   ![](assets/send-time_opt_valentine_1.png)

1. From the delivery dashboard, select the **Schedule** block.

   ![](assets/send-time_opt_valentine_2.png)

1. Select the **Messages to be sent automatically on the date** option specified below. Then in the **Start sending from** field, set the contact date, in our case February 14th at 8:00 AM so that every recipient receives it on Valentine's Day.

   ![](assets/send-time_opt_valentine.png)

1. In the **Time zone of the contact date** field, select at which time zone your delivery should be sent by default.

   If a profile's **Time zone** is left as **Default**, the recipients will receive the delivery depending on the chosen time zone here.

1. From the **Optimize the sending time per recipient** drop-down menu, choose **Send at the recipient's time zone**. This allows recipients to receive the Valentine's day email on the 14 of February depending on their time zone.

   ![](assets/send-time_opt_valentine_3.png)

1. After confirming your schedule for your delivery, click the **Prepare** button then **Confirm** your delivery.

   Make sure to confirm the send at least 24 hours in advance. Otherwise, depending on their locations, some recipients might receive the delivery before the actual Valentine's day event.

   ![](assets/send-time_opt_valentine_4.png)

No matter where they are located, all recipients will receive the message on February 14th at 8:00 AM their local time.
