---
title: Generating a unique ID for profiles and custom resources
seo-title: Generating a unique ID for profiles and custom resources
description: Generating a unique ID for profiles and custom resources
seo-description: 
page-status-flag: never-activated
uuid: 64f445ba-2eb5-4412-9ed2-013744de339f
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: adding-or-extending-a-resource
discoiquuid: 41e39d86-413e-44cb-b73b-0ffd143133ce
isreadyforlocalization: true
index: y
internal: n
snippet: y
---

# Generating a unique ID for profiles and custom resources{#generating-a-unique-id-for-profiles-and-custom-resources}

Generating a unique ID for profiles and custom resources

By default, profiles and custom resources have no business ID when they are created. You can enable an option that generates automatically a unique ID when elements are created. This ID can be used to:

* Identify exported records easily in an external tool.
* Reconcile records when importing updated data processed in another application.

It can be enabled for profiles and custom resources only.

1. Create an extension to the profiles resource or create a new resource.
1. In the data structure definition, check the **Add automatic ID field** option, under the **Fields** section.
1. Save and publish the modification made to the resource. If you want this mechanism to apply for elements created via the API, check the option to extend the API.

The **ACS ID** field is now available and automatically populated when new elements are created manually, from the API, or inserted from an import workflow. The ACS ID field is a UUID field and is indexed.

When exporting profiles or custom resources, you can now add the **ACS ID** column if it has been enabled for that resource. You can reuse this ID in your external tools to identify records.

![](assets/export_id_field.png)

When re-importing data that have been processed/updated in another application (for example a CRM), you can reconcile it easily with this unique ID.

>[!NOTE]
>
>The **ACS ID** field: is not updated for profiles or elements created before activating the option. Only new records will have and ACS ID. is in read-only mode. You cannot modify it.

