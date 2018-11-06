---
title: Step 2: Configure the resource data structure
seo-title: Step 2: Configure the resource data structure
description: Step 2: Configure the resource data structure
seo-description: Learn how to configure the data structure.
uuid: dfc80631-f4fe-478e-8d47-d22e92fc833a
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/developing/using/step-2--configure-the-resource-data-structure
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-10T02 18 39.282-0400
cq-lastreplicated: 2018-09-07T14 51 57.451-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: adding-or-extending-a-resource
cq-template: /apps/help/templates/article-3
discoiquuid: 27e20bae-8275-4d46-a849-dc6bd8f4eb57
firstPublishExternalDate: 2018-09-07T14:51:54.919-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 55.169-0400
jcr-createdby: admin
jcr-description: Step 2  Configure the resource data structure
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T14:51:54.919-0400
lochandoffdate: 2018-09-10T02 18 39.282-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Step 2: Configure the resource data structure
publishexternaldate: 2018-09-07T14 51 54.919-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/developing/using/step-2--configure-the-resource-data-structure.html
sha1: 784dce5255ac98f7e6890887d979cf2d90c3436f
topicBrowsingSortDate: 2018-09-07T14:51:54.919-0400
index: y
internal: n
snippet: y
---

# Step 2: Configure the resource data structure

Step 2: Configure the resource data structure

After creating a new custom resource, you must configure the data structure.

When editing the resource, in the **Data structure** tab, you can add:

* Fields
* Identification keys
* Indexes
* Links

## Adding Fields to a Resource

You can add new fields to a resource to store data that are not part of the out of the box data model.

1. Use the **Create element** button to create a field.
1. Specify a label, an ID, a field type, and define the maximum length authorized for this field.

   The **ID** field is mandatory and must be unique for each field added.

   >[!NOTE]
   >
   >If you leave the **Label** field empty, it will automatically be completed from the ID.

   ![](assets/schema_extension_4.png)

1. To modify one of the fields, check the corresponding box and use the **Show detail of the element selected** button.

   ![](assets/schema_extension_24.png)

1. In the **Field definition** screen, you can define a category that will be used for the audience and targeting, or even add a description.

   Check the **Specify a list of authorized values** option to define the values that will be offered to the user (enumeration values).

   ![](assets/schema_extension_5.png)

1. Once you have added your fields, check the **Add audit fields** box to include fields detailing the creation date, the user that created the resource, the date, and the author of the last modification.
1. Check the **Add access authorization management fields** box to include the fields stating who has access rights to that particular resource.

   These fields appear in the data and metadata that can be displayed once the database update has been carried out. For more on this, refer to the [Step 5: Update the database structure](../../developing/using/step-5--update-the-database-structure.md) section.

1. To modify the way in which the name of the resource elements will appear in the lists and creation steps, check the **Personalize the resource title** box. Select a field from those you created for this resource.

   ![](assets/schema_extension_18.png)

The fields of your resource are now defined.

## Defining identification keys

Each resource must have at least one unique key. For example, you can specify a key so that two products cannot have the same ID in a purchase table.

1. Use the **Create element** button to create a key.

   The **Label** and **ID** fields are completed by default, but you can edit them.

1. To define the elements making up this key, select the fields from those that you created for this resource.

   ![](assets/schema_extension_7.png)

   Created keys are displayed in the **Personalized keys** section.

1. If you would like to have a technical key, which will be automatically and incrementally generated, specify it in the **Automatic primary key** section by providing the size for the storage.

   ![](assets/schema_extension_6.png)

Your identification keys for the resource are now created.

## Defining indexes

An index can reference one or several resource fields. Indexes allow the database to sort records in order to recover them more easily. They optimize the performances of SQL queries.

Defining indexes is recommended but not mandatory.

1. Use the **Create element** button to create an index.

   The **Label** and **ID** fields are completed by default, but you can edit them.

1. To define the elements making up this index, select the fields from those that you created for this resource.

The indexes that were created appear in the list in the **Index** section.

## Defining links with other resources

A link details the association that one table has with other tables.

1. Use the **Create element** button to create a link to a target resource.
1. Resources are shown in alphabetical order and can be filtered by name. Their technical name is displayed in brackets. Select an element from the list and confirm.

   ![](assets/schema_extension_9.png)

1. Select the **Link type** according to cardinality. Depending on the cardinality type selected, the behavior if the records are deleted or duplicated may vary.
1. In the **New link** screen, the **Label** and **ID** fields are completed by default, but you can edit them.

   >[!CAUTION]
   >
   >It is not possible to rename a link after creation. To rename a link, you must delete it and create it again.

1. The **Category for the audience and targeting** list allows you to select a category from the query editor tool.
1. The **Reverse link definition** section allows you to display the label and ID of the resource from which you defined the link.
1. Define all of the records referenced by the link in the **Behavior in case of deletion/duplication** section.

   ![](assets/schema_extension_16.png)

1. In the **Join definition** section, you can choose to use the primary keys. Otherwise, specify new criteria: select a source field from the fields that you created for this resource and select an expression for the destination field or link a constant value to a field of the linked resource.

   ![](assets/schema_extension_17.png)

The links created are displayed in the list in the **Links** section.

**Example: Links to the 'Profiles' resource**

When you have added a link from a new resource to the **Profiles** resource, a new tab is automatically added in the profiles' detail view.

For example, in a new **Products (Products)** custom resource, a link to the profiles is added:

![](assets/custom_resource_link_to_profile.png)

By adding this link, a **Products** tab, named after the **Label** of the new resource, is added to the profiles detail screen. The result is immediately visible after publishing the custom resource from the **Profiles & audiences** > **Profiles** menu. By clicking on a profile, the information from the **Products** custom resource appears in a new tab.

## Defining sending logs extension

The sending log extension allows you:

* to extend dynamic report capabilites by **adding profile custom fields**
* to extend the sending logs data with **segment code and profile data**

**Extend with a segment code**

For more information on segment code, refer to the [Segmentation](../../automating/using/segmentation.md) section.

The user can extend the logs with the segment code coming from the workflow engine.

The segment code must be defined into the workflow.

To activate this extension, check the option **Add segment code**.

![](assets/sendingLogsExtension_1.png)

**Extend with a profile field**

>[!NOTE]
>
>The administrator should have extended the Profile resource with a custom field.

![](assets/sendingLogsExtension_2.png)

Click **Add field** and select any custom field from the profile resource.

In order to generate a new sub-dimension linked to the Profile dimension, check the **Add this field in Dynamic reporting as a new dimension** option.

![](assets/sendingLogsExtension_3.png)

From Dynamic Reporting, you can drag and drop the custom field dimension into a freeform table.

For more information on Dynamic Reporting, refer to the [List of components](../../reporting/using/list-of-components-.md).

>[!CAUTION]
>
>The number of fields sent to Dynamic Reporting is limited to 20.

