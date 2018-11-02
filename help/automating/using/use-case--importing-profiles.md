---
title: Use case: Importing profiles
seo-title: Use case: Importing profiles
description: Use case: Importing profiles
seo-description: 
page-status-flag: never-activated
uuid: dc90fce0-f140-4063-aa01-b4d1e62a667c
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/automating/using/use-case--importing-profiles
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-01-10T15 19 36.184-0500
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: importing-and-exporting-data
cq-template: /apps/help/templates/article-3
discoiquuid: e05f9930-e029-4a84-ad25-b693e4248322
firstPublishExternalDate: 2018-01-10T15:19:36.178-0500
herogradient: light
jcr-created: 2018-01-11T19 01 28.220-0500
jcr-createdby: admin
jcr-description: Use case  Importing profiles
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-01-10T15:19:36.178-0500
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Use case: Importing profiles
publishexternaldate: 2018-01-10T15 19 36.178-0500
publishExternalURL: https://helpx.adobe.com/campaign/standard/automating/using/use-case--importing-profiles.html
sha1: 03e0d4d503f0dd7d47ef1b57a904623bfeade5cc
topicBrowsingSortDate: 2018-01-10T15:19:36.178-0500
index: y
internal: n
snippet: y
---

# Use case: Importing profiles

Use case: Importing profiles

Learn how to import profiles with this example.

## About this use case

You would like to add new client profiles to your Adobe Campaign instance. You have a flat structure file (.txt for example) that contains the list of these profiles and their data (first name, last name, email, etc.).

To enrich your instance with this data, you can use an **Extract Transform Load** type workflow which allows you to import this data.

The different stages of this use case are:

* [Step 1: Create the workflow](../../automating/using/use-case--importing-profiles.md#step-1--create-the-workflow)
* [Step 2: Add a Transfer file activity](../../automating/using/use-case--importing-profiles.md#step-2--add-a-transfer-file-activity)
* [Step 3: Add a Load file activity](../../automating/using/use-case--importing-profiles.md#step-3--add-a-load-file-activity)
* [Step 4: Add an Update data activity](../../automating/using/use-case--importing-profiles.md#step-4--add-an-update-data-activity)
* [Step 5: Execute the workflow](../../automating/using/use-case--importing-profiles.md#step-5--execute-the-workflow)

**Pre-requisites**:

* You need to have the right to execute workflows. See [Roles](../../administration/using/list-of-roles.md) and [List of authorizations](../../administration/using/list-of-authorizations.md).
* You need a configured external account to transfer the source file containing the profile data via FTP. See [External accounts](../../administration/using/external-accounts.md).

**Related topics**:

* [Building a workflow](../../automating/using/building-a-workflow.md)
* [Executing a workflow](../../automating/using/executing-a-workflow.md)
* [About data management activities](../../automating/using/about-data-management-activities.md)
* [Importing profiles with a workflow](https://docs.campaign.adobe.com/doc/standard/en/Videos/importing_profiles.mp4) video

## Step 1: Create the workflow

You can create a workflow from a program, a campaign, or the marketing activity list. For more on this, refer to the [Creating a workflow](../../automating/using/building-a-workflow.md#creating-a-workflow) section.

## Step 2: Add a Transfer file activity

Once you have created your workflow, add a **Transfer file** file activity to upload the source file containing the profile data.

1. In the workflow created previously, go to the **Activities &gt; Data management ** menu, select the **Transfer file** activity, then drag and drop it into your workflow.

   ![](assets/wkf_etl_03.png)

1. Open the activity by double-clicking its icon.
1. Select **File download** as the action and **FTP** for the protocol.
1. Select the **Use connection parameters defined in an external account** option so that you can specify the external account configurations.

   >[!NOTE]
   >
   >The external account configuration must be carried out by the administrator of your Adobe Campaign instance.

   Select the account from the drop-down list.

1. In the **File path on the remote server** field, enter the path of the file to be retrieved.

   ![](assets/wkf_etl_09.png)

1. **If no files are found**, select the **Generate an error** option. The workflow will be stopped if Adobe Campaign does not detect a source file.
1. Confirm your activity and save your workflow.

The **Transfer file** activity is configured to recover your source file via the FTP protocol.

**Related topic**:

[Transfer file](../../automating/using/transfer-file.md)

## Step 3: Add a Load file activity

Right after the **Transfer file** activity, place a **Load file** activity to structure the uploaded file's data.

1. Go to the **Activities &gt; Data management** menu and add a **Load file** activity after the **Transfer file** activity in your workflow.

   ![](assets/wkf_etl_05.png)

1. Open the activity by double-clicking its icon.
1. In the **Execution &gt; File to load** tab, select the **Use the file specified in the inbound transition** option.

   By selecting this option, you are letting Adobe Campaign know that you would like to use the data in the file that will have been downloaded once the **Transfer file** activity is executed. 

1. Drag and drop a file in the space provided to define the structure of the file that will be downloaded by the workflow. This can be the same file that was used in the **Transfer file** activity.

   ![](assets/wkf_etl_10.png)

1. The **File structure** is automatically detected by Adobe Campaign. You can check it by clicking the corresponding tab and selecting the **File format** category.
1. In the **Column definition** tab, check whether the column processing has been carried out correctly by Adobe Campaign. If necessary, click the data to edit it.

   ![](assets/wkf_etl_12.png)

1. Confirm your activity and save your workflow.

The **Load file** activity is now configured to make the data in the file downloaded by the **Transfer file** activity available in a structured way.

**Related topic**:

[Load file](../../automating/using/load-file.md)

## Step 4: Add an Update data activity

Right after the **Load file** activity, place a **Update data** activity to insert the profile data into the Adobe Campaign database.

1. Go to the **Activities &gt; Data management** menu and add an **Update data** activity after the **Load file** activity in your workflow.

   ![](assets/wkf_etl_07.png)

1. Open the activity by double-clicking its icon and select the **Insert or update** operation type.
1. Leave the **Dimension to update** as **Profiles** and click the  ![](assets/add_darkgrey-24px.png) or **Add an element** button to add a new reconciliation key.

   >[!NOTE]
   >
   >This key will be used by Adobe Campaign when importing the file, to identify any profiles that are already in the instance.

1. In the **Source expression** category of the window that appears, click the **Select an expression** button.
1. Choose the name of the **email** column in the data to import and confirm.
1. For the **Destination** category, select the name of the column that corresponds to the column chosen during step 7, then confirm the reconciliation key.

   Adobe Campaign will use the email of any identified profiles to verify whether they are already present in the instance, and if this is the case, it will update them if necessary.

   ![](assets/wkf_etl_14.png)

1. In the **Fields to update** tab, click the  ![](assets/add_darkgrey-24px.png) button **Add an element** to add fields that will be updated when the workflow is started.

   Select the source expression, namely the label of a source file column.

   ![](assets/wkf_etl_18.png)

   Select a destination, namely the label of the field to update in the dimension selected in Adobe Campaign.

   ![](assets/wkf_etl_19.png)

   Click **Add**.

1. You will need to repeat this operation for every field in your source file that you would like to recover.

   ![](assets/wkf_etl_20.png)

1. Confirm your activity and save your workflow.

Your workflow is now completely configured.

**Related topic**:

[Update data](../../automating/using/update-data.md)

## Step 5: Execute the workflow

### Starting the workflow

Now that your workflow is configured, you have to start it to recover the data in your source file and enrich your Adobe Campaign instance.

1. Start your workflow by clicking the **Start** button in the action bar.

   ![](assets/wkf_etl_22.png)

   Adobe Campaign executes your workflow.

1. If an error is encountered while it is executing, click the activity that has encountered the error then click the **Workflow log and tasks** button to view the log entries and find out exactly which error occurred on this activity.

**Related topic**:

[Executing a workflow](../../automating/using/executing-a-workflow.md)

### Verifying the data

Once the workflow has finished executing, you can check whether the data has been correctly imported.

1. Navigate within Adobe Campaign to view the list of **Profiles**.
1. Use the **Search** function to find any profiles present in your source file.

   ![](assets/wkf_etl_26.png)

The profiles were imported correctly by the workflow. You can now integrate them into an audience, or send them emails.

**Related topic**:

[Managing audiences](../../audiences/using/about-audiences.md)
