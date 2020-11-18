---
title: Segmentation according to age groups
description: This page presents a segmentation of database profiles according to their age group. The aim of the workflow is to send a specific email for each age group.
page-status-flag: never-activated
uuid: 77796f18-cad5-4e7a-9d7b-4ed0dd8943bf
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: targeting-activities
discoiquuid: 0ccd9d02-772e-406b-874a-5381dd0c8709
context-tags: segmentation,main
---

# Segmentation according to age groups {#segmentation-age-groups}

The following example shows a segmentation of database profiles according to their age group.

The aim of the workflow is to send a specific email for each age group. Considering the fact that this workflow is part of a test campaign, each segment can only contain a maximum of 100 profiles that are selected randomly in order to use audiences that are limited and representative at the same time.

![](assets/wkf_segment_example_4.png)

The workflow is made up of the following elements:

* A [Scheduler activity](../../automating/using/segmentation.md) to specify the workflow's execution date.
* A [Query](../../automating/using/query.md) activity to target profiles of people whose birthday and email address have been entered.
* A [Segmentation](../../automating/using/segmentation.md) activity to create 3 segments divided into different outbound transitions: 18-25-year old, 26-32-year old and profiles that are over 32 years old. The segments are defined according to the following parameters:

  ![](assets/wkf_segment_example_3.png)

    * A filter on the age to define the segment's age group

      ![](assets/wkf_segment_new_segment.png)

    * A **[!UICONTROL Random sampling]** type limit that is linked to a **[!UICONTROL Maximum size]** limit of 100

      ![](assets/wkf_segment_example_1.png)

* An [Email delivery](../../automating/using/email-delivery.md) activity per segment.
