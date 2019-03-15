---
title: Creating or extending the resource
seo-title: Creating or extending the resource
description: Creating or extending the resource
seo-description: Discover how to define a resource from scratch.
uuid: 1a716b90-ad82-44cd-9e51-8b8604c0d296
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: adding-or-extending-a-resource
discoiquuid: ecdbbb27-ee2c-4fba-a435-20bc3c79c73d
index: y
internal: n
snippet: y
---

# Creating or extending the resource{#creating-or-extending-the-resource}

Administrators can create a new resource from scratch or create an extension of an existing resource if you need work on data that are not part of the out-of-the-box data model.

Only the following out-of-the-box resources can be extended:

* **[!UICONTROL Campaign (campaign)]** 
* **[!UICONTROL Deliveries (delivery)]** 
* **[!UICONTROL Landing page (Landingpage)]** 
* **[!UICONTROL Profiles (profile)]** 
* **[!UICONTROL Program (program)]** 
* **[!UICONTROL Service (service)]** 
* **[!UICONTROL Subscriptions to an application (appSubscriptionRcp)]** 
* **[!UICONTROL Test profiles (seedMember)]** 
* **[!UICONTROL Workflow (workflow)]**

To create or extend a resource:

1. From **[!UICONTROL Administration]** > **[!UICONTROL Development]** > **[!UICONTROL Custom Resources]** , click the **[!UICONTROL Create]** button.
1. Choose the action you want to perform:

    * **[!UICONTROL Create a new resource]** : Enter the **[!UICONTROL Label]** and **[!UICONTROL ID]** fields. The **[!UICONTROL ID]** field is mandatory. If you leave the Label field empty, it will automatically be completed from the ID.
    
      ![](assets/schema_extension_2.png)

    * **[!UICONTROL Extend an existing resource]** : Select the resource you want to extend.
    
      ![](assets/schema_extension_10.png)

1. Click **[!UICONTROL Create]** to create the resource, which will then take on the **[!UICONTROL Draft]** status in case of new resource or the **[!UICONTROL Editing]** status in case of extension.

The new resource is created and can now be configured. For more on resource configuration, refer to [Configuring the resource's data structure](../../developing/using/configuring-the-resource-s-data-structure.md).
