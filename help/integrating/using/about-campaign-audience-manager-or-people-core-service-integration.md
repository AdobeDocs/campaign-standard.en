---
title: About Campaign-Audience Manager or People core service integration
seo-title: About Campaign-Audience Manager or People core service integration
description: About Campaign-Audience Manager or People core service integration
seo-description: With the Audience Manager / People core service integration, you can share audiences or segments within the different Adobe Experience Cloud solutions.
uuid: ef9d83d4-c29a-4600-8dea-3fea12ce77f4
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-audience-manager-or-people-core-service
discoiquuid: c832ca5b-4f9c-4acf-9ab2-355da07e9681
isreadyforlocalization: false
index: y
internal: n
snippet: y
---

# About Campaign-Audience Manager or People core service integration{#about-campaign-audience-manager-or-people-core-service-integration}

About Campaign-Audience Manager or People core service integration

Adobe Campaign allows you to exchange and share audiences/segments with the different Adobe Experience Cloud applications. Integrating **Adobe Campaign** with **People core service** (also known as **Profiles & Audiences core service**) or Adobe Audience Manager allows you to:

* Import audiences/segments from different Adobe Experience Cloud solutions into Adobe Campaign. Audiences can be imported from the **[!UICONTROL Audiences]** menu in Adobe Campaign.
* Export audiences as shared audiences/segments. These audiences can be used in the different Adobe Experience Cloud solutions that you use. Audiences can be exported after targeting activities in a workflow, using the **[!UICONTROL Save audience]** activity.

Integration supports two types of Adobe Experience Cloud IDs:

* **Visitor ID**: this type of ID allows you to reconcile Adobe Experience Cloud visitors with Adobe Campaign profiles.
* **Declared ID**: this type of ID allows you to reconcile any type of data with profiles in the Adobe Campaign database. This integration supports regular declared IDs, hashed declared IDs and encrypted declared IDs.

  Encryption allows you to share encrypted data in data sources (for example PII) using the declared ID by specifying the encryption algorithm.

  For example, with the ability to decrypt encrypted email addresses or SMS numbers, you can also send triggered messages to your users even if their profile does not exist in the Adobe Campaign database.

>[!CAUTION]
>
>Depending on the data exchanged, importing audiences in Adobe Campaign may be subject to legal restrictions

