---
title: Targeting data
seo-title: Targeting data
description: Targeting data
seo-description: Learn the different ways to target and select the data you need.
uuid: c2dcf1a7-137f-4244-8b6f-7e49f0aa0227
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: workflow-general-operation
discoiquuid: 3c2fb56e-728c-46f4-a46e-370474333fac
index: y
internal: n
snippet: y
---

# Targeting data{#targeting-data}

Targeting data

## Selecting data {#selecting-data}

You can select data using the following activities:

* The **[!UICONTROL Query]** activity allows you to filter and extract a population of elements from the Adobe Campaign database.
* The **[!UICONTROL Incremental query]** activity allows you to filter and extract a population of elements from the Adobe Campaign database. Each time this activity is executed, the results from the previous executions are excluded. This allows you to target only new elements.
* The **[!UICONTROL Read audience]** activity allows you to retrieve an existing audience and to refine it by applying additional filtering conditions.

## Segmenting data {#segmenting-data}

Adobe Campaign lets you process sets on inbound data. You can thus combine several populations, exclude part of it or only keep data common to several targets.

* The **[!UICONTROL Union]** activity allows you to regroup the result of multiple activities into a single target.
* The **[!UICONTROL Intersection]** activity allows you to keep only the elements common to the different inbound populations in the activity.
* The **[!UICONTROL Exclusion]** activity allows you to exclude elements from one population according to certain criteria.
* The **[!UICONTROL Segmentation]** activity lets you create one or several segments from a population calculated by activities placed earlier in the workflow. At the end of the activity, they can be processed in one single transition or different transitions.

## Enriching data {#enriching-data}

The identified and collected data can be enriched, aggregated and manipulated to optimize target construction. You can simplify and optimize targeting processes, by including data that is not modeled in the data mart.

The **[!UICONTROL Additional data]** tab of the **[!UICONTROL Query]** and **[!UICONTROL Incremental query]** activities allows you to enrich the data targeted by the query and transfer this data to the following workflow activities, where it can be utilized. In particular, you can add:

* Simple data
* Aggregates
* Collections

