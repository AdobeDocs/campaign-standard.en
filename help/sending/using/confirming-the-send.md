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

Once ready, follow the steps below to send your message.

1. Click the **[!UICONTROL Confirm send]** button found in the message's action bar.

    ![](assets/confirm_delivery.png)

1. Finalize the send by clicking the **[!UICONTROL OK]** button.

    ![](assets/confirm_delivery1.png)

The message is being sent. The **[!UICONTROL Deployment]** block shows the progress of the send.

>[!NOTE]
>
>If the message is scheduled, it will be sent when sending time is reached. For more on scheduling messages, refer to [this section](../../sending/using/about-scheduling-messages.md).

If you are using a recurring delivery with no aggregation period, you can request confirmation before the delivery is sent. To do this, when configuring your message, open the **[!UICONTROL Schedule]** block of the delivery dashboard and activate the dedicated option.

![](assets/confirmation_recurring_deliveries.png)

## About message indicators {#message-indicators}

Once the message is sent to the contacts, the **[!UICONTROL Deployment]** zone shows your KPIs (Key Performance Indicator) data , including:

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

### Delivered status report {#delivered-status-report}

<!--All messages will show as Sent as soon as they are successfully relayed from Campaign to the Enhanced MTA. They will stay in that state unless or until a bounce for that message is communicated back from the Enhanced MTA to Campaign. You should wait until the end of the validity period to see the final Success percentage, and the final number of Sent and Failed messages. Consequently:-->

For the email channel, in the **[!UICONTROL Summary]** view of each message, the **[!UICONTROL Delivered]** percentage will start out at 100% and then progressively go down throughout the validity period of the delivery as the soft and hard bounces get reported back<!--from the Enhanced MTA to Campaign-->.

Soft-bouncing messages do not show as **[!UICONTROL Failed]** after day one of the delivery. They will be retried and stay in the retry queue until the end of the delivery [validity period](../../administration/using/configuring-email-channel.md#validity-period-parameters). For more on retries after a delivery temporary failure, see [this section](../../sending/using/understanding-delivery-failures.md#retries-after-a-delivery-temporary-failure).

>[!NOTE]
>
>You should wait until the end of the validity period to see the final **[!UICONTROL Delivered]** percentage, and the final number of actually delivered and failed messages in the [sending logs](../../sending/using/monitoring-a-delivery.md#sending-logs).

### Email Feedback service (beta) {#email-feedback-service}

With the Email Feedback service capability, the status of each email is accurately reported, because feedback is captured directly from the Enhanced MTA (Message Transfer Agent).

>[!NOTE]
>
>The Email Feedback service capability is currently available as a beta.

Once the delivery has started, there is no change in the **[!UICONTROL Delivered]** percentage when the message is successfully relayed from Campaign to the Enhanced MTA. <!--The delivery logs show the **[!UICONTROL Taken into account by the service provider]** status for the targeted addresses.-->

<!--Soft-bouncing messages will show as Failed while they are retried on each additional day of the validity period for the delivery. They will stay in the Enhanced MTA retry queue throughout the delivery validity period.??-->

Soft-bouncing messages do no increment the error counter and they are not added to the quarantined address list. They are retried and will stay in the retry queue throughout the delivery [validity period](../../administration/using/configuring-email-channel.md#validity-period-parameters).

When the message is actually delivered to the targeted profiles, the delivery logs show the **[!UICONTROL Sent]** status for each address that successfully received the message. The **[!UICONTROL Delivered]** percentage is then updated.