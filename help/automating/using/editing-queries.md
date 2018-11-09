---
title: Editing queries
seo-title: Editing queries
description: Editing queries
seo-description: Build a population thanks to the predefined filters and rules.
uuid: e4145657-21e8-443e-b926-eb030d39910d
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/automating/using/editing-queries
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-10T07 28 45.257-0400
cq-lastreplicated: 2018-09-07T15 08 47.570-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: filtering-data
cq-template: /apps/help/templates/article-3
discoiquuid: a766ad1f-654f-46cf-b1dd-19b13230ac86
firstPublishExternalDate: 2018-09-07T15:08:47.178-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 14.442-0400
jcr-createdby: admin
jcr-description: Editing queries
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T15:08:47.178-0400
lochandoffdate: 2018-09-10T07 28 45.256-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Editing queries
publishexternaldate: 2018-09-07T15 08 47.178-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/automating/using/editing-queries.html
sha1: 33c880ee1cb4828d065c3444847a4421d88c8672
topicBrowsingSortDate: 2018-09-07T15:08:47.178-0400
index: y
internal: n
snippet: y
---

# Editing queries{#editing-queries}

Editing queries

## About query editor {#about-query-editor}

The query editor is a wizard that allows you to filter data contained in the Adobe Campaign database.

This feature lets you build a population to better target your recipients thanks to the predefined filters and rules.

Several application functionalities use it in order to:

* Create **Query** type **audiences**
* Define **email** targets
* Define populations in **workflow** activities

## Query editor interface {#query-editor-interface}

The query editor is made up of a **Palette** and a **Workspace**.

![](assets/query_editor_overview.png)

### Palette {#palette}

The palette, located on the left-hand side of the editor, is divided into two tabs, which contain elements divided into thematic blocks. These tabs are:

* The **Shortcuts**, available by default, or created by the instance administrator. Here you will find fields, nodes, groupings, 1-1 links, 1-N links and other predefined filters.
* The **Explorer** which allows you to access all available fields in the target resource: nodes, grouping elements, links (1-1 and 1-N).

The elements contained in the tabs must be moved into the workspace in order to be configured and taken into account for the query. Depending on the targeting dimension selected (see [Targeting dimensions and resources](../../automating/using/query.md#targeting-dimensions-and-resources)), you can:

* Select audiences or profiles one by one
* Use predefined filters
* Define simple rules for fields of your choice
* Define advanced rules that allow you to apply functions to certain fields

### Workspace {#workspace}

The workspace is the central zone in which you can configure and combine rules, audiences, and predefined filters added from the palette.

When you move an element from the palette into the workspace, a new window opens and you can start [Creating queries](../../automating/using/editing-queries.md#creating-queries).

## Creating queries {#creating-queries}

The query editor can be used to define an audience or test profile in a message, a population in a workflow and to create a query type audience.

Queries can be defined in the **Audience** window while creating a delivery or in a **Query** activity while creating a workflow.

1. Move an element from the palette into the workspace. The window for editing the rule opens.

    * For a string or numerical **field**, specify the comparison operator and the value. 
    
      ![](assets/query_editor_audience_definition2.png)

    * For a date or date and time **field**, you can choose to define a specific date, a range between two dates, or a period relative to the query's execution date.
    
      ![](assets/query_editor_date_field.png)

    * For a Boolean **field**, check the boxes linked to the possible values for the field.
    * For a **grouping** field, select the grouping field on which you want to create the rule, then define the condition in the same way as for the other fields.
    
      ![](assets/query_editor_audience_definition4.png)

    * For a **1-1** link with another database resource, select a value directly from the table targeted.
    
      ![](assets/query_editor_audience_definition5.png)

    * For a **1-N** link with another database resource, you can define a sub-query on the fields of this second resource.

      You do not need to specify a sub-condition.

      For example, you can only select the **Exists** operator on the profile tracking logs and approve the rule. The rule will return all of the profiles for which tracking logs exist.
    
      ![](assets/query_editor_audience_definition6.png)

    * For a **predefined filter**, enter or select the elements you like according to the criteria offered.

      Administrators can create filters to facilitate complex and repetitive queries. These will appear in the query editor in the form of pre-configured rules and they limit the number of steps needed to be carried out by the user.
    
      ![](assets/query-editor_filter_email-audience_filter.png)

1. You can specify a name for your rule. This is then displayed as the rule name in the workspace. If the rule is not given a name, an automatic description of the conditions is displayed.
1. To combine the workspace elements, interlock them into one another to create different groups and/or group levels. You can then select a logical operator to combine elements on the same level:

    * **AND**: an intersection of two criteria. Only the elements matching each criterion are taken into account.
    * **OR**: a union of two criteria. Elements matching at least one of the two criteria are taken into account.
    * **EXCEPT**: exclusion criteria. Elements matching the first criterion are taken into account unless they also match the second criterion.

1. You can now calculate and preview the number of elements targeted by your query using the  ![](assets/count.png) and  ![](assets/preview.png)

   buttons from the action bar.

   ![](assets/query_editor_combining_rules.png)

If you would like to modify an element of the query, click on the edit icon. The rule is opened as it was previously configured and you can then carry out any necessary adjustments.

Your queries are now created and defined, this allows you to build a population to better personalize your deliveries.

**Related Topics:**

* [Advanced functions](../../automating/using/advanced-expression-editing.md)
* [Defining filters](../../developing/using/step-4--define-filters.md)

