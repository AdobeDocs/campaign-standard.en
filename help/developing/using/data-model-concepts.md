---
title: Data model concepts
seo-title: Data model concepts
description: Data model concepts
seo-description: Learn about the Adobe Campaign data model and how to modify it.
uuid: 3c68791f-2b09-4be3-b0a5-d8b36cff0cbc
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: about-custom-resources
discoiquuid: eb1a6eb0-a4f2-4194-aa7d-9f0632d894f5
index: y
internal: n
snippet: y
---

# Data model concepts{#data-model-concepts}

Adobe Campaign comes with a pre-defined data model. This data model can be modified by [administrators](../../administration/using/types-of-users.md#functional-administrators) who are able to add new resources or extensions to existing resources.

>[!CAUTION]
>
>Creating and modifying resources are sensitive operations which must be performed by expert users only.

The **[!UICONTROL Administration]** > **[!UICONTROL Development]** menu, accessed via the Adobe Campaign logo, allows you to manage your **custom resources**, **publish** them, and **access the diagnostic tools**.

The data used by Adobe Campaign is defined through different resources.

You can **enrich the data template** that is provided by creating your own custom resources, such as purchase or product tables.

Out-of-the-box resources (such as campaigns, emails, or audiences) cannot be modified. However, custom resources can be extended to add new fields.

>[!NOTE]
>
>You can find a datamodel representation for the out-of-the-box resources [here](https://docs.campaign.adobe.com/doc/standard/en/datamodel/datamodel.html).

You can also **configure the navigation** in the screens corresponding to the resource created.

Extension fields are generated with a prefix so that they never conflict with the out-of-the-box fields.
