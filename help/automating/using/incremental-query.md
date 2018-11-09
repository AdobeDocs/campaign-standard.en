---
title: Incremental query
seo-title: Incremental query
description: Incremental query
seo-description: The Incremental query activity allows you to filter and extract a population of elements from the Adobe Campaign database.
uuid: b382cb39-3382-4a73-96ab-a76bc71dbde6
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/automating/using/incremental-query
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-10T07 24 40.033-0400
cq-lastreplicated: 2018-09-07T14 51 40.189-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: targeting-activities
cq-template: /apps/help/templates/article-3
discoiquuid: 6e4034fe-7bc4-497e-a3f4-1da8793c896e
firstPublishExternalDate: 2018-09-07T14:51:38.403-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 03.037-0400
jcr-createdby: admin
jcr-description: Incremental query
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T14:51:38.403-0400
lochandoffdate: 2018-09-10T07 24 40.032-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Incremental query
publishexternaldate: 2018-09-07T14 51 38.403-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/automating/using/incremental-query.html
sha1: 984624f46d317b397baea8335c2c8fd786052524
topicBrowsingSortDate: 2018-09-07T14:51:38.403-0400
index: y
internal: n
snippet: y
---

# Incremental query{#incremental-query}

Incremental query

## Description {#description}

![](assets/incremental.png)

The **Incremental query** activity allows you to filter and extract a population of elements from the Adobe Campaign database. Each time this activity is executed, the results from the previous executions are excluded. This allows you to target only new elements.

You can define **Additional data** for the targeted population via a dedicated tab. This data is stored in additional columns and can only be used for the workflow in progress.

The activity uses the query editor tool. This tool is detailed in a [dedicated section](../../automating/using/editing-queries.md#about-query-editor).

## Context of use {#context-of-use}

An **Incremental query** has to be linked to a **Scheduler** in order to define the execution frequency of the workflow, and therefore the query.

The **Processed data** tab, which is specific to this activity, allows you to view any results of the activity's previous executions, if required.

The **Incremental query** activity can be used for various types of uses:

* Segmenting individuals to define the target of a message, audience, etc.
* Exporting data.

## Configuration {#configuration}

1. Drag and drop an **Incremental query** activity into your workflow.
1. Select the activity, then open it using the  ![](assets/edit_darkgrey-24px.png)

   button from the quick actions that appear.
1. If you would like to run a query on a resource other than the profile resource, go to the activity's **Properties** tab and select a **Resource** and a **Targeting dimension**.

   The **Resource** allows you to refine the filters displayed in the palette whereas the **Targeting dimension**, contextual with regard to the resource selected, corresponds to the type of population that you would like to obtain (identified profiles, deliveries, data linked to the selected resource, etc.).

1. In the **Target** tab, run your query by defining and combining rules.
1. In the **Processed data** tab, choose the incremental mode you want to use for the next executions of the workflow:

    * **Use the exclusion of the results of previous executions**: the results of previous executions for each new execution are excluded.
    * **Use a date field**: the next executions only take into account the results having the selected date field greater or equal to the last execution date of the **Incremental query** activity. You can select any date field pertaining to the resource selected in the **Properties** tab. This mode has better performance when querying large resources such as log data.

      After the first execution of the workflow, you can see in this tab the last execution date that will be used for the next execution. It is automatically updated every time the workflow is executed. You still have the possibility to override this value by manually entering a new one so that it fits your needs.

   >[!NOTE]
   >
   >The **Use a date field** mode allows more flexibility depending on the date field that is selected. For example, if the selected field corresponds to a modification date, the date field mode will allow you to retrieve data that were recently updated, while the other mode will simply exclude recordings that were already targeted in a previous execution, even if they have been modified since the last execution of the workflow.

   ![](assets/incremental_query_usedatefield.png)

1. You can define **Additional data** for the targeted population via a dedicated tab. This data is stored in additional columns and can only be used for the workflow in progress. In particular, you can add data from the Adobe Campaign database tables linked to the query's targeting dimension. Consult the [Enriching data](../../automating/using/query.md#enriching-data) section.
1. Confirm the configuration of your activity and save your workflow.

## Enriching data {#enriching-data}

Just as for a query, you can enrich the data from an **Incremental query**. Consult the [Enriching data](../../automating/using/query.md#enriching-data) section.

## Example: incremental query on subscribers to a service {#example-incremental-query-on-subscribers-to-a-service}

The following example shows the configuration of an **Incremental query** activity which filters the profiles in the Adobe Campaign database that are subscribed to the **Running Newsletter** service, to send them a welcome email containing a promo code.

The workflow is up made up of the following elements:

![](assets/incremental_query_example1.png)

* A **Scheduler** activity, to execute the workflow every Monday at 6 am.

  ![](assets/incremental_query_example2.png)

* An **Incremental query** activity, which targets all of the current subscribers during the first execution, then only the new subscribers of that week during the following executions.

  ![](assets/incremental_query_example3.png)

* An **Email delivery** activity. The workflow is executed once a week, but you can aggregate the emails sent and the results per month, for example to generate reports over a period of an entire month and not just a single week.

  To do this, choose to create a **Recurring email** here regrouping the emails and the results **By month**.

  Define the content of your email and insert the welcome promo code.

  For more on this, refer to the [Email delivery](../../automating/using/email-delivery.md) and [Defining email content](../../designing/using/about-email-content-design.md#using-the-email-content-editor) sections.

Then start the workflow execution. Each week the new subscribers will receive the welcome email with the promo code.

## Example: incremental query on delivery logs {#example-incremental-query-on-delivery-logs}

You can use an **Incremental query** activity to regularly export new logs in files. It can be useful for example if you want to use your log data in external reporting or BI tools.

A complete example is available in the [Exporting logs](../../automating/using/exporting-logs.md) section.
