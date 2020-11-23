---
solution: Campaign Standard
product: campaign
title: Data reconciliation using relations
description: The following example demonstrates a workflow that updates the database using the purchasing data in a file.
audience: automating
content-type: reference
topic-tags: data-management-activities
context-tags: reconciliation,main
---

# Data reconciliation using relations {#reconciliation-relations}

The following example demonstrates a workflow that updates the database using the purchasing data in a file. The purchasing data contains data referencing elements from other dimensions, such as the client emails and product codes.

>[!NOTE]
>
>The **Transactions** and **Products** resources used in this example do not exist in the Adobe Campaign database by default. They were therefore created beforehand using the [Custom resources](../../developing/using/data-model-concepts.md) function. The profiles that correspond to the email addresses in the imported file, as well as the products, were loaded into the database beforehand.

The workflow is made up of the following activities:

![](assets/reconciliation_example1.png)

* A [Load file](../../automating/using/load-file.md) activity, which loads and detects the data of the file to import. The imported file contains the following data:

    * Transaction date
    * Client email address
    * Code of product purchased

  ```
  date;client;product
  2015-05-19 09:00:00;mail1@email.com;ZZ1
  2015-05-19 09:01:00;mail2@email.com;ZZ2
  2015-05-19 09:01:01;mail3@email.com;ZZ2
  2015-05-19 09:01:02;mail4@email.com;ZZ2
  2015-05-19 09:02:00;mail5@email.com;ZZ3
  2015-05-19 09:03:00;mail6@email.com;ZZ4
  2015-05-19 09:04:00;mail7@email.com;ZZ5
  2015-05-19 09:05:00;mail8@email.com;ZZ7
  2015-05-19 09:06:00;mail9@email.com;ZZ6
  ```

* A [Reconciliation](../../automating/using/reconciliation.md) activity to bind purchasing data to database profiles as well as products. It is therefore necessary to define a relation between the file data and the profile table as well as the product table. This configuration is carried out in the activity's **[!UICONTROL Relations]** tab:

    * Relation with the **Profiles**: the file's **client** column is linked to the **email** field of the **Profiles** dimension.
    * Relation with the **Products**: the file's **product** column is linked to the **productCode** field of the **Profiles** dimension.

  Columns are added to the inbound data in order to reference the foreign keys of the linked dimensions.

  ![](assets/reconciliation_example3.png)

* An [Update data](../../automating/using/update-data.md) activity allows you to define the database fields to update using the imported data. As the data was already identified as belonging to the **Transactions** dimension in the previous activity, here you can use the **[!UICONTROL Directly using the targeting dimension]** identification option.

  By using the option that automatically detects fields to update, the links configured in the previous activity (to profiles and products) are added to the list of **[!UICONTROL Fields to update]**. You must also make sure that the field that corresponds to the transaction date is correctly added to this list.

  ![](assets/reconciliation_example5.png)

  ![](assets/reconciliation_example4.png)
