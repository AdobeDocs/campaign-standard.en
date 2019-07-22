---
title: Transfer file
seo-title: Transfer file
description: Transfer file
seo-description: The Transfer file activity allows you to receive or send files, test whether there are files present, or list files in Adobe Campaign.
page-status-flag: never-activated
uuid: a2f18118-b681-4310-aee0-9e82179d2032
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: data-management-activities
discoiquuid: 752f2aed-f897-485e-b329-f3cc1756ee8e
context-tags: fileTransfer,main
internal: n
snippet: y
---

# Transfer file{#transfer-file}

## Description {#description}

![](assets/file_transfer.png)

The **[!UICONTROL Transfer file]** activity allows you to receive or send files, test whether there are files present, or list files in Adobe Campaign.

## Context of use {#context-of-use}

The way in which the data will be extracted is defined when the activity is configured. The file to load may be a list of contacts, for example.

You can use this activity to recover data that will then be structured with the **[!UICONTROL Load file]** activity.

## Configuration {#configuration}

1. Drop a **[!UICONTROL Transfer file]** activity into your workflow.
1. Select the activity, then open it using the ![](assets/edit_darkgrey-24px.png) button from the quick actions that appear.
1. Use the drop-down list in the **[!UICONTROL Action]** field to select one of the following activity actions:

   ![](assets/wkf_file_transfer_01.png)

    * **File download**: allows you to download a file.
    * **File upload**: allows you to upload a file. Uploading a file from Adobe Campaign file generates a log entry in the **[!UICONTROL Export audits]** menu. For more information on export audits, refer to the [Auditing exports](../../administration/using/auditing-export-logs.md) section.
    * **Test to see if file exists**: allows you to check whether there is a file.
    * **File listing**: allows you to list the files present in Adobe Campaign.

   Depending on the action selected, one or several protocols are available:

    * **HTTP**: this protocol allows you to start downloading a file from an external account or from a URL.

        * Click the **[!UICONTROL Use connection parameters defined in an external account]** option, then select the account you would like and specify the path of the file to download.
        
          ![](assets/wkf_file_transfer_03.png)

        * Click the **[!UICONTROL Quick configuration]** option, then enter the URL in the field that appears.
        
          ![](assets/wkf_file_transfer_04.png)

    * **S3**: this protocol allows you to start downloading a file from a URL or an external account via Amazon Simple Storage Service (S3).

        * Select the external account and specify the path of the file to download.
        
          ![](assets/wkf_file_transfer_08.png)

    * **SFTP**: this protocol allows you to start downloading a file from a URL or an external account.

        * Click the **[!UICONTROL Use connection parameters defined in an external account]** option, then select the account you would like and specify the path of the file to download.
        
          ![](assets/wkf_file_transfer_07.png)

          >[!CAUTION]
          >
          >Wildcards are supported.

        * Click the **[!UICONTROL Quick configuration]** option, then enter the URL in the field that appears.
        * If you want to sort the imported files, select the **[!UICONTROL Sort alphanumerically]** option from the **[!UICONTROL Additional options]** section. The files will then be processed in a sequential order.
        
          ![](assets/wkf_file_transfer_sort.png)

    * **File(s) present on the Adobe Campaign server**: this protocol corresponds to the repository containing the file(s) to recover.

      Metacharacters, or wildcards (for example &#42; or ?) can be used to filter files.

      Fill in this field and confirm your activity to use this protocol.

      >[!NOTE]
      >
      >The path must be relative to the storage space directory of the Adobe Campaign server. Files are located in the **sftp&lt;yourinstancename&gt;/ **directory. You also cannot browse the directories above the storage space. For example: **user&lt;yourinstancename>/my_recipients.csv** is correct. **../hello/my_recipients.csv** is incorrect. **//myserver/hello/myrecipients.csv** is incorrect.

   Select your protocol and complete the associated fields.

   The **[!UICONTROL Use a dynamic file path]** option, available for each protocol, lets you use a standard expression and events variables to personalize the name of the file to transfer. For more on this, refer to the [Customizing activities with events variables](../../automating/using/calling-a-workflow-with-external-parameters.md#customizing-activities-with-events-variables) section.

1. The **[!UICONTROL Additional options]** section, available depending on the protocol selected, allows you to add parameters to your protocol. You can:

    * **[!UICONTROL Delete the source files after transfer]** 
    * **[!UICONTROL Disable passive mode]** 
    * **[!UICONTROL List all files]**: this option is available when selecting the **[!UICONTROL File listing]** action. It allows you to index all the files present on the server in the **vars.filenames** event variable in which the file names are separated by the **'n'** characters.

1. The **[!UICONTROL If no files are found]** section of the **[!UICONTROL Advanced options]** tab allows you to configure specific actions if any errors or inexistent files are detected when the activity is started.

   You can also define retries. The different retries appear in the workflow execution log.

   ![](assets/wkf_file_transfer_09.png)

1. Confirm the configuration of your activity and save your workflow.

## Historization settings {#historization-settings}

Every time a **[!UICONTROL Transfer file]** activity is executed, it stores the uploaded or downloaded files in a dedicated folder. One folder is created for each **[!UICONTROL Transfer file]** activity of a workflow. Therefore, it is important to be able to limit the size of this folder in order to preserve physical space on the server.

To do that, you can define **[!UICONTROL Historization settings]** in the **[!UICONTROL Advanced options]** of the **[!UICONTROL Transfer File]** activity.

**[!UICONTROL Historization settings]** allow to define a maximum number of files or total size for the activity's folder. By default, 100 files and 50 MB are authorized.

Every time the activity is executed, the folder is checked as follows:

* Only files created more than 24 hours before the execution of the activity are taken into account.
* If the number of files taken into account is greater than the value of the **[!UICONTROL Maximum number of files]** parameter, the oldest files are deleted until the **[!UICONTROL Maximum number of files]** allowed is reached.
* If the total size of files taken into account is greater than the value of the **[!UICONTROL Maximum size (in MB)]** parameter, the oldest files are deleted until the **[!UICONTROL Maximum size (in MB)]** allowed is reached.

>[!NOTE]
>
>If the activity is not executed again, its folder will not be checked nor purged. With this in mind, be cautious when transferring large files.

## Example {#example}

The following example shows the configuration of a **File transfer** activity which will then be followed by a **Load file** activity then an **Update data** activity. The goal of this workflow is to add or update the Adobe Campaign database profiles with the data recovered by the workflow.

1. Drag and drop a **Transfer file** activity into your workflow.
1. Select the activity, then open it using the ![](assets/edit_darkgrey-24px.png) button from the quick actions that appear.
1. In the **[!UICONTROL Protocol]** tab, select **SFTP**.
1. Select the **Use connection parameters defined in an external account** option.
1. Enter the name of the external account.
1. Enter the **File path on the remote server**.

   ![](assets/wkf_file_transfer_07.png)

1. Confirm your activity and save your workflow.

