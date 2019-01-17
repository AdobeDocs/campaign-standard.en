---
title: Workflow operating principles
seo-title: Workflow operating principles
description: Workflow operating principles
seo-description: Learn the main aspects of workflows.
uuid: d031162c-4292-4107-87f2-d353883e8d40
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: about-workflows-and-data-management
discoiquuid: b81621bf-0804-4424-8141-757209566e4c
isreadyforlocalization: false
index: y
internal: n
snippet: y
---

# Workflow operating principles{#workflow-operating-principles}

Workflow operating principles

A workflow is a **sequence of configurable activities**. Each activity has a specific role in the process. The result of each activity is forwarded to the following activity by a **transition**, represented by an arrow.

The type of data exchanged between one activity and another can affect the way the following activities are configured. For example, if a population is established before email delivery activity, it can serve as the target for the email in question.

You can open activities to check or edit parameters before or after executing the workflow.

You can open transitions to check that the data sent is correct during or after executing the workflow. To access the detail view of the transitions, you have to check the **[!UICONTROL Keep interim results]** option in the **[!UICONTROL Execution]** section of the workflow properties.

![](assets/workflow_overview.png)

