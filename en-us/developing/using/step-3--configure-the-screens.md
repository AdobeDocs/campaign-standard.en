---
title: Step 3: Configure the screens
seo-title: Step 3: Configure the screens
description: Step 3: Configure the screens
seo-description: Learn how to define new Adobe Campaign screens based on the resource data structure.
uuid: 5b23edb4-80b2-4b10-a314-2a4ca6181b54
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/developing/using/step-3--configure-the-screens
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-26T02 53 25.394-0400
cq-lastreplicated: 2018-07-23T05 59 10.019-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: adding-or-extending-a-resource
cq-template: /apps/help/templates/article-3
discoiquuid: d6fb1a9a-d643-4298-85da-06a4cb5be240
firstPublishExternalDate: 2018-07-23T05:59:09.975-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 03 04.102-0400
jcr-createdby: admin
jcr-description: Step 3  Configure the screens
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T05:59:09.975-0400
lochandoffdate: 2018-07-26T02 53 25.393-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Step 3: Configure the screens
publishexternaldate: 2018-07-23T05 59 09.975-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/developing/using/step-3--configure-the-screens.html
sha1: 6509a202eedc2f00c9b205931a6b90a0a6945008
topicBrowsingSortDate: 2018-07-23T05:59:09.975-0400
index: y
internal: n
snippet: y
---

# Step 3: Configure the screens

Step 3: Configure the screens

When creating a resource or when adding new fields to an existing resource, you can define how you want them to appear in the interface.

This step is not mandatory as you will still be able to populate your resource and access its data through workflows, audiences and REST API.

In the **Screen definition** tab, you can:

* Add access to the custom resource in the navigation pane
* Personalize the way in which the list of elements that make up the resource is presented
* Define the way the detail view of each element of the resource is displayed

## Enabling access from the navigation menu

If you want your resource to have a dedicated screen, you can make it available from the navigation menu.

1. From the **Screen definition** tab of the resource, unfold the **Navigation** section.
1. Check the **Add an entry in the 'Client data' section** box to allow access to this resource from the navigation pane. 

   ![](assets/schema_extension_19.png)

The resource will appear as a sub-entry within the **Client data** section.

## Defining the default list configuration

The **List configuration** section of the screen definition lets you define the columns and information that will be displayed by default in the overview of a resource.

1. Check the **Customize the list configuration** box to define the way the columns of the resource are displayed.
1. Use the **Add an element** button to select a field from those that you have created.
1. The field created is displayed in the list. You can edit its label and its width.

   ![](assets/schema_extension_20.png)

1. In the **Simple search** section, check the **Specify the fields to be taken into account in the search** to define which fields will be included in the search.

   >[!CAUTION]
   >
   >This configuration replaces the fields used in the default search.

1. In the **Advanced search** section, check the **Add search fields** box to add additional fields beyond the simple search field. For example, if you select the "date" field from the fields that you have created, the user will be able to perform a search that only refers to the date.
1. You can modify the order of the fields for the two search types.
1. For an advanced search, you can add fields that link to a linked resource. These filters appear in the **Search** menu of the generated screen.

The overview screen of the resource is now defined.

## Defining the detail screen configuration

The **Detail screen configuration** section of the screen definition lets you define the columns and information that will be displayed detail screen of each element of the resource.

1. Check the **Define a detail screen** box to configure the screen that corresponds to each element of the resource. If you do not check this box, the detail view of elements of this resource will not be accessible.

   You can add all of the fields from your custom resource in one click. To do this, click the  ![](assets/addAllFieldsIcon.png)

   icon. 

1. Use the **Add an element** button.
1. Select an element from those created for this resource and specify a field type:

    * **Input field**: is an editable field.
    * **Value**: is a read-only field.
    * **List**: is a table.

   ![](assets/schema_extension_23.png)

1. The element added is displayed in the list. You can edit its label.

   ![](assets/schema_extension_22.png)

1. For an extended resource, you can customize the title of the section where the new elements will appear.

The detail screen of the resource is now configured.

## Actions on data section

These settings allow you to display a control bar in the custom resource screen. There are three options available:

![](assets/schema_extension_actions.png)

* **Authorize creating**: this option allows you to activate creating elements of the resource. The user can therefore add additional records.

  >[!NOTE]
  >
  >You must first activate the detail screen linked to the resource to make this option available.

* **Authorize duplicating**: this option allows you to activate duplicating records linked to the custom resource.
* **Authorize deleting**: this option allows you to activate deleting records linked to the custom resource.

