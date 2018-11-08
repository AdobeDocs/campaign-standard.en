---
title: Update data
seo-title: Update data
description: Update data
seo-description: The Update data activity allows you to perform a mass update on fields in the database.
uuid: 31f1dee0-0a1f-4434-994c-2a77e9ba0c35
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/automating/using/update-data
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-10T07 27 43.993-0400
cq-lastreplicated: 2018-09-07T15 08 13.207-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: data-management-activities
cq-template: /apps/help/templates/article-3
discoiquuid: bc366c8d-54d3-4952-adee-400c68f8c04d
firstPublishExternalDate: 2018-09-07T15:08:12.976-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 24.117-0400
jcr-createdby: admin
jcr-description: Update data
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T15:08:12.976-0400
lochandoffdate: 2018-09-10T07 27 43.991-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Update data
publishexternaldate: 2018-09-07T15 08 12.976-0400
publishExternalURL: "https://helpx.adobe.com/campaign/standard/automating/using/update-data.html"
sha1: d1345b41779f797b54c1becb6d9137f76f018ba7
topicBrowsingSortDate: 2018-09-07T15:08:12.976-0400
index: y
internal: n
snippet: y
---

# Update data{#update-data}

Update data

## Description {#description}

![](assets/data_update.png)

The **Update data** activity allows you to perform a mass update on fields in the database.

## Context of use {#context-of-use}

The **Update data** activity can be used after importing a file in order to insert the data recovered into the Adobe Campaign database. Several options allow you to personalize updating the data.

## Configuration {#configuration}

1. Drag and drop an **Update data** activity into your workflow.
1. Select the activity, then open it using the  ![](assets/edit_darkgrey-24px.png)

   button from the quick actions that appear.
1. Specify the **Operation type** to be carried out:

    * **Insert or update**: insert data or update it if it the records already exist in the database.
    * **Insert only**: insert data only. The records that already exist are not updated. If reconciliation criteria are defined, only the non-reconciled records will be added.

      Check the **Generate an outbound transition for rejects** box if the data imported contains certain records that already exist in the database to avoid any possible errors.
    
    * **Update**: update data of the records that already exist in the database only.
    * **Delete**: delete data.

1. In the **Identification** field, specify how to identify the records in the database:

    * **Using the targeting dimension**: select the **Dimension to update** then specify the **Keys for finding records**. For more this, refer to [Targeting dimensions and resources](../../automating/using/query.md#targeting-dimensions-and-resources).
    * If the data entered matches an existing targeting dimension, select the **Using one or more links** option. Then select the **Dimension to update**.

   If the operation type selected requires an update, you must use reconciliation keys.

1. In the **Fields to update** tab, specify the fields on which the update will be applied and, if necessary, add conditions so that this update is carried out. To do this, use the **Taken into account if** column. The conditions are applied one after the other in list order. Use the arrows on the right to change the order of the updates. You can use the same destination field multiple times.

   You can automatically link fields using the  ![](assets/wkf_magic_wand-24px.png)

   button. Automatic linking detects fields with the same name.

   During an **Insert or update** type operation, you can individually select the operation to apply for each field. To do this, select the value you would like in the **Operation** column.

   >[!NOTE]
   >
   >**Managing updates** The **lastModified**, **modifiedBy**, **created** and **createdBy** fields are automatically updated when an update data activity is run, unless their configuration is explicitly carried out on the field update table. The update is only carried out on the records where at least one difference has been detected. If the values are the same, no update is carried out.

1. If needed, manage the activity's [Transitions](../../automating/using/executing-a-workflow.md#managing-an-activity-s-outbound-transitions) to access the advanced options for the outbound population.

   If you have selected **Insert only** and the data imported may contain records that are already present in the database, check the **Generate an outbound transition for the rejects** box to avoid any possible errors.

1. Confirm the configuration of your activity and save your workflow.

## Example {#example}

The following activity shows the configuration of an **Update data** activity following a **Load file** activity. The aim of this workflow is to add or update profiles to the Adobe Campaign database with the data recovered from the file. The reconciliation key used is the email address.

The file loaded is a **.txt** format file containing the following example data:

```
lastname;firstname;email;birthdate
jackman;megan;megan.jackman@testmail.com;07/08/1975
phillips;edward;phillips@testmail.com;09/03/1986
weaver;justin;justin_w@testmail.com;11/15/1990
martin;babeth;babeth_martin@testmail.net;11/25/1964
reese;richard;rreese@testmail.com;02/08/1987
cage;nathalie;cage.nathalie227@testmail.com;07/03/1989
xiuxiu;andrea;andrea.xiuxiu@testmail.com;09/12/1992
grimes;daryl;daryl_890@testmail.com;12/06/1979
tycoon;tyreese;tyreese_t@testmail.net;10/08/1971
```

The **Update data** activity is configured as follows:

![](assets/deduplication_example2_writer1.png)  ![](assets/deduplication_example2_writer2.png)

