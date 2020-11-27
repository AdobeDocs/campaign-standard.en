---
solution: Campaign Standard
product: campaign
title: Creating workflow templates to import data
description: Learn how to create workflow templates to import data.
audience: automating
content-type: reference
topic-tags: workflow-general-operation

---

# Creating workflow templates to import data {#import-workflow-template}

Using an import template is a best practice if you need to regularly import files with the same structure.

This example shows how to pre-set a workflow that can be reused for importing profiles coming from a CRM in the Adobe Campaign database.

1. Create a new workflow template from **[!UICONTROL Resources > Templates > Workflow templates]**.
1. Add the following activities:

    * **[!UICONTROL Load file]**: Define the expected structure of the file containing the data to import.

      >[!NOTE]
      >
      >You can only import data from a single file. If the workflow has multiple **[!UICONTROL Load file]** activities, the same file will be used each time.

    * **[!UICONTROL Reconciliation]**: Reconcile the imported data with database data.
    * **[!UICONTROL Segmentation]**: Create filters to process records differently depending on whether they could be reconciled or not.
    * **[!UICONTROL Deduplication]**: Deduplicate the data from the incoming file before it is inserted in the database.
    * **[!UICONTROL Update data]**: Update the database with the imported profiles.

   ![](assets/import_template_example0.png)

1. Configure the **[!UICONTROL Load file]** activity:

    * Define the expected structure by uploading a sample file. The sample file should contain only a few lines but all the columns necessary for the import. Check and edit the file format to make sure that the type of each column is set correctly: text, date, integer, etc. For example:

      ```
      lastname;firstname;birthdate;email;crmID
      Smith;Hayden;23/05/1989;hayden.smith@mailtest.com;123456
      ```

    * In the **[!UICONTROL File to load]** section, select **[!UICONTROL Upload a new file from the local machine]** and leave the field blank. Each time a new workflow is created from this template, you can specify here the file you want, as long at it corresponds to the defined structure.

      You can use any of the options but you have to modify the template accordingly. For example, if you select **[!UICONTROL Use the file specified in the inbound transition]**, you can add a **[!UICONTROL Transfer file]** activity before to retrieve the file to import from a FTP/SFTP server.

      If you want users to be able to download a file containing errors that occurred during an import, check the **[!UICONTROL Keep the rejects in a file]** option and specify the **[!UICONTROL File name]**.

      ![](assets/import_template_example1.png)

1. Configure the **[!UICONTROL Reconciliation]** activity. The purpose of this activity in this context is to identify the incoming data.

    * In the **[!UICONTROL Relations]** tab, select **[!UICONTROL Create element]** and define a link between the imported data and the recipients targeting dimension (see [Targeting dimensions and resources](../../automating/using/query.md#targeting-dimensions-and-resources)). In this example, the **CRM ID** custom field is used to create the join condition. Use the field or combination of fields you need as long it allows to identify unique records.
    * In the **[!UICONTROL Identification]** tab, leave the **[!UICONTROL Identify the document from the working data]** option unchecked.

   ![](assets/import_template_example2.png)

1. Configure the **[!UICONTROL Segmentation]** activity to retrieve reconciled recipients in one transition and recipients that could not be reconciled but who have enough data in a second transition.

   The transition with reconciled recipients can then be used to update the database. The transition with unknown recipients can then be used to create new recipient entries in the database if a minimum set of information is available in the file.

   Recipients that cannot be reconciled and do not have enough data are selected in a complement outbound transition and can be exported in a separate file or simply ignored.

    * In the **[!UICONTROL General]** tab of the activity, set the **[!UICONTROL Resource type]** to **[!UICONTROL Temporary resource]** and select **[!UICONTROL Reconciliation]** as the targeted set.
    * In the **[!UICONTROL Advanced options]** tab, check the **[!UICONTROL Generate complement]** option to be able to see if any record cannot be inserted in the database. If you need, you can then apply further processing to the complementary data: file export, list update, etc.
    * In the first segment of the **[!UICONTROL Segments]** tab, add a filtering condition on the inbound population to select only records for which the profile's CRM ID is not equal to 0. This way, data from the file that are reconciled with profiles from the database are selected in that subset.

      ![](assets/import_template_example3.png)

    * Add a second segment that selects unreconciled records that have enough data to be inserted in the database. For example: email address, first name and last name. Records that are not reconciled have their profile's CRM ID value equal to 0.

      ![](assets/import_template_example3_2.png)

    * All records that are not selected in the first two subsets are selected in the **[!UICONTROL Complement]**.

1. Configure the **[!UICONTROL Update data]** activity located after the first outbound transition of the **[!UICONTROL Segmentation]** activity configured previously.

    * Select **[!UICONTROL Update]** as **[!UICONTROL Operation type]** since the inbound transition only contains recipients already present in the database.
    * In the **[!UICONTROL Identification]** tab, select **[!UICONTROL Using reconciliation criteria]** and define a key between the **[!UICONTROL Dimension to update]** - Profiles in this case - and the link created in the **[!UICONTROL Reconciliation]** activity. In this example, the **CRM ID** custom field is used.

      ![](assets/import_template_example6.png)

    * In the **[!UICONTROL Fields to update]** tab, indicate the fields from the Profiles dimension to update with the value of the corresponding column from the file. If the names of the file columns are identical or almost identical to the names of the recipients dimension fields, you can use the magic wand button to automatically match the different fields.

      ![](assets/import_template_example6_2.png)

      >[!NOTE]
      >
      >If you plan on sending direct mails to these profiles, make sure to include a postal address as this information is essential to the direct mail provider. Also make sure that the **[!UICONTROL Address specified]** box in your profiles' information is checked. To update this option from a workflow, simply add an element to the fields to update, and specify **1** as **[!UICONTROL Source]** and select the `postalAddress/@addrDefined` field as **[!UICONTROL Destination]**. For more on direct mail and the use of the **[!UICONTROL Address specified]** option, see [this document](../../channels/using/about-direct-mail.md#recommendations).

1. Configure the **[!UICONTROL Deduplication]** activity located after the transition containing unreconciled profiles:

    * In the **[!UICONTROL Properties]** tab, set the **[!UICONTROL Resource type]** to the temporary resource generated from the **[!UICONTROL Reconciliation]** activity of the workflow.

      ![](assets/import_template_example4.png)

    * In this is example, the email field is used to find unique profiles. You can use any field you are sure is filled and part of a unique combination.
    * Choose a **[!UICONTROL Deduplication method]**. In this case, the application decides automatically which records are kept in case of duplicates.

   ![](assets/import_template_example7.png)

1. Configure the **[!UICONTROL Update data]** activity located after the **[!UICONTROL Deduplication]** activity configured previously.

    * Select **[!UICONTROL Insert only]** as **[!UICONTROL Operation type]** since the inbound transition only contains profiles not present in the database.
    * In the **[!UICONTROL Identification]** tab, select **[!UICONTROL Using reconciliation criteria]** and define a key between the **[!UICONTROL Dimension to update]** - Profiles in this case - and the link created in the **[!UICONTROL Reconciliation]** activity. In this example, the **CRM ID** custom field is used.

      ![](assets/import_template_example6.png)

    * In the **[!UICONTROL Fields to update]** tab, indicate the fields from the Profiles dimension to update with the value of the corresponding column from the file. If the names of the file columns are identical or almost identical to the names of the recipients dimension fields, you can use the magic wand button to automatically match the different fields.

      ![](assets/import_template_example6_2.png)

      >[!NOTE]
      >
      >If you plan on sending direct mails to these profiles, make sure to include a postal address as this information is essential to the direct mail provider. Also make sure that the **[!UICONTROL Address specified]** box in your profiles' information is checked. To update this option from a workflow, simply add an element to the fields to update, and specify **1** as **[!UICONTROL Source]** and select the **[postalAddress/@addrDefined]** field as **[!UICONTROL Destination]**. For more on direct mail and the use of the **[!UICONTROL Address specified]** option, see [this document](../../channels/using/about-direct-mail.md#recommendations).

1. After the third transition of the **[!UICONTROL Segmentation]** activity, add a **[!UICONTROL Extract file]** activity and a **[!UICONTROL Transfer file]** activity if you want to keep track of data not inserted in the database. Configure those activities to export the column you need and to transfer the file on a FTP or SFTP server where you can retrieve it.
1. Add an **[!UICONTROL End]** activity and save the workflow template.

The template can now be used and is available for every new workflow. All is needed is then to specify the file containing the data to import in the **[!UICONTROL Load file]** activity.

![](assets/import_template_example9.png)
