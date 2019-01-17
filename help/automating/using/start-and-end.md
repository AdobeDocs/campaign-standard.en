---
title: Start and end
seo-title: Start and end
description: Start and end
seo-description: The Start and End activities allow you to clearly mark where your workflow starts and ends.
uuid: 8d9985d6-7bdb-4243-be44-2ff7061b5d6a
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: execution-activities
discoiquuid: 8d865dc7-c7b6-4264-80a4-8f2289344ebf
isreadyforlocalization: false
index: y
internal: n
snippet: y
---

# Start and end{#start-and-end}

Start and end

## Description {#description}

![](assets/start.png) ![](assets/end.png)

The **[!UICONTROL Start]** and **[!UICONTROL End]** activities allow you to clearly mark where your workflow starts and ends.

## Context of use {#context-of-use}

Executing a workflow starts with activities without an inbound transition, and stops when there are no longer any tasks in progress. Nevertheless, you can add **[!UICONTROL Start]** and **[!UICONTROL End]** activities to clearly mark the starting and ending points of a workflow. This is especially helpful for relatively complex workflows.

It is a best practice to use an **[!UICONTROL End]** activity instead of leaving the last transition of a workflow on its own to ensure that the workflow properly ends.

## Configuration {#configuration}

1. Drag and drop a **[!UICONTROL Start]** or **[!UICONTROL End]** activity into your workflow.
1. Put the **[!UICONTROL Start]** activity in front of other activities such as queries, and the **[!UICONTROL End]** activity after a series of activities.
1. Select the activity, then open it using the  ![](assets/edit_darkgrey-24px.png)

   button from the quick actions that appear.
1. You can configure the **End** object so that it interrupts all of the workflow's ongoing tasks, including those that have not finished. To do this, select the corresponding option.
1. Confirm the configuration of your activity and save your workflow.

## Triggering another workflow {#triggering-another-workflow}

Using the **[!UICONTROL External signal]** tab of an **[!UICONTROL End]** activity, you can trigger another workflow. Refer to the [External signal](../../automating/using/external-signal.md) section.

## Example {#example}

The following example shows how a complex workflow is executed with a **[!UICONTROL Start]** activity and several **[!UICONTROL End]** activities. The **[!UICONTROL Stop all tasks in progress]** box has been checked for the first **[!UICONTROL End]** activity. Once the corresponding task is finished, the entire workflow will be stopped: it will have the same effect as if the  ![](assets/stop_darkgrey-24px.png) button had been selected (refer to the [Action bar](../../automating/using/workflow-interface.md#action-bar) section)

![](assets/wkf_start_end_example.png)

