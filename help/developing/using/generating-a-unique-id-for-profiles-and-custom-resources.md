---
title: Generating a unique ID for profiles and custom resources
seo-title: Generating a unique ID for profiles and custom resources
description: Generating a unique ID for profiles and custom resources
seo-description: 
uuid: 2132998b-acd5-47e4-9f75-00027d64c0c0
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/developing/using/generating-a-unique-id-for-profiles-and-custom-resources
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-26T02 53 35.449-0400
cq-lastreplicated: 2018-07-23T05 59 14.444-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: adding-or-extending-a-resource
cq-template: /apps/help/templates/article-3
discoiquuid: 63f70526-df51-498a-b785-46b02a34219e
firstPublishExternalDate: 2018-07-23T05:59:14.387-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 36.518-0400
jcr-createdby: admin
jcr-description: Generating a unique ID for profiles and custom resources
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T05:59:14.387-0400
lochandoffdate: 2018-07-26T02 53 35.448-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Generating a unique ID for profiles and custom resources
publishexternaldate: 2018-07-23T05 59 14.387-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/developing/using/generating-a-unique-id-for-profiles-and-custom-resources.html
sha1: cd74c20568200cd27e549f9b9b7e03fdd2a72df5
topicBrowsingSortDate: 2018-07-23T05:59:14.387-0400
index: y
internal: n
snippet: y
---

# Generating a unique ID for profiles and custom resources

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

