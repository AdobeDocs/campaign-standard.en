---
title: About scheduling messages
seo-title: About scheduling messages
description: About scheduling messages
seo-description: Learn how to schedule your messages.
uuid: 51537cf4-c99c-4188-ab8f-5e3a07f5fa43
content-encoding: UTF-8
aemsrcnodepath: /content/help/en/campaign/standard/sending/using/about-scheduling-messages
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-30T04 53 50.164-0400
cq-lastreplicated: 2018-07-23T06 02 20.182-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: sheduling-messages
cq-template: /apps/help/templates/article-3
discoiquuid: 165fd73c-e9c7-4b3e-9175-3d550592fad1
firstPublishExternalDate: 2018-07-23T06:02:20.146-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 01 52.411-0400
jcr-createdby: admin
jcr-description: About scheduling messages
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T06:02:20.146-0400
lochandoffdate: 2018-07-30T04 53 50.164-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: About scheduling messages
publishexternaldate: 2018-07-23T06 02 20.146-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/sending/using/about-scheduling-messages.html
sha1: 7403ed2da5968c9cfb971ac519e7868036951e3a
topicBrowsingSortDate: 2018-07-23T06:02:20.146-0400
index: y
internal: n
snippet: y
---

# About scheduling messages

About scheduling messages

>[!CAUTION]
>
>Whenever making changes to a delivery’s schedule, be sure to re-prepare the delivery by clicking on the **Prepare** button before clicking **Confirm**.

In the message dashboard, the **Schedule** block allows you to define when messages will be sent.

![](assets/delivery_dashboard.png)

The **Schedule** properties let you set sending options:

* **Messages to be sent once confirmed**: messages are sent as soon as the send is confirmed. See [Confirming send](../../sending/using/confirming-send.md).

  ![](assets/delivery_planning_1.png)

* **Messages to be sent automatically on the date specified below**: messages will be sent at a later date and time. Specify the **contact date** in the **Start sending from** field.

  You can prepare and confirm the send, but messages will only be sent starting the selected date and time. Preparing and confirming the send are presented in the [Preparing the send](../../sending/using/preparing-the-send.md) and [Confirming send](../../sending/using/confirming-send.md) sections.

  The **Time zone of the contact date** drop-down list allows you to modify the time zone that will be taken into account for the sending time. For example, if you enter 9:00 AM in the **Start sending from** field and if you select Brussels, Copenhagen, Madrid, Paris (GMT+1) in the **Time zone of the contact date** drop-down list, all recipients will receive the message at 9:00 AM Paris time. Therefore, a recipient located in Moscow (GMT+3) will receive the message at 11:00 AM Moscow time.

  If you would like to manually confirm the send, check the **Request confirmation before sending messages** option. This option is enabled by default.

  ![](assets/delivery_planning.png)

>[!CAUTION]
>
>When duplicating a delivery, all scheduling settings are deleted. Unless you schedule a new contact date, the duplicated delivery will be sent as soon as the send is confirmed.

