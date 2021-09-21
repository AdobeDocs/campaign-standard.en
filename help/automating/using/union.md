---
title: Union
description: The Union activity allows you to regroup the result of multiple activities into a single target.
audience: automating
content-type: reference
topic-tags: targeting-activities
context-tags: union,main
feature: Workflows
role: Data Architect
level: Intermediate
exl-id: 3189745c-dcc9-4719-b080-85ffa3bb66be
---
# Union{#union}

## Description {#description}

![](assets/union.png)

The **[!UICONTROL Union]** activity allows you to regroup the result of multiple activities into a single target.

>[!NOTE]
>
>The sets do not necessarily need to be homogeneous.

## Context of use {#context-of-use}

The **[!UICONTROL Union]** activity is used to combine the populations from inbound transitions when performing a segmentation, defining an audience, or when preparing the message target for example.

**Related topics:**

* [Use case: Union on two refined audiences](../../automating/using/union-on-two-refined-audiences.md)

## Configuration {#configuration}

1. Drag and drop a **[!UICONTROL Union]** activity into your workflow.
1. Connect it to the other activities that come before it, such as queries.
1. Select the activity, then open it using the ![](assets/edit_darkgrey-24px.png) button from the quick actions that appear.
1. Select the **[!UICONTROL Reconciliation type]** to define how duplicates are from the confrontation between inbound populations are handled:

    * **[!UICONTROL Keys only]**: this is the default mode. The activity only keeps one element when elements from the different inbound transitions have the same key. This option can only be used if the inbound populations are homogeneous.
    * **[!UICONTROL All shared columns]**: The data is reconciled on the basis of all the columns in common with the inbound transitions. Therefore, you have to select the primary set that will be kept in case of a duplicate. This option can be used if the inbound population targeting dimensions are different.
    * **[!UICONTROL A selection of columns]**: select this option to define the list of columns on which the data reconciliation will be applied. You must first select the primary set (that which contains the source data), then the columns to use for the join.

1. Check the **[!UICONTROL Use common additional data only]** box if you would like to keep only the additional data that is in all inbound transitions.
1. If you would like to limit the size of the final population, check the **[!UICONTROL Limit size of generated population]** box. The size can be specified in the **[!UICONTROL Maximum number of records]** field.
1. If needed, manage the activity's [Transitions](../../automating/using/activity-properties.md) to access the advanced options for the calculated population.
1. Confirm the configuration of your activity and save your workflow.

## Example {#example}

The following example shows the result of two query activities that aim to regroup profiles from the Adobe Campaign database who are between 18 and 27 years old and those who are between 34 and 40 years old. The result contains all the profiles of the two queries or the maximum number of records, if applicable, as specified during the configuration.

![](assets/wkf_union_example.png)
