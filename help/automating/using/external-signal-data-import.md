---
title: External signal and data import
description: The following example illustrates the External signal activity used with data import.
audience: automating
content-type: reference
topic-tags: execution-activities
context-tags: signal,main
feature: Workflows
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: e2997cf5-861b-4202-aeb7-3a47c4d55bef
---
# External signal and data import {#external-signal-data-import}

The following example illustrates the **[!UICONTROL External signal]** activity in a typical use case. A data import is performed in a source workflow. Once the import is done and the database updated, a second workflow is triggered. This second workflow is used to update an aggregate on the imported data.

The source workflow is presented as follows:

* A [Load file](../../automating/using/load-file.md) activity uploads a file containing new purchase data. Note that the [database has been extended](../../developing/using/data-model-concepts.md) accordingly as purchase data are not present by default in the datamart.

  For example:

  ```
  tcode;tdate;customer;product;tamount
  aze123;21/05/2015;dannymars@example.com;A2;799
  aze124;28/05/2015;dannymars@example.com;A7;8
  aze125;31/07/2015;john.smith@example.com;A7;8
  aze126;14/12/2015;john.smith@example.com;A10;4
  aze127;02/01/2016;dannymars@example.com;A3;79
  aze128;04/03/2016;clara.smith@example.com;A8;149
  ```

* A [Reconciliation](../../automating/using/reconciliation.md) activity creates the links between the imported data and the database so that the transactions data are properly connected to profiles and products.
* An [Update data](../../automating/using/update-data.md) activity inserts and updates the Transactions resource of the database with the incoming data.
* An [End](../../automating/using/start-and-end.md) activity triggers the destination workflow, which is used to update aggregates.

![](assets/signal_example_source1.png)

The destination workflow is presented as follows:

* An [External signal](../../automating/using/external-signal.md) activity waits for the source workflow to be successfully finished.
* A [Query](../../automating/using/query.md#enriching-data) activity targets profiles and enrich them with a collection set to retrieve the last purchase date.
* An [Update data](../../automating/using/update-data.md) activity stores the additional data in a dedicated custom field. Note that the profile resource has been extended to add the **Last purchase date** field.

![](assets/signal_example_source2.png)
