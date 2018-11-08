---
title: About Campaign-Audience Manager or People core service integration
seo-title: About Campaign-Audience Manager or People core service integration
description: About Campaign-Audience Manager or People core service integration
seo-description: With the Audience Manager / People core service integration, you can share audiences or segments within the different Adobe Experience Cloud solutions.
uuid: 2aa83a0d-9c59-4b3e-81e4-ddb909c34f2a
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/integrating/using/about-campaign-audience-manager-or-people-core-service-integration
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-10T02 18 53.980-0400
cq-lastreplicated: 2018-09-07T15 06 35.759-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-audience-manager-or-people-core-service
cq-template: /apps/help/templates/article-3
discoiquuid: 3774c48e-94cd-410e-8c0c-c5d55b25acef
firstPublishExternalDate: 2018-09-07T15:06:34.603-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 36.146-0400
jcr-createdby: admin
jcr-description: About Campaign-Audience Manager or People core service integration
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T15:06:34.603-0400
lochandoffdate: 2018-09-10T02 18 53.980-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: About Campaign-Audience Manager or People core service integration
publishexternaldate: 2018-09-07T15 06 34.603-0400
publishExternalURL: "https://helpx.adobe.com/campaign/standard/integrating/using/about-campaign-audience-manager-or-people-core-service-integration.html"
sha1: 3903a9b3f2a7c3dff3906b873816981c84a9a14e
topicBrowsingSortDate: 2018-09-07T15:06:34.603-0400
index: y
internal: n
snippet: y
---

# About Campaign-Audience Manager or People core service integration{#about-campaign-audience-manager-or-people-core-service-integration}

About Campaign-Audience Manager or People core service integration

Adobe Campaign allows you to exchange and share audiences/segments with the different Adobe Experience Cloud applications. Integrating **Adobe Campaign** with **People core service** (also known as **Profiles & Audiences core service**) or Adobe Audience Manager allows you to:

* Import audiences/segments from different Adobe Experience Cloud solutions into Adobe Campaign. Audiences can be imported from the **Audiences** menu in Adobe Campaign.
* Export audiences as shared audiences/segments. These audiences can be used in the different Adobe Experience Cloud solutions that you use. Audiences can be exported after targeting activities in a workflow, using the **Save audience** activity.

Integration supports two types of Adobe Experience Cloud IDs:

* **Visitor ID**: this type of ID allows you to reconcile Adobe Experience Cloud visitors with Adobe Campaign profiles.
* **Declared ID**: this type of ID allows you to reconcile any type of data with profiles in the Adobe Campaign database. This integration supports regular declared IDs, hashed declared IDs and encrypted declared IDs.

  Encryption allows you to share encrypted data in data sources (for example PII) using the declared ID by specifying the encryption algorithm.

  For example, with the ability to decrypt encrypted email addresses or SMS numbers, you can also send triggered messages to your users even if their profile does not exist in the Adobe Campaign database.

>[!CAUTION]
>
>Depending on the data exchanged, importing audiences in Adobe Campaign may be subject to legal restrictions

