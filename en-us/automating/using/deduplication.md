---
title: Deduplication
seo-title: Deduplication
description: Deduplication
seo-description: The Deduplication activity allows you to delete duplicates in the result(s) of the inbound activities.
uuid: 48b63db4-afdf-44f9-8dbd-9f6aa39c1396
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/automating/using/deduplication
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-25T09 29 32.741-0400
cq-lastreplicated: 2018-07-23T05 57 08.337-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: targeting-activities
cq-template: /apps/help/templates/article-3
discoiquuid: 4f5c96d5-a4d5-449b-9405-7054516e6697
firstPublishExternalDate: 2018-07-23T05:57:08.294-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 58.928-0400
jcr-createdby: admin
jcr-description: Deduplication
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T05:57:08.294-0400
lochandoffdate: 2018-07-25T09 29 32.740-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Deduplication
publishexternaldate: 2018-07-23T05 57 08.294-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/automating/using/deduplication.html
sha1: b9d00ec832f864f64c568aac110b4c8f8301c956
topicBrowsingSortDate: 2018-07-23T05:57:08.294-0400
index: y
internal: n
snippet: y
---

# Deduplication

Deduplication

## Description

![](assets/deduplication.png)

The **Deduplication** activity allows you to delete duplicates in the result(s) of the inbound activities.

## Context of use

The **Deduplication** activity is generally used following targeting activities or after importing a file and before activities that allow the use of targeted data.

During deduplication, inbound transitions are processed separately. For example, if profile 'A' is present in the result of query 1, and also in the result of query 2, it will not be deduplicated.

It is therefore advised that a deduplication only has one inbound transition. To do this, you can combine your different queries by using activities that correspond to your targeting needs such as a union activity, an intersection activity, etc. For example:

![](assets/dedup_bonnePratique.png) 

## Configuration

To configure a deduplication activity, you must enter a label, the method and the deduplication criteria, as well as the options relating to the result.

1. Drag and drop a **Deduplication** activity into your workflow.
1. Select the activity, then open it using the  ![](assets/edit_darkgrey-24px.png)

   button from the quick actions that appear.

   ![](assets/deduplication_1.png)

1. Select the **Resource type** on which the deduplication has to be carried out:

    * **Database resource** if the deduplication is carried out on data that already exists in the database. Select the **Filtering dimension** and the **Targeting dimension**, depending on the data that you want to deduplicate. By default, deduplication is carried out on the **profiles**.
    * **Temporary resource** if the deduplication is carried out on the workflow's temporary data: select the **Targeted set** containing the data to deduplicate. This use case can be encountered after importing a file or if the data in the database was enriched (with a segment code, for example).

1. Select the **Number of unique records to keep**. The default value for this field is 1. The value 0 allows you to keep all the duplicates.

   For example, if records A and B are considered duplicates of record Y, and a record C is considered as a duplicate of record Z:

    * If the value of the field is 1: only the Y and Z records are kept.
    * If the value of the field is 0: all the records are kept.
    * If the value of the field is 2: records C and Z are kept and two records from A, B, and Y are kept, by chance or depending on the deduplication method selected thereafter.

1. Define the **Duplicate identification** criteria by adding conditions in the list provided. Specify the fields and/or expressions for which the identical values allow the duplicates to be identified: email address, first name, last name, etc. The order of the conditions allows you to specify those to process first.
1. In the drop-down list, select the **Deduplication method** to use:

    * **Choose for me**: randomly selects the record to be kept out of the duplicates.
    * **Following a list of values**: lets you define a value priority for one or more fields. To define the values, select a field or create an expression, then add the value(s) into the appropriate table. To define a new field, click the **Add** button located above the list of values.
    
      ![](assets/deduplication_2.png)

    * **Non-empty value**: this lets you keep records for which the value of the selected expression is not empty as a priority.
    
      ![](assets/deduplication_3.png)

    * **Using an expression**: this lets you keep the records in which the value of the expression entered is the smallest or the biggest. 
    
      ![](assets/deduplication_4.png)

1. If needed, manage the activity's [Transitions](../../automating/using/executing-a-workflow.md#managing-an-activity-s-outbound-transitions) to access the advanced options for the outbound population.
1. Confirm the configuration of your activity and save your workflow.

## Example 1: Identifying duplicates before a delivery

The following example illustrates a deduplication that lets you exclude the duplicates of a target before sending an email. This means you avoid sending a communication several times to the same profile.

The workflow is made up of:

![](assets/deduplication_example_workflow.png)

* A **Query** which allows you to define the target of the email. Here, the workflow targets all profiles aged between 18 and 25 that have been in the client database for more than a year.

  ![](assets/deduplication_example_query.png)

* A **Deduplication** activity, which allows you to identify the duplicates that come from the preceding query. In this example, only one record is saved for each duplicate. The duplicates are identified using the email address. This means that the email delivery can only be sent once for each email address to be present in the targeting.

  The deduplication method selected is **Non-empty value**. This allows you to ensure that amongst the records kept in case of duplicates, priority is given to those in which the **First name** has been provided. This will make it more coherent if the first name is used in the personalization fields of the email content.

  In addition, an extra transition is added to keep the duplicates and to be able to list them.

  ![](assets/deduplication_example_dedup.png)

* An **Email delivery** placed after the main outbound transition of the deduplication. The configuration for email deliveries is detailed in the [Email delivery](../../automating/using/email-delivery.md) section.
* A **Save audience** activity placed after the additional transition of the deduplication to save the duplicates in a **Duplicates** audience. This audience can be reused to directly exclude its members from every email delivery.

## Example 2: Deduplicating the data from an imported file

This example shows how to deduplicate data from a file imported before loading the data into the database. This procedure improves the quality of the data loaded in the database.

The workflow is made up of:

![](assets/deduplication_example2_workflow.png)

* A file that contains a list of profiles is imported using a **Load file** activity. In this example, the file imported is in .csv format and contains 10 profiles:

  ```
  lastname;firstname;dateofbirth;email
  Smith;Hayden;23/05/1989;hayden.smith@example.com
  Mars;Daniel;17/11/1987;dannymars@example.com
  Smith;Clara;08/02/1989;hayden.smith@example.com
  Durance;Allison;15/12/1978;allison.durance@example.com
  Lucassen;Jody;28/03/1988;jody.lucassen@example.com
  Binder;Tom;19/01/1982;tombinder@example.com
  Binder;Tommy;19/01/1915;tombinder@example.com
  Connor;Jade;10/10/1979;connor.jade@example.com
  Mack;Clarke;02/03/1985;clarke.mack@example.com
  Ross;Timothy;04/07/1986;timross@example.com
  ```

  This file can also be used as a sample file to detect and define the format of the columns. From the **Column definition** tab, make sure that each column of the imported file is configured correctly.

  ![](assets/deduplication_example2_fileloading.png)

* A **Deduplication** activity. Deduplication is carried out directly after importing the file and before inserting the data into the database. It should therefore be based on the **Temporary resource** from the **Load file** activity.

  For this example, we want to keep a single entry per unique email address contained in the file. Duplicate identification is therefore carried out on the **email** column of the temporary resource. Yet, two email addresses appear twice in the file. Two lines will therefore be considered as duplicates.

  ![](assets/deduplication_example2_dedup.png)

* An **Update data** activity allows you to insert the data kept from the deduplication process into the database. It is only when the data is updated that the imported data is identified as belonging to the profile dimension.

  Here, we would like to **Insert only** the profiles that do not already exist in the database. We are going to do this by using the file's email column and the email field from the **Profile** dimension as the reconciliation key.

  ![](assets/deduplication_example2_writer1.png)

  Specify the mappings between the file's columns from which you want to insert the data and the database fields from the **Fields to update** tab.

  ![](assets/deduplication_example2_writer2.png)

Then start the workflow. The records saved from the deduplication process are then added to the profiles in your database.
