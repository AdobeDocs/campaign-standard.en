---
title: Resource statuses
seo-title: Resource statuses
description: Resource statuses
seo-description: Discover the different resource statuses according to their publication state.
uuid: 3aed73cc-5c97-455b-84f5-13c05a527326
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: about-custom-resources
discoiquuid: c1ffda41-e88b-42b8-8a00-ce6f83a92fff
index: y
internal: n
snippet: y
---

# Resource statuses{#resource-statuses}

Resource statuses

Resources can have different statuses according to their publication or activation status.

There are two columns dedicated to displaying these statuses in the **[!UICONTROL Custom resources]** screen.

![](assets/schema_colonne_1.png)

**Publication statuses**

* **Draft**: the resource has just been created or re-drafted. To create the database tables as well as the corresponding APIs the resource must be republished. If a resource is being re-drafted, it is automatically rendered inactive following the publication step.
* **Pending re-draft**: the resource was re-drafted. The re-draft process will occur during the next publication. Re-drafting is irreversible. Several warning messages warn the user of this fact both when re-drafting, then when preparing to publish.

  For more on re-drafting, see [Deleting a resource](../../developing/using/deleting-a-resource.md).

  >[!NOTE]
  >
  >The **[!UICONTROL Cancel re-draft]** option is available when the resource that you want to re-draft still contains links through other resources with the "Published" status. This option allows you to revert the "re-draft" process. The custom resources will then go back to their original statuses.

* **Published**: the resource has been published. If the resource is modified after the last modified date, then a message appears asking the user to republish in order to take into account the latest modifications.

The **[!UICONTROL Do not publish latest modifications]** field prevents modifications from being taken into account during future publications.

This field can be configured in the custom resource definition.
