---
title: Deleting a resource
description: Learn how to delete a resource 
audience: developing
content-type: reference
topic-tags: adding-or-extending-a-resource

feature: Data Model
role: Developer
level: Experienced
exl-id: 4ddfdbcc-a154-4c10-a97e-73ad888d1f1f
---
# Deleting a resource{#deleting-a-resource}

To delete a resource, the resource in question must be a **[!UICONTROL Draft]**. The resource is in **[!UICONTROL Draft]** status if:

* It has just been created and has not yet been published.
* If it has already been published, the resource has to be re-drafted.

>[!IMPORTANT]
>
>Re-drafting and deleting a custom resource are sensitive operations which can impact other resources. These actions must be performed by an expert user only.

To re-draft and delete a published resource:

1. Select the resource you want to re-draft.
1. Click the **[!UICONTROL Re-draft]** button in the action bar.

   ![](assets/schema_extension_uc26.png)

1. Click **[!UICONTROL Ok]**.

   >[!IMPORTANT]
   >
   >This action is definitive: the resource's database table or colums and their data will be permanently deleted when the modification is published, which can result in broken links from other custom resources. Only the resource definition will remain available.

   ![](assets/schema_extension_uc27.png)

   >[!NOTE]
   >
   >If you re-draft an extension of the out-of-the-box **Profiles (profile)** resource, you must also re-draft any **Test profile (seedMember)** extension you may have defined. For more on extending the profile resource, see [this section](../../developing/using/extending-the-profile-resource-with-a-new-field.md).

1. Publish the resource. For more detailed steps, refer to [Publishing a custom resource](../../developing/using/updating-the-database-structure.md#publishing-a-custom-resource).

   The resource then goes into **Draft** mode and its activation status is **[!UICONTROL Inactive]**.

1. In **[!UICONTROL List]** mode, check the resource to delete then click the ![](assets/delete_darkgrey-24px.png) **[!UICONTROL Delete element]** icon.

   ![](assets/schema_extension_uc28.png)

Your resource is deleted from the data model.

>[!NOTE]
>
>If a field of a custom resource used on an event is modified or deleted, the corresponding event will automatically be unpublished. See [Unpublishing a transactional event](../../channels/using/publishing-transactional-event.md#unpublishing-an-event).
