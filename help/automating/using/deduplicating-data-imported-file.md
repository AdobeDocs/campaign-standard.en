---
solution: Campaign Standard
product: campaign
title: Deduplicating the data from an imported file
description: This example shows how to deduplicate data from a file imported before loading the data into the database.
audience: automating
content-type: reference
topic-tags: targeting-activities
context-tags: dedup,main
feature: Workflows
role: Data Architect
level: Intermediate
exl-id: 631eb661-a696-4352-aa58-9097b391723e
---
# Deduplicating the data from an imported file {#deduplicating-the-data-from-an-imported-file}

This example shows how to deduplicate data from a file imported before loading the data into the database. This procedure improves the quality of the data loaded in the database.

The workflow is made up of:

![](assets/deduplication_example2_workflow.png)

* A file that contains a list of profiles is imported using a [Load file](../../automating/using/load-file.md) activity. In this example, the file imported is in .csv format and contains 10 profiles:

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

  This file can also be used as a sample file to detect and define the format of the columns. From the **[!UICONTROL Column definition]** tab, make sure that each column of the imported file is configured correctly.

  ![](assets/deduplication_example2_fileloading.png)

* A [Deduplication](../../automating/using/deduplication.md) activity. Deduplication is carried out directly after importing the file and before inserting the data into the database. It should therefore be based on the **[!UICONTROL Temporary resource]** from the **[!UICONTROL Load file]** activity.

  For this example, we want to keep a single entry per unique email address contained in the file. Duplicate identification is therefore carried out on the **email** column of the temporary resource. Yet, two email addresses appear twice in the file. Two lines will therefore be considered as duplicates.

  ![](assets/deduplication_example2_dedup.png)

* An [Update data](../../automating/using/update-data.md) activity allows you to insert the data kept from the deduplication process into the database. It is only when the data is updated that the imported data is identified as belonging to the profile dimension.

  Here, we would like to **[!UICONTROL Insert only]** the profiles that do not already exist in the database. We are going to do this by using the file's email column and the email field from the **Profile** dimension as the reconciliation key.

  ![](assets/deduplication_example2_writer1.png)

  Specify the mappings between the file's columns from which you want to insert the data and the database fields from the **[!UICONTROL Fields to update]** tab.

  ![](assets/deduplication_example2_writer2.png)

Then start the workflow. The records saved from the deduplication process are then added to the profiles in your database.
