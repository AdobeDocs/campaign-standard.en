---
title: Optimizing the sending time
description: Learn how to set up sending time and improve the open rate of your messages.
audience: sending
content-type: reference
topic-tags: sheduling-messages
feature: Send Time Optimization
role: User
level: Intermediate
exl-id: f35b46c6-de88-4efa-b3b7-8bb9024e40a8
TQID: https://experienceleague.adobe.com/FjL5t1ohvrgDdqLiCr03z1Nbq6IukIBysKkmXJ7561c
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
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
