---
solution: Campaign Standard
product: campaign
title: Optimizing the sending time
description: Learn how to set up sending time and improve the open rate of your messages.
audience: sending
content-type: reference
topic-tags: sheduling-messages

feature: Send Time Optimization
role: Business Practitioner
level: Intermediate
---

# Optimizing the sending time{#optimizing-the-sending-time}

To improve the open rate of your messages, you can manually define a sending time per recipient. Each profile will receive the message at the specified date and time, whenever possible.

Defining a sending time can be done at the delivery level or using a workflow.

For emails, depending on the server load and the amount of retries, best effort will be made to send the message on the date and time scheduled for each recipient.

* Retries depend on the Internet provider and your reputation. The message may not be accepted on the first attempt and several retries may be performed. See [List of email channel parameters](../../administration/using/configuring-email-channel.md).
* Delays in receiving the email may occur due to insufficient bandwidth.

You can view when the message was sent to each recipient in the [sending logs](../../sending/using/monitoring-a-delivery.md#sending-logs).

Several options are available:

* **[!UICONTROL No optimization]**: Messages are sent at the user's time.

  For example, if your time zone is GMT+1 and if you enter 9:00 AM in the **[!UICONTROL Start sending from]** field, a recipient located in the GMT+3 time zone will receive the message at 11:00 AM local time for that recipient.

* **[!UICONTROL Send at the recipient's time zone]**: All recipients will receive the message with their time zone taken into account.

  For example, if you enter 9:00 AM in the **[!UICONTROL Start sending from]** field, a recipient located in the GMT+3 time zone will receive the message at 9:00 AM local time for that recipient.

  See [Sending messages at the recipient's time zone](../../sending/using/sending-messages-at-the-recipient-s-time-zone.md).

* **[!UICONTROL Send at a custom date defined by a formula]**: Each recipient will receive the message at the date and time configured by the specified formula.

  See [Computing the sending date](../../sending/using/computing-the-sending-date.md).

