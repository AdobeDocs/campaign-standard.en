---
title: "Workflow use-case: Control group"
seo-title: "Workflow use-case: Control group"
description: "Workflow use-case: Control group"
seo-description: "Workflow use-case: Control group"
page-status-flag: never-activated
uuid: 396a3de1-6ffa-4385-ac9f-15fdeae5a366
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: execution-activities
discoiquuid: 377821e6-69f8-41cc-a1ad-8a2f5ed4d409
context-tags: workflow,use-case,query,segmentation,delivery 
internal: n
snippet: y
---

# Workflow use-case: Building a control group {#building-control-group}

To measure the impact of a delivery, you may want to exclude some profiles from your target so that they will not receive a given message. This control group can be used to make a comparison with the behavior of the target population which received the message.

To do this in Adobe Campaign Standard, you can build a workflow including the following activities:
* A Query activity to target a given population.
* A Segmentation activity to isolate a random control group from this population.
* An Email delivery activity to send a message to the main target, which will be tracked as usual in the sending logs.
* An Update data activity to track the profiles excluded from the target in a custom table, outside the message sending logs.

![](assets/wkf_control-group.png)

## Creating a custom table {#creating-table}

1. From **[!UICONTROL Administration]** > **[!UICONTROL Development]** > **[!UICONTROL Custom Resources]**, click **[!UICONTROL Create]**.
1. Configure the screen definition.
2. Update the database structure to publish the resource.

For more on creating a custom table, see [Key steps to add a resource](../../developing/using/key-steps-to-add-a-resource.md).

## Creating a workflow {#creating-a-workflow}

1. In **[!UICONTROL Marketing Activities]**, click **[!UICONTROL Create]** and select **[!UICONTROL Workflow]**.
1. Select **[!UICONTROL New Workflow]** as workflow type and click **[!UICONTROL Next]**.
1. Enter the properties of the workflow and click **[!UICONTROL Create]**.

## Creating a Query activity {#create-a-query-activity}

1. In **[!UICONTROL Activities]** > **[!UICONTROL Targeting]**, drag and drop a **[!UICONTROL Query activity]**.
1. Double-click the activity to define your target.
1. For example, in **[!UICONTROL Shortcuts]**, drag and drop **[!UICONTROL Profiles]**, select **[!UICONTROL Age]** with the operator **[!UICONTROL Greater than]** and type 25 in the **[!UICONTROL Value]** field.
1. Click **[!UICONTROL Confirm]**.

## Creating a Segmentation activity {#creating-a-segmentation-activity}

1. Drag and drop a **[!UICONTROL Segmentation]** activity and double-click it.
1. In the **[!UICONTROL Segments]** tab, select a segment to edit.
1. In the **[!UICONTROL Configuration]** tab of that segment, select the **[!UICONTROL Limit the population of this segment]** option.

    ![](assets/wkf_control-segment-configuration.png)

1. In the **[!UICONTROL Limitation]** tab, make sure the **[!UICONTROL Random sampling]** option is selected.

    ![](assets/wkf_control-segment-limitation.png)

1. Define a percentage of the initial population, for example 10% and click **[!UICONTROL Confirm]**. The control group will be made up of 10% from the targeted population, selected randomly.
1. In the **[!UICONTROL Advanced options]** tab, select the **[!UICONTROL Generate complement]** option and fill in the **[!UICONTROL Transition label]** and **[!UICONTROL Segment code]** fields.

    ![](assets/wkf_control-segment-advanced.png)

1. Click **[!UICONTROL Confirm]**.

## Creating an Email activity {#creating-an-email-activity}

1. In **[!UICONTROL Activities]** > **[!UICONTROL Channels]**, drag and drop an **[!UICONTROL Email Delivery]** after the main target segment.
1. Click the activity and select ![](assets/edit_darkgrey-24px.png) to edit it.
1. Select **[!UICONTROL Single send email]** and click **[!UICONTROL Next]**.
1. Select an email template and click **[!UICONTROL Next]**.
1. Enter the email properties and click **[!UICONTROL Next]**.
1. To create the layout of your email, click on **[!UICONTROL Use the Email Designer]**.
1. Edit and save your content.
1. In the Schedule section of the message dashboard, unselect the **[!UICONTROL Request confirmation before sending messages}** option.

## Creating an Update data activity {#creating-update-data-activity}

1. Drag and drop an **[!UICONTROL Update data]** activity after the control group segment.
1. Select the activity, then open it using the ![](assets/edit_darkgrey-24px.png) button from the quick actions that appear.
1. In the **[!UICONTROL Identification]** tab, select the custom table that you previously created.

    ![](assets/wkf_control-update-identification.png)

1. In the **[!UICONTROL Fields to update]** tab, specify the fields on which the update will be applied.
1. Click **[!UICONTROL Confirm]**.

Once the workflow is run, the message is sent to the main target and tracked in the sending logs for these profiles. The population of the control group is excluded and its data is exported to the custom table.

You can now compare how the recipients of the message will react compared to the small group who was excluded from the message and did not receive it.

**Related topics:**

* [Publishing a custom resource](../../developing/using/updating-the-database-structure.md#publishing-a-custom-resource)
* [Building a workflow](../../automating/using/building-a-workflow.md)
* [Query activity](../../automating/using/query.md)
* [Segmentation activity](../../automating/using/segmentation.md)
* [Email delivery activity](../../automating/using/email-delivery.md)
* [Monitoring a delivery](../../asending/using/monitoring-a-delivery.md)
