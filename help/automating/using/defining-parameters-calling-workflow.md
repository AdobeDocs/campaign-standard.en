---
title: Defining the parameters when calling the workflow
description: This section details how to call a workflow with external parameters.
audience: automating
content-type: reference
topic-tags: workflow-general-operation
feature: Workflows
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: f7de0186-4136-4603-8f80-9f58c641cd9d
TQID: https://experienceleague.adobe.com/-YjlK1Op8P08sxb--BOHl8AWyciX4BqPnCPQ3lpD3Co
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
feature_v2:
  - id: b12f6872-9271-4369-85e5-86969a0b99a2
    internal-label: APIs
subfeature_v2:
  - id: bf97c196-a4d1-4fa3-a151-e68a114c8ac0
    internal-label: REST API
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
---
# Defining the parameters when calling the workflow {#defining-the-parameters-when-calling-the-workflow}

This section details how to define parameters when calling a workflow. For more on how to perform this operation from an API call, refer to the [REST APIs documentation](../../api/using/triggering-a-signal-activity.md).

Before defining the parameters, make sure that:

* The parameters have been declared in the **[!UICONTROL External Signal]** activity. See [this page](../../automating/using/declaring-parameters-external-signal.md).
* The workflow containing the signal activity is running.

To configure the **[!UICONTROL End]** activity, follow the steps below:

1. Open the **[!UICONTROL End]** activity, then select the **[!UICONTROL External signal]** tab.
1. Select the workflow and the external signal activity that you want to call.
1. Click the **[!UICONTROL Create element]** button to add a parameter, then fill in its name and value.

    * **[!UICONTROL Name]**: the name that has been declared in the **[!UICONTROL External signal]** activity (see [this page](../../automating/using/declaring-parameters-external-signal.md)).
    * **[!UICONTROL Value]**: the value that you want to assign to the parameter. The value should follow the **Standard syntax**, described in [this section](../../automating/using/advanced-expression-editing.md#standard-syntax).

   ![](assets/extsignal_definingparameters_2.png)

   >[!CAUTION]
   >
   >Make sure that all the parameters have been declared in the **[!UICONTROL External signal]** activity. Otherwise, an error will occur when running the activity.

1. Once the parameters have been defined, confirm the activity, then save your workflow.
