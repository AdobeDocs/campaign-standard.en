---
title: Targeting data
seo-title: Targeting data
description: Targeting data
seo-description: Learn the different ways to target and select the data you need.
page-status-flag: never-activated
uuid: 0645d6e5-6a7e-4917-874a-7e7725f06abd
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: workflow-general-operation
discoiquuid: 382ea74e-1662-4c64-96d7-676040586913

internal: n
snippet: y
---

# Targeting data{#targeting-data}

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

