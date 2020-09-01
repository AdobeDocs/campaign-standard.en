---
title: Calling a workflow with external parameters
description: This section details thow to call a workflow with external parameters.
page-status-flag: never-activated
uuid: beccd1b6-8e6d-4504-9152-9ff537459c4a
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: workflow-general-operation
discoiquuid: 1676da91-55e3-414f-bcd3-bb0804b682bd

internal: n
snippet: y
---

# Calling a workflow with external parameters{#calling-a-workflow-with-external-parameters}

Campaign Standard lets you call a workflow with parameters (an audience name to target, a file name to import, a part of message content, etc.). This way, you can easily integrate your Campaign automations with your external system.

Let's take the following example, where we want to send emails directly from a CMS. In that case, you can configure your system to select the audience and email content into the CMS. Clicking on Send will then call a Campaign workflow with these parameters, enabling you to use them into the workflow to define the audience and URL content to use in the delivery.

The process to call a workflow with parameters is the following:

1. Declare the parameters in the **[!UICONTROL External signal]** activity. See [Declaring the parameters in the External signal activity](../../automating/using/calling-a-workflow-with-external-parameters.md#declaring-the-parameters-in-the-external-signal-activity).
1. Configure the **[!UICONTROL End]** activity or the API call to define the parameters and trigger the workflow **[!UICONTROL External signal]** activity.

Once the workflow has been triggered, the parameters are ingested into the workflow's events variables and can be used within the workflow. See [Customizing a workflow with external parameters](../../automating/using/calling-a-workflow-with-external-parameters.md#customizing-a-workflow-with-external-parameters).

![](assets/extsignal_process.png)
