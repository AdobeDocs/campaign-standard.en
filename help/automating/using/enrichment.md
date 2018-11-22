---
title: Enrichment
seo-title: Enrichment
description: Enrichment
seo-description: The Enrichment activity is an advanced activity that allows you to define additional data to process in your workflow.
page-status-flag: never-activated
uuid: b18efaa4-ea7a-4013-945c-2862124b61b6
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/automating/using/enrichment
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: targeting-activities
discoiquuid: aacfae1c-6fe0-4b84-bbb4-2ebfe86da50c
isreadyforlocalization: false
navTitle: Enrichment
publishexternaldate: 2018-11-20
sha1: 259ea694485ca4bc6830e120e94ae9baf58e746e
index: y
internal: n
snippet: y
---

# Enrichment{#enrichment}

Enrichment

## Description {#description}

![](assets/enrichment.png)

The **Enrichment** activity is an advanced activity that allows you to define additional data to process in your workflow.

## Context of use {#context-of-use}

The **Enrichment** activity is generally used following targeting activities or after importing a file and before activities that allow the use of targeted data.

This activity contains more advanced enrichment functions than the **Query** activity. Some simple cases of enrichment can be directly performed in the [Query activity](../../automating/using/query.md#enriching-data).

With the **Enrichment** activity, you can leverage the inbound transition and configure the activity to complete the output transition with additional data. It allows to combine data coming from multiple sets, or to create links to a temporary resource.

## Configuration {#configuration}

To configure an **Enrichment** activity:

1. Drag and drop an **Enrichment** activity into your workflow.
1. Select the activity, then open it using the  ![](assets/edit_darkgrey-24px.png)

   button from the quick actions that appear.
1. If the activity has several inbound transitions, select the **Primary set**. The additional data configured in this activity will be added to this primary set in the outbound transition.

   If the primary set already contains additional data, you can choose to keep them or to remove them. If you uncheck the **Keep all additional data from the main set** option, only the additional data configured in the **Enrichment** are kept in the outbound transition.

1. If there are several inbound transitions, define relations between the primary set and the other inbound data in the **Advanced Relations** tab of the activity. You can add several relations using the **Add element** button.

   When defining a new relation, select the set of inbound data that you want to link to the primary set. Then define the type of relation. Several types of relations are available, depending on the inbound data and your data model:

    * **1 cardinality simple link**: each record of the incoming data is associated to one and only one record from the primary set. Each record from the primary set has one associated record in the linked data.
    * **N cardinality collection link**: 0, 1 or more (N) records from the linked data can be associated to 1 record of the primary set.
    * **0 or 1 cardinality simple link**: records from the primary set can be associated with 0 or 1 record from the linked data, but not more than one.

   Once the **Cardinality** is defined, define a **Reconciliation criteria**. The **Source expression** of the reconciliation criteria can be a field from the target resource, an [expression](../../automating/using/advanced-expression-editing.md) or directly a value specified between quotes.

   Define a **Label** and an **ID** that will be easy to identify later in the workflow.

   >[!NOTE]
   >
   >You can only define relations between the primary set and the other inbound transitions connected to the **Enrichment** activity. For simpler cases aiming at defining relations with database resources, use a [Reconciliation](../../automating/using/reconciliation.md) activity.

1. Define the additional data from the **Additional data** tab of the activity. You can define additional data (simple fields, aggregates and collections) related to the targeting dimension of the primary set or based on the links created in the **Advanced relations** tab of the **Enrichment** activity.

   Consult the [Enriching data](../../automating/using/query.md#enriching-data) section.

1. Confirm the configuration of your activity and save your workflow.

The data is now available to use in the activities connected after the **Enrichment**. For example, you can find it under the **Additional data (targetData)** link of the personalization fields explorer in an email content.

## Example: Enriching profile data with data contained in a file {#example-enriching-profile-data-with-data-contained-in-a-file}

This example shows how to enrich profile data with purchase data contained in a file. We consider here that the purchase data are stored in a third-party system. Each profile can have several purchases stored in the file. The final goal of the workflow is to send an email to the target profiles who have purchased at least two items to thank them for their loyalty.

The workflow is configured as follows:

![](assets/enrichment_example_workflow.png)

* A **Query** activity that targets the profiles who will receive the message.
* A **Load file** activity that loads the purchase data. For example:

  ```
  tcode;tdate;customer;product;tamount
  aze123;21/05/2017;dannymars@example.com;TV;799
  aze124;28/05/2017;dannymars@example.com;Headphones;8
  aze125;31/07/2017;john.smith@example.com;Headphones;8
  aze126;14/12/2017;john.smith@example.com;Plastic Cover;4
  aze127;02/01/2018;dannymars@example.com;Case Cover;79
  aze128;04/03/2017;clara.smith@example.com;Phone;149
  ```

  With this example file, we will use the email address to reconcile the data with the database profiles. You can also enable unique IDs as described in [this document](../../developing/using/generating-a-unique-id-for-profiles-and-custom-resources.md).

* An **Enrichment** activity that creates a link between the transaction data loaded from the file and the profiles selected in the **Query**. The link is defined in the **Advanced relations** tab of the activity. The link is based on the transition coming from the **Load file** activity. It uses the "email" field of the profile resource and the "customer" column of the imported file as reconciliation criteria. 

  ![](assets/enrichment_example_workflow2.png)

  Once the link is created, two sets of **Additional data** are added:

    * A collection of two lines corresponding to the two last transactions of each profile. For this collection, the product name, the transaction date, and the price of the product are added as additional data. A descending sort is applied on the data. To create the collection, from the **Additional data** tab:

      Select the link previously defined in the **Advanced relations** tab of the activity.
    
      ![](assets/enrichment_example_workflow3.png)    
    
      Check **Collection** and specify the number of lines to retrieve (2 in this example). In this screen, you can customize the **Alias** and the **Label** of the collection. These values will be visible in the following activities of the workflow when referring to this collection.
    
      ![](assets/enrichment_example_workflow4.png)    
    
      As **Data** to keep for the collection, select the columns that will be used in the final delivery.
    
      ![](assets/enrichment_example_workflow6.png)    
    
      Apply a descending sort on the transaction date to make sure to retrieve the latest transactions.
    
      ![](assets/enrichment_example_workflow7.png)

    * An aggregate counting the total number of transactions for each profile. This aggregate will be used later to filter profiles that have at least two transactions recorded. To create the aggregate, from the **Additional data** tab:

      Select the link previously defined in the **Advanced relations** tab of the activity.
    
      ![](assets/enrichment_example_workflow3.png)    
    
      Select **Aggregate**.
    
      ![](assets/enrichment_example_workflow8.png)    
    
      As **Data** to keep, define a **Count All** aggregate. If you need, specify a custom alias to find it faster in the following activities.
    
      ![](assets/enrichment_example_workflow9.png)

* A **Segmentation** activity with only one segment, that retrieves profiles of the initial target that have at least two transactions recorded. Profiles with only one transaction are excluded. To do that, the query of the segmentation is made on the aggregate defined previously.

  ![](assets/enrichment_example_workflow5.png)

* An **Email delivery** activity that uses the additional data defined in the **Enrichment** to dynamically retrieve the two last purchases made by the profile. The additional data can be found in the **Additional data (TargetData)** node when adding a personalization field.

  ![](assets/enrichment_example_workflow10.png)

