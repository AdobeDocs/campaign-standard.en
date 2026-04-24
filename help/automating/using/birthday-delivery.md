---
title: Birthday delivery
description: This example is a birthday workflow. Every day an email is sent to profiles whose birthday it is on that day.
audience: automating
content-type: reference
topic-tags: channel-activities
context-tags: delivery,workflow,main
feature: Workflows
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: 535ddbce-d8ba-4578-9e37-10604291c95d
TQID: https://experienceleague.adobe.com/LXiYfz5VXaY7j0pOHWUCGJzp5F4bCsSCmFzEqsQG18E
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
---
# Birthday delivery {#birthday-delivery}

![](assets/wkf_delivery_example_1.png)

This example is a birthday workflow. Every day an email is sent to profiles whose birthday it is on that day.

To build the workflow, follow these steps:

* The [Scheduler](../../automating/using/scheduler.md) allows you to start the workflow every day at 8am.

  ![](assets/wkf_delivery_example_2.png)

* The [Query](../../automating/using/query.md) activity allows you to calculate the profiles who have provided an email and whose birthday it is on the current day, every time the workflow is executed. The birthday calculation is carried out using a predefined filter available in the palette in the query editing tool.

  ![](assets/wkf_delivery_example_3.png)

* The [Email delivery](../../automating/using/email-delivery.md) is recurring. The sends are aggregated by month. So, all emails sent in a month are aggregated into a single view. In one year, 365 deliveries are therefore executed but they are regrouped into 12 views (also called **recurring executions**) in the Adobe Campaign interface. History and report details are displayed every month and not for every send.

  ![](assets/wkf_delivery_example_4.png)
