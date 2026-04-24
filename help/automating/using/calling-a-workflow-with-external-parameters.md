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
TQID: https://experienceleague.adobe.com/Pin9vFRMMylFFKw6VSvQowwXvzAn1Ihg76e2cSoaeyw
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
# Overview {#calling-a-workflow-with-external-parameters}

Campaign Standard lets you call a workflow with parameters (an audience name to target, a file name to import, a part of message content, etc.). This way, you can easily integrate your Campaign automations with your external system.

Let's take the following example, where we want to send emails directly from a CMS. In that case, you can configure your system to select the audience and email content into the CMS. Clicking on Send will then call a Campaign workflow with these parameters, enabling you to use them into the workflow to define the audience and URL content to use in the delivery.

The process to call a workflow with parameters is the following:

1. Declare the parameters in the **[!UICONTROL External signal]** activity. See [Declaring the parameters in the External signal activity](../../automating/using/declaring-parameters-external-signal.md).
1. Configure the **[!UICONTROL End]** activity or the API call to define the parameters and trigger the workflow **[!UICONTROL External signal]** activity. See [this page](../../automating/using/defining-parameters-calling-workflow.md)
1. Once the workflow has been triggered, the parameters are ingested into the workflow's events variables and can be used within the workflow. See [this page](../../automating/using/customizing-workflow-external-parameters.md).

![](assets/extsignal_process.png)
