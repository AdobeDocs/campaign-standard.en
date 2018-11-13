---
title: "Step 5: Update the database structure"
seo-title: "Step 5: Update the database structure"
description: "Step 5: Update the database structure"
seo-description: Discover how to update the Adobe Campaign database.
uuid: 57686637-42d6-4859-af1f-4007ac676fba
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/developing/using/step-5--update-the-database-structure
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-10T02 19 00.675-0400
cq-lastreplicated: 2018-09-07T14 53 58.784-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: adding-or-extending-a-resource
cq-template: /apps/help/templates/article-3
discoiquuid: ed860878-e499-4f18-8e5b-7c6c357d31ed
firstPublishExternalDate: 2018-09-07T14:53:56.680-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 03 02.614-0400
jcr-createdby: admin
jcr-description: Step 5  Update the database structure
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T14:53:56.680-0400
lochandoffdate: 2018-09-10T02 19 00.674-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: "Step 5: Update the database structure"
publishexternaldate: 2018-09-07T14 53 56.680-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/developing/using/step-5--update-the-database-structure.html
sha1: f29b5f45e29b35dba7a96f0473d93dc3f7b2105c
topicBrowsingSortDate: 2018-09-07T14:53:56.680-0400
index: y
internal: n
snippet: y
---

# Step 5: Update the database structure{#step-update-the-database-structure}

Step 5: Update the database structure

To make your modifications to the data model effective and to be able to use them, the database structure needs to be updated.

>[!NOTE]
>
>Custom resources are automatically refreshed during automatic updates performed by Adobe.

## Publishing a custom resource {#publishing-a-custom-resource}

To apply the changes carried out on the resources, you must perform a database update.

>[!NOTE]
>
>If a field of a custom resource used on an event is modified or deleted, the corresponding event will automatically be unpublished. See [Configuring Transactional messaging](../../administration/using/configuring-transactional-messaging.md).

1. From the advanced menu, via the Adobe Campaign logo, select **Administration** > **Development**, then **Publication**.

   ![](assets/schema_extension_12.png)

1. By default, the option **Determine modifications since the last publication** is checked, which means that only the changes carried out since the last update will be applied.

   >[!NOTE]
   >
   >The **Repair database structure** reestablishes a correct configuration if the publication failed before completing. Any modification that was carried out directly in the database and not using custom resources will be deleted.

1. Click the **Prepare publication** button to start the analysis.

   ![](assets/schema_extension_13.png)

1. Once the publication has been carried out, click the **Publish** button to apply your new configurations.
1. Once published, the **Summary** pane of each resource indicates that the status is now **Published** and specifies the date of the last publication.

   >[!NOTE]
   >
   >If you make new changes to a resource, you must repeat this operation for the changes to be applied.

   If resources have the **Pending re-draft** status before publishing, then an additional message will appear inviting you to check your actions because publishing will result in definitive changes (deleting columns, tables...). To help you carry out this last change, an **SQL Script** tab is available. It provides the SQL command that will be executed during the publication. 

   ![](assets/schema_extension_scriptSQL.png)

   >[!NOTE]
   >
   >You can stop the Re-draft process by clicking the **Cancel re-draft** button. This action will revert the resource's status back to its original one.

## Publishing a resource with API extension {#publishing-a-resource-with-api-extension}

When you extend the custom resources **Profiles** or **Services**, you can perform an update of the Profiles and Services API to integrate the fields declared in the custom resources extension.

When you define a custom resource and you create a link between the resources Profiles or Services and the custom resource, you can perform an update to include the new resource in the API.

This option is available in the publication screen.

![](assets/extendPandSAPI.png)

>[!NOTE]
>
>By default, the custom resource is integrated, but, for a specific behavior, if you don't want to publish this resource, you can select the option **Hide this resource from APIs** available in the **Resource Properties**.

After the **Prepare Publication** step, Adobe Campaign displays the delta between the current version of the API and the future version after the publication in the tab **Profiles & Services API Preview**. If you extend the API for the first time, the delta compares the out-of-the-box custom resource definition with your extension.

The information displayed in the tab is divided into three sections: added, deleted and modified elements.

![](assets/extendPandSAPI_diff.png)

The analysis of the delta is a mandatory step as the publication step will modify the API behavior and will most likely affect the surrounding development in a domino effect.

>[!NOTE]
>
>This publication updates the **profilesAndServicesExt** API. The **profilesAndSedrvices** API is not updated.

For more information on the Adobe Campaign API, consult the dedicated Adobe Campaign documentation on [Adobe IO](https://docs.campaign.adobe.com/doc/standard/en/adobeio.html).
