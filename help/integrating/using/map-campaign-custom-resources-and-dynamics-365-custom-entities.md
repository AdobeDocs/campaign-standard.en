---
title: Map Campaign custom resources and Dynamics 365 custom entities
description: Learn how to map resources and entities in the context of the integration between Adobe Campaign Standard and Microsoft Dynamics 365.
page-status-flag: never-activated
uuid: ed6c1b76-87f7-4d23-b5e2-0765297a905c
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-ms-dynamics
discoiquuid: 6c0c3c5b-b596-459e-87dd-a06bb7d633d2

internal: n
snippet: y
---

# Map Campaign resources and Dynamics 365 entities

Learn how to map custom resources and custom entities in the context of the integration between Adobe Campaign Standard and Microsoft Dynamics 365. 

>[!CAUTION]
>
>This capability is not available out of the box as part of the product. The implementation requires Adobe Consulting to be engaged. Please reach out to your Adobe representative to find out more.

## Prerequisites

The [Microsoft Dynamics 365-Adobe Campaign Standard integration](../../integrating/using/working-with-campaign-standard-and-microsoft-dynamics-365.md) supports custom entities, enabling custom entities in Dynamics 365 to be synchronized to corresponding custom resources in Campaign.

The new data in the custom resources can be used for several purposes, including segmentation and personalization.

The integration supports both linked and non-linked tables. Linking is supported up to three levels (i.e., level1->level2->level3).

>[!CAUTION]
>
>If any Campaign custom resource record contains personal information, specific recommendations apply. Learn more [in this section](../../integrating/using/notices-and-recommendations-for-acs-and-ms-dynamics.md#privacy-linked-resources).

## Notices

When configuring custom entity data flows, it is important to be aware of the following:

* Creating and modifying Campaign custom resources are sensitive operations which must be performed by expert users only.
* For custom entity data flows, change tracking must be enabled within Dynamics 365 for synchronized custom entities.
* If a parent and linked child record are created close to the same time in Dynamics 365, due to the parallel processing of the integration, there is a slight chance that a new child record could be written to Campaign before its parent record.

* If the parent and child are linked on the Campaign side using the **1 cardinality simple link** option, the child record will remain hidden and inaccessible (via UI or API) until the parent record arrives in Campaign.

* (Assuming **1 cardinality simple link** in Campaign) If the child record is updated or deleted in Dynamics 365, and that change is written to Campaign before the parent record shows up in Campaign (not likely, but a remote possibility), that update or delete will not be processed in Campaign and an error will be thrown. In the case of update, the record in question will need to be updated in Dynamics 365 again in order to sync the updated record. In the case of delete, the record in question will need to be taken care of separately on the Campaign side since there is no longer a record in Dynamics 365 to delete or update.

* If you run into a situation where you believe you have hidden child records and no way to access them, you can temporarily change the cardinality link type to **0 or 1 cardinality simple link** to access those records.

A more comprehensive overview of Campaign custom resources can be found [in this section](../../developing/using/key-steps-to-add-a-resource.md).
