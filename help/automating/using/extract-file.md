---
title: Extract file
seo-title: Extract file
description: Extract file
seo-description: The Extract file activity allows you to export data from Adobe Campaign in the form of an external file.
uuid: d50c9ca6-9b94-4efa-a1c8-3401e8de0c23
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: data-management-activities
discoiquuid: c16c5285-48eb-4010-879f-a14aa646f586
isreadyforlocalization: false
index: y
internal: n
snippet: y
---

# Extract file{#extract-file}

Extract file

## Description {#description}

![](assets/export.png)

The **[!UICONTROL Extract file]** activity allows you to export data from Adobe Campaign in the form of an external file.

## Context of use {#context-of-use}

The way in which the data will be extracted is defined when configuring the activity.

>[!CAUTION]
>
>The **[!UICONTROL Extract file]** activity must be placed after a **[!UICONTROL Query]** activity in order to be used.

## Configuration {#configuration}

1. Drag and drop an **[!UICONTROL Extract file]** activity into your workflow.

   ![](assets/wkf_data_export1.png)

1. Select the activity, then open it using the  ![](assets/edit_darkgrey-24px.png)

   button from the quick actions that appear.
1. Enter the label of the **Output file**. The label of the file will automatically be completed with the date and time it was created so that it is unique. For example: recipients_20150815_081532.txt for a file generated the 15th of August 2015 at 08:15:32.
1. If you like, you can zip the output file by selecting **[!UICONTROL Compression]** in the **[!UICONTROL Add a pre-processing step]** field. The output file will be compressed into a GZIP file (.gz).
1. Click the  ![](assets/add_darkgrey-24px.png) or **[!UICONTROL Add an element]** button to add an output column.

   ![](assets/wkf_data_export2.png)

   A new window will open.

   ![](assets/wkf_data_export3.png)

1. Enter an expression. To do this, you can select an existing expression or create a new one using the **expression editor**.
1. Confirm your expression.

   The expression is added to the output columns.

1. Create as many columns as you need. You can edit columns by clicking their expressions and labels.

   If you are exporting profiles and want to use them in an external tool, make sure you export a unique identifier. By default, not all profiles have a unique identifier, depending on the way they are added to the database. For more information, refer to the [Generating a unique ID for profiles](../../developing/using/generating-a-unique-id-for-profiles-and-custom-resources.md) section.

1. Click the **[!UICONTROL File structure]** tab to configure the output, date, and number formats for the file that will be exported.

   Check the **[!UICONTROL Export labels instead of internal values of enumerations]** option in case you export enumeration values. This option allows to retrieve shorter labels that are easy to understand instead of IDs.

1. In the **[!UICONTROL Properties]** tab, select the **[!UICONTROL Do not generate a file if the inbound transition is empty]** option to avoid creating and uploading empty files on SFTP servers if the inbound transition is empty.
1. Confirm the configuration of your activity and save your workflow.

## Example {#example}

The following example illustrates how to configure an **[!UICONTROL Extract file]** activity after a **[!UICONTROL Query]** activity.

The aim of this workflow is to export a list of profiles in the form of an external file so that the data can be used outside of Adobe Campaign.

1. Drag and drop an **[!UICONTROL Extract file]** activity into your workflow and place it after the **[!UICONTROL Query]** activity.

   In this example, the query is carried out on all profiles aged 18 to 30.

1. Open the Extract file activity to edit it.
1. Name the output file.
1. Add output columns.

   In this example, the email, age, date of birth, first name and last name of the profiles are added as output columns.

   ![](assets/wkf_data_export6.png)

1. Click the **[!UICONTROL File structure]** tab to define:

    * CSV output format
    
      ![](assets/wkf_data_export7.png)

    * Date format
    
      ![](assets/wkf_data_export9.png)

1. Confirm your activity.
1. Drag and drop a **[!UICONTROL Transfer file]** activity after the **[!UICONTROL Extract file]** activity to recover the extract file on an external account.
1. Open the activity and choose the **[!UICONTROL File upload]** action.

   ![](assets/wkf_data_export11.png)

1. Select the external account and enter the path of the folder on the server.

   ![](assets/wkf_data_export12.png)

1. Confirm your activity and save your workflow.
1. Start the workflow.

   When the workflow has been executed correctly, the extracted file is available on the external account.

