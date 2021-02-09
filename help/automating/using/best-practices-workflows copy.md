---
solution: Campaign Standard
product: campaign
title: Preventing overlapping execution of scheduled workflows
description: Learn how to prevent overlapping execution of scheduled workflows.
audience: automating
content-type: reference
topic-tags: workflow-general-operation
context-tags: workflow,overview;workflow,main
---

# Preventing overlapping execution of scheduled workflows {#preventing-overlapping-execution-of-scheduled-workflows}

This sections provides best practices for long running scheduled workflows, so that the next execution of a scheduled workflow does not accidentally overlap with the previous unfinished (pending) execution of that same workflow. 

## About scheduled workflows execution

In Campaign Standard, the workflow engine guarantees that a workflow instance is executed by only one process (see [Architecture](../../workflow/using/architecture.md)).

Blocking activities such as imports, long running queries or writes into the database prevent the execution of any other task when running.

On the other hand, non-blocking activities do not block the execution of other tasks (usually activities waiting for an event such as the **[!UICONTROL Scheduler]**, the **[!UICONTROL Wait]** activity etc.).

This can lead to a scenario where a schedule-based workflow can start executing even when the previous run of that same workflow has not yet finished, potentially leading to unexpected data issues.

Therefore, when designing a scheduled workflow which includes multiple activities, you need to make sure that the workflow is not rescheduled until it is finished. To do this, you need to configure your workflow as shown below, in order to prevent its execution if one or more tasks from a previously execution of that workflow is still pending.

## Configuring the workflow

To check if one or more tasks from a previous workflow execution is still pending, you need to use a **[!UICONTROL Query]** and a **[!UICONTROL Test]** activity.

1. Add a **[!UICONTROL Query]** activity right after the **[!UICONTROL Scheduler]** activity, then configure it as follows.

1. Change the activity's resource to **[!UICONTROL WorkflowTaskDetail]**, meaning it will target the workflow's current tasks.

    ![](assets/scheduled-wkf-resource.png)

1. Configure the query wit the conditions below:

    ![](assets/scheduled-wkf-query.png)

    * The first condition filters out the current task (query2) as well as the next schedule task (schedule2) belonging to the current workflow.

        >[!NOTE]
        >
        >When the Scheduler activity starts, it immediately adds another schedule task to run at the next scheduled time and start the workflow. Therefore, it is important to filter both the query as well as schedule tasks when looking for pending tasks from a previous execution.

    * The second condition determines whether any tasks from a previous run of the workflow are still active (pending), which corresponds to the 0 execution status.

1. Add a **[!UICONTROL Test]** activity in order to check for the number of pending tasks returned by the **[!UICONTROL Query]** activity. To do this, configure two outbound transitions.

    * Continue the workflow execution if there are no pending tasks,
    * Cancel the workflow execution of there are any pending tasks.

    ![](assets/scheduled-wkf-test.png)

You can now configure the rest of your workflow as needed. If the workflow execution is canceled due to pending tasks, when the workflow runs again as per the schedule, it can go through these steps. This will ensure that the workflow execution will proceed only if there are no active (pending) tasks from a previous execution.
