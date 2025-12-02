---
title: Execution commands
description: Learn how to use workflows execution commands.
audience: automating
content-type: reference
topic-tags: workflow-general-operation
context-tags: workflow,overview;workflow,main
feature: Workflows
old-role: Data Architect
role: Developer
level: Beginner
exl-id: fddd88b1-603a-465b-b5e7-624632c0d5cd
---
# Execution commands {#execution-commands}

The icons in the action bar allow you to start, track, and modify a workflow's execution. See [Action bar](../../automating/using/workflow-interface.md#action-bar).

![](assets/wkf_execution_2.png)

The actions available are as follows:

**Start**

The ![](assets/play_darkgrey-24px.png) button starts executing a workflow, which then takes on the **In progress** (blue) status. If the workflow was paused, it is resumed, otherwise it is started and the initial activities are then activated.

>[!NOTE]
>
>Starting is an asynchronous process: the request is saved and will be processed as soon as possible by the workflow execution engine.

**Pause**

The ![](assets/pause_darkgrey-24px.png) button pauses the execution. The workflow takes on the **Warning** (yellow) status. No new activities will be activated until it is resumed, but operations in progress are not suspended.

**Stop**

The ![](assets/stop_darkgrey-24px.png) button stops a workflow that is being executed, which will then take on the **Finished** (green) status. The operations in progress are interrupted if possible, and imports or SQL queries in progress are immediately canceled. You cannot resume from the workflow from the same place that it was stopped.

**Restart**

The ![](assets/pauseplay_darkgrey-24px.png) button involves stopping, then restarting a workflow. In most cases, this allows you to restart quicker. It can also be useful to automate restarting once stopping takes a certain amount of time, because the ![](assets/play_darkgrey-24px.png) button is only available when the stop is effective.

When one or multiple activities in a workflow are selected, there are other actions you can carry out, such as:

**Immediate execution**

The ![](assets/pending_darkgrey-24px.png) button starts any pending activities selected as soon as possible.

**Normal execution**

The ![](assets/check_darkgrey-24px.png) button reactivates any paused or deactivated activities.

**Execution suspended**

The ![](assets/check_pause_darkgrey-24px.png) button pauses the workflow at the selected activity: this task as well as all those that follow it (in the same branch) are not executed.

**No execution**

The ![](assets/checkdisable.png) button deactivates any selected activities.

>[!NOTE]
>
>Quick actions let you access different actions concerning one particular activity and appear when an activity is selected.
