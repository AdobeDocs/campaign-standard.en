---
title: Optimizing the sending time
seo-title: Optimizing the sending time
description: Optimizing the sending time
seo-description: Learn how to set up sending time and improve the open rate of your messages.
uuid: 799269f7-da92-4a35-b77a-44bb4a1641fc
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/sending/using/optimizing-the-sending-time
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-30T04 53 50.570-0400
cq-lastreplicated: 2018-07-23T06 02 21.137-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: sheduling-messages
cq-template: /apps/help/templates/article-3
discoiquuid: b9161e29-bf4f-4092-a982-631610e61f0f
firstPublishExternalDate: 2018-07-23T06:02:21.097-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 01 22.648-0400
jcr-createdby: admin
jcr-description: Optimizing the sending time
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T06:02:21.097-0400
lochandoffdate: 2018-07-30T04 53 50.570-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Optimizing the sending time
publishexternaldate: 2018-07-23T06 02 21.097-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/sending/using/optimizing-the-sending-time.html
sha1: e2a8ea56869bceac750957c77e060e9f000f362c
topicBrowsingSortDate: 2018-07-23T06:02:21.097-0400
index: y
internal: n
snippet: y
---

# Optimizing the sending time

Optimizing the sending time

To improve the open rate of your messages, you can manually define a sending time per recipient. Each profile will receive the message at the specified date and time, whenever possible.

Defining a sending time can be done at the delivery level or using a workflow.

For emails, depending on the server load and the amount of retries, best effort will be made to send the message on the date and time scheduled for each recipient.

* Retries depend on the Internet provider and your reputation. The message may not be accepted on the first attempt and several retries may be performed. See [List of email channel parameters](../../administration/using/configuring-email-channel.md#list-of-email-channel-parameters).
* Delays in receiving the email may occur due to insufficient bandwidth.

You can view when the message was sent to each recipient in the [sending logs](../../sending/using/monitoring-a-delivery.md#sending-logs).

Several options are available:

* **No optimization**: Messages are sent at the user's time.

  For example, if your time zone is GMT+1 and if you enter 9:00 AM in the **Start sending from** field, a recipient located in the GMT+3 time zone will receive the message at 11:00 AM local time for that recipient.

* **Send at the recipient's time zone**: All recipients will receive the message with their time zone taken into account.

  For example, if you enter 9:00 AM in the **Start sending from** field, a recipient located in the GMT+3 time zone will receive the message at 9:00 AM local time for that recipient.

  See [Sending messages at the recipient's time zone](../../sending/using/sending-messages-at-the-recipient-s-time-zone.md).

* **Send at a custom date defined by a formula**: Each recipient will receive the message at the date and time configured by the specified formula.

  See [Computing the sending date](../../sending/using/computing-the-sending-date.md).

