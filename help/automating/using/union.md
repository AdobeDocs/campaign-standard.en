---
title: Union
seo-title: Union
description: Union
seo-description: The Union activity allows you to regroup the result of multiple activities into a single target.
page-status-flag: never-activated
uuid: b402b7cb-39f6-4ae0-9d68-6db4c467ec46
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/automating/using/union
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: targeting-activities
discoiquuid: e7d6ed8e-fe46-4094-9dee-90f319686add
isreadyforlocalization: false
navTitle: Union
publishexternaldate: 2018-11-20
sha1: 1a48426b5d19a45a385d91e5d99611d17e6a0fbc
index: y
internal: n
snippet: y
---

# Union{#union}

Union

## Description {#description}

![](assets/union.png)

The **Union** activity allows you to regroup the result of multiple activities into a single target.

>[!NOTE]
>
>The sets do not necessarily need to be homogeneous.

## Context of use {#context-of-use}

The **Union** activity is used to combine the populations from inbound transitions when performing a segmentation, defining an audience, or when preparing the message target for example.

## Configuration {#configuration}

1. Drag and drop a **Union** activity into your workflow.
1. Connect it to the other activities that come before it, such as queries.
1. Select the activity, then open it using the  ![](assets/edit_darkgrey-24px.png)

   button from the quick actions that appear.
1. Select the **Reconciliation type** to define how duplicates are from the confrontation between inbound populations are handled:

    * **Keys only**: this is the default mode. The activity only keeps one element when elements from the different inbound transitions have the same key. This option can only be used if the inbound populations are homogeneous.
    * **All shared columns**: The data is reconciled on the basis of all the columns in common with the inbound transitions. Therefore, you have to select the primary set that will be kept in case of a duplicate. This option can be used if the inbound population targeting dimensions are different.
    * **A selection of columns**: select this option to define the list of columns on which the data reconciliation will be applied. You must first select the primary set (that which contains the source data), then the columns to use for the join.

1. Check the **Use common additional data only** box if you would like to keep only the additional data that is in all inbound transitions.
1. If you would like to limit the size of the final population, check the **Limit size of generated population** box. The size can be specified in the **Maximum number of records** field.
1. If needed, manage the activity's [Transitions](../../automating/using/executing-a-workflow.md#managing-an-activity-s-outbound-transitions) to access the advanced options for the calculated population.
1. Confirm the configuration of your activity and save your workflow.

## Example {#example}

The following example shows the result of two query activities that aim to regroup profiles from the Adobe Campaign database who are between 18 and 27 years old and those who are between 34 and 40 years old. The result contains all the profiles of the two queries or the maximum number of records, if applicable, as specified during the configuration.

![](assets/wkf_union_example.png)

