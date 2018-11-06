---
title: About scheduling messages
seo-title: About scheduling messages
description: About scheduling messages
seo-description: Learn how to schedule your messages.
uuid: ec238e7d-fbe9-4fac-afb4-231b661eb65c
content-encoding: UTF-8
aemsrcnodepath: /content/help/en/campaign/standard/sending/using/about-scheduling-messages
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-08T08 23 05.105-0400
cq-lastreplicated: 2018-09-07T15 11 19.314-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: sheduling-messages
cq-template: /apps/help/templates/article-3
discoiquuid: fb31fee4-fb9e-494a-a9de-f827b5054f37
firstPublishExternalDate: 2018-09-07T15:11:19.254-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 01 52.411-0400
jcr-createdby: admin
jcr-description: About scheduling messages
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T15:11:19.254-0400
lochandoffdate: 2018-09-08T08 23 05.104-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: About scheduling messages
publishexternaldate: 2018-09-07T15 11 19.254-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/sending/using/about-scheduling-messages.html
sha1: e585771b7455f5c66bb080ae0cbf87bec535ac8b
topicBrowsingSortDate: 2018-09-07T15:11:19.254-0400
index: y
internal: n
snippet: y
---

# About scheduling messages

About scheduling messages

>[!CAUTION]
>
>Whenever making changes to a delivery’s schedule, you must re-prepare the delivery by clicking on the **Prepare** button before clicking **Confirm**.

In the message dashboard, the **Schedule** block allows you to define when messages will be sent.

![](assets/delivery_dashboard.png)

The **Schedule** properties let you set sending options:

* **Messages to be sent once confirmed**: messages are sent as soon as the send is confirmed. See [Confirming the send](../../sending/using/confirming-the-send.md).

  ![](assets/delivery_planning_1.png)

* **Messages to be sent automatically on the date specified below**: messages will be sent at a later date and time. Specify the **contact date** in the **Start sending from** field.

  You can prepare and confirm the send, but messages will only be sent starting the selected date and time. Preparing and confirming the send are presented in the [Preparing the send](../../sending/using/preparing-the-send.md) and [Confirming the send](../../sending/using/confirming-the-send.md) sections.

  The **Time zone of the contact date** drop-down list allows you to modify the time zone that will be taken into account for the sending time. For example, if you enter 9:00 AM in the **Start sending from** field and if you select Brussels, Copenhagen, Madrid, Paris (GMT+1) in the **Time zone of the contact date** drop-down list, all recipients will receive the message at 9:00 AM Paris time. Therefore, a recipient located in Moscow (GMT+3) will receive the message at 11:00 AM Moscow time.

  If you would like to manually confirm the send, check the **Request confirmation before sending messages** option. This option is enabled by default.

  ![](assets/delivery_planning.png)

>[!CAUTION]
>
>When duplicating a delivery, all scheduling settings are deleted. Unless you schedule a new contact date, the duplicated delivery will be sent as soon as the send is confirmed.

**Related topics**:

* [Optimizing the sending time](../../sending/using/optimizing-the-sending-time.md)
* [Sending messages at the recipient's time zone](../../sending/using/sending-messages-at-the-recipient-s-time-zone.md)
* [Computing the sending date](../../sending/using/computing-the-sending-date.md)

