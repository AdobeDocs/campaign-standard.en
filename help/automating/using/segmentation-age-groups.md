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
internal: n
snippet: y
---

# Segmentation according to age groups {#segmentation-age-groups}

The following example shows a segmentation of database profiles according to their age group.

The aim of the workflow is to send a specific email for each age group. Considering the fact that this workflow is part of a test campaign, each segment can only contain a maximum of 100 profiles that are selected randomly in order to use audiences that are limited and representative at the same time.

For more on how to use the **[!UICONTROL Segmentation]** activity, refer to [this section](../../automating/using/segmentation.md).

![](assets/wkf_segment_example_4.png)

The workflow is made up of the following elements:

* A **[!UICONTROL Scheduler]** activity to specify the workflow's execution date. Refer to the [Scheduler](../../automating/using/scheduler.md) section.
* A **[!UICONTROL Query]** activity to target profiles of people whose birthday and email address have been entered. Refer to the [Query](../../automating/using/query.md) section.
* A **[!UICONTROL Segmentation]** activity to create 3 segments divided into different outbound transitions: 18-25-year old, 26-32-year old and profiles that are over 32 years old. The segments are defined according to the following parameters:

  ![](assets/wkf_segment_example_3.png)

    * A filter on the age to define the segment's age group
    
      ![](assets/wkf_segment_new_segment.png)

    * A **[!UICONTROL Random sampling]** type limit that is linked to a **[!UICONTROL Maximum size]** limit of 100
    
      ![](assets/wkf_segment_example_1.png)

* An **[!UICONTROL Email delivery]** activity per segment. Refer to the [Email delivery](../../automating/using/email-delivery.md) section.
