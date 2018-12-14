---
title: Targeting data
seo-title: Targeting data
description: Targeting data
seo-description: Learn the different ways to target and select the data you need.
page-status-flag: never-activated
uuid: 29b35fc0-dbab-4c46-a98a-e54a702ff637
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: workflow-general-operation
discoiquuid: ffd61ce4-7249-42eb-9922-f350b4cc9ae1
isreadyforlocalization: true
index: y
internal: n
snippet: y
---

# Targeting data{#targeting-data}

Targeting data

## Selecting data {#selecting-data}

You can select data using the following activities:

* The **Query** activity allows you to filter and extract a population of elements from the Adobe Campaign database.
* The **Incremental query** activity allows you to filter and extract a population of elements from the Adobe Campaign database. Each time this activity is executed, the results from the previous executions are excluded. This allows you to target only new elements.
* The **Read audience** activity allows you to retrieve an existing audience and to refine it by applying additional filtering conditions.

## Segmenting data {#segmenting-data}

Adobe Campaign lets you process sets on inbound data. You can thus combine several populations, exclude part of it or only keep data common to several targets.

* The **Union** activity allows you to regroup the result of multiple activities into a single target.
* The **Intersection** activity allows you to keep only the elements common to the different inbound populations in the activity.
* The **Exclusion ** activity allows you to exclude elements from one population according to certain criteria.
* The **Segmentation** activity lets you create one or several segments from a population calculated by activities placed earlier in the workflow. At the end of the activity, they can be processed in one single transition or different transitions.

## Enriching data {#enriching-data}

The identified and collected data can be enriched, aggregated and manipulated to optimize target construction. You can simplify and optimize targeting processes, by including data that is not modeled in the data mart.

The **Additional data** tab of the **Query** and **Incremental query** activities allows you to enrich the data targeted by the query and transfer this data to the following workflow activities, where it can be utilized. In particular, you can add:

* Simple data
* Aggregates
* Collections

