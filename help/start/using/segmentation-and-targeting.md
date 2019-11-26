---
title: Segmentation and targeting
description: "Learn about profiles, targeting and audience creation in Campaign: build audiences, import contacts share audiences with Experience Cloud solutions, and avoid marketing fatigue."
page-status-flag: never-activated
uuid: 71f53808-0309-49f6-a4ee-3446eac9758a
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: start
content-type: reference
topic-tags: about-adobe-campaign
discoiquuid: d8c8a318-9433-4aec-b378-fd0beb50e9fb

internal: n
snippet: y
---

# Segmentation and targeting{#segmentation-and-targeting}

## Profiles {#profiles}

Use Adobe Campaign’s flexible data model to enrich your customer profile data and add new attributes or tables. Then, use these customer profiles for more accurate segmentation, personalization, and reporting.

Adobe Campaign profiles represent all of the contacts stored in the database. Each profile corresponds to one entry in the database which contains the necessary information for that profile to be targeted, qualified and individually tracked. This means that a profile can be: a client, a prospect, an individual subscribed to a newsletter, a recipient, a user, or any other denomination depending on the organization.

The customer profiles feature integrates all of your customer data in one place:

![](assets/mkt_hist_view.png)

Adobe Campaign proposes various mechanisms for profile acquisition: collecting data online via [landing pages](../../channels/using/getting-started-with-landing-pages.md), manual or [automated import mechanisms](../../automating/using/about-data-import-and-export.md), [direct input](../../audiences/using/creating-profiles.md) in the Adobe Campaign interface, bulk creation through [Campaign APIs](../../api/using/about-campaign-standard-apis.md).

**Related topics:**

* Learn about different types of profiles in the [Profiles](../../audiences/using/about-profiles.md) section.
* Access the number of **Active Profiles** in your organization in [this section](../../audiences/using/active-profiles.md).
* Learn how to customize your data, handle complex data management tasks, such as calculations, aggregates, de-dupes, and merges, using [workflow targeting capabilities](../../automating/using/about-targeting-activities.md)

## Audiences {#audiences}

To enable you to deliver relevant and effective messages, and engage your customers effectively, Adobe Campaign integrates advanced analysis and targeting functionalities. Thanks to the workflows and the query editor, you can build audiences that will be targeted by your different campaigns, depending on the information that you have on them, their activities, their language, their preferences or their marketing history. This allows you to filter subscribed profiles for example, or create target audiences on an unlimited number of criteria.

Audiences are presented [in this page](../../audiences/using/about-audiences.md) and detailed in the [Audiences](../../audiences/using/creating-audiences.md) section.

**Related topics:**

* Learn how to reach multilingual audiences across multiple regions by sending [multilingual push notifications](../../channels/using/creating-a-multilingual-push-notification.md) or [multilingual emails](../../channels/using/creating-a-multilingual-email.md)
* Learn how to [create queries](../../audiences/using/creating-audiences.md#creating-query-audiences) to build audiences
* Learn how to [create list audiences](../../audiences/using/creating-audiences.md#creating-list-audiences) in a workflow
* Learn how to [import an audience from a file](../../audiences/using/creating-audiences.md#creating-file-audiences) in a workflow
* Learn how to [share audiences](../../audiences/using/creating-audiences.md#creating-experience-cloud-audiences) with Experience Cloud solutions

## General Data Protection Regulation {#general-data-protection-regulation}

GDPR is the European Union’s (EU) new privacy law that harmonizes and modernizes data protection requirements. GDPR applies to Adobe Campaign customers who hold data for Data Subjects residing in the EU. In addition to the privacy capabilities already available in Adobe Campaign (including consent management, data retention settings, and user roles), we are taking this opportunity in our role as a Data Processor to include additional capabilities, to help facilitate your readiness as a Data Controller for certain GDPR requests.

Refer to this [guide](https://docs.campaign.adobe.com/doc/standard/getting_started/en/ACS_GDPR.html) to learn more about the tools and functionalities that Adobe Campaign provides to help you become GDPR compliant.

## Fatigue management {#fatigue-management}

Fatigue rules allow marketers to set global cross-channel business rules that will automatically exclude over-solicited profiles from campaigns.

To implement fatigue rules, you define a maximum number of messages per profile and select a period on which the rule will apply. During delivery preparation, profiles are excluded from the delivery if applicable, depending on the number of messages already sent to them.

**Related topics:**

* Learn how to [design fatigue rules](../../administration/using/fatigue-rules.md#examples) through a set of samples
* Learn how to create [typology rules](../../administration/using/about-typology-rules.md)
* Use [filter rules](../../administration/using/filtering-rules.md) to refine the audience of your messages
