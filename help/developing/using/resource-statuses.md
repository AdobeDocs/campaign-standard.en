---
title: Resource statuses
seo-title: Resource statuses
description: Resource statuses
seo-description: Discover the different resource statuses.
page-status-flag: never-activated
uuid: 0766640b-d502-4a40-aeef-525d3d7d8513
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/developing/using/resource-statuses
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: about-custom-resources
discoiquuid: b489e253-6f90-4338-bc3e-535ffb29fe2d
isreadyforlocalization: false
navTitle: Resource statuses
publishexternaldate: 2018-11-20
sha1: 622f48d2baf0c91c758d992ccb72f0a2d0587858
index: y
internal: n
snippet: y
---

# Resource statuses{#resource-statuses}

Resource statuses

Resources can have different statuses according to their publication or activation status.

There are two columns dedicated to displaying these statuses in the **Custom resources** screen.

![](assets/schema_colonne_1.png)

**Publication statuses**

* **Draft**: the resource has just been created or re-drafted. To create the database tables as well as the corresponding APIs the resource must be republished. If a resource is being re-drafted, it is automatically rendered inactive following the publication step.
* **Pending re-draft**: the resource was re-drafted. The re-draft process will occur during the next publication. Re-drafting is irreversible. Several warning messages warn the user of this fact both when re-drafting, then when preparing to publish.

  >[!NOTE]
  >
  >The **Cancel re-draft** option is available when the resource that you want to re-draft still contains links through other resources with the "Published" status. This option allows you to revert the "re-draft" process. The custom resources will then go back to their original statuses.

* **Published**: the resource has been published. If the resource is modified after the last modified date, then a message appears asking the user to republish in order to take into account the latest modifications.

The **Do not publish latest modifications** field prevents modifications from being taken into account during future publications.

This field can be configured in the custom resource definition.
