---
title: About send time optimization
seo-title: About send time optimization
description: About send time optimization
seo-description: Learn how to improve the success rate of your messages.
page-status-flag: never-activated
uuid: 6e0364cd-e9f6-4085-aa23-722053370d04
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/sending/using/about-send-time-optimization
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-01-10T15 31 16.999-0500
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: sheduling-messages
cq-template: /apps/help/templates/article-3
discoiquuid: 9156880d-eaba-4985-9a07-d9210953a46f
firstPublishExternalDate: 2018-01-10T15:31:16.993-0500
herogradient: light
jcr-created: 2018-01-11T19 01 30.325-0500
jcr-createdby: admin
jcr-description: About send time optimization
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-01-10T15:31:16.993-0500
lr-lastreplicatedby: sauviat@adobe.com
navTitle: About send time optimization
publishexternaldate: 2018-01-10T15 31 16.993-0500
publishExternalURL: https://helpx.adobe.com/campaign/standard/sending/using/about-send-time-optimization.html
sha1: 7768ad5d698a6c27323ad5a1ccea810f1ac22ec6
topicBrowsingSortDate: 2018-01-10T15:31:16.993-0500
index: y
internal: n
snippet: y
---

# About send time optimization

About send time optimization

To improve the success rate of your messages, you can manually define a sending time per recipient. Each profile will receive the message at the specified date and time, whenever possible.

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

  See [Sending at the recipient's time zone](../../sending/using/sending-at-the-recipient-s-time-zone.md).

* **Send at a custom date defined by a formula**: Each recipient will receive the message at the date and time configured by the specified formula.

  See [Computing the sending date](../../sending/using/computing-the-sending-date.md).

