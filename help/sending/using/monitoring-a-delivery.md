---
title: Monitoring a delivery in Adobe Campaign Standard
description: Discover how to monitor a delivery in Adobe Campaign Standard.
audience: sending
content-type: reference
topic-tags: monitoring-messages
context-tags: delivery,main
feature: Performance Monitoring
role: User
level: Beginner
exl-id: ddc92077-df73-411d-a161-3263581e6945
---
# Monitoring a delivery{#monitoring-a-delivery}

There are several ways to monitor a delivery and to measure its impact. As a functional administrator, you can access message logs and delivery logs.

>[!IMPORTANT]
>
>Only Functional [administrators](../../administration/using/users-management.md#functional-administrators), with **[!UICONTROL Administration]** role and access to **All** units can access sending logs, message logs, tracking logs, exclusion or subscription logs. A non-admin user can target these logs but starting on a linked table (profiles, delivery).

* **Message logs**: These logs can be accessed directly from the message dashboard. They show the detail of the sending, which target has been excluded and why, as well as the tracking information such as opens and clicks.

  To view the message logs, click the icon at the bottom right of the **[!UICONTROL Deployment]** block.

  Several tabs contain information (if it exists) regarding the **[!UICONTROL Sending logs]**, **[!UICONTROL Exclusion logs]**, **[!UICONTROL Exclusion causes]**, **[!UICONTROL Tracking logs]** and **[!UICONTROL Tracked URLs]**. See [Delivery logs](#delivery-logs).

  ![](assets/sending_delivery1.png)

  The log contains all messages relating to the delivery and the proofs. Specific icons allow you to identify errors or warnings. For more on this, see [Approving messages](../../sending/using/previewing-messages.md).

  You can export the log by clicking the **[!UICONTROL Export list]** button.

  ![](assets/sending_delivery2.png)

* **Job logs**: A list of the batch jobs triggered by the delivery can be accessed from the message dashboard by selecting **[!UICONTROL Job history]** from the **[!UICONTROL Summary]** drop-down list. 

  Select any job from the list to see the details of the selected **[!UICONTROL Batch job]**. 

  ![](assets/sending_delivery8.png)

* **Delivery alerts**: To keep track of delivery successes or failures, Adobe Campaign provides an email alerting system that sends notifications to inform users of important system activities.
* **Reports**: From the message dashboard, you can access several reports for this specific message. You also have a **[!UICONTROL Reports]** menu that allows you to access a complete list of built-in or custom reports that you can use to outline specific metrics related to your message or campaign.
* An administrator can also export logs in a separate file that can be processed in your own reporting or BI tools. For more on this, see [Exporting logs](../../automating/using/exporting-logs.md).

**Related topics:**

* [Receiving alerts when failures happen](../../sending/using/receiving-alerts-when-failures-happen.md)
* [Reports](../../reporting/using/about-dynamic-reports.md)

## Delivery logs {#delivery-logs}

### Sending logs {#sending-logs}

The **[!UICONTROL Sending logs]** tab offers a history of every occurrence of this delivery. The list of sent messages and their statuses is stored here. It allows you to view the delivery status for each recipient.

For each profile with a **[!UICONTROL Sent]** status, the **[!UICONTROL Date]** column shows when the message was sent.

![](assets/sending_delivery3.png)

To access the details of a specific sending log, click the pencil icon on the right of the corresponding row.

![](assets/sending_access-sending-log.png)

All the sending log details are read-only. You can also see a preview of the mirror page.

![](assets/sending_sending-log.png)

>[!NOTE]
>
>To display the mirror page rendering in the Campaign user interface, the mirror page server URL must be secure. In that case, use https:// rather than http:// to set up this URL when [configuring your brand](../../administration/using/branding.md#configuring-and-using-brands).

### Exclusion logs {#exclusion-logs}

The **[!UICONTROL Exclusion logs]** tab lists all the messages that have been excluded from the target sent and specifies the reason for the send failure.

![](assets/sending_delivery4.png)

### Exclusion causes {#exclusion-causes}

The **[!UICONTROL Exclusion causes]** tab displays the volume (in number of messages) of messages that were excluded from the target send.

![](assets/sending_delivery5.png)
