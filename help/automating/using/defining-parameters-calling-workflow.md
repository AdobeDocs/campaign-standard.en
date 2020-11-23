---
solution: Campaign Standard
product: campaign
title: Calling a workflow with external parameters
description: This section details thow to call a workflow with external parameters.
audience: automating
content-type: reference
topic-tags: workflow-general-operation

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
