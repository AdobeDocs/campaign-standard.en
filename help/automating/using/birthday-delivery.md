---
title: Birthday delivery
description: This example is a birthday workflow. Every day an email is sent to profiles whose birthday it is on that day.
page-status-flag: never-activated
uuid: 7de53431-84ae-4d21-8361-2775ad314ed2
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: channel-activities
discoiquuid: 5f288cf6-f8ff-4ac9-9c1a-8010260554bb
context-tags: delivery,workflow,main
internal: n
snippet: y
---

# Birthday delivery {#birthday-delivery}

![](assets/wkf_delivery_example_1.png)

This example is a birthday workflow. Every day an email is sent to profiles whose birthday it is on that day.

For more on how to use the **[!UICONTROL Email delivery]** activity, refer to [this section](../../automating/using/email-delivery.md).

To build the workflow, follow these steps:

* The **[!UICONTROL Scheduler]** allows you to start the workflow every day at 8am.

  ![](assets/wkf_delivery_example_2.png)

* The **[!UICONTROL Query]** activity allows you to calculate the profiles who have provided an email and whose birthday it is on the current day, every time the workflow is executed. The birthday calculation is carried out using a predefined filter available in the palette in the query editing tool.

  ![](assets/wkf_delivery_example_3.png)

* The **[!UICONTROL Email]** is recurring. The sends are aggregated by month. So, all emails sent in a month are aggregated into a single view. In one year, 365 deliveries are therefore executed but they are regrouped into 12 views (also called **recurring executions**) in the Adobe Campaign interface. History and report details are displayed every month and not for every send.

  ![](assets/wkf_delivery_example_4.png)
