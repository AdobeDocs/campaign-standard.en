---
title: Overview
description: This section details how to call a workflow with external parameters.
audience: automating
content-type: reference
topic-tags: workflow-general-operation

feature: Workflows
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: 538056e6-b5c0-4258-a34b-524fe6e3cbbe
---
# Overview {#calling-a-workflow-with-external-parameters}

Campaign Standard lets you call a workflow with parameters (an audience name to target, a file name to import, a part of message content, etc.). This way, you can easily integrate your Campaign automations with your external system.

Let's take the following example, where we want to send emails directly from a CMS. In that case, you can configure your system to select the audience and email content into the CMS. Clicking on Send will then call a Campaign workflow with these parameters, enabling you to use them into the workflow to define the audience and URL content to use in the delivery.

The process to call a workflow with parameters is the following:

1. Declare the parameters in the **[!UICONTROL External signal]** activity. See [Declaring the parameters in the External signal activity](../../automating/using/declaring-parameters-external-signal.md).
1. Configure the **[!UICONTROL End]** activity or the API call to define the parameters and trigger the workflow **[!UICONTROL External signal]** activity. See [this page](../../automating/using/defining-parameters-calling-workflow.md)
1. Once the workflow has been triggered, the parameters are ingested into the workflow's events variables and can be used within the workflow. See [this page](../../automating/using/customizing-workflow-external-parameters.md).

![](assets/extsignal_process.png)
