---
title: Workflow life cycle
description: Learn more about workflow life cycle
page-status-flag: never-activated
uuid: ff02b74e-53e8-49c6-bf8e-0c729eaa7d25
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: workflow-general-operation
discoiquuid: 906c85ea-83b7-4268-86da-cd353f1dc591
context-tags: workflow,overview;workflow,main
internal: n
snippet: y
---

# Workflow life cycle {#life-cycle}

A workflow's life cycle includes three main steps and each step is linked to a status and a color:

* **Editing** (gray)

  This is the initial design phase of a workflow (refer to [Creating a workflow](../../automating/using/building-a-workflow.md#creating-a-workflow)). The workflow is not yet handled by the server and can be modified without any risk.

* **In progress** (blue)

  Once the initial design phase is complete, the workflow can be started and is handled by the server.

* **Finished** (green)

  A workflow is finished once there are no longer any tasks in progress or when an operator has explicitly stopped the instance.

Once it has been started, a workflow may also have two other statuses:

* **Warning** (yellow)

  The workflow could not finish or was paused using the ![](assets/pause_darkgrey-24px.png) or ![](assets/check_pause_darkgrey-24px.png) buttons.

* **Erroneous** (red)

  An error occurred when a workflow was executed. The workflow was stopped and the user must carry out an action. To find out more about this error, use the ![](assets/printpreview_darkgrey-24px.png) button to access the workflow log (refer to [Monitoring](#monitoring)).

The list of marketing activities allows you to display all the workflows as well as their statuses. For more on this, see [Managing marketing activities](../../start/using/marketing-activities.md#about-marketing-activities).

![](assets/wkf_execution_3.png)
