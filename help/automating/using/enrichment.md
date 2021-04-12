---
solution: Campaign Standard
product: campaign
title: Enrichment
description: The Enrichment activity is an advanced activity that allows you to define additional data to process in your workflow.
audience: automating
content-type: reference
topic-tags: targeting-activities
context-tags: enrichment,main
feature: Workflows
role: Data Architect
level: Intermediate
exl-id: c8af67b0-6789-4b4e-9d01-e2dfa14f1e8f
---
# Enrichment{#enrichment}

## Description {#description}

![](assets/enrichment.png)

The **[!UICONTROL Enrichment]** activity is an advanced activity that allows you to define additional data to process in your workflow.

## Context of use {#context-of-use}

The **[!UICONTROL Enrichment]** activity is generally used following targeting activities or after importing a file and before activities that allow the use of targeted data.

This activity contains more advanced enrichment functions than the **[!UICONTROL Query]** activity. Some simple cases of enrichment can be directly performed in the [Query activity](../../automating/using/query.md#enriching-data).

With the **[!UICONTROL Enrichment]** activity, you can leverage the inbound transition and configure the activity to complete the output transition with additional data. It allows to combine data coming from multiple sets, or to create links to a temporary resource.

**Related topics**

* [Use case: Enriching profile data with data contained in a file](../../automating/using/enriching-profile-data-file.md).
* [Use case: Sending an email with enriched fields](../../automating/using/sending-email-enriched-fields.md)

## Configuration {#configuration}

To configure an **[!UICONTROL Enrichment]** activity:

1. Drag and drop an **[!UICONTROL Enrichment]** activity into your workflow.
1. Select the activity, then open it using the ![](assets/edit_darkgrey-24px.png) button from the quick actions that appear.
1. If the activity has several inbound transitions, select the **[!UICONTROL Primary set]**. The additional data configured in this activity will be added to this primary set in the outbound transition.

   If the primary set already contains additional data, you can choose to keep them or to remove them. If you uncheck the **[!UICONTROL Keep all additional data from the main set]** option, only the additional data configured in the **[!UICONTROL Enrichment]** are kept in the outbound transition.

1. If there are several inbound transitions, define relations between the primary set and the other inbound data in the **[!UICONTROL Advanced Relations]** tab of the activity. You can add several relations using the **[!UICONTROL Add element]** button.

   When defining a new relation, select the set of inbound data that you want to link to the primary set. Then define the type of relation. Several types of relations are available, depending on the inbound data and your data model:

    * **[!UICONTROL 1 cardinality simple link]**: each record of the incoming data is associated to one and only one record from the primary set. Each record from the primary set has one associated record in the linked data.
    * **[!UICONTROL N cardinality collection link]**: 0, 1 or more (N) records from the linked data can be associated to 1 record of the primary set.
    * **[!UICONTROL 0 or 1 cardinality simple link]**: records from the primary set can be associated with 0 or 1 record from the linked data, but not more than one.

   Once the **[!UICONTROL Cardinality]** is defined, define a **[!UICONTROL Reconciliation criteria]**. The **[!UICONTROL Source expression]** of the reconciliation criteria can be a field from the target resource, an [expression](../../automating/using/advanced-expression-editing.md) or directly a value specified between quotes.

   Define a **[!UICONTROL Label]** and an **[!UICONTROL ID]** that will be easy to identify later in the workflow.

   >[!NOTE]
   >
   >You can only define relations between the primary set and the other inbound transitions connected to the **[!UICONTROL Enrichment]** activity. For simpler cases aiming at defining relations with database resources, use a [Reconciliation](../../automating/using/reconciliation.md) activity.

1. Define the additional data from the **[!UICONTROL Additional data]** tab of the activity. You can define additional data (simple fields, aggregates and collections) related to the targeting dimension of the primary set or based on the links created in the **[!UICONTROL Advanced relations]** tab of the **[!UICONTROL Enrichment]** activity.

   Consult the [Enriching data](../../automating/using/query.md#enriching-data) section.

1. Confirm the configuration of your activity and save your workflow.

The data is now available to use in the activities connected after the **[!UICONTROL Enrichment]**. For example, you can find it under the **[!UICONTROL Additional data (targetData)]** link of the personalization fields explorer in an email content.
