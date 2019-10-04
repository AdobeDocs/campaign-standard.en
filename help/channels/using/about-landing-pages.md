---
title: About landing pages
seo-title: About landing pages
description: About landing pages
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

# About landing pages{#about-landing-pages}

Campaign comes with landing pages which are web forms that can be used to capture information on your audiences, offer subscriptions to a service, display data and grow your database. Landing pages can also be used for acquiring or updating existing profiles.

## Landing pages life cycle {#landing-pages-life-cycle}

The full life cycle of a landing page is as follows:

1. Creation: design and set the content of the landing page.
1. Test: simulate the landing page execution on a test profile.
1. Publication: publish the landing page to push it live.
1. Expiration or depublication: unpublish manually or wait for the landing page to expire, then it is no longer available.

![](assets/lp_livecycle.png)

Once created and published, you can make the landing page accessible via a website or by [inserting a direct link to the landing page into an email](../../designing/using/links.md#inserting-a-link).

## Landing page limitations{#landing-page-limitations}

The section below lists the limitations you should be aware of, before starting setting up landing pages.

**Writing and updating data**

* Landing pages are limited to **[!UICONTROL Profile]** and **[!UICONTROL Subscription]** resources only. Record can be saved and updated from **[!UICONTROL Profile]** and a subscription/unsubscription to a **[!UICONTROL Service]**.
To learn more on resources configuration, see [Configuring the resource's data structure](../../developing/using/configuring-the-resource-s-data-structure.md).

>[!CAUTION]
>
>A landing page cannot display or update data from any other resource than **[!UICONTROL Profile]** and **[!UICONTROL Subscription]**.

**Preloading**

* Landing page cannot display a list of records automatically, it cannot list services that profiles already subscribed to. For more information on services, refer to this [page](../../audiences/using/creating-a-service.md).

* Landing page with a pre-filled form (data is preloaded with the page) can only be accessed from a Adobe Campaign email. It is not possible to access such a form from a website page.

**Reconciliation**

* The reconciliation behavior is the following: as soon as a match is found, the reconciliation process stops. This means that reconciliation can only be done on one profile record and not on multiple records when there are duplicates.

For example, you want to send the following acquisition landing page to your profiles to update your Campaign database with your profiles' mobile numbers.

![](assets/landing_page_limitation_1.png)

If one of your profile fills in your landing page with new information but has already a duplicated profile, the matching profile with the earliest creation date will be updated since profiles are prioritized depending on their creation date only.

Here only the first profile was updated since it was the oldest entry.

![](assets/landing_page_limitation_2.png)

**Testing landing page**

* Landing pages work only on profiles and not test profiles meaning that landing pages cannot be tested as part of an email proof.

**Related topics:**

* [Creating a landing page](https://helpx.adobe.com/campaign/kt/acs/using/acs-create-edit-landing-page-feature-video-use.html) video
* [Use a landing page to subscribe a service](../../audiences/using/creating-a-service.md)