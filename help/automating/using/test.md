---
title: Test
description: The Test activity enables a transition based on a test result.
page-status-flag: never-activated
uuid: 1562ec7a-253a-4f4f-b66a-c2948b57775a
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: execution-activities
discoiquuid: 2650bf1f-0bce-4049-a226-2369f6666b95
context-tags: jstest,main
internal: n
snippet: y
---

# Test{#test}

## Description {#description}

![](assets/test.png)

The **[!UICONTROL Test]** activity enables a transition based on a test result.

## Context of use {#context-of-use}

A **Test** activity activates the first transition that satisfies the condition associated to it.

If no condition is satisfied and if the **Use default transition** option is activated, a default transition will be activated.

![](assets/wkf_test_activity_example.png)

Conditions can be based on **functions**, or on **variables**, for example events variables that have been declared into the workflow's **[!UICONTROL External signal]** activity.

**Related topics:**

* [List of functions](../../automating/using/list-of-functions.md)
* [Calling a workflow with external parameters](../../automating/using/calling-a-workflow-with-external-parameters.md)

## Configuration {#configuration}

1. Drag and drop a **[!UICONTROL Test]** activity into the workflow.
1. Select the activity, then open it using the ![](assets/edit_darkgrey-24px.png) button from the quick actions that appear.
1. Define each condition's attributes:

   When editing the **[!UICONTROL Condition]** field, two buttons provide help to call events variables and edit expressions combining variables and functions:

    * ![](assets/extsignal_picker.png): select the events variable among all variables that are available in the workflow (see [Customizing a workflow with external parameters](../../automating/using/calling-a-workflow-with-external-parameters.md#customizing-a-workflow-with-external-parameters))
    
      ![](assets/wkf_test_activity_variables.png)

    * ![](assets/extsignal_expression_editor.png): edit expressions combining variables and functions. For more on the Expression editor, refer to [this section](../../automating/using/advanced-expression-editing.md).
    
      ![](assets/wkf_test_activity_variables_expression.png)

