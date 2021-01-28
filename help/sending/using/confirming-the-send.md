---
solution: Campaign Standard
product: campaign
title: Confirming the send
description: Learn how to finalize the message preparation.
audience: sending
content-type: reference
topic-tags: sending-and-tracking-messages
context-tags: delivery,deployment,back
---

# Confirming the send{#confirming-the-send}

Once you have finished preparing your messages and the approval steps have been carried out, you can send them. For more on messages preparation, refer to [Preparing the send](../../sending/using/preparing-the-send.md).

Only users with the **[!UICONTROL Start deliveries]** role can confirm send. For more on this, refer to the [List of roles](../../administration/using/list-of-roles.md) section.

<!--Users without this role will see the following message: 

![](assets/confirm_delivery_2.png)-->

## Sending the message {#sending-message}

Once preparation is complete, follow the steps below to send your message.

1. Click the **[!UICONTROL Confirm send]** button found in the message's action bar.

    ![](assets/confirm_delivery.png)

1. Finalize the send by clicking the **[!UICONTROL OK]** button.

    ![](assets/confirm_delivery1.png)

1. Wait while the message is being sent. The **[!UICONTROL Deployment]** block shows the progress of the send.

>[!NOTE]
>
>If the message is scheduled, it will be sent when sending time is reached. For more on scheduling messages, refer to [this section](../../sending/using/about-scheduling-messages.md).

If you are using a recurring delivery with no aggregation period, you can request confirmation before the delivery is sent. To do this, when configuring your message, open the **[!UICONTROL Schedule]** block of the delivery dashboard and activate the dedicated option.

![](assets/confirmation_recurring_deliveries.png)

## Understanding message indicators {#message-indicators}

Once the message is sent to the contacts, the **[!UICONTROL Deployment]** zone shows your KPIs (Key Performance Indicator) data, including:

* The number of messages to deliver
* The number of messages sent
* The percentage of messages delivered
* The percentage of bounces and errors
* The percentage of open messages
* The percentage of clicks in the messages (for emails)

  >[!NOTE]
  >
  >The **[!UICONTROL Open rate]** and **[!UICONTROL Click-through rate]** are updated every hour.

![](assets/sending_delivery.png)

If the KPIs take too long to update or do not take into account the results from the sending logs, click the **[!UICONTROL Compute stats]** button in the **[!UICONTROL Deployment]** window.

![](assets/sending_delivery7.png)

The message can be viewed in the history of one of the targeted profiles. See [Integrated customer profile](../../audiences/using/integrated-customer-profile.md).

Once a message is sent, you can track the behavior of its recipients, and monitor it to measure its impact. For more on this, refer to these sections:

* [Tracking messages](../../sending/using/tracking-messages.md)
* [Monitoring a delivery](../../sending/using/monitoring-a-delivery.md)

### Delivered indicator reporting {#delivered-status-report}

>[!NOTE]
>
>This section applies to email channel only.

<!--All messages will show as Sent as soon as they are successfully relayed from Campaign to the Enhanced MTA. They will stay in that state unless or until a bounce for that message is communicated back from the Enhanced MTA to Campaign.-->

For the email channel, in the **[!UICONTROL Summary]** view of each message, the **[!UICONTROL Delivered]** percentage starts out at 100% and then progressively goes down throughout the validity period of the delivery, as the soft and hard bounces get reported back<!--from the Enhanced MTA to Campaign-->.

Indeed, all messages show as **[!UICONTROL Sent]** in the [sending logs](../../sending/using/monitoring-a-delivery.md#sending-logs) as soon as they are successfully relayed from Campaign to the Enhanced MTA (Message Transfer Agent). They remain in that status unless or until a bounce for that message is communicated back from the Enhanced MTA to Campaign.

When hard-bouncing messages get reported back from the Enhanced MTA, their status changes from **[!UICONTROL Sent]** to **[!UICONTROL Failed]** and the **[!UICONTROL Delivered]** percentage is decreased accordingly.

When soft-bouncing messages get reported back from the Enhanced MTA, they still show as **[!UICONTROL Sent]** and the **[!UICONTROL Delivered]** percentage is not yet updated. Soft-bouncing messages are [retried](../../sending/using/understanding-delivery-failures.md#retries-after-a-delivery-temporary-failure) throughout the delivery [validity period](../../administration/using/configuring-email-channel.md#validity-period-parameters):

* If a retry is successful before the end of the validity period, the message status remains as **[!UICONTROL Sent]** and the **[!UICONTROL Delivered]** percentage remains unchanged.

* Otherwise, the status changes to **[!UICONTROL Failed]** and the **[!UICONTROL Delivered]** percentage is decreased accordingly.

<!--Soft-bouncing messages increment an error counter. When the error counter reaches the limit threshold or when the validity period is over, their status changes to **[!UICONTROL Failed]**.-->

<!--For more on retries after a delivery temporary failure, see [this section](../../sending/using/understanding-delivery-failures.md#retries-after-a-delivery-temporary-failure).-->

Consequently, you should wait until the end of the validity period to see the final **[!UICONTROL Delivered]** percentage, and the final number of actually **[!UICONTROL Sent]** and **[!UICONTROL Failed]** messages.

### Email Feedback Service (beta) {#email-feedback-service}

>[!NOTE]
>
>This section applies to email channel only.

With the Email Feedback Service (EFS) capability, the status of each email is accurately reported, because feedback is captured directly from the Enhanced MTA (Message Transfer Agent).

>[!IMPORTANT]
>
>The Email Feedback Service is currently available as a beta capability.

Once the delivery has started, there is no change in the **[!UICONTROL Delivered]** percentage when the message is successfully relayed from Campaign to the Enhanced MTA.

![](assets/efs-sending.png)

The delivery logs show the **[!UICONTROL Pending]** status for each targeted address.

![](assets/efs-pending.png)

When the message is actually delivered to the targeted profiles and once this information is reported back in real time from the Enhanced MTA, the delivery logs show the **[!UICONTROL Sent]** status for each address that successfully received the message. The **[!UICONTROL Delivered]** percentage is increased accordingly with each successful delivery.

When hard-bouncing messages get reported back from the Enhanced MTA, their log status changes from **[!UICONTROL Pending]** to **[!UICONTROL Failed]** and the **[!UICONTROL Bounces + errors]** percentage is increased accordingly.

When soft-bouncing messages get reported back from the Enhanced MTA, their log status also changes from **[!UICONTROL Pending]** to **[!UICONTROL Failed]** and the **[!UICONTROL Bounces + errors]** percentage is increased accordingly. The **[!UICONTROL Delivered]** percentage remains unchanged. Soft-bouncing messages are then retried throughout the delivery [validity period](../../administration/using/configuring-email-channel.md#validity-period-parameters):

* If a retry is successful before the end of the validity period, the message status changes to **[!UICONTROL Sent]** and the **[!UICONTROL Delivered]** percentage is increased accordingly.

* Otherwise, the status remains as **[!UICONTROL Failed]**. The **[!UICONTROL Delivered]** and **[!UICONTROL Bounces + errors]** percentages remain unchanged.
  
For more on retries after a delivery temporary failure, see [this section](../../sending/using/understanding-delivery-failures.md#retries-after-a-delivery-temporary-failure).

<!--Soft-bouncing messages increment an error counter. When the error counter reaches the limit threshold or when the validity period is over, the address goes into quarantine and the status remains as **[!UICONTROL Failed]**. For more on conditions for sending an address to quarantine, see [this section](../../help/sending/using/understanding-quarantine-management.md#conditions-for-sending-an-address-to-quarantine).-->

| Step | KPI summary<br>without EFS | Sending logs status<br>without EFS | KPI summary<br>with EFS | Sending logs status<br>with EFS |
|--- |--- |--- | --- | --- |
| Message is successfully relayed from Campaign to the Enhanced MTA | <ul><li>**[!UICONTROL Delivered]** percentage starts out at 100%</li><li>**[!UICONTROL Bounces + errors]** percentage starts out at 0%</li></ul>| Sent | <ul><li>No change in **[!UICONTROL Delivered]** percentage</li><li>No change in **[!UICONTROL Bounces + errors]** percentage</li></ul> | Pending |
| Hard-bouncing messages get reported back from the Enhanced MTA | <ul><li>**[!UICONTROL Delivered]** percentage is decreased accordingly</li><li>**[!UICONTROL Bounces + errors]** percentage is increased accordingly</li></ul> | Failed | <ul><li>No change in **[!UICONTROL Delivered]** percentage</li><li>**[!UICONTROL Bounces + errors]** percentage is increased accordingly</li></ul> | Failed |
| Soft-bouncing messages get reported back from the Enhanced MTA | <ul><li>No change in **[!UICONTROL Delivered]** percentage</li><li>No change in **[!UICONTROL Bounces + errors]** percentage</li></ul> | Sent | <ul><li>**[!UICONTROL Delivered]** percentage remains unchanged</li><li>**[!UICONTROL Bounces + errors]** percentage is increased accordingly</li></ul> | Failed |
| Soft-bouncing messages retries successful | <ul><li>No change in **[!UICONTROL Delivered]** percentage</li><li>No change in **[!UICONTROL Bounces + errors]** percentage</li></ul> | Sent | <ul><li>**[!UICONTROL Delivered]** percentage is increased accordingly</li><li>**[!UICONTROL Bounces + errors]** percentage is decreased accordingly</li></ul> | Sent |
| Soft-bouncing messages retries failed | <ul><li>**[!UICONTROL Delivered]** percentage is decreased accordingly</li><li>No change in **[!UICONTROL Bounces + errors]** percentage </li></ul> | Failed | <ul><li> No change in **[!UICONTROL Delivered]** percentage </li><li> No change in **[!UICONTROL Bounces + errors]** percentage </li></ul> | Failed |
