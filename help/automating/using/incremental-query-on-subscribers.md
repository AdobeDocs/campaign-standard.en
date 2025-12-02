---
title: Incremental query on subscribers to a service
description: The following example presents how to configure an Incremental query activity to filter subscribers to a service.
audience: automating
content-type: reference
topic-tags: targeting-activities
context-tags: incremental,main
feature: Workflows
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: c80ed1f6-ad8a-4448-a6df-b9881327228a
---
# Incremental query on subscribers to a service {#example--incremental-query-on-subscribers-to-a-service}

The following example shows the configuration of an **[!UICONTROL Incremental query]** activity which filters the profiles in the Adobe Campaign database that are subscribed to the **Running Newsletter** service, to send them a welcome email containing a promo code.

The workflow is up made up of the following elements:

![](assets/incremental_query_example1.png)

* A [Scheduler](../../automating/using/scheduler.md) activity, to execute the workflow every Monday at 6 am.

  ![](assets/incremental_query_example2.png)

* An [Incremental query](../../automating/using/incremental-query.md) activity, which targets all of the current subscribers during the first execution, then only the new subscribers of that week during the following executions.

  ![](assets/incremental_query_example3.png)

* An [Email delivery](../../automating/using/email-delivery.md) activity. The workflow is executed once a week, but you can aggregate the emails sent and the results per month, for example to generate reports over a period of an entire month and not just a single week.

  To do this, choose to create a **[!UICONTROL Recurring email]** here regrouping the emails and the results **[!UICONTROL By month]**.

  Define the content of your email and insert the welcome promo code. For more on this, refer to [Defining email content](../../designing/using/personalization.md) sections.

Then start the workflow execution. Each week the new subscribers will receive the welcome email with the promo code.
