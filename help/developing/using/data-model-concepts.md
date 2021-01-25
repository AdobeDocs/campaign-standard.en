---
solution: Campaign Standard
product: campaign
title: Data model concepts
description: Learn about the Adobe Campaign data model and how to modify it.
audience: developing
content-type: reference
topic-tags: about-custom-resources
context-tags: cusResource,overview;eventCusResource,overview
---

# Data model concepts{#data-model-concepts}

Adobe Campaign comes with a pre-defined data model. This data model can be modified by [administrators](../../administration/using/users-management.md#functional-administrators) who are able to add new resources or extensions to existing resources.

>[!CAUTION]
>
>Creating and modifying resources are sensitive operations which must be performed by expert users only.

The **[!UICONTROL Administration]** > **[!UICONTROL Development]** menu, accessed via the Adobe Campaign logo, allows you to manage your **custom resources**, **publish** them, and **access the diagnostic tools**.

The data used by Adobe Campaign is defined through different resources. You can **enrich the data template** that is provided by creating your own custom resources, such as purchase or product tables.

Built-in resources (such as campaigns, emails, or audiences) cannot be modified. However, custom resources can be extended to add new fields.

Extension fields are generated with a prefix so that they never conflict with the built-in fields.

>[!NOTE]
>
>You can find a datamodel representation for the built-in resources in [this page](../../developing/using/datamodel-introduction.md).

You can also [configure the navigation](configuring-the-screen-definition.md) in the screens corresponding to the resource created.

It is possible to **export and import** custom resources, for example from a development to a production environment. For more on this, refer to this [step-by-step use case](../../automating/using/exporting-importing-custom-resources.md).

>[!CAUTION]
>
>Only Functional [administrators](../../administration/using/users-management.md#functional-administrators), with **[!UICONTROL Administration]** role and access to **All** units can access sending logs, message logs, tracking logs, exclusion or subscription logs. A non-admin user can target these logs but starting on a linked table (profiles, delivery).
