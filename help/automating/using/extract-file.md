---
title: Extract file
seo-title: Extract file
description: Extract file
seo-description: The Extract file activity allows you to export data from Adobe Campaign in the form of an external file.
uuid: a8365187-e7e2-4c2e-a0ad-48339da54be0
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/automating/using/extract-file
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-10T07 28 20.512-0400
cq-lastreplicated: 2018-09-07T15 08 37.155-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: data-management-activities
cq-template: /apps/help/templates/article-3
discoiquuid: 0282a6e5-9cab-43ed-999e-89218c13a133
firstPublishExternalDate: 2018-09-07T15:08:36.885-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 41.622-0400
jcr-createdby: admin
jcr-description: Extract file
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T15:08:36.885-0400
lochandoffdate: 2018-09-10T07 28 20.510-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Extract file
publishexternaldate: 2018-09-07T15 08 36.885-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/automating/using/extract-file.html
sha1: 28139f7f216d1e57341bdfd2418663a8ac54fefc
topicBrowsingSortDate: 2018-09-07T15:08:36.885-0400
index: y
internal: n
snippet: y
---

# Extract file

Extract file

## Description

![](assets/export.png)

The **Extract file** activity allows you to export data from Adobe Campaign in the form of an external file.

## Context of use

The way in which the data will be extracted is defined when configuring the activity.

>[!CAUTION]
>
>The **Extract file** activity must be placed after a **Query** activity in order to be used.

## Configuration

1. Drag and drop an **Extract file** activity into your workflow.

   ![](assets/wkf_data_export1.png)

1. Select the activity, then open it using the  ![](assets/edit_darkgrey-24px.png)

   button from the quick actions that appear.
1. Enter the label of the **Output file**. The label of the file will automatically be completed with the date and time it was created so that it is unique. For example: recipients_20150815_081532.txt for a file generated the 15th of August 2015 at 08:15:32.
1. If you like, you can zip the output file by selecting **Compression** in the **Add a pre-processing step** field. The output file will be compressed into a GZIP file (.gz).
1. Click the  ![](assets/add_darkgrey-24px.png) or **Add an element** button to add an output column.

   ![](assets/wkf_data_export2.png)

   A new window will open.

   ![](assets/wkf_data_export3.png)

1. Enter an expression. To do this, you can select an existing expression or create a new one using the **expression editor**.
1. Confirm your expression.

   The expression is added to the output columns.

1. Create as many columns as you need. You can edit columns by clicking their expressions and labels.

   If you are exporting profiles and want to use them in an external tool, make sure you export a unique identifier. By default, not all profiles have a unique identifier, depending on the way they are added to the database. For more information, refer to the [Generating a unique ID for profiles](../../developing/using/generating-a-unique-id-for-profiles-and-custom-resources.md) section.

1. Click the **File structure** tab to configure the output, date, and number formats for the file that will be exported.

   Check the **Export labels instead of internal values of enumerations** option in case you export enumeration values. This option allows to retrieve shorter labels that are easy to understand instead of IDs.

1. Confirm the configuration of your activity and save your workflow.

## Example

The following example illustrates how to configure an **Extract file** activity after a **Query** activity.

The aim of this workflow is to export a list of profiles in the form of an external file so that the data can be used outside of Adobe Campaign.

1. Drag and drop an **Extract file** activity into your workflow and place it after the **Query** activity.

   In this example, the query is carried out on all profiles aged 18 to 30.

1. Open the Extract file activity to edit it.
1. Name the output file.
1. Add output columns.

   In this example, the email, age, date of birth, first name and last name of the profiles are added as output columns.

   ![](assets/wkf_data_export6.png)

1. Click the **File structure** tab to define:

    * CSV output format
    
      ![](assets/wkf_data_export7.png)

    * Date format
    
      ![](assets/wkf_data_export9.png)

1. Confirm your activity.
1. Drag and drop a **Transfer file** activity after the **Extract file** activity to recover the extract file on an external account.
1. Open the activity and choose the **File upload** action.

   ![](assets/wkf_data_export11.png)

1. Select the external account and enter the path of the folder on the server.

   ![](assets/wkf_data_export12.png)

1. Confirm your activity and save your workflow.
1. Start the workflow.

   When the workflow has been executed correctly, the extracted file is available on the external account.

