---
title: "Optional: Deleting a resource"
seo-title: "Optional: Deleting a resource"
description: "Optional: Deleting a resource"
seo-description: 
uuid: d58d88c3-c6a0-4e5c-a7d3-11f0aa65ae3b
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: adding-or-extending-a-resource
discoiquuid: 804e952c-2c4b-4002-a8b9-43e48274945b
isreadyforlocalization: false
index: y
internal: n
snippet: y
---

# Optional: Deleting a resource{#optional-deleting-a-resource}

Optional: Deleting a resource

To delete a resource, the resource in question must be a **[!UICONTROL Draft]** . The resource is in **[!UICONTROL Draft]** status if:

* It has just been created and has not yet been published.
* If it has already been published, the resource has to be re-drafted.

To re-draft a published resource:

1. Select the resource.
1. Click the **[!UICONTROL Re-draft]** button in the action bar.
1. Click **[!UICONTROL Ok]** .

   >[!CAUTION]
   >
   >This action is definitive: the resource's data will be deleted when the modification is published.

1. Publish the resource.

   The resource then goes into **Draft** mode and its activation status is **[!UICONTROL Inactive]** .

1. In **[!UICONTROL List]** mode, check the resource to delete then click the  ![](assets/delete_darkgrey-24px.png)

   icon.

Your resource is deleted from the data model.

>[!NOTE]
>
>If a field of a custom resource used on an event is modified or deleted, the corresponding event will automatically be unpublished. See [Configuring Transactional messaging](../../administration/using/configuring-transactional-messaging.md).

