---
title: Workflow operating principles
description: Learn the main aspects of workflows.
page-status-flag: never-activated
uuid: 85755e85-617b-4a9b-bb30-96ba8333f4f0
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: about-workflows-and-data-management
discoiquuid: 3a13785d-1ef7-4043-9927-2d495b83709f

internal: n
snippet: y
---

# Workflow operating principles{#workflow-operating-principles}

A workflow is a **sequence of configurable activities**. Each activity has a specific role in the process. The result of each activity is forwarded to the following activity by a **transition**, represented by an arrow.

The type of data exchanged between one activity and another can affect the way the following activities are configured. For example, if a population is established before email delivery activity, it can serve as the target for the email in question.

You can open activities to check or edit parameters before or after executing the workflow.

You can open transitions to check that the data sent is correct during or after executing the workflow. To access the detail view of the transitions, you have to check the **[!UICONTROL Keep interim results]** option in the **[!UICONTROL Execution]** section of the workflow properties.

![](assets/workflow_overview.png)

