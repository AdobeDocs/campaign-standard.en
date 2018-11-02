---
title: Targeting data
seo-title: Targeting data
description: Targeting data
seo-description: Learn the different ways to target and select the data you need.
uuid: 8d0c90dc-12e6-4693-b8a4-0c3cb5b2a0e4
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/automating/using/targeting-data
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-25T09 29 13.651-0400
cq-lastreplicated: 2018-07-23T05 56 50.589-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: workflow-general-operation
cq-template: /apps/help/templates/article-3
discoiquuid: da45bac0-5dd0-400f-97d0-8a4e5e4b2306
firstPublishExternalDate: 2018-07-23T05:56:50.538-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 36.995-0400
jcr-createdby: admin
jcr-description: Targeting data
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T05:56:50.538-0400
lochandoffdate: 2018-07-25T09 29 13.651-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Targeting data
publishexternaldate: 2018-07-23T05 56 50.538-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/automating/using/targeting-data.html
sha1: aeb7cf223249af9f1005fda8d4f0f31bd060f376
topicBrowsingSortDate: 2018-07-23T05:56:50.538-0400
index: y
internal: n
snippet: y
---

# Targeting data

Targeting data

## Selecting data

You can select data using the following activities:

* The **Query** activity allows you to filter and extract a population of elements from the Adobe Campaign database.
* The **Incremental query** activity allows you to filter and extract a population of elements from the Adobe Campaign database. Each time this activity is executed, the results from the previous executions are excluded. This allows you to target only new elements.
* The **Read audience** activity allows you to retrieve an existing audience and to refine it by applying additional filtering conditions.

## Segmenting data

Adobe Campaign lets you process sets on inbound data. You can thus combine several populations, exclude part of it or only keep data common to several targets.

* The **Union** activity allows you to regroup the result of multiple activities into a single target.
* The **Intersection** activity allows you to keep only the elements common to the different inbound populations in the activity.
* The **Exclusion ** activity allows you to exclude elements from one population according to certain criteria.
* The **Segmentation** activity lets you create one or several segments from a population calculated by activities placed earlier in the workflow. At the end of the activity, they can be processed in one single transition or different transitions.

## Enriching data

The identified and collected data can be enriched, aggregated and manipulated to optimize target construction. You can simplify and optimize targeting processes, by including data that is not modeled in the data mart.

The **Additional data** tab of the **Query** and **Incremental query** activities allows you to enrich the data targeted by the query and transfer this data to the following workflow activities, where it can be utilized. In particular, you can add:

* Simple data
* Aggregates
* Collections

