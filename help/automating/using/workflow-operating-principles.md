---
title: Workflow operating principles
seo-title: Workflow operating principles
description: Workflow operating principles
seo-description: Learn the main aspects of workflows.
page-status-flag: never-activated
uuid: 00a73f7d-b902-466d-81ce-50e1f5fd2404
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/automating/using/workflow-operating-principles
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: about-workflows-and-data-management
discoiquuid: 1722051c-c4ea-4f95-b0e8-b576da5112eb
isreadyforlocalization: false
navTitle: Workflow operating principles
publishexternaldate: 2018-11-20
sha1: e3a7c0864608da14d96d71aebf7de033796537e0
index: y
internal: n
snippet: y
---

# Workflow operating principles{#workflow-operating-principles}

Workflow operating principles

A workflow is a **sequence of configurable activities**. Each activity has a specific role in the process. The result of each activity is forwarded to the following activity by a **transition**, represented by an arrow.

The type of data exchanged between one activity and another can affect the way the following activities are configured. For example, if a population is established before email delivery activity, it can serve as the target for the email in question.

You can open activities to check or edit parameters before or after executing the workflow.

You can open transitions to check that the data sent is correct during or after executing the workflow. To access the detail view of the transitions, you have to check the **Keep interim results** option in the **Execution** section of the workflow properties.

![](assets/workflow_overview.png)

