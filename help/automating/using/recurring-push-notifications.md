---
title: Sending a recurring push notification with a workflow
description: In this example, a personalized push notification is sent every first day of the month at 8 pm to the subscribers of your mobile application depending on their time zones.
page-status-flag: never-activated
uuid: 994d8fe3-29f0-4b5c-89ee-c6be7c60a31b
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: channel-activities
discoiquuid: e61bdaee-4b48-4845-a2a5-574b577ea796

internal: n
snippet: y
---

# Sending a recurring push notification with a workflow {#sending-a-recurring-push-notification-with-a-workflow}

![](assets/wkf_push_example_1.png)

In this example, a personalized push notification is sent every first day of the month at 8 pm to the subscribers of your mobile application depending on their time zones.

To build the workflow, follow these steps:

1. The [Scheduler](../../automating/using/scheduler.md) activity allows you to start the workflow days before the start of the delivery to be able to send the notification to every subscriber at 8 pm in any given time zone:

    * In the **[!UICONTROL Execution frequency]** field, select Monthly.
    * Select 8 pm in the **[!UICONTROL Time]** field.
    * Choose at which day the delivery will be sent every month.
    * Select a start date for your workflow, at least one day prior to the start of your delivery. Otherwise, some recipients might receive the message a day later if the selected time has already passed in their time zones.
    * In the **[!UICONTROL Execution options]** tab, select at which time zone your workflow will start in the **[!UICONTROL Time zone]** field. Here, for example, the workflow will start at 8 pm Pacific time, one week before the first day of the month to allow some time for the deliveries to be created for all applicable time zones.

    >[!NOTE]
    >
    >By default, the selected time zone is the one defined in the workflow properties (see [Building a workflow](../../automating/using/building-a-workflow.md)).

   ![](assets/wkf_push_example_5.png)

1. The [Query](../../automating/using/query.md) activity allows you to target your VIP customers aged between 20-30, who have subscribed to your mobile application and who did not open the email you sent:

    * Select an audience (your VIP customers) and filter on their age.
    * Drag and drop the **Subscriptions to an application** element into the workspace. Select **Exists** and select the mobile application that you want to use.
    * Select the email that you sent to your customers.
    * Drag and drop the **Delivery logs (logs)** element into the workspace and select **Exists** to target all of the customers who received the email.
    * Drag and drop the **Tracking logs (tracking)** element into the workspace and select **Does not exist** to target all of the customers who did not open the email.

      ![](assets/wkf_push_example_2.png)

1. The [Push notification delivery](../../automating/using/push-notification-delivery.md) activity allows you to enter the content of your message and to select the personalization fields that you want to use:

    * Select the **[!UICONTROL Recurring notification]** option.
    * Define the push notification content. For more information on push notification content, refer to this [section](../../channels/using/preparing-and-sending-a-push-notification.md).
    * In the **[!UICONTROL Schedule]** block, select **[!UICONTROL Messages to be sent automatically on the time zone specified below]**. Here, we chose the **[!UICONTROL Time zone of the contact date]** Pacific as in the workflow **[!UICONTROL Scheduler]**.
    * In the **[!UICONTROL Optimize the sending time per recipient]** field, select **[!UICONTROL Send at the recipient's time zone]**.

      ![](assets/wkf_push_example_4.png)

1. Click the **[!UICONTROL Start]** button to start your recurring workflow.

   ![](assets/wkf_push_example_3.png)

Your workflow is now running. It will start at the chosen start date of the **[!UICONTROL Scheduler]** at 8 pm Pacific time, the recurring push will then be sent every first day of the month at 8 pm depending on the customers time zone.
