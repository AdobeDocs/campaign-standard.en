---
title: Deduplication
description: The Deduplication activity allows you to delete duplicates in the result(s) of the inbound activities.
audience: automating
content-type: reference
topic-tags: targeting-activities
context-tags: dedup,main
feature: Workflows
role: Data Architect
level: Intermediate
exl-id: 57c56e4a-892c-46d6-9bb4-6a345a8d9f5b
---
# Deduplication{#deduplication}

## Description {#description}

![](assets/deduplication.png)

The **[!UICONTROL Deduplication]** activity allows you to delete duplicates in the result(s) of the inbound activities.

## Context of use {#context-of-use}

The **[!UICONTROL Deduplication]** activity is generally used following targeting activities or after importing a file and before activities that allow the use of targeted data.

During deduplication, inbound transitions are processed separately. For example, if profile 'A' is present in the result of query 1, and also in the result of query 2, it will not be deduplicated.

It is therefore advised that a deduplication only has one inbound transition. To do this, you can combine your different queries by using activities that correspond to your targeting needs such as a union activity, an intersection activity, etc. For example:

![](assets/dedup_bonnepratique.png)

**Related topics**

* [Use case: Identifying duplicates before a delivery](../../automating/using/identifying-duplicated-before-delivery.md)
* [Use case: Deduplicating the data from an imported file](../../automating/using/deduplicating-data-imported-file.md)

## Configuration {#configuration}

To configure a deduplication activity, you must enter a label, the method and the deduplication criteria, as well as the options relating to the result.

1. Drag and drop a **[!UICONTROL Deduplication]** activity into your workflow.
1. Select the activity, then open it using the ![](assets/edit_darkgrey-24px.png) button from the quick actions that appear.

   ![](assets/deduplication_1.png)

1. Select the **[!UICONTROL Resource type]** on which the deduplication has to be carried out:

    * **[!UICONTROL Database resource]** if the deduplication is carried out on data that already exists in the database. Select the **[!UICONTROL Filtering dimension]** and the **[!UICONTROL Targeting dimension]**, depending on the data that you want to deduplicate. By default, deduplication is carried out on the **profiles**.
    * **[!UICONTROL Temporary resource]** if the deduplication is carried out on the workflow's temporary data: select the **[!UICONTROL Targeted set]** containing the data to deduplicate. This use case can be encountered after importing a file or if the data in the database was enriched (with a segment code, for example).

1. Select the **[!UICONTROL Number of unique records to keep]**. The default value for this field is 1. The value 0 allows you to keep all the duplicates.

   For example, if records A and B are considered duplicates of record Y, and a record C is considered as a duplicate of record Z:

    * If the value of the field is 1: only the Y and Z records are kept.
    * If the value of the field is 0: all the records are kept.
    * If the value of the field is 2: records C and Z are kept and two records from A, B, and Y are kept, by chance or depending on the deduplication method selected thereafter.

1. Define the **[!UICONTROL Duplicate identification]** criteria by adding conditions in the list provided. Specify the fields and/or expressions for which the identical values allow the duplicates to be identified: email address, first name, last name, etc. The order of the conditions allows you to specify those to process first.
1. In the drop-down list, select the **[!UICONTROL Deduplication method]** to use:

    * **[!UICONTROL Choose for me]**: randomly selects the record to be kept out of the duplicates.
    * **[!UICONTROL Following a list of values]**: lets you define a value priority for one or more fields. To define the values, select a field or create an expression, then add the value(s) into the appropriate table. To define a new field, click the **[!UICONTROL Add]** button located above the list of values.
    
      ![](assets/deduplication_2.png)

    * **[!UICONTROL Non-empty value]**: this lets you keep records for which the value of the selected expression is not empty as a priority.
    
      ![](assets/deduplication_3.png)

    * **[!UICONTROL Using an expression]**: this lets you keep the records in which the value of the expression entered is the smallest or the biggest. 
    
      ![](assets/deduplication_4.png)

1. If needed, manage the activity's [Transitions](../../automating/using/activity-properties.md) to access the advanced options for the outbound population.
1. Confirm the configuration of your activity and save your workflow.
