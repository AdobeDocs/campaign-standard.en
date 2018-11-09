---
title: Workflow interface
seo-title: Workflow interface
description: Workflow interface
seo-description: Learn the interface and options to create, edit and execute a workflow.
uuid: 45ab21e1-892e-413e-9101-4d4d266cc9b3
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/automating/using/workflow-interface
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-10T07 22 33.778-0400
cq-lastreplicated: 2018-09-07T14 44 41.605-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: about-workflows-and-data-management
cq-template: /apps/help/templates/article-3
discoiquuid: 0880642f-09e1-42ef-ac3f-5305a65600fb
firstPublishExternalDate: 2018-09-07T14:44:39.260-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 01 21.688-0400
jcr-createdby: admin
jcr-description: Workflow interface
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T14:44:39.260-0400
lochandoffdate: 2018-09-10T07 22 33.776-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Workflow interface
publishexternaldate: 2018-09-07T14 44 39.260-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/automating/using/workflow-interface.html
sha1: b864320521f3ff1447999c086b3e3ea994f9bd10
topicBrowsingSortDate: 2018-09-07T14:44:39.260-0400
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

Transitions following activities that process data contain the intermediary populations. You can access them if you check the **Keep interim results** option in the **Execution** section of the workflow properties.

When an activity is selected, quick actions appear around the activity, allowing you to interact with it. For example, to configure an activity, select it then open it using the  ![](assets/edit_darkgrey-24px_table.png)

button in the quick actions.

Certain functions are only enabled in the workspace:

* Select several activities and transitions by drawing a zone around them.
* Press **Ctrl** + left click to select several activities and/or transitions.
* Press **Enter** to view the detail of the currently selected activity or transition.
* Press **Delete** to delete the currently selected activity.

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
   <td> <img height="21px" src="assets/PrintPreview_darkgrey-24px_table.png" /> <br /> </td> 
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
   <td> <img height="21px" src="assets/checkDisable.png" /> <br /> </td> 
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
   <td> <img height="21px" src="assets/checkDisable.png" /> <br /> </td> 
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
   <td> Forces immediate processing of the selection. This button is only available for the <strong>Scheduler</strong> and <strong>Wait</strong> activities.<br /> </td> 
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

