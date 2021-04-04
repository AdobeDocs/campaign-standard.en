---
solution: Campaign Standard
product: campaign
title: Calling a workflow with external parameters
description: This section details thow to call a workflow with external parameters.
audience: automating
content-type: reference
topic-tags: workflow-general-operation

feature: Workflows
role: Data Architect
level: Intermediate
exl-id: e6148b40-f608-4aab-81f6-756608c6828e
---
# Declaring the parameters in the External signal activity {#declaring-the-parameters-in-the-external-signal-activity}

The first step to call a workflow with parameters is to declare them in an **[!UICONTROL External signal]** activity.

1. Open the **[!UICONTROL External signal]** activity, then select the **[!UICONTROL Parameters]** tab.
1. Click the **[!UICONTROL Create element]** button, then specify the name and type of each parameter.

   >[!CAUTION]
   >
   >Make sure that the name and number of parameters are identical to what is defined when calling the workflow (see [this page](../../automating/using/defining-parameters-calling-workflow.md)). Moreover, the parameters' types must be consistent with the values that are expected.

   ![](assets/extsignal_declaringparameters_1.png)

1. Once the parameters have been declared, finish the workflow configuration, then run it.
