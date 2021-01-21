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

Users without this role will see the following message: 

![](assets/confirm_delivery_2.png)

To send your delivery, click the **[!UICONTROL Confirm send]** button found in the message's action bar.

![](assets/confirm_delivery.png)

You will be asked to finalize the send definitively by clicking the **[!UICONTROL OK]** button.

![](assets/confirm_delivery1.png)

The message is being sent.

>[!NOTE]
>
>If the message is scheduled, it will be sent when sending time is reached. For more on scheduling messages, refer to [this section](../../sending/using/about-scheduling-messages.md).

If you are using a recurring delivery with no aggregation period, you can request confirmation before the delivery is sent. To do this, open the **[!UICONTROL Schedule]** block of the delivery dashboard, then activate the dedicated option.

![](assets/confirmation_recurring_deliveries.png)

The **[!UICONTROL Deployment]** block shows the progress of the send.

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

If the KPIs take too long to update or don't take into account the results from the sending logs, click the **[!UICONTROL Compute stats]** button in the **[!UICONTROL Deployment]** window.

![](assets/sending_delivery7.png)

The message can be viewed in the history of one of the client profiles that makes up part of the audience. See [Integrated customer profile](../../audiences/using/integrated-customer-profile.md).

Once a message is sent, you can track the behavior of its recipients, and monitor it in order to measure its impact. For more on this, refer to these sections:

* [Tracking messages](../../sending/using/tracking-messages.md)
* [Monitoring a delivery](../../sending/using/monitoring-a-delivery.md)

## Sent status report

For customers who upgraded to the Enhanced MTA:

All messages will show as Sent as soon as they are successfully relayed from Campaign to the Enhanced MTA. They will stay in that state unless or until a bounce for that message is communicated back from the Enhanced MTA to Campaign. You should wait until the end of the validity period to see the final Success percentage, and the final number of Sent and Failed messages. Consequently:
* In the Summary view of each message, the Success percentage will start out at 100% and then go down throughout the validity period of the delivery as the soft and hard bounces get reported back from the Enhanced MTA to Campaign.
* Soft-bouncing messages will no longer show as Failed after day one of the delivery, and be retried on each additional day of the validity period for the delivery. They will stay in the Enhanced MTA retry queue throughout the delivery validity period.

>[!NOTE]
>
>You should wait until the end of the validity period to see the final Success percentage, and the final number of Sent and Failed messages.
>
>The fact that the Success percentage will go to 100% very quickly indicates that your instance has been upgraded to the Enhanced MTA.

## Email Feedback Service

With the new Email Feedback Service (currently available as beta), the status of each message is accurately reported.

The messages first show as Pending when they are successfully relayed from Campaign to the Enhanced MTA. The delivery logs show the Taken into account by the service provider status for these messages.

Soft-bouncing messages will show as Failed while they are retried on each additional day of the validity period for the delivery. They will stay in the Enhanced MTA retry queue throughout the delivery validity period.