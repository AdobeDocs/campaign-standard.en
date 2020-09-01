---
title: Read audience
description: The Read audience activity allows you to retrieve an existing audience and to refine it by applying additional filtering conditions.
page-status-flag: never-activated
uuid: 58c54e71-f4a7-4ae9-80a3-33c379ab1db9
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: targeting-activities
discoiquuid: 674684e5-8830-4d2f-ba97-59ed4ba7422f
context-tags: readAudience,main
internal: n
snippet: y
---

# Read audience{#read-audience}

## Description {#description}

![](assets/prefill.png)

The **[!UICONTROL Read audience]** activity allows you to retrieve an existing audience and to refine it by applying additional filtering conditions.

## Context of use {#context-of-use}

The **[!UICONTROL Read audience]** activity is a simpler version of the **[!UICONTROL Query]** activity designed for cases where you only need to select an existing audience.

**Related topics**

* [Use case: Union on two refined audiences](../../automating/using/union-on-two-refined-audiences.md)
* [Use case: Reconcile a File audience with the database](../../automating/using/reconcile-file-audience-with-database.md)

## Configuration {#configuration}

1. Drop a **[!UICONTROL Read audience]** activity into your workflow.
1. Select the activity, then open it using the ![](assets/edit_darkgrey-24px.png) button from the quick actions that appear.
1. Select the audience you want to retrieve from the **[!UICONTROL Properties]** tab.

   You can retrieve audiences of the following types: **[!UICONTROL List]**, **[!UICONTROL Query]**, **[!UICONTROL File]** and **[!UICONTROL Experience Cloud]**. For more information on audience types, refer to the [Audiences](../../audiences/using/about-audiences.md) documentation.

   The **[!UICONTROL Use a dynamic audience]** option lets you define the name of the audience to target based on the workflow's events variables. For more on this, refer to this section: [](../../automating/using/customizing-workflow-events-variables.md) section.

   ![](assets/readaudience_activity1.png)

1. If you want to apply additional filtering to the selected audience, add conditions via the **[!UICONTROL Source filtering]** tab of the activity.

   For more information about creating filtering conditions, refer to the [Creating queries](../../automating/using/editing-queries.md#creating-queries) documentation.

1. Confirm the configuration of your activity and save your workflow.
