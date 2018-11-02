---
title: Managing packages
seo-title: Managing packages
description: Managing packages
seo-description: Administrators can define packages to exchange resources between different Adobe Campaign instances through structured XML files.
uuid: 6aa9cedb-38cd-45aa-98a6-f1d999859473
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/automating/using/managing-packages
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-25T09 30 00.209-0400
cq-lastreplicated: 2018-07-23T05 57 56.747-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: importing-and-exporting-data
cq-template: /apps/help/templates/article-3
discoiquuid: 378c72ac-13ab-4014-a6b5-d9d7238407a6
firstPublishExternalDate: 2018-07-23T05:57:56.673-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 27.347-0400
jcr-createdby: admin
jcr-description: Managing packages
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T05:57:56.673-0400
lochandoffdate: 2018-07-25T09 30 00.209-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Managing packages
publishexternaldate: 2018-07-23T05 57 56.673-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/automating/using/managing-packages.html
sha1: 0228a2bd1786d5fba55a55c86baf5999d8c1c9ed
topicBrowsingSortDate: 2018-07-23T05:57:56.673-0400
index: y
internal: n
snippet: y
---

# Managing packages

Managing packages

Administrators can define packages to exchange resources between different Adobe Campaign instances through structured XML files. These can be configuration parameters or data.

This may be useful for transferring data from one server to another or for replicating the configuration of an instance.

Packages are available under the **Administration** &gt; **Deployment** > **Package exports** or **Package imports** menus. The two menus function similarly.

The elements of each list are displayed by default according to their modification or installation date, from the most recent to the least recent.

![](assets/packages_1.png)

To display and modify the content of an element, click its label. Refer to the [Exporting a package](../../automating/using/managing-packages.md#exporting-a-package) and [Importing a package](../../automating/using/managing-packages.md#importing-a-package) sections.

## Package exports

### Standard packages

**Platform** and **Administration** are two built-in packages, each containing a predefined list of resources to be exported. They can be opened in read-only mode and they are only suitable for exporting.

![](assets/packages_14.png)

>[!CAUTION]
>
>Exporting packages is not authorized if the resources exported have default IDs. Therefore, the IDs of exportable resources must be changed by using a name that is different from the templates provided as standard by Adobe Campaign Standard. For example, to export test profiles, an ID containing the value "SDM" or "sdm" must not be used. When trying to export packages containing default IDs, you can see errors such as: "The 'Brands (branding)' entity type uses a default ID ('BRD1') that may cause a conflict when importing the package. Change this name and repeat the operation."

The package export steps are described in the [Exporting a package](../../automating/using/managing-packages.md#exporting-a-package) section.

* The **Platform** package regroups all the resources added during technical configuration: custom resources, custom resource sets, triggers, and application options with the **System** type.
* The **Administration** package regroups all the objects added during business configuration such as: campaign templates, content templates, delivery templates, landing page templates, program templates and workflow templates.

  It also includes the following objects: content blocks, target mappings, external accounts, geographical and organizational units, application options with the **User** type, roles, typologies, typology rules and users.

>[!NOTE]
>
>The contents of these two packages cannot me modified. In contrast, these packages always contain the most up-to-date data available. You can [create your own packages](../../automating/using/managing-packages.md#creating-a-package) to export specific elements.

### Creating a package

You need to create a package if you need to export specific sets of data.

To create a package, you need the administration rights.

1. From **Administration** &gt; **Deployment** > **Package exports**, click the **Create** button in the list of package contents.

   The element is created immediately. To cancel creating it, go back to the list and check the corresponding box to delete it.

1. In the package content screen, specify a name and an ID.
1. Click the **Edit properties** button if you would like to add a description and restrict access to certain users.

   ![](assets/packages_18.png)

1. Use the **Create element** button in the **Export content** tab to select the resources you wish to export.

   ![](assets/packages_2.png)

1. Resources are shown in alphabetical order and can be filtered by name. Their technical name is displayed in brackets. Select an element from the list and confirm.

   ![](assets/packages_3.png)

1. The resource name is displayed in the **Export content** tab. To modify a resource, check the corresponding box and use the **Show detail of the element selected** button.

   ![](assets/packages_4.png)

1. Using the query editor allows you to filter the elements to be exported. For more on this, refer to the [Editing queries](../../automating/using/editing-queries.md#creating-queries) section.

   ![](assets/packages_5.png)

   >[!NOTE]
   >
   >You can export up to 5000 objects per resource.

1. Once you have specified all the resources to be exported, save your selection.

Your package is now created and is ready to be exported.

### Exporting a package

Exporting a package allows you to save a specific state of a resource that you will be able to reimport on another instance or later on the same instance.

>[!CAUTION]
>
>Exporting packages is not authorized if the resources exported have out-of-the-box IDs. Therefore, the IDs of exportable resources must be changed by using a name that is different from the templates provided as standard by Adobe Campaign Standard. For example, to export test profiles, an ID containing the value "SDM" or "sdm" must not be used.

1. From **Administration** &gt; **Deployment** > **Package exports**, select a package to access its detail.
1. Check that the package contains the data you need.
1. Click the **Start export** button.

The exported file is stored in the download folder of the browser in use. It is automatically named "package_xxx.xml", whereby "xxx" corresponds to the package ID.

When the operation has finished, several sections appear:

* **Export status**: this section shows whether the operation has been carried out correctly.

  ![](assets/packages_6.png)

* You can consult the different steps of the export via the **Log** tab. This contains the statuses of all the former exports.

  ![](assets/packages_7.png)

>[!NOTE]
>
>When selecting an element from the package content list that has already been exported, the **Log** and **Last export** tabs are still available.

## Package imports

### System updates

The package import list above anything contains the automatic imports linked to updates performed by Adobe.

![](assets/packages_15.png)

The **Execution logs** tab stores all of the import steps. A side panel displays the general information.

![](assets/packages_11.png)

>[!NOTE]
>
>These elements are accessible in read-only mode.

### Importing a package

An administrator can manually import a package originating from an export executed earlier from an Adobe Campaign instance. For more on this, refer to the [Package exports](../../automating/using/managing-packages.md#package-exports) section.

The manual package import consists of two steps: first, you have to upload a file, then you can import its content.

1. From **Administration** &gt; **Deployment** > **Package imports**, click the **Create** button in the package import list.

   The element is created immediately. To cancel creating it, go back to the list and check the corresponding box to delete it.

1. Specify a name and an ID for the new import.
1. Select the file you wish to upload by dragging and dropping it, or by clicking the **Select from folder** link.

   Imported files must be either XML or ZIP (containing an XML file) format.

   ![](assets/packages_16.png)

   >[!NOTE]
   >
   >To replace the uploaded document, start by deleting the file via the X icon to the right of its name, then repeat the operation.

1. Once the file is uploaded, import its content into the database by using the **Start import** button.

   ![](assets/packages_19.png)

When the operation has finished, several sections appear:

* **Import status**: this section shows whether the operation has been carried out correctly.
* You can consult the different steps of the import via the **Execution logs** tab. This is particularly important to view errors.

  ![](assets/packages_20.png)

Once a package has been imported, you cannot re-import it from the same element. You can only modify its label and ID.

To re-import the same package, you have to go back to the package import list, create an element, and then upload the selected file again.
