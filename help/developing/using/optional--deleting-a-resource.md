---
title: "Optional: Deleting a resource"
seo-title: "Optional: Deleting a resource"
description: "Optional: Deleting a resource"
seo-description: 
page-status-flag: never-activated
uuid: 4ea57db5-dac7-458f-8eb9-c72964c9575c
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/developing/using/optional--deleting-a-resource
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: adding-or-extending-a-resource
discoiquuid: 75a654b7-2655-46cd-9d68-8b7701f6a8bc
isreadyforlocalization: false
navTitle: "Optional: Deleting a resource"
publishexternaldate: 2018-11-20
sha1: 0d42fb1fff4d25362632f4ae0b5bec26a2f821ca
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

