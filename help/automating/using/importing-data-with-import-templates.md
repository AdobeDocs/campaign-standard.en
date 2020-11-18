---
title: Importing data with import templates
description: Learn how to collect data to feed your Campaign database.
page-status-flag: never-activated
uuid: bfc03235-2032-448a-a9ed-21ff2a83fa09
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: importing-and-exporting-data
discoiquuid: fb511bb8-6be7-43f6-86ab-94d5cfa3efc9

---

# Importing data with import templates{#importing-data-with-import-templates}

Importing data allows you to collect data to feed your Campaign's database.

Alternatively to [Workflows](../../automating/using/get-started-workflows.md), Adobe Campaign offers a simplified import function that allows the user to manage certain types of import that were defined by an administrator.

The operating principle is as follows: an **administrator** defines and manages import templates (see [Defining import templates](../../automating/using/importing-data-with-import-templates.md#setting-up-import-templates)). These import templates are then made available to users with simplified views under the **[!UICONTROL Profiles & audiences]** > **[!UICONTROL Imports]** menu.

These users therefore just have to select the type of import they want to carry out and upload the file with the data to import. The workflow defined by the administrator is executed transparently for the user, who can access the details of the result of the import once it has finished.

>[!NOTE]
>
>Import data function can be managed by users with **[!UICONTROL GENERIC IMPORT (import)]** and **[!UICONTROL WORKFLOW (workflow)]** roles. For more on roles, refer to [this section](../../administration/using/list-of-roles.md).

Imports can be filtered according to the template from which they were executed, their execution date, and their execution status.

1. From the imports overview, click the **[!UICONTROL Create]** button. The wizard opens.
1. Select the type of import that you would like to carry out. The import types correspond to the available import templates.
1. If necessary, download the sample file linked to the template to your computer to view the data types expected in the file to be imported.
1. Download the file containing the data to import in the wizard.
1. Start the import. The wizard closes and takes you back to the list of imports carried out with the template used.
1. Refresh your page and select the import that you have just carried out to view the execution detail.

   ![](assets/simplified_import1.png)

The details of the import execution are now available. Both the file that was imported, as well as the file containing the rejected data (data that was not imported), can be downloaded to your computer.

## Setting up import templates {#setting-up-import-templates}

Import templates allow the administrator to pre-define a certain number of technical import configurations. These templates can then be made available to standard users to carry out and upload files.

An import template is defined by the functional administrator and can be managed under the **[!UICONTROL Resources]** > **[!UICONTROL Templates]** > **[!UICONTROL Import templates]** menu.

![](assets/import_template_list.png)

Three default read-only templates are available:

* **[!UICONTROL Update Direct mail quarantines and delivery logs]**: this template can serve as a basis for new imports to update quarantines and delivery logs for Direct mail. The template's workflow contains the following activities: 
* **[!UICONTROL Import data]**: this template can serve as a basis for new imports to insert data from a file into the database. This template's workflow contains the following activities:

    * **[!UICONTROL Load file]**: this activity allows you to upload a file on the Adobe Campaign server.
    * **[!UICONTROL Update data]**: this activity allows you to insert data from the file in the database.

* **[!UICONTROL Import list]**: this template can serve as a basis for new imports to create a **List** type audience from data in a file. This template's workflow contains the following activities:

    * **[!UICONTROL Load file]**: this activity allows you to upload a file on the Adobe Campaign server.
    * **[!UICONTROL Reconciliation]**: this activity allows you to link a targeting dimension to imported data. This then allows you to create a **List** type audience. If the targeting dimension of the imported data is not known, the audience is **File** type. See [Targeting dimensions and resources](../../automating/using/query.md#targeting-dimensions-and-resources).
    * **[!UICONTROL Save audience]**: this activity allows you to save data imported in the form of a **List** type audience. The name of the saved audience corresponds to the name of the file imported by the user, and a suffix specifying the date and time of the import will be added. For example: 'profiles_20150406_151448'.

These default templates are read-only and are not visible to standard users. To create a template that will be available to users, follow these steps:

1. Duplicate a default template. The duplicated template contains three tabs:

    * **[!UICONTROL Properties]**: the import template's general parameters. This tab allows you to enable the template and to upload a sample file.
    * **[!UICONTROL Workflow]**: import workflow. This tab allows you to define the workflow activities. These activities are not visible during simplified imports carried out by users.
    * **[!UICONTROL Executed imports]**: list of imports carried out using this template. You can view the status, details and results of each import that has been carried out using this template. You can directly access the workflow (carried out in a transparent manner for the user) from this list.

1. From the **[!UICONTROL Properties]** tab, rename the template and add a description. Users will be able to view the description when the template is available.

   ![](assets/simplified_import_model1.png)

1. Go to the **[!UICONTROL Workflow]** tab. From here you can enrich the workflow offered by default by adding new activities according to your needs.

   For more on how to configure the workflow activities, refer to the use case describe in this section: [Example: Import workflow template](../../automating/using/creating-import-workflow-templates.md). This use case will help you setting up a workflow that can be reused for importing profiles coming from a CRM in the Adobe Campaign database.

1. Save your template so that the workflow's configuration is correctly taken into account.
1. Upload a sample file from the **[!UICONTROL Properties]** tab. The file uploaded can only have columns necessary for future imports or sample data. Data in the sample file allows you to test the simplified import once the workflow has been defined.

   ![](assets/import_template_sample.png)

   This sample file will then be available for users using the template to carry out an import. They will be able to download it to their computer, for example to fill it with data to import. Make sure to take this into account when adding a sample file.

1. Save your template. The sample file is now taken into account. At any moment you can download it to your computer to check the content, or modify it by checking the **[!UICONTROL Drop a new sample file]** option.

   ![](assets/simplified_import_model2.png)

1. Go back to the **[!UICONTROL Workflow]** tab and open the **[!UICONTROL Load file]** activity to check and adjust the column configuration of the sample file that was uploaded at the previous step.
1. Test the import by starting the workflow. The sample file uploaded at step **5** has to contain data.

   The data from the sample file is then genuinely imported. Please make sure the data used is small and fictitious to ensure that your database is not compromised.

1. Go to the workflow execution log, available in the action bar. If you encounter an error, check that the activities are configured correctly.

   ![](assets/simplified_import_model3.png)

1. In the **[!UICONTROL Properties]** tab, set the **[!UICONTROL Import template status]** to **[!UICONTROL Available]**, then save the template. To stop using this template, you can set the **[!UICONTROL Import template status]** to **[!UICONTROL Archived]**.

The template workflow can be modified by re-uploading the sample file and checking the **[!UICONTROL Load file]** configuration.

The import template is now available for the users and can be used to upload files.

**Related topics:**

* [Workflows](../../automating/using/get-started-workflows.md)
* [Example: Import workflow template](../../automating/using/creating-import-workflow-templates.md)
