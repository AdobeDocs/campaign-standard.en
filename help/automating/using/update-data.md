---
solution: Campaign Standard
product: campaign
title: Update data
description: The Update data activity allows you to perform a mass update on fields in the database.
audience: automating
content-type: reference
topic-tags: data-management-activities
context-tags: writer,main
feature: Workflows
role: Data Architect
level: Intermediate
---

# Update data{#update-data}

## Description {#description}

![](assets/data_update.png)

The **[!UICONTROL Update data]** activity allows you to perform a mass update on fields in the database.

## Context of use {#context-of-use}

The **Update data** activity can be used after importing a file in order to insert the data recovered into the Adobe Campaign database. Several options allow you to personalize updating the data.

**Related topics:**

* [Use case: Updating data based on a file](../../automating/using/update-database-file.md)
* [Updating data based on an automatic file download](../../automating/using/update-data-automatic-download.md)

## Configuration {#configuration}

1. Drag and drop an **[!UICONTROL Update data]** activity into your workflow.
1. Select the activity, then open it using the ![](assets/edit_darkgrey-24px.png) button from the quick actions that appear.
1. Specify the **[!UICONTROL Operation type]** to be carried out:

    * **[!UICONTROL Insert or update]**: insert data or update it if it the records already exist in the database.
    * **[!UICONTROL Insert only]**: insert data only. The records that already exist are not updated. If reconciliation criteria are defined, only the non-reconciled records will be added.

      Check the **[!UICONTROL Generate an outbound transition for rejects]** box if the data imported contains certain records that already exist in the database to avoid any possible errors.
    
    * **[!UICONTROL Update]**: update data of the records that already exist in the database only.
    * **[!UICONTROL Delete]**: delete data.

   >[!NOTE]
   >
   >The **[!UICONTROL Batch size]** field enables you to define the maximum batch size for the data to upload.

1. In the **[!UICONTROL Identification]** tab, specify how to identify the records in the database:

    * **[!UICONTROL Using the targeting dimension]**: select the **[!UICONTROL Dimension to update]** then specify the **[!UICONTROL Keys for finding records]**. For more this, refer to [Targeting dimensions and resources](../../automating/using/query.md#targeting-dimensions-and-resources).
    * If the data entered matches an existing targeting dimension, select the **[!UICONTROL Using one or more links]** option. Then select the **[!UICONTROL Dimension to update]**.

   If the operation type selected requires an update, you must use reconciliation keys.

1. In the **[!UICONTROL Fields to update]** tab, specify the fields on which the update will be applied and, if necessary, add conditions so that this update is carried out. To do this, use the **[!UICONTROL Taken into account if]** column. The conditions are applied one after the other in list order. Use the arrows on the right to change the order of the updates. You can use the same destination field multiple times.

   You can automatically link fields using the ![](assets/wkf_magic_wand-24px.png) button. Automatic linking detects fields with the same name.

   During an **[!UICONTROL Insert or update]** type operation, you can individually select the operation to apply for each field. To do this, select the value you would like in the **[!UICONTROL Operation]** column.

   >[!NOTE]
   >
   >**Managing updates** The **[!UICONTROL lastModified]**, **[!UICONTROL modifiedBy]**, **[!UICONTROL created]** and **[!UICONTROL createdBy]** fields are automatically updated when an update data activity is run, unless their configuration is explicitly carried out on the field update table. The update is only carried out on the records where at least one difference has been detected. If the values are the same, no update is carried out.

1. If needed, manage the activity's [Transitions](../../automating/using/activity-properties.md) to access the advanced options for the outbound population.

   If you have selected **[!UICONTROL Insert only]** and the data imported may contain records that are already present in the database, check the **[!UICONTROL Generate an outbound transition for the rejects]** box to avoid any possible errors.

1. Confirm the configuration of your activity and save your workflow.
