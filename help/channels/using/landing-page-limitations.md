---
title: Landing page limitations
seo-title: Landing page limitations
description: Landing page limitations
seo-description: Discover Campaign landing pages and their life cycle.
page-status-flag: never-activated
uuid: b316bf47-7d98-46fa-ab4f-67ff50de8095
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: landing-pages
discoiquuid: ca8d1698-6e8a-4f5a-b017-74a152e14286
context-tags: landingPage,wizard;landingPage,overview;landingPage,main
internal: n
snippet: y
---

# Landing page limitations{#landing-page-limitations}
**Writing and Updating data**

* Landing pages are limited to **[!UICONTROL Profile]** and **[!UICONTROL Subscription]** resources only. Record can be saved and updated from **[!UICONTROL Profile]** and a subscription/unsubscription to a **[!UICONTROL Service]**. This means that a landing page cannot display or update data from any other resource.
To learn more on resources, see [Configuring the resource's data structure](../../developing/using/configuring-the-resource-s-data-structure.md).

**Preloading**

* Landing page cannot display a list of records automatically, it cannot list services that profiles already subscribed to. For more information on services, refer to this [page](../../audiences/using/creating-a-service.md).
* Landing page with a pre-filled form, data to load with the page, can only be accessed from a Adobe Campaign email. It is not possible to access such a form from a website page.


**Reconciliation**

* The reconciliation behavior is the following: as soon as a match is found, the reconciliation process stops meaning that reconciliation can only be done on one profile record and not on multiple records or duplicates. 
Profiles are prioritized depending on their creation date thus only the matching profile with the earliest creation date will be updated.

**Testing landing page**
* Landing pages work only on profiles and not test profiles meaning that landing pages cannot be tested as part of an email proof.

