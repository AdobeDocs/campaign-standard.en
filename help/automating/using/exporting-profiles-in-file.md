---
title: Exporting profiles in an external file
description: This use case shows how to export a list of profiles in the form of an external file so that the data can be used outside of Adobe Campaign.
page-status-flag: never-activated
uuid: 631f0fbd-9e8d-4f77-a338-fcb7f4fc1774
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: data-management-activities
discoiquuid: a06509f9-4731-4187-b43d-3bfa361284d3
context-tags: fileExport,main
internal: n
snippet: y
---

# Exporting profiles in an external file {#exporting-profiles-external-file}

The following example illustrates how to configure an **[!UICONTROL Extract file]** activity after a **[!UICONTROL Query]** activity.

The aim of this workflow is to export a list of profiles in the form of an external file so that the data can be used outside of Adobe Campaign.

1. Drag and drop an [Extract file](../../automating/extract-file.md) activity into your workflow and place it after the [Query](../../automating/query.md) activity.

   In this example, the query is carried out on all profiles aged 18 to 30.

1. Open the **[!UICONTROL Extract file]** activity to edit it.
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
1. Drag and drop a [Transfer file](../../automating/transfer-file.md) activity after the **[!UICONTROL Extract file]** activity to recover the extract file on an external account.
1. Open the activity and choose the **[!UICONTROL File upload]** action.

   ![](assets/wkf_data_export11.png)

1. Select the external account and enter the path of the folder on the server.

   ![](assets/wkf_data_export12.png)

1. Confirm your activity and save your workflow.
1. Start the workflow.

   When the workflow has been executed correctly, the extracted file is available on the external account.
