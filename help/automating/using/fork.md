---
title: Fork
description: The Fork activity allows you to create outbound transitions to start several activities at the same time.
audience: automating
content-type: reference
topic-tags: execution-activities
context-tags: fork,main
feature: Workflows
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: 1a5e1ecd-b3f1-4dbe-a816-12d27a3bc0f7
TQID: https://experienceleague.adobe.com/1-9VY3TjBBHAb-7bFikis3Ue5eWy5KXKSR4hXxXDLwc
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
---
# Fork{#fork}

## Description {#description}

![](assets/fork.png)

The **[!UICONTROL Fork]** activity allows you to create outbound transitions to start several activities at the same time.

## Context of use {#context-of-use}

The **[!UICONTROL Fork]** activity allows you to carry out several different activities independently within the same workflow.

## Configuration {#configuration}

1. Drag and drop a **[!UICONTROL Fork]** activity into your workflow.
1. Connect it to the other activities that come before it, such as queries.
1. Select the activity, then open it using the ![](assets/edit_darkgrey-24px.png) button from the quick actions that appear.
1. Specify the number of outbound transitions by creating, deleting or duplicating them. You can also attribute a name and a label to them.
1. Confirm the configuration of your activity and save your workflow.

## Example {#example}

The following example shows an intersection of two query activities that target profiles from the Adobe Campaign database, in this case, women living in Paris. The fork activity therefore allows you to use several activities at the same time: one that saves the audience to remember the calculated population, and another that segments the population to send two different emails with a targeted content for each segment. The first email is sent to Parisian women aged between 18 and 40 and another targeting Parisian women aged over 40.

![](assets/wkf_fork_example.png)
