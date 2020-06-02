---
title: Incremental query on subscribers to a service
description: The following example presents how to configure an Incremental query activity to filter subscribers to a service.
page-status-flag: never-activated
uuid: 73b42422-e815-43ef-84c0-97c4433ccc98
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: targeting-activities
discoiquuid: 80961e73-42ec-463a-8496-cff69fab0475
context-tags: incremental,main
internal: n
snippet: y
---

# Incremental query on subscribers to a service {#example--incremental-query-on-subscribers-to-a-service}

The following example shows the configuration of an **[!UICONTROL Incremental query]** activity which filters the profiles in the Adobe Campaign database that are subscribed to the **Running Newsletter** service, to send them a welcome email containing a promo code.

For more on how to use the **[!UICONTROL Incremental query]** activity, refer to [this section](../../automating/using/incremental-query.md).

The workflow is up made up of the following elements:

![](assets/incremental_query_example1.png)

* A **[!UICONTROL Scheduler]** activity, to execute the workflow every Monday at 6 am.

  ![](assets/incremental_query_example2.png)

* An **[!UICONTROL Incremental query]** activity, which targets all of the current subscribers during the first execution, then only the new subscribers of that week during the following executions.

  ![](assets/incremental_query_example3.png)

* An **[!UICONTROL Email delivery]** activity. The workflow is executed once a week, but you can aggregate the emails sent and the results per month, for example to generate reports over a period of an entire month and not just a single week.

  To do this, choose to create a **[!UICONTROL Recurring email]** here regrouping the emails and the results **[!UICONTROL By month]**.

  Define the content of your email and insert the welcome promo code.

  For more on this, refer to the [Email delivery](../../automating/using/email-delivery.md) and [Defining email content](../../designing/using/personalization.md) sections.

Then start the workflow execution. Each week the new subscribers will receive the welcome email with the promo code.
