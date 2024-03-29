---
title: Personalizing an email with additional data
description: This use case presents how to add different types of additional data to a query and use it as a personalization field in an email.
audience: automating
content-type: reference
topic-tags: targeting-activities
context-tags: query,main
feature: Workflows
role: Data Architect
level: Intermediate
exl-id: b207dc73-03dc-4f25-95e5-573e4b4bce54
---
# Personalizing an email with additional data {#example--personalizing-an-email-with-additional-data}

The following example illustrates adding different types of additional data to a query and its use as a personalization field in an email. For more on how to enrich the data targeted by a **[!UICONTROL Query]** activity, refer to [this section](../../automating/using/query.md#enriching-data).

For this example, [custom resources](../../developing/using/data-model-concepts.md) are used:

* The **profile** resource was extended in order to add a field which allows each profile's loyalty points to be saved.
* A **transactions** resource was created and identifies all purchases carried out by the profiles in the database. The date, price, and product purchased is saved for each transaction.
* A **products** resource was created and references the products available for purchase.

The objective is to send an email to the profiles for which at least one transaction has been saved. Via this email, the clients will receive a reminder of the last transaction carried out as well as an overview of all of their transactions: the number of products purchased, total spent, a reminder of the total number of loyalty points that they have accrued.

The workflow is presented as follows:

![](assets/enrichment_example1.png)

1. Add a [Query](../../automating/using/query.md) activity, which allows you to target the profiles that have carried out at least one transaction.

   ![](assets/enrichment_example2.png)

1. From the query's **[!UICONTROL Additional data]** tab, define the different data to be displayed in the final email:

    * The simple field of the **profile** dimension corresponding to the loyalty points. Refer to the [Adding a simple field](../../automating/using/query.md#adding-a-simple-field) section.
    * Two aggregates based on the transactions collection: the number of products purchased and the total amount spent. You can add them from the **[!UICONTROL Data]** tab of the aggregate configuration window, using the **Count** and **Sum** aggregates. Refer to the [Adding an aggregate](../../automating/using/query.md#adding-an-aggregate) section.
    * A collection returning the amount spent, the date, and the product of the last transaction effected.

      To do this, you have to add the different fields that you want to display from the **[!UICONTROL Data]** tab of the collection configuration window.

      To return only the most recent transaction, you have to enter "1" for the **[!UICONTROL Number of lines to return]** and apply a descending sort on the **Date** field of the collection from the **[!UICONTROL Sort]** tab.

      Refer to the [Adding a collection](../../automating/using/query.md#adding-a-collection) and [Sorting additional data](../../automating/using/query.md#sorting-additional-data) sections.

   ![](assets/enrichment_example4.png)

1. If you would like to check that the data is correctly transferred by the activity's outbound transition, start the workflow for the first time (without the **[!UICONTROL Email delivery]** activity) and open the query's outbound transition.

   ![](assets/enrichment_example5.png)

1. Add an [Email delivery](../../automating/using/email-delivery.md) activity. In the email content, insert the personalization fields corresponding to the data calculated in the query. You can find it via the **[!UICONTROL Additional data (targetData)]** link of the personalization fields explorer.

   ![](assets/enrichment_example3.png)

Your workflow is now ready to be executed. The profiles targeted in the query will receive a personalized email containing the data calculated from their transactions.
