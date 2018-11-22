---
title: Optimizing the sending time
seo-title: Optimizing the sending time
description: Optimizing the sending time
seo-description: Learn how to set up sending time and improve the open rate of your messages.
page-status-flag: never-activated
uuid: bcf77133-9d3d-40a7-987c-7a22ae9b1406
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/sending/using/optimizing-the-sending-time
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: sheduling-messages
discoiquuid: cf549d54-4ea1-4bb1-afa2-84f5c51b414f
isreadyforlocalization: false
navTitle: Optimizing the sending time
publishexternaldate: 2018-11-20
sha1: b7b7f4ff59252cbffa554261aeb46a97a3b83144
index: y
internal: n
snippet: y
---

# Optimizing the sending time{#optimizing-the-sending-time}

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

