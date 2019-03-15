---
title: Deleting a resource
seo-title: Deleting a resource
description: Deleting a resource
seo-description: Learn how to delete a resource 
uuid: 99bb60f6-8695-4988-a998-3b5659d4b6aa
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: adding-or-extending-a-resource
discoiquuid: b4838904-10de-4932-a81e-cba14207e73e
index: y
internal: n
snippet: y
---

# Deleting a resource{#deleting-a-resource}

To delete a resource, the resource in question must be a **[!UICONTROL Draft]** . The resource is in **[!UICONTROL Draft]** status if:

* It has just been created and has not yet been published.
* If it has already been published, the resource has to be re-drafted.

>[!CAUTION]
>
>Re-drafting and deleting a custom resource are sensitive operations which can impact other resources. These actions must be performed by an expert user only.

To re-draft a published resource:

1. Select the resource you want to re-draft.
1. Click the **[!UICONTROL Re-draft]** button in the action bar.

   ![](assets/schema_extension_uc26.png)

1. Click **[!UICONTROL Ok]** .

   >[!CAUTION]
   >
   >This action is definitive: the resource's database table and its data will be permanently deleted when the modification is published, which can result in broken links from other custom resources. Only the resource definition will remain available.

   ![](assets/schema_extension_uc27.png)

1. Publish the resource. For more detailed steps, refer to [Publishing a custom resource](../../developing/using/updating-the-database-structure.md#publishing-a-custom-resource).

   The resource then goes into **Draft** mode and its activation status is **[!UICONTROL Inactive]** .

1. In **[!UICONTROL List]** mode, check the resource to delete then click the ![](assets/delete_darkgrey-24px.png) **[!UICONTROL Delete element]** icon.

   ![](assets/schema_extension_uc28.png)

Your resource is deleted from the data model.

>[!NOTE]
>
>If a field of a custom resource used on an event is modified or deleted, the corresponding event will automatically be unpublished. See [Configuring Transactional messaging](../../administration/using/configuring-transactional-messaging.md).

