---
title: Extract file
description: The Extract file activity allows you to export data from Adobe Campaign in the form of an external file.
page-status-flag: never-activated
uuid: 631f0fbd-9e8d-4f77-a338-fcb7f4fc1774
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: data-management-activities
discoiquuid: a06509f9-4731-4187-b43d-3bfa361284d3
context-tags: fileExport,main
---

# Extract file{#extract-file}

## Description {#description}

![](assets/export.png)

The **[!UICONTROL Extract file]** activity allows you to export data from Adobe Campaign in the form of an external file.

## Context of use {#context-of-use}

The way in which the data will be extracted is defined when configuring the activity.

>[!CAUTION]
>
>The **[!UICONTROL Extract file]** activity must be placed after a **[!UICONTROL Query]** activity in order to be used.

**Related topics:**

* [Use case: Exporting profiles in an external file](../../automating/using/exporting-profiles-in-file.md)

## Configuration {#configuration}

1. Drag and drop an **[!UICONTROL Extract file]** activity into your workflow.

   ![](assets/wkf_data_export1.png)

1. Select the activity, then open it using the ![](assets/edit_darkgrey-24px.png) button from the quick actions that appear.
1. Enter the label of the **Output file**. The label of the file will automatically be completed with the date and time it was created so that it is unique. For example: recipients_20150815_081532.txt for a file generated the 15th of August 2015 at 08:15:32.

   >[!NOTE]
   >
   >It is possible to use the **[!UICONTROL formatDate]** function in this field to specify the file name.

1. If you like, you can zip the output file by selecting **[!UICONTROL Compression]** in the **[!UICONTROL Add a pre-processing step]** field. The output file will be compressed into a GZIP file (.gz).

   The **[!UICONTROL Add a pre-processing step]** field also allows you to encrypt a file before extracting it. For more on how to work with encrypted files, refer to [this section](../../automating/using/managing-encrypted-data.md)

1. Click the ![](assets/add_darkgrey-24px.png) or **[!UICONTROL Add an element]** button to add an output column.

   ![](assets/wkf_data_export2.png)

   A new window will open.

   ![](assets/wkf_data_export3.png)

1. Enter an expression. To do this, you can select an existing expression or create a new one using the **expression editor**.
1. Confirm your expression.

   The expression is added to the output columns.

1. Create as many columns as you need. You can edit columns by clicking their expressions and labels.

   If you are exporting profiles and want to use them in an external tool, make sure you export a unique identifier. By default, not all profiles have a unique identifier, depending on the way they are added to the database. For more information, refer to the [Generating a unique ID for profiles](../../developing/using/configuring-the-resource-s-data-structure.md#generating-a-unique-id-for-profiles-and-custom-resources) section.

1. Click the **[!UICONTROL File structure]** tab to configure the output, date, and number formats for the file that will be exported.

   Check the **[!UICONTROL Export labels instead of internal values of enumerations]** option in case you export enumeration values. This option allows to retrieve shorter labels that are easy to understand instead of IDs.

1. In the **[!UICONTROL Properties]** tab, select the **[!UICONTROL Do not generate a file if the inbound transition is empty]** option to avoid creating and uploading empty files on SFTP servers if the inbound transition is empty.
1. Confirm the configuration of your activity and save your workflow.
