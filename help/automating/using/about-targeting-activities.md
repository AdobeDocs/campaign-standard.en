---
title: About targeting activities
description: Targeting activities can be accessed from the left-hand side of the screen.
page-status-flag: never-activated
uuid: a6cbc431-1ae3-428e-b2c9-893454b32ae2
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: targeting-activities
discoiquuid: 5f7607a1-5f71-4d66-9688-3e5a1774f1b4

internal: n
snippet: y
---

# About targeting activities{#about-targeting-activities}

From the palette, on the left-hand side of the screen, unfold the **[!UICONTROL Targeting]** section.

These activities are specific to targeting, manipulating population data, and filtering activities. They let you build one or more targets by defining sets and splitting or combining these sets using intersection, union, or exclusion operations.

![](assets/wkf_targeting_activities.png)

The **[!UICONTROL Targeting]** section provides the following activities:

* [Query](../../automating/using/query.md)
* [Incremental query](../../automating/using/incremental-query.md)
* [Union](../../automating/using/union.md)
* [Intersection](../../automating/using/intersection.md)
* [Exclusion](../../automating/using/exclusion.md)
* [Segmentation](../../automating/using/segmentation.md)
* [Read audience](../../automating/using/read-audience.md)
* [Save audience](../../automating/using/save-audience.md)
* [Deduplication](../../automating/using/deduplication.md)
* [Enrichment](../../automating/using/enrichment.md)

**[!UICONTROL Targeting]** activities allows you to define **segment codes** for their outbound transitions. You can then create reports based on these segment codes in order to measure the efficiency of your maketing campaigns. For more on this, refer to [this section](../../reporting/using/creating-a-report-workflow-segment.md).

## Selecting data {#selecting-data}

You can select data using the following activities:

* The **[!UICONTROL Query]** activity allows you to filter and extract a population of elements from the Adobe Campaign database. See the [Query](../../automating/using/query.md) section.
* The **[!UICONTROL Incremental query]** activity allows you to filter and extract a population of elements from the Adobe Campaign database. Each time this activity is executed, the results from the previous executions are excluded. This allows you to target only new elements See the. [Incremental query](../../automating/using/incremental-query.md) section.
* The **[!UICONTROL Read audience]** activity allows you to retrieve an existing audience and to refine it by applying additional filtering conditions.See the [Read audience](../../automating/using/read-audience.md) section.

## Segmenting data {#segmenting-data}

Adobe Campaign lets you process sets on inbound data. You can thus combine several populations, exclude part of it or only keep data common to several targets.

* The **[!UICONTROL Union]** activity allows you to regroup the result of multiple activities into a single target. See the [Union](../../automating/using/union.md) section.
* The **[!UICONTROL Intersection]** activity allows you to keep only the elements common to the different inbound populations in the activity. See the [Intersection](../../automating/using/intersection.md) section.
* The **[!UICONTROL Exclusion]** activity allows you to exclude elements from one population according to certain criteria. See the [Exclusion](../../automating/using/exclusion.md) section.
* The **[!UICONTROL Segmentation]** activity lets you create one or several segments from a population calculated by activities placed earlier in the workflow. At the end of the activity, they can be processed in one single transition or different transitions. See the [Segmentation](../../automating/using/segmentation.md) section.

## Enriching data {#enriching-data}

The identified and collected data can be enriched, aggregated and manipulated to optimize target construction. You can simplify and optimize targeting processes, by including data that is not modeled in the data mart.

The **[!UICONTROL Additional data]** tab of the **[!UICONTROL Query]** and **[!UICONTROL Incremental query]** activities allows you to enrich the data targeted by the query and transfer this data to the following workflow activities, where it can be utilized. In particular, you can add:

* Simple data
* Aggregates
* Collections

**Related topics**

* [Use case: Create a once-a-week email delivery](../../automating/using/workflow-weekly-offer.md)
* [Use case: Creating a delivery segmented on location](../../automating/using/workflow-segmentation-location.md)
* [Use case: Creating deliveries with a complement](../../automating/using/workflow-created-query-with-complement.md)
* [Use case: Retargeting workflow sending a new delivery to non-openers](../../automating/using/workflow-cross-channel-retargeting.md)
