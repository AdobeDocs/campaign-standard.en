---
title: Step 4 Define filters
seo-title: Step 4 Define filters
description: Step 4 Define filters
seo-description: Discover the filter feature to manage large data set.
uuid: 47aa521b-a979-4e6e-aec5-d5aaa806ab58
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/developing/using/step-4--define-filters
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-10T02 18 52.051-0400
cq-lastreplicated: 2018-09-07T14 53 22.890-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: adding-or-extending-a-resource
cq-template: /apps/help/templates/article-3
discoiquuid: cee5563b-cbe1-4e8a-a417-e2ffd3385498
firstPublishExternalDate: 2018-09-07T14:53:20.708-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 01 59.704-0400
jcr-createdby: admin
jcr-description: Step 4  Define filters
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T14:53:20.708-0400
lochandoffdate: 2018-09-10T02 18 52.051-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Step 4 Define filters
publishexternaldate: 2018-09-07T14 53 20.708-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/developing/using/step-4--define-filters.html
sha1: dfb4ac9beddab540737849799b4e5a2ccdcfa812
topicBrowsingSortDate: 2018-09-07T14:53:20.708-0400
index: y
internal: n
snippet: y
---

# Step 4: Define filters

Step 4: Define filters

In the **Filter definition** tab, you can create advanced filters that users can directly access when creating complex queries, such as when defining an audience.

This step is not mandatory as you will still be able to populate your resource and access its data through workflows, audiences and REST API.

![](assets/custom_resource_filter-definition.png)

These filters are used in the query editor in the form of pre-configured rules. They allow you to limit the number of steps necessary to get the desired configuration, which can be particularly beneficial for repetitive segmentations.

For example, you can create a filter enabling to select all transactions greater than a certain amount within the last three months.

To do this, you need to extend the **Profiles** resource and define a filter linking to a transaction table (that you have previously created) with a rule indicating that the transaction price must be greater than or equal to a given parameter and that the transaction date must fall within a range corresponding to the last three months.

1. Make sure you create and publish a transaction table. See [Step 1: Define the resource](../../developing/using/step-1--define-the-resource.md).

   >[!NOTE]
   >
   >This procedure uses the example of a custom transaction table. For your case, adjust it to your business needs.

1. Before defining a filter related to the transaction table in the **Profiles** resource, make sure you define the link to this table and publish your changes. See [Defining links with other resources](../../developing/using/step-2--configure-the-resource-data-structure.md#defining-links-with-other-resources) and [Step 5: Update the database structure](../../developing/using/step-5--update-the-database-structure.md).
1. In the **Definition** tab of your new filter's definition screen, select the transaction table.

   ![](assets/custom_resource_filter-definition_example-empty.png)

1. In the **Add a rule - Profiles/Transactions** window, drag and drop the transaction table into the workspace. In the next window that is displayed, select the field that you want to use.

   ![](assets/custom_resource_filter-definition_example-field.png)

1. In the **Optional parameter settings** of the **Add a rule - Transactions** window, check the **Switch to parameters** box.

   In the **Filter conditions**, select the **Greater than or equal to** operator. In the **Parameters** field, enter a name and click the plus sign to create the new parameter.

   ![](assets/custom_resource_filter-definition_example-parameter.png)

1. Confirm your changes. This definition corresponds to a configurable field that the user must fill in later to execute the query.

   ![](assets/custom_resource_filter-definition_ex_edit-rule.png)

1. Combine this rule with another rule specifying that the transaction date must fall within a range corresponding to the last three months.

   ![](assets/custom_resource_filter-definition_example.png)

1. Choose the category in which your filter will be displayed.

   ![](assets/custom_resource_filter-definition_category.png)

1. In the **Parameters** tab of the filter definition screen, modify the description and the label to clearly indicate the subject of your filter to the users. This information will appear in the query editor.

   ![](assets/custom_resource_filter-definition_parameters.png)

   If you define multiple configurable fields, you can modify the order in which they appear in the interface.

1. Save your changes and publish the resources. For more on this, refer to the [Step 5: Update the database structure](../../developing/using/step-5--update-the-database-structure.md) section.

Once the **Profiles** resource extension is published, the users will see this filter under the shortcuts tab in the [query editor](../../automating/using/editing-queries.md) interface.

This will allow the user to easily define their audience when creating an email to send to all of the clients that spent more than a certain amount over the last three months.

![](assets/custom_resource_filter-definition_email-audience.png)

Rather than configuring it themselves, they simply have to enter the desired amount in the dialog box that appears.

![](assets/custom_resource_filter-definition_email-audience_filter.png)

