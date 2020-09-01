---
title: External signal
description: The External signal activity triggers a workflow when some conditions are successfully met in another workflow.
page-status-flag: never-activated
uuid: 884b6daf-bfd9-440b-8336-004b80c76def
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: execution-activities
discoiquuid: 911c71b5-da8b-4916-b645-13bba6d21715
context-tags: signal,main
internal: n
snippet: y
---

# External signal{#external-signal}

## Description {#description}

![](assets/signal.png)

The **[!UICONTROL External signal]** activity triggers a workflow when some conditions are successfully met in another workflow or from a REST API call.

## Context of use {#context-of-use}

The **[!UICONTROL External signal]** activity is used to organize and orchestrate different processes that are part of the same customer journey into different workflows. It allows to start one workflow from another, enabling to support more complex customer journeys, while being able to better monitor and react in case of issue.

The **[!UICONTROL External signal]** activity is designed to be placed as the first activity of a workflow. It can be triggered from the **[!UICONTROL End]** activity of another workflow or from a REST API call (for more on this, refer to the [API documentation](../../api/using/triggering-a-signal-activity.md)).

When triggered, external parameters can be defined and be available in the workflow events variables. The process to call a workflow with external parameters is detailed in [this section](../../automating/using/calling-a-workflow-with-external-parameters.md).

>[!NOTE]
>
>The activity cannot be triggered more often than every 10 minutes.

Note that an **[!UICONTROL External signal]** activity can be triggered from several different events. In that case, the **[!UICONTROL External signal]** is triggered as soon as one of the source workflows or API call is executed. It does not require that all source workflows are finished.

**Related topics**

* [Use case: External signal activity and data import](../../automating/using/external-signal-data-import.md).
* [Use case: Calling a workflow to create an audience from a file using external parameters](../../automating/using/use-case-calling-workflow.md)

## Configuration {#configuration}

When configuring an external signal, it is important to first configure the **[!UICONTROL External signal]** activity in the destination workflow. Once this configuration is done, the **[!UICONTROL External signal]** activity of this workflow becomes available to configure the **[!UICONTROL End]** activity of the source workflow.

1. Drag and drop an **[!UICONTROL External signal]** activity into your destination workflow.
1. Select the activity, then open it using the ![](assets/edit_darkgrey-24px.png) button from the quick actions that appear.
1. Edit the label of the activity. This label is needed when configuring the source workflow that triggers the **[!UICONTROL External signal]**.

   If you want to call the workflow with parameters, use the **[!UICONTROL Parameters]** area to declare them. For more on this, refer to this section: [](../../automating/using/declaring-parameters-external-signal-activity.md).

   ![](assets/external_signal_configuration.png)

1. Confirm the configuration of your activity, add any other activity you need and save your workflow.

   >[!NOTE]
   >
   >If you want to trigger the destination workflow from another workflow, proceed with the following steps. If you want to trigger the destination workflow from a REST API call, consult the [API documentation](../../api/using/triggering-a-signal-activity.md) to get more details.

1. Open the source workflow and select an **[!UICONTROL End]** activity. If there is no **[!UICONTROL End]** activity available, add one after the last activity of a branch of the workflow.

   Some activities do not have any outbound transition by default. From the **[!UICONTROL Properties]** tab of these activities, you can add an outbound transition.

   For example, in an **[!UICONTROL Update data]** activity, go to the **[!UICONTROL Transitions]** tab and check the **[!UICONTROL Add an outbound transition without the population]** option. This option allows to add a transition that does not contain any data and do not consume any unnecessary space on your system. It is just used to connect the extra **[!UICONTROL End]** activity that triggers the destination workflow.

   ![](assets/external_signal_empty_transition.png)

1. In the **[!UICONTROL External signal]** tab of the **[!UICONTROL End]** activity, select the destination workflow as well as the **[!UICONTROL External signal]** activity to trigger within that workflow.

   When you set an **[!UICONTROL End]** activity to trigger another workflow, its icon is updated with an additional signal symbol.

   If you want to call the workflow with parameters, use the **[!UICONTROL Parameters and values]** area. For more on this, refer to this section: [](../../automating/using/defining-parameters-calling-workflow.md).

   ![](assets/external_signal_end.png)

1. Save the source workflow.

Once the **[!UICONTROL End]** activity of the source workflow or the REST API call is executed, the destination workflow is automatically triggered from the **[!UICONTROL External signal]** activity.

>[!NOTE]
>
>The destination workflow must be started manually before it can be triggered. When started, the **[!UICONTROL External activity]** is activated and waits for the signal from the source workflow.
