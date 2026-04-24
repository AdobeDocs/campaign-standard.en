---
title: About scheduling messages
description: Learn how to schedule your messages.
audience: sending
content-type: reference
topic-tags: sheduling-messages
context-tags: delivery,schedule,back
feature: Send Time Optimization
role: User
exl-id: 6b26615b-4aa6-401d-a12d-25cef4cd0524
TQID: https://experienceleague.adobe.com/N0t5qvKiceoZEekhToXAk1PfNe1HE22vAaobLr32oME
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
---
# About scheduling messages{#about-scheduling-messages}

>[!IMPORTANT]
>
>Whenever making changes to a delivery’s schedule, you must re-prepare the delivery by clicking on the **Prepare** button before clicking **Confirm**.

In the message dashboard, the **[!UICONTROL Schedule]** block allows you to define when messages (email, SMS or Push notifications) will be sent.

![](assets/delivery_dashboard.png)

The **[!UICONTROL Schedule]** properties let you set sending options for your emails, SMS or push notifications:

* **[!UICONTROL Messages to be sent once confirmed]**: messages are sent as soon as the send is confirmed. See [Confirming the send](../../sending/using/confirming-the-send.md).

  ![](assets/delivery_planning_1.png)

* **[!UICONTROL Messages to be sent automatically on the date specified below]**: messages will be sent at a later date and time. Specify the **contact date** in the **Start sending from** field.

  You can prepare and confirm the send, but messages will only be sent starting the selected date and time. Preparing and confirming the send are presented in the [Preparing the send](../../sending/using/preparing-the-send.md) and [Confirming the send](../../sending/using/confirming-the-send.md) sections.

  The **[!UICONTROL Time zone of the contact date]** drop-down list allows you to modify the time zone that will be taken into account for the sending time. For example, if you enter 9:00 AM in the **[!UICONTROL Start sending from]** field and if you select Brussels, Copenhagen, Madrid, Paris (GMT+1) in the **[!UICONTROL Time zone of the contact date]** drop-down list, all recipients will receive the message at 9:00 AM Paris time. Therefore, a recipient located in Moscow (GMT+3) will receive the message at 11:00 AM Moscow time.

  If you would like to manually confirm the send, check the **[!UICONTROL Request confirmation before sending messages]** option. This option is enabled by default.

  ![](assets/delivery_planning.png)

>[!IMPORTANT]
>
>When duplicating a delivery, all scheduling settings are deleted. Unless you schedule a new contact date, the duplicated delivery will be sent as soon as the send is confirmed.

**Related topics**:

* [Optimizing the sending time](../../sending/using/optimizing-the-sending-time.md)
* [Sending messages at the recipient's time zone](../../sending/using/sending-messages-at-the-recipient-s-time-zone.md)
* [Computing the sending date](../../sending/using/computing-the-sending-date.md)
