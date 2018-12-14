---
title: "Optional: Deleting a resource"
seo-title: "Optional: Deleting a resource"
description: "Optional: Deleting a resource"
seo-description: 
page-status-flag: never-activated
uuid: e08fee17-56a0-4582-b4c0-4cbbc60c5958
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: adding-or-extending-a-resource
discoiquuid: bc84cc4e-6fb8-481d-bffc-514e0ec5659e
isreadyforlocalization: true
index: y
internal: n
snippet: y
---

# Optional: Deleting a resource{#optional-deleting-a-resource}

Optional: Deleting a resource

To delete a resource, the resource in question must be a **Draft**. The resource is in **Draft** status if:

* It has just been created and has not yet been published.
* If it has already been published, the resource has to be re-drafted.

To re-draft a published resource:

1. Select the resource.
1. Click the **Re-draft** button in the action bar.
1. Click **Ok**.

   >[!CAUTION]
   >
   >This action is definitive: the resource's data will be deleted when the modification is published.

1. Publish the resource.

   The resource then goes into **Draft** mode and its activation status is **Inactive**.

1. In **List** mode, check the resource to delete then click the  ![](assets/delete_darkgrey-24px.png)

   icon.

Your resource is deleted from the data model.

>[!NOTE]
>
>If a field of a custom resource used on an event is modified or deleted, the corresponding event will automatically be unpublished. See [Configuring Transactional messaging](../../administration/using/configuring-transactional-messaging.md).

