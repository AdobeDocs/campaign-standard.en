---
title: Reconciliation
description: The Reconciliation activity allows you to link unidentified data to existing resources.
audience: automating
content-type: reference
topic-tags: data-management-activities
context-tags: reconciliation,main
feature: Workflows
role: Data Architect
level: Intermediate
exl-id: ed2e3793-6164-48af-9043-42dc43fa8ed4
---
# Reconciliation{#reconciliation}

## Description {#description}

![](assets/reconciliation.png)

The **[!UICONTROL Reconciliation]** activity allows you to link unidentified data to existing resources.

While the **Enrichment** activity allows you to define additional data to process in your workflow (use an **Enrichment** activity to combine data coming from multiple sets, or to create links to a temporary resource), the **Reconciliation** activity allows you to link unidentified data to existing resources. Reconciliation operation implies that the data of the linked dimensions are already in the database. Use cases are available in [this section](#use-cases-reconciliation).

## Context of use {#context-of-use}

The **[!UICONTROL Reconciliation]** activity is essentially used for Data Management purposes and implies two different use cases:

* Adding relations: a **[!UICONTROL Links]** tab allows you to add links between the inbound data and several other Adobe Campaign database dimensions.

  For example, a file containing purchasing data may also contain information to identify the products purchased as well as the buyer. Two additional dimensions (besides that of **Purchases**) are therefore concerned by the file data: the **Products** and **Profiles** dimensions. Relations then need to be created between these and the **Purchases** dimension (refer to the following example).

  When defining a relation, a column is added to the inbound data in order to reference the foreign key of the linked dimension.

  >[!NOTE]
  >
  >This operation implies that the data of the linked dimensions are already in the database. For example, if you import a file of purchases showing which product was purchased, at what time, by which client, etc., the product as well as the client must already exist in the database.

* Data identification: an **[!UICONTROL Identification]** tab allows you to simply link inbound data to columns of an existing dimension in the Adobe Campaign database. After the activity, the data is identified as belonging to the defined dimension.

  For example, you can then perform a save audience, database update, etc.

For example, the **[!UICONTROL Reconciliation]** activity can be placed after a load data activity to import non-standard data into the database.


## Configuration {#configuration}

1. Drag and drop a **[!UICONTROL Reconciliation]** activity into your workflow, following a transition containing a population whose targeting dimension does not directly come from Adobe Campaign. For more on this, refer to [Targeting dimensions and resources](../../automating/using/query.md#targeting-dimensions-and-resources).
1. Select the activity, then open it using the ![](assets/edit_darkgrey-24px.png) button from the quick actions that appear.
1. If you would like to define links between the inbound data and other database dimensions, go to the **[!UICONTROL Links]** tab.

   Add as many relations as necessary. For each relation, first select the linked dimension, then in the link detail, specify the corresponding fields.

1. If you would like to simply identify the inbound data, go to the **[!UICONTROL Identification]** tab and check the **[!UICONTROL Identify the document from the working data]** box.

   Select the targeting dimension to which you want to reconcile the inbound data.

   Add reconciliation criteria to link an inbound transition record to a selected targeting dimension record. If several criteria are specified, they must all be verified in order for the link between all their data to work.

   Choose the **[!UICONTROL Processing unidentified source lines]** mode:

    * **[!UICONTROL Ignore them]**: only the identifiable data is kept in the activity's outbound transition.
    * **[!UICONTROL Keep in the outbound population]**: all the data from the inbound transition is kept in the activity's outbound transition.

1. Confirm the configuration of your activity and save your workflow.


## Use cases{#use-cases-reconciliation}

Learn how to use this activity in the following use cases:

* [Use case: Data reconciliation using relations](../../automating/using/reconciliation-using-relations.md)
* [Use case: Data update using reconciliation](../../automating/using/data-update-reconciliation.md)
* [Use case: Reconcile a File audience with the database](../../automating/using/reconcile-file-audience-with-database.md)