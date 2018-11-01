---
title: Using import templates
seo-title: Using import templates
description: Using import templates
seo-description: Import templates allow to reduce the settings needed and to import data faster.
page-status-flag: de-activated
uuid: 2b744e87-4f77-4eb7-b38c-d32eb6ecfeb1
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/automating/using/using-import-templates
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-03-26T06 13 55.101-0400
cq-lastreplicated: 2018-03-26T06 13 55.132-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Deactivate
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: importing-and-exporting-data
cq-template: /apps/help/templates/article-3
discoiquuid: b1b27966-7122-40a3-8d23-81a1a5c5c082
firstPublishExternalDate: 2018-02-15T06:14:48.508-0500
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 33.818-0400
jcr-createdby: admin
jcr-description: Using import templates
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-02-15T06:14:48.508-0500
lochandoffdate: 2018-03-14T17 34 30.034-0400
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Using import templates
sha1: 0136ab6517aae4429f9a44f08b3488e50a3868de
unpublishexternaldate: 2018-03-26T06 13 55.094-0400
index: y
internal: n
snippet: y
---

# Using import templates

Using import templates

## <p>About import templates</p>

Alternatively to [Workflows](../../automating/using/discovering-workflows.md), Adobe Campaign offers a simplified import function that allows the user to manage certain types of import that were defined by an administrator.

The operating principle is as follows: an **administrator** defines and manages import templates. These import templates are then made available to users with simplified views. These users therefore just have to select the type of import they want to carry out and upload the file with the data to import. The workflow defined by the administrator is executed transparently for the user, who can access the details of the result of the import once it has finished.

Two default templates are available as read-only:

* **Import data**: this template can serve as a basis for new imports to insert data from a file into the database. This template's workflow contains the following activities:

    * **Load file**: this activity allows you to upload a file on the Adobe Campaign server.
    * **Update data**: this activity allows you to insert data from the file in the database.

* **Import list**: this template can serve as a basis for new imports to create a **List** type audience from data in a file. This template's workflow contains the following activities:

    * **Load file**: this activity allows you to upload a file on the Adobe Campaign server.
    * **Reconciliation**: this activity allows you to link a targeting dimension to imported data. This then allows you to create a **List** type audience. If the targeting dimension of the imported data is not known, the audience is **File** type. See [Targeting dimensions and resources](../../automating/using/query.md#targeting-dimensions-and-resources).
    * **Save audience**: this activity allows you to save data imported in the form of a **List** type audience. The name of the saved audience corresponds to the name of the file imported by the user, and a suffix specifying the date and time of the import will be added. For example: 'profiles_20150406_151448'.

## <p>Defining import templates</p>

Import templates allow the administrator to pre-define a certain number of technical import configurations. These templates can then be made available to standard users to carry out and upload files.

An import template is defined by the functional administrator and can be managed under the **Resources** &gt; **Templates** &gt; **Import templates** menu.

1. Duplicate a default template. The duplicated template contains three tabs:

    * **Properties**: the import template's general parameters. This tab allows you to enable the template and to upload a sample file.
    * **Workflow**: import workflow. This tab allows you to define the workflow activities. These activities are not visible during simplified imports carried out by users.
    * **Executed imports**: list of imports carried out using this template. You can view the status, details and results of each import that has been carried out using this template. You can directly access the workflow (carried out in a transparent manner for the user) from this list.

   ![](assets/simplified_import_model1.png)

1. From the **Properties** tab, rename the template and add a description. Users will be able to view the description when the template is available.
1. Go to the **Workflow** tab. From here you can enrich the workflow offered by default by adding new activities according to your needs.

   The workflow must have a **Load file** activity. Do not upload a file directly in this activity.

   If you want users to be able to download a file containing errors that occurred during an import, check the **Keep the rejects in a file** option in the **Load file** activity and specify the **File name**.

   You can only import data from a single file. If the workflow has multiple **Load file** activities, the same file will be used each time.

1. Save your template so that the workflow's configuration is correctly taken into account.
1. Upload a sample file from the **Properties** tab. The file uploaded can only have columns necessary for future imports or sample data. Data in the sample file allows you to test the simplified import once the workflow has been defined.

   This sample file will then be available for users using the template to carry out an import. They will be able to download it to their computer, for example to fill it with data to import. Make sure to take this into account when adding a sample file.

1. Save your template. The sample file is now taken into account. At any moment you can download it to your computer to check the content, or modify it by checking the **Drop a new sample file** option.

   ![](assets/simplified_import_model2.png)

1. Go back to the **Workflow** tab and open the **Load file** activity to check and adjust the column configuration of the sample file that was uploaded at the previous step.
1. Test the import by starting the workflow. The sample file uploaded at step **5** has to contain data.

   The data from the sample file is then genuinely imported. Please make sure the data used is small and fictitious to ensure that your database is not compromised.

1. Go to the workflow execution log, available in the action bar. If you encounter an error, check that the activities are configured correctly.

   ![](assets/simplified_import_model3.png)

1. In the **Properties** tab, set the **Import template status** to **Available**, then save the template. To stop using this template, you can set the **Import template status** to **Archived**.

The template workflow can be modified by re-uploading the sample file and checking the **Load file** configuration.

The import template is now available for the users and can be used to upload files.

**Related topics:**

* [Workflows](../../automating/using/discovering-workflows.md)
* [Importing data](../../automating/using/importing-data.md)

## <p>Importing data</p>

Importing data allows you to collect data to feed your Campaign's database.

Import data function can be managed by users with **GENERIC IMPORT (import)** and **WORKFLOW (workflow)** roles under the **Profiles & audiences** &gt; **Imports** menu. This menu offers a simple way to import data, using import templates defined by an administrator.

Imports can be filtered according to the template from which they were executed, their execution date, and their execution status.

1. From the imports overview, click the **Create** button. The wizard opens.
1. Select the type of import that you would like to carry out. The import types correspond to the available import templates.
1. If necessary, download the sample file linked to the template to your computer to view the data types expected in the file to be imported.
1. Download the file containing the data to import in the wizard.
1. Start the import. The wizard closes and takes you back to the list of imports carried out with the template used.
1. Refresh your page and select the import that you have just carried out to view the execution detail.

   ![](assets/simplified_import1.png)

The details of the import execution are now available. Both the file that was imported, as well as the file containing the rejected data (data that was not imported), can be downloaded to your computer.

**Related topic:**

[Roles](../../administration/using/list-of-roles.md)
