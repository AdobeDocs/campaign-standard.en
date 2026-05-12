---
title: Get started with profiles and audiences
description: Define targeted populations, select audiences, filter recipients, collect data and update profiles.
audience: audiences
content-type: reference
topic-tags: about-profiles-and-audiences
feature: Profiles
role: User
level: Beginner
exl-id: b4de2f1a-09ec-486d-b1ef-66208cbe211f
TQID: https://experienceleague.adobe.com/SC-25nzjfan6OmPZny5QnaeheMiHf2OiJXO9SGVimfo
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
feature_v2:
  - id: a075b2c1-7748-4328-b7f6-343aa314616a
    internal-label: Campaigns
  - id: a658c786-869b-4194-a780-2594d663adda
    internal-label: Data management
  - id: afa4204e-6d08-4e29-bc35-26aafb656d48
    internal-label: Profiles and audiences
subfeature_v2:
  - id: af6750fd-3c1b-4ad2-9fe3-99e81510998d
    internal-label: Data retention
  - id: d6330382-c886-4f7a-a4f7-74e3f36c0d9c
    internal-label: Audiences
  - id: f5293531-9312-4099-bfa3-9e67df6a8750
    internal-label: Query Editor
  - id: f529d0bd-1401-4c88-9833-43228cc1d40f
    internal-label: Profiles
  - id: fcb46c0f-76e1-48bc-9dd0-fcf9d97526cf
    internal-label: Workflows
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
    internal-label: Data management
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
    internal-label: Customer profiles
---
# Get started with profiles and audiences{#about-profiles-and-audiences}

<table>
<tr>
<td><img src="assets/do-not-localize/icon_segment.svg" width="60px"><p><a href="#segmenting-targeting">Segmenting and targeting</a></p></td>
<td><img src="assets/do-not-localize/icon_permission.svg" width="60px"><p><a href="#permission">Permission and consent</a></p></td>
<td><img src="assets/do-not-localize/icon_privacy.svg" width="60px"><p><a href="#privacy">Privacy compliance</a></p></td></tr>
</table>

Campaign integrated customer profiles allows you to track every interaction with customers across all channels within one single view, allowing you to deliver relevant and personalized messages to your customers.

Segment your database into audiences to optimize the target of your marketing campaigns.

Manage customers permission and consent using services and landing pages to set up easy opt-in and opt-out mechanisms.

## Segmenting and targeting {#segmenting-targeting}

<img src="assets/do-not-localize/icon_segment.svg" width="60px">

When you create campaigns or messages, you can specify the target of the deliveries by selecting from contacts in Campaign database, using simple or advanced criteria, or selecting audiences.

Identify customers more effectively across all your channels using **integrated customer profiles**, **customized segments** and **control groups**. When you know your customers, interests, demographics, and channel preferences, it’s easier to create personalized experiences that get noticed.

Adobe Campaign builds rich customer profiles in real time, allowing you to deliver more relevant and personalized offers as your customer’s preferences change. In addition, Adobe Campaign integrates advanced analysis, data management and targeting functionalities to build audiences.

**Profiles** are individual contacts stored in the database. Each profile corresponds to one entry in the database which contains the necessary information for that profile to be targeted, qualified and individually tracked: Adobe Campaign can track every interaction from both online and offline channels and merge it into a single profile.

**Audiences** are lists of profiles built on a specific criteria, or set of criteria. Using workflows and the query editor, you can construct audiences that will be targeted by your marketing campaigns, depending on the information that you have on them, their activities, and their marketing history. This allows you to filter subscribed profiles, sample, or create target audiences on an unlimited number of criteria.

Read more:

* [About profiles](../../audiences/using/about-profiles.md)
* [Active profiles](../../audiences/using/active-profiles.md)
* [Managing test profiles](../../audiences/using/managing-test-profiles.md)
* [Enriching Campaign database](../../audiences/using/enriching-campaign-database.md)
* [About audiences](../../audiences/using/about-audiences.md)
* [Selecting an audience in a message](../../audiences/using/selecting-an-audience-in-a-message.md)
* [Adding a control group](../../sending/using/control-group.md)

## Permission and consent {#permission}

<img src="assets/do-not-localize/icon_permission.svg"  width="60px">

Before starting to send messages to a contact, you need to make sure that you get their permission. If not, your emails might be marked as a spam and this will impact your platform deliverability. To make sure to build a healthy profile database, secure this permission as a first step.

With Campaign, we recommend you to use **easy opt-in and opt-out mechanisms** through [services](../../audiences/using/creating-a-service.md), and [landing pages](../../channels/using/getting-started-with-landing-pages.md) to update your contact information and grow your database.

Providing **unsubscription links** in your messages will enable Profiles to be added to the denylist, when necessary, and therefore to improve your platform deliverability. For more on denylist management, refer to [About opt-in and opt-out in Campaign](../../audiences/using/about-opt-in-and-opt-out-in-campaign.md).

>[!IMPORTANT]
>
>You are required to respect the [Adobe Campaign acceptable use policy](https://www.adobe.com/legal/terms/aup.html).

Read more:

* [About subscriptions](../../audiences/using/about-subscriptions.md)
* [About opt-in and opt-out in Campaign](../../audiences/using/about-opt-in-and-opt-out-in-campaign.md)

## Privacy compliance {#privacy}

<img src="assets/do-not-localize/icon_privacy.svg" width="60px">

Adobe Campaign offers a set of tools to help you with your **Privacy Compliance** for GDPR, CCPA, and other privacy laws.

Learn more in this [this article](https://helpx.adobe.com/campaign/kb/campaign-privacy.html) about Privacy Management and the features we provide to manage Right to Access, Right to be Forgotten, consent, data retention and user roles.

Privacy and Consent in Campaign and how to manage them are presented in [this section](../../start/using/privacy.md). You will also find best best practices, to help you with your Privacy compliance when using our service.

## Additional resources

* [Ingest Adobe Experience Platform audiences into Campaign](../../integrating/using/ingest-aep-data.md)
* [Working with Microsoft Dynamics 365](../../integrating/using/d365-acs-get-started.md)
* [Adobe Shared Audiences](../../integrating/using/sharing-audiences-with-audience-manager-or-people-core-service.md)
* [Using workflows to import profiles](../../automating/using/creating-import-workflow-templates.md)
* [Profiles and audiences videos](https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/profiles-and-audiences/creating-profiles-and-audiences.html)
