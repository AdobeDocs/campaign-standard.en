---
title: "Step 5: Update the database structure"
seo-title: "Step 5: Update the database structure"
description: "Step 5: Update the database structure"
seo-description: Discover how to update the Adobe Campaign database.
uuid: 0556221f-c568-4d9b-8eab-96a2f805764d
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: adding-or-extending-a-resource
discoiquuid: a221d012-cc81-4513-9423-dc07f101bafd
isreadyforlocalization: false
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

1. From the advanced menu, via the Adobe Campaign logo, select **[!UICONTROL Administration]** > **[!UICONTROL Development]** , then **[!UICONTROL Publication]** .

   ![](assets/schema_extension_12.png)

1. By default, the option **[!UICONTROL Determine modifications since the last publication]** is checked, which means that only the changes carried out since the last update will be applied.

   >[!NOTE]
   >
   >The **[!UICONTROL Repair database structure]** reestablishes a correct configuration if the publication failed before completing. Any modification that was carried out directly in the database and not using custom resources will be deleted.

1. Click the **[!UICONTROL Prepare publication]** button to start the analysis.

   ![](assets/schema_extension_13.png)

1. Once the publication has been carried out, click the **[!UICONTROL Publish]** button to apply your new configurations.
1. Once published, the **[!UICONTROL Summary]** pane of each resource indicates that the status is now **[!UICONTROL Published]** and specifies the date of the last publication.

   >[!NOTE]
   >
   >If you make new changes to a resource, you must repeat this operation for the changes to be applied.

   If resources have the **[!UICONTROL Pending re-draft]** status before publishing, then an additional message will appear inviting you to check your actions because publishing will result in definitive changes (deleting columns, tables...). To help you carry out this last change, an **[!UICONTROL SQL Script]** tab is available. It provides the SQL command that will be executed during the publication. 

   ![](assets/schema_extension_scriptSQL.png)

   >[!NOTE]
   >
   >You can stop the Re-draft process by clicking the **[!UICONTROL Cancel re-draft]** button. This action will revert the resource's status back to its original one.

## Publishing a resource with API extension {#publishing-a-resource-with-api-extension}

When you extend the custom resources **[!UICONTROL Profiles]** or **[!UICONTROL Services]** , you can perform an update of the Profiles and Services API to integrate the fields declared in the custom resources extension.

When you define a custom resource and you create a link between the resources Profiles or Services and the custom resource, you can perform an update to include the new resource in the API.

This option is available in the publication screen.

![](assets/extendPandSAPI.png)

>[!NOTE]
>
>By default, the custom resource is integrated, but, for a specific behavior, if you don't want to publish this resource, you can select the option **[!UICONTROL Hide this resource from APIs]** available in the **[!UICONTROL Resource Properties]** .

After the **[!UICONTROL Prepare Publication]** step, Adobe Campaign displays the delta between the current version of the API and the future version after the publication in the tab **[!UICONTROL Profiles & Services API Preview]** . If you extend the API for the first time, the delta compares the out-of-the-box custom resource definition with your extension.

The information displayed in the tab is divided into three sections: added, deleted and modified elements.

![](assets/extendPandSAPI_diff.png)

The analysis of the delta is a mandatory step as the publication step will modify the API behavior and will most likely affect the surrounding development in a domino effect.

>[!NOTE]
>
>This publication updates the **[!UICONTROL profilesAndServicesExt]** API. The **[!UICONTROL profilesAndSedrvices]** API is not updated.

For more information on the Adobe Campaign API, consult the dedicated Adobe Campaign documentation on [Adobe IO](https://docs.campaign.adobe.com/doc/standard/en/adobeio.html).
