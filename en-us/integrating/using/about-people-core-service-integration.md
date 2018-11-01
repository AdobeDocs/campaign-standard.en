---
title: About People core service Integration
seo-title: About People core service Integration
description: About People core service Integration
seo-description: With the People core service integration, you can share audiences or segments within the different Adobe Marketing Cloud solutions.
page-status-flag: never-activated
uuid: 1388cedd-ae35-4c9f-ba1b-0c0289e7b00e
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/integrating/using/about-people-core-service-integration
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-01-10T15 24 08.750-0500
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: people-core-service-integration
cq-template: /apps/help/templates/article-3
discoiquuid: 2c156a04-b6f2-48e1-a136-f8946ed5628b
firstPublishExternalDate: 2018-01-10T15:24:08.743-0500
herogradient: light
jcr-created: 2018-01-11T19 02 24.702-0500
jcr-createdby: admin
jcr-description: About People core service Integration
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-01-10T15:24:08.743-0500
lr-lastreplicatedby: sauviat@adobe.com
navTitle: About People core service Integration
publishexternaldate: 2018-01-10T15 24 08.743-0500
publishExternalURL: https://helpx.adobe.com/campaign/standard/integrating/using/about-people-core-service-integration.html
sha1: d8bac4d985a2dfc2bcefde00d3230b77bf797a82
topicBrowsingSortDate: 2018-01-10T15:24:08.743-0500
index: y
internal: n
snippet: y
---

# About People core service Integration

About People core service Integration

Adobe Campaign allows you to exchange and share audiences/segments with the different Adobe Marketing Cloud applications. Integrating **Adobe Campaign** with **People core service** (also known as **Profiles & Audiences core service**) or Adobe Audience Manager allows you to:

* Import audiences/segments from different Adobe Marketing Cloud solutions into Adobe Campaign. Audiences can be imported from the **Audiences** menu in Adobe Campaign.
* Export audiences as Adobe Marketing Cloud audiences/segments. These audiences can be used in the different Adobe Marketing Cloud solutions that you use. Audiences can be exported after targeting activities in a workflow, using the **Save audience** activity.

Integration supports two types of Adobe Marketing Cloud IDs:

* **Visitor ID**: this type of ID allows you to reconcile Adobe Marketing Cloud visitors with Adobe Campaign profiles.
* **Declared ID**: this type of ID allows you to reconcile any type of data with profiles in the Adobe Campaign database. This integration supports regular declared IDs, hashed declared IDs and encrypted declared IDs.

  Encryption allows you to share encrypted data in data sources (for example PII) using the declared ID by specifying the encryption algorithm.

  For example, with the ability to decrypt encrypted email addresses or SMS numbers, you can also send triggered messages to your users even if their profile does not exist in the Adobe Campaign database.

>[!CAUTION]
>
>Depending on the data exchanged, importing audiences in Adobe Campaign may be subject to legal restrictions

