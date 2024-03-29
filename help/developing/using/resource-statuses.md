---
title: Resource statuses
description: Discover the different resource statuses according to their publication state.
audience: developing
content-type: reference
topic-tags: about-custom-resources

feature: Data Model
role: Developer
level: Experienced
exl-id: 7290ebc5-8a58-4b7f-99bf-d942e37c944e
---
# Resource statuses{#resource-statuses}

Depending on to their publication or activation status, resources can have different statuses.

There are two columns dedicated to displaying these statuses in the **[!UICONTROL Custom resources]** screen.

![](assets/schema_colonne_1.png)

**Publication statuses**

* **Draft**: the resource has just been created or re-drafted. To create the database tables as well as the corresponding APIs, the resource must be republished. If a resource is being re-drafted, it automatically becomes inactive after the publication step.
* **Pending re-draft**: the resource was re-drafted. The re-draft process will occur during the next publication. Re-drafting is irreversible. Several warning messages are displayed to inform the user, both when re-drafting and preparing to publish.

  For more on re-drafting, see [Deleting a resource](../../developing/using/deleting-a-resource.md).

  >[!NOTE]
  >
  >The **[!UICONTROL Cancel re-draft]** option is available when the resource that you want to re-draft still contains links through other resources with the "Published" status. This option allows you to revert the "re-draft" process. The custom resources will then go back to their original statuses.

* **Published**: the resource has been published. If the resource is modified after the last modified date, then a message is displayed to invite you to republish the resource in order to take into account the latest modifications.

The **[!UICONTROL Do not publish latest modifications]** field prevents modifications from being taken into account during future publications.

This field can be configured in the custom resource definition.
