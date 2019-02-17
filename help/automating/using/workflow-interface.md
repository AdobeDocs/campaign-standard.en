---
title: Workflow interface
seo-title: Workflow interface
description: Workflow interface
seo-description: Learn the interface and options to create, edit and execute a workflow.
uuid: bffa5a47-e47d-47e4-82c6-b5cb91521274
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: about-workflows-and-data-management
discoiquuid: 36fbc765-157b-495b-a1ee-ea67a91777ca
index: y
internal: n
snippet: y
---

# Workflow interface{#workflow-interface}

Workflow interface

You can create workflows to manage entire processes in your campaigns and programs.

The workflow editing screen is made up of the following elements:

* The [Palette](../../automating/using/workflow-interface.md#palette), which references the available activities
* The [Workspace](../../automating/using/workflow-interface.md#workspace), in which the activities are configured and organized
* The [Action bar](../../automating/using/workflow-interface.md#action-bar), which is made up of buttons that allow you to interact with the workflow and/or its components.
* The [Quick actions](../../automating/using/workflow-interface.md#quick-actions), which appear around a selected activity, allow you to interact with it.

![](assets/wkf_overview.png)

## Palette {#palette}

The palette is on the left-hand side of the screen. All available activities are sorted into several categories:

* [Targeting](../../automating/using/about-targeting-activities.md): activities specific to targeting, manipulating population data, and filtering activities
* [Execution](../../automating/using/about-execution-activities.md): activities specific to organizing and executing workflows
* [Channels](../../automating/using/about-channel-activities.md): activities representing the different available communication channels
* [Data Management (ETL)](../../automating/using/about-data-management-activities.md): activities specific to manipulating data

To use an activity from the palette in your workflow, drag and drop it into your workspace.

You have to configure each activity added from the palette before starting the workflow.

![](assets/workflow_palette.png)

## Workspace {#workspace}

The workspace is the central zone in the workflow editor. It is in this zone that you can drop your activities, link them together using transitions, and configure them.

To link two activities, move the end of the arrow from the first activity up to the following activity until they connect. You can also move the activity towards the point of the arrow behind it in order to link it to the preceding activity. If you move any of the activities, they will stay linked.

Transitions following activities that process data contain the intermediary populations. You can access them if you check the **[!UICONTROL Keep interim results]** option in the **[!UICONTROL Execution]** section of the workflow properties.

When an activity is selected, quick actions appear around the activity, allowing you to interact with it. For example, to configure an activity, select it then open it using the ![](assets/edit_darkgrey-24px_table.png) button in the quick actions.

Certain functions are only enabled in the workspace:

* Select several activities and transitions by drawing a zone around them.
* Press **Ctrl** + left click to select several activities and/or transitions.
* Press **Enter** to view the detail of the currently selected activity or transition.
* Press **Delete** to delete the currently selected activity.
* Press **Ctrl + C** to copy the selected activities, and **Ctrl + V** to paste them into the workspace.

![](assets/workflow_workspace.png)

## Action bar {#action-bar}

Depending on the elements selected in the workspace or on the workflow's execution status, the buttons available in the action bar may vary.

<table> 
 <thead> 
  <tr> 
   <th> Button<br /> </th> 
   <th> No selection<br /> </th> 
   <th> Single-selection<br /> </th> 
   <th> Multi-selection<br /> </th> 
   <th> Running<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <img height="21px" src="assets/edit_darkgrey-24px.png" /> <br /> </td> 
   <td> <img height="21px" src="assets/check_blue-12px_table.png" /> <br /> </td> 
   <td> <img height="21px" src="assets/check_blue-12px_table.png" /> <br /> </td> 
   <td> <img height="21px" src="assets/check_blue-12px_table.png" /> <br /> </td> 
   <td> <img height="21px" src="assets/check_blue-12px_table.png" /> <br /> </td> 
   <td> Allows you to edit the workflow's properties.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/play_darkgrey-24px_table.png" /> <br /> </td> 
   <td> <img height="21px" src="assets/check_blue-12px_table.png" /> <br /> </td> 
   <td> <img height="21px" src="assets/check_blue-12px_table.png" /> <br /> </td> 
   <td> <img height="21px" src="assets/check_blue-12px_table.png" /> <br /> </td> 
   <td> </td> 
   <td> Starts the workflow.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/pause_darkgrey-24px_table.png" /> <br /> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> <img height="21px" src="assets/check_blue-12px_table.png" /> <br /> </td> 
   <td> Pauses the workflow.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/stop_darkgrey-24px_table.png" /> <br /> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> <img height="21px" src="assets/check_blue-12px_table.png" /> <br /> </td> 
   <td> Interrupts workflow execution. Cannot be resumed from where it was stopped.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/pauseplay_darkgrey-24px_table.png" /> <br /> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> <img height="21px" src="assets/check_blue-12px_table.png" /> <br /> </td> 
   <td> Restarts the workflow.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/printpreview_darkgrey-24px_table.png" /> <br /> </td> 
   <td> <img height="21px" src="assets/check_blue-12px_table.png" /> <br /> </td> 
   <td> <img height="21px" src="assets/check_blue-12px_table.png" /> <br /> </td> 
   <td> <img height="21px" src="assets/check_blue-12px_table.png" /> <br /> </td> 
   <td> <img height="21px" src="assets/check_blue-12px_table.png" /> <br /> </td> 
   <td> Opens the workflow's execution log.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/checkcircle_darkgrey-24px_table.png" /> <br /> </td> 
   <td> <img height="21px" src="assets/check_blue-12px_table.png" /> <br /> </td> 
   <td> <img height="21px" src="assets/check_blue-12px_table.png" /> <br /> </td> 
   <td> </td> 
   <td> <img height="21px" src="assets/check_blue-12px_table.png" /> <br /> </td> 
   <td> Enables multi-selection mode. The workflow must be made up of at least two activities.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/closecircle_darkgrey-24px_table.png" /> <br /> </td> 
   <td> </td> 
   <td> </td> 
   <td> <img height="21px" src="assets/check_blue-12px_table.png" /> <br /> </td> 
   <td> </td> 
   <td> Disables multi-selection mode.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/targeted.png" /> <br /> </td> 
   <td> </td> 
   <td> <img height="21px" src="assets/check_blue-12px_table.png" /> <br /> </td> 
   <td> </td> 
   <td> </td> 
   <td> Opens the selected transition.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/check_darkgrey-24px_table.png" /> <br /> </td> 
   <td> </td> 
   <td> </td> 
   <td> <img height="21px" src="assets/check_blue-12px_table.png" /> <br /> </td> 
   <td> <img height="21px" src="assets/check_blue-12px_table.png" /> <br /> </td> 
   <td> Re-enables selection if it has previously been disabled or marked as paused.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/check_pause_darkgrey-24px_table.png" /> <br /> </td> 
   <td> </td> 
   <td> </td> 
   <td> <img height="21px" src="assets/check_blue-12px_table.png" /> <br /> </td> 
   <td> <img height="21px" src="assets/check_blue-12px_table.png" /> <br /> </td> 
   <td> Pauses the workflow at the selected activity.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/checkdisable.png" /> <br /> </td> 
   <td> </td> 
   <td> </td> 
   <td> <img height="21px" src="assets/check_blue-12px_table.png" /> <br /> </td> 
   <td> <img height="21px" src="assets/check_blue-12px_table.png" /> <br /> </td> 
   <td> Disables the activity.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/delete_darkgrey-24px_table.png" /> <br /> </td> 
   <td> </td> 
   <td> </td> 
   <td> <img height="21px" src="assets/check_blue-12px_table.png" /> <br /> </td> 
   <td> <img height="21px" src="assets/check_blue-12px_table.png" /> <br /> </td> 
   <td> Deletes the activities that are selected.<br /> </td> 
  </tr> 
  <tr> 
   <td> <br /> </td> 
   <td> </td> 
   <td> </td> 
   <td> <img height="21px" src="assets/check_blue-12px_table.png" /> <br /> </td> 
   <td> <img height="21px" src="assets/check_blue-12px_table.png" /> <br /> </td> 
   <td> Copies the activities that are selected.<br /> </td> 
  </tr> 
  <tr> 
   <td> <br /> </td> 
   <td> <br /> </td> 
   <td> <br /> </td> 
   <td> <img height="21px" src="assets/check_blue-12px_table.png" /> <br /> </td> 
   <td> <img height="21px" src="assets/check_blue-12px_table.png" /> <br /> </td> 
   <td> Pastes the activities that have been copied.<br /> </td> 
  </tr> 
 </tbody> 
</table>

## Quick actions {#quick-actions}

When an activity is selected, quick action buttons appear around the activity, allowing you to interact with it.

<table> 
 <thead> 
  <tr> 
   <th> Button<br /> </th> 
   <th> No selection<br /> </th> 
   <th> Single-selection<br /> </th> 
   <th> Multi-selection<br /> </th> 
   <th> Running<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <img height="21px" src="assets/close_darkgrey-24px_table.png" /> <br /> </td> 
   <td> </td> 
   <td> <img height="21px" src="assets/check_blue-12px_table.png" /> <br /> </td> 
   <td> </td> 
   <td> <img height="21px" src="assets/check_blue-12px_table.png" /> <br /> </td> 
   <td> Disables selecting the activity.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/edit_darkgrey-24px.png" /> <br /> </td> 
   <td> </td> 
   <td> <img height="21px" src="assets/check_blue-12px_table.png" /> <br /> </td> 
   <td> </td> 
   <td> <img height="21px" src="assets/check_blue-12px_table.png" /> <br /> </td> 
   <td> Opens the selected activity.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/copy_24px.png" /> <br /> </td> 
   <td> </td> 
   <td> <img height="21px" src="assets/check_blue-12px_table.png" /> <br /> </td> 
   <td> </td> 
   <td> <img height="21px" src="assets/check_blue-12px_table.png" /> <br /> </td> 
   <td> Copies the selected activity.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/wkf_dlv_act_params_icon.png" /> <br /> </td> 
   <td> </td> 
   <td> <img height="21px" src="assets/check_blue-12px_table.png" /> <br /> </td> 
   <td> </td> 
   <td> <img height="21px" src="assets/check_blue-12px_table.png" /> <br /> </td> 
   <td> Opens the advanced options of the Email or SMS delivery activity selected.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/check_darkgrey-24px_table.png" /> <br /> </td> 
   <td> </td> 
   <td> <img height="21px" src="assets/check_blue-12px_table.png" /> <br /> </td> 
   <td> </td> 
   <td> <img height="21px" src="assets/check_blue-12px_table.png" /> <br /> </td> 
   <td> Re-enables selection if it has previously been disabled or marked as paused.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/check_pause_darkgrey-24px_table.png" /> <br /> </td> 
   <td> </td> 
   <td> <img height="21px" src="assets/check_blue-12px_table.png" /> <br /> </td> 
   <td> </td> 
   <td> <img height="21px" src="assets/check_blue-12px_table.png" /> <br /> </td> 
   <td> Pauses the workflow at the selected activity.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/checkdisable.png" /> <br /> </td> 
   <td> </td> 
   <td> <img height="21px" src="assets/check_blue-12px_table.png" /> <br /> </td> 
   <td> </td> 
   <td> <img height="21px" src="assets/check_blue-12px_table.png" /> <br /> </td> 
   <td> Disables the activity.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/pending_darkgrey-24px_table.png" /> <br /> </td> 
   <td> </td> 
   <td> <img height="21px" src="assets/check_blue-12px_table.png" /> <br /> </td> 
   <td> </td> 
   <td> </td> 
   <td> Forces immediate processing of the selection. This button is only available for the <span class="uicontrol">Scheduler</span> and <span class="uicontrol">Wait</span> activities.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/delete_darkgrey-24px_table.png" /> <br /> </td> 
   <td> </td> 
   <td> <img height="21px" src="assets/check_blue-12px_table.png" /> <br /> </td> 
   <td> </td> 
   <td> <img height="21px" src="assets/check_blue-12px_table.png" /> <br /> </td> 
   <td> Deletes the activities that are selected.<br /> </td> 
  </tr> 
 </tbody> 
</table>

## Duplicating workflow activities {#duplicating-workflow-activities}

The workspace lets you duplicate workflow activities by copy-pasting them into the same workflow, or into another workflow from the same Campaign instance.

Once an activity duplicated, its whole configuration is kept. For delivery activities (Email, SMS, Push Notification...), the delivery object attached to the activity is duplicated.

>[!NOTE]
>
>Workflow activities cannot be duplicated from an instance to another. Activities from technical workflows cannot be duplicated.

To duplicate an activity, follow the steps below:

1. Select the activity, then click the **[!UICONTROL Copy selection]** button from the quick actions.

   You can also use the **Ctrl + C** keyboard shortcut.

   ![](assets/wkf_copypaste1.png)

1. Right-click in the target workflow workspace, then click the **[!UICONTROL Paste]** button.

   You can also use the **CTRL + V** keyboard shortcut.

   ![](assets/wkf_copypaste2.png)

1. The activity is duplicated, with all the settings that have been initially configured.

It is also possible to copy-paste multiple activites, enabling you to duplicate an entire worflow.

To do this, select the activities by drawing a zone around them. then click the **[!UICONTROL Copy selection]** button from the action bar (or press **Ctrl + C**). You can then paste them into the desired location.

![](assets/wkf_copypaste3.png)

