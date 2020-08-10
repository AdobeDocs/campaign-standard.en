---
title: Managing execution options
description: Learn how to manage workflows execution options.
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

# Managing execution options {#managing-execution-options}

To modify a workflow's execution options, use the ![](assets/edit_darkgrey-24px.png) button to access the workflow properties and select the **[!UICONTROL Execution]** section.

![](assets/wkf_execution_6.png)

Possible options are:

* **[!UICONTROL Default affinity]**: this field allows you to force a workflow or a workflow activity to execute on a particular machine.

* **[!UICONTROL History in days]**: specifies the number of days after which the history must be purged. The history contains elements related to the workflow : logs, tasks, events (technical objects linked to the workflow operation), as well as files downloaded by the **[!UICONTROL Transfer file]** activity. Default value is 30 days for out-of-the-box workflow templates.

  Purge of the history is performed by the Database cleanup technical workflow, which is executed by default everyday (see [List of technical workflows](../../administration/using/technical-workflows.md).)

  >[!IMPORTANT]
  >
  >If the **[!UICONTROL History in days]** field is left blank, its value will be considered as "1", meaning that the history will purged after 1 day.

* **[!UICONTROL Save SQL queries in the log]**: allows you to save the SQL queries from the workflow into the logs.

* **[!UICONTROL Keep interim results]**: check this option if you would like to be able to view the detail of transitions. Warning: checking this option may significantly slow down the workflow execution.

* **[!UICONTROL Execute in the engine (do not use in production)]**: allows you to execute the workflow locally, for development environment testing purposes.

* **[!UICONTROL Severity]**: allows you to specify a level of priority for executing workflows in your Adobe Campaign instance. Critical workflows will be executed first.

The **[!UICONTROL Error management]** section provides additional options that allow you to manage how workflows behave in case of errors. These options are detailed in the [Error management](../../automating/using/monitoring-workflow-execution.md#error-management) section.
