---
title: Executing a workflow
seo-title: Executing a workflow
description: Executing a workflow
seo-description: Learn how to execute and monitor a workflow.
uuid: 7c44e7cc-7047-4726-ab13-f2e7fba4ccef
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/automating/using/executing-a-workflow
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-25T09 29 18.262-0400
cq-lastreplicated: 2018-07-23T05 56 54.148-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: workflow-general-operation
cq-template: /apps/help/templates/article-3
discoiquuid: ede5efb6-5df5-4629-a48d-816588c41676
firstPublishExternalDate: 2018-07-23T05:56:54.110-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 52.754-0400
jcr-createdby: admin
jcr-description: Executing a workflow
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T05:56:54.110-0400
lochandoffdate: 2018-07-25T09 29 18.262-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Executing a workflow
publishexternaldate: 2018-07-23T05 56 54.110-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/automating/using/executing-a-workflow.html
sha1: 447f835c415e8dcbdbe26d9ef28eccddc0788d72
topicBrowsingSortDate: 2018-07-23T05:56:54.110-0400
index: y
internal: n
snippet: y
---

# Executing a workflow

Executing a workflow

## About workflow execution

A workflow is always started manually. However, once started, it can remain inactive, depending on the information specified in a [Scheduler](../../automating/using/scheduler.md) activity.

>[!CAUTION]
>
>We recommend that you don't run more than 5 workflows simultaneously. When too many workflows are executed at the same time, the system can run out of resources and become unstable. We also recommend that you spread out your workflows over time.

Execution related actions (start, stop, pause, etc.) are **asynchronous** processes: the command is saved and will become effective once the server is available to apply it.

In a workflow, the result of each activity is generally sent to the following activity via a transition, represented by an arrow.

A transition is unterminated if it is not linked to a destination activity.

![](assets/wkf_execution_1.png)

>[!NOTE]
>
>A workflow containing unterminated transitions can still be executed: a warning message will be generated and the workflow will pause once it reaches the transition, but this will not generate an error. You can also start a workflow without having completely finished the design and you can complete it as you go along.

Once an activity has been executed, the number of records sent in the transition is displayed above it.

![](assets/wkf_transition_count.png)

You can open transitions to check that the data sent is correct during or after executing the workflow. You can view the data and the data structure.

By default, only the details of the last transition of the workflow can be accessed. To be able to access the results of the preceding activities, you need to check the **Keep interim results** option in the **Execution** section of the workflow properties, before starting the workflow.

>[!NOTE]
>
>This option consumes a lot of memory and is designed to help constructing a workflow and ensuring it is correctly configured and behaving. Leave it unchecked on production instances.

When a transition is open, you can edit its **Label** or link a **Segment code** to it. To do this, edit the corresponding fields and confirm your modifications.

## Controlling a workflow from the REST API

Using the REST API, you can **start**, **pause**, **resume** and **stop** a workflow.

You can find more details and examples of REST calls in the [API documentation.](https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#controlling-a-workflow)

## Life cycle

A workflow's life cycle includes three main steps and each step is linked to a status and a color:

* **Editing** (gray)

  This is the initial design phase of a workflow (refer to [Creating a workflow](../../automating/using/building-a-workflow.md#creating-a-workflow)). The workflow is not yet handled by the server and can be modified without any risk.

* **In progress** (blue)

  Once the initial design phase is complete, the workflow can be started and is handled by the server.

* **Finished** (green)

  A workflow is finished once there are no longer any tasks in progress or when an operator has explicitly stopped the instance.

Once it has been started, a workflow may also have two other statuses:

* **Warning** (yellow)

  The workflow could not finish or was paused using the  ![](assets/pause_darkgrey-24px.png) or  ![](assets/check_pause_darkgrey-24px.png)

  buttons.

* **Erroneous** (red)

  An error occurred when a workflow was executed. The workflow was stopped and the user must carry out an action. To find out more about this error, use the  ![](assets/PrintPreview_darkgrey-24px.png) button to access the workflow log (refer to [Monitoring](../../automating/using/executing-a-workflow.md#monitoring)).

The list of marketing activities allows you to display all the workflows as well as their statuses. For more on this, see [Managing marketing activities](../../start/using/marketing-activities.md#about-marketing-activities).

![](assets/wkf_execution_3.png)

## Execution commands

The icons in the action bar allow you to start, track, and modify a workflow's execution. See [Action bar](../../automating/using/workflow-interface.md#action-bar).

![](assets/wkf_execution_2.png)

The actions available are as follows:

**Start**

The  ![](assets/play_darkgrey-24px.png) button starts executing a workflow, which then takes on the **In progress** (blue) status. If the workflow was paused, it is resumed, otherwise it is started and the initial activities are then activated.

>[!NOTE]
>
>Starting is an asynchronous process: the request is saved and will be processed as soon as possible by the workflow execution engine.

**Pause**

The  ![](assets/pause_darkgrey-24px.png) button pauses the execution. The workflow takes on the **Warning** (yellow) status. No new activities will be activated until it is resumed, but operations in progress are not suspended.

**Stop**

The  ![](assets/stop_darkgrey-24px.png) button stops a workflow that is being executed, which will then take on the **Finished** (green) status. The operations in progress are interrupted if possible, and imports or SQL queries in progress are immediately canceled. You cannot resume from the workflow from the same place that it was stopped.

**Restart**

The  ![](assets/pauseplay_darkgrey-24px.png) button involves stopping, then restarting a workflow. In most cases, this allows you to restart quicker. It can also be useful to automate restarting once stopping takes a certain amount of time, because the  ![](assets/play_darkgrey-24px.png)

button is only available when the stop is effective.

When one or multiple activities in a workflow are selected, there are other actions you can carry out, such as:

**Immediate execution**

The  ![](assets/pending_darkgrey-24px.png)

button starts any pending activities selected as soon as possible.

**Normal execution**

The  ![](assets/check_darkgrey-24px.png)

button reactivates any paused or deactivated activities.

**Execution suspended**

The  ![](assets/check_pause_darkgrey-24px.png)

button pauses the workflow at the selected activity: this task as well as all those that follow it (in the same branch) are not executed.

**No execution**

The  ![](assets/checkDisable.png)

button deactivates any selected activities.

>[!NOTE]
>
>Quick actions let you access different actions concerning one particular activity and appear when an activity is selected.

## Monitoring

The  ![](assets/PrintPreview_darkgrey-24px.png)

icon opens the workflow log and task menu.

The workflow history is saved for the duration specified in the workflow execution options (refer to [Workflow properties](../../automating/using/executing-a-workflow.md#workflow-properties)). During this duration, all the messages are therefore saved, even after a restart. If you do not want to save the messages from a previous execution, you have to purge the history by clicking the  ![](assets/delete_darkgrey-24px.png)

button.

The **Log** tab contains the execution history of all the activities or any selected activities. It indexes the operations carried out and execution errors by chronological order.

![](assets/wkf_execution_4.png)

The **Tasks** tab details the execution sequencing of the activities. Click a task to get more information.

![](assets/wkf_execution_5.png)

In these two lists:

* Click the counter to see the total number of activities according to the filter applied. The counter is displayed by default if the number of elements in the list is less than 30.
* The **Configure list** button allows you to choose the information displayed, define the column order, and sort the list.
* You can use filters to find the information you need quicker. Use the search field to look for a specific text in workflow activity names (for example: "query") and logs.

## Error management

When an error occurs, the workflow is paused and the activity that was being executed when the error was encountered flashes red.

The workflow status turns red and the error is recorded in the log.

You can configure the workflow so that it does not pause and continues executing without any errors. To do this, go to the workflow properties via the  ![](assets/edit_darkgrey-24px.png) button and, in the **Execution** section, select the **Ignore** option in the **In case of error** field.

In this case, the erroneous task is aborted. This mode is particularly suited to workflows designed to re-attempt the operation later (periodic actions).

>[!NOTE]
>
>You can apply this configuration individually for each activity. To do this, select an activity and open it using the quick action  ![](assets/edit_darkgrey-24px.png) . Then select the error management mode in the **Execution options** tab. See [Activity execution options](../../automating/using/executing-a-workflow.md#activity-execution-options).

The **Execution** section of the workflow properties also allows you to define a number of **Consecutive errors** that are authorized before the workflow execution is automatically suspended. As long as this number is not reached, the erroneous elements are ignored and the other workflow branches are executed normally. If this number is reached, the workflow is suspended and the workflow supervisors are automatically notified (email and in-app notification). See [Workflow properties](../../automating/using/executing-a-workflow.md#workflow-properties) and [Adobe Campaign notifications](../../administration/using/adobe-campaign-notifications.md).

The supervisors can also be defined in the execution properties of the workflow.

## Workflow properties

To modify a workflow's execution options, use the  ![](assets/edit_darkgrey-24px.png) button to access the workflow properties and select the **Execution** section.

The **Default affinity** field allows you to force a workflow or a workflow activity to execute on a particular machine.

In the **History in days** field, specify the duration after which the history must be purged.

You can choose to check the **Save SQL queries in the log** and **Execute in the engine (do not use in production)** options if necessary.

Check the **Keep interim results** option if you would like to be able to view the detail of transitions. Warning: checking this option may significantly slow down the workflow execution.

The **Severity** field allows you to specify a level of priority for executing workflows in your Adobe Campaign instance. Critical workflows will be executed first.

The **Supervisors** field is where you can define the group of people to notify (email and in-app notification) if the workflow encounters an error. If no group is defined, nobody will be notified. For more on Adobe Campaign notifications, refer to [Adobe Campaign notifications](../../administration/using/adobe-campaign-notifications.md).

The **In case of error** field allows you to specify the action to be carried out should the activity encounter an error. There are two options available for this:

* **Suspend the process**: the workflow is automatically suspended. The workflow status is then **Erroneous** and the color associated turns red. Once the problem is resolved, restart the workflow.
* **Ignore**: the activity is not executed, and as a result neither are any of the activities that follow it (in the same branch). This may prove useful for recurring tasks. If the branch has a scheduler placed upstream, this should trigger on the next execution date.

  By selecting this option, you can also define a number of **Consecutive errors** that are authorized:

    * If the number specified is **0**, or as long as the number specified is not reached, activities that encounter errors are ignored. The other workflow branches are executed normally.
    * If the number specified is reached, the whole of the workflow is suspended and becomes **Erroneous**. If supervisors have been defined, they are automatically notified by an email.

![](assets/wkf_execution_6.png)

## Activity properties

### General properties of an activity

Each activity has a **Properties** tab. This tab allows you to modify the activity's general parameters, particularly the label and the ID. Configuring this tab is optional.

### Managing an activity's outbound transitions

By default, certain activities do not have an outbound transition. You can add one from the **Transitions** tab or from the activity's **Properties** tab to apply other processes to your population in the same workflow.

Depending on the activities, you can add several types of outbound transitions:

* Standard transition: population computed by the activity
* Transition without population: this type of outbound transition can be added to continue the workflow and does not contain any population to not consume any unnecessary space on the system.
* Rejects: population rejected. For example, if the activity's inbound data could not be processed because it was incorrect or incomplete.
* Complement: population remaining after executing the activity. For example, if a segmentation activity is configured to only save a percentage of the inbound population.

If applicable, specify a **Segment code** for the activity's outbound transition. This segment code will allow you to identify where subsets from the target population come from, and may, later on, serve for message personalization purposes.

### Activity execution options

In the activity's properties screen, there is an **Advanced options** tab that lets you define the activity's execution mode and behavior in case of errors.

To access these options, select an activity in a workflow, then open it using the  ![](assets/edit_darkgrey-24px.png)

button from the action bar.

![](assets/wkf_advanced_parameters.png)

The **Execution** field allows you to define the action to be carried out when the task is started. There are three options for this:

* **Normal**: the activity is executed normally. 
* **Enable but do not execute**: the activity is paused, and as a consequence so are any future processes that follow. This can turn out to be useful if you would like to be present when the task is started.
* **Do not enable**: the activity is not executed, and as a consequence, neither are all the activities that follow (in the same branch).

The **In case of error** field allows you to specify the action to be carried out should the activity encounter an error. There are two options available for this:

* **Suspend the process**: the workflow is automatically suspended. The workflow status is then **Erroneous** and the color associated turns red. Once the problem is resolved, restart the workflow.
* **Ignore**: the activity is not executed, and as a result neither are any of the activities that follow it (in the same branch). This may prove useful for recurring tasks. If the branch has a scheduler placed upstream, this should trigger on the next execution date.

The **Behavior** field allows you to define the procedure to follow if asynchronous tasks are used. There are two options available for this:

* **Multiple tasks authorized**: multiple tasks can be executed at the same time even if the first one did not finish.
* **The current task has priority**: once a task is in progress, this takes priority. As long as one task is still in progress, no other task will be executed.

The **Max. execution duration** field allows you to specify a duration such as "30s" or "1h". If the activity is not finished after the duration specified has been elapsed, an alert is triggered. This has no impact on how the workflow functions.

The **Affinity** field allows you to force a workflow or a workflow activity to execute on a particular machine. To do this, you must specify one or several affinities for the workflow or activity in question.

The **Time zone** field allows you to select the time zone of the activity. Adobe Campaign allows you to manage the time differences between multiple countries on the same instance. The setting applied is configured when the instance is created.

The **Comment** field is a free field that allows you to add a note.
