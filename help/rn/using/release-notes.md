---
title: Latest Release Notes
description: This page details content of the latest Campaign Standard release
feature: Overview
role: User
level: Beginner
exl-id: e1f55a9b-be51-4f57-8719-fed7efc89113
---

# Latest Release Notes {#latest-release}

<!--
![Control Panel](assets/do-not-localize/cp-icon.png) **New Control Panel release**. [Learn more](https://experienceleague.adobe.com/docs/control-panel/using/release-notes.html){target="_blank"}.-->


## Early release notes {#e-new-release}

This section lists improvements and changes included in the next Campaign Standard release.

>[!CAUTION]
>
>This content is subject to changes without prior notice until the stage environments upgrade date. Learn more in the [Release planning page](../../rn/using/release-planning.md).

### Release 25.1 - 2025 Winter Release {#winter-25}

#### Security fixes {#winter-25-security}

* This release brings security fixes.
* This release comes with the following security upgrade: Apache Tomcat has been upgraded to v10.1.33.

#### Other fixes {#winter-25-fixes}

* Fixed a duplicate problem in templates (CAMP-56340)
* Fixed a tracking regression when dynamic URLs were used in Adobe Experience Manager templates (CAMP-51932)
* Fixes a performance issue on the billing process (CAMP-56796)
* Fixed an HTML encoding issue with the `>` character on JSSP web pages (CAMP-56497)
* Fixed an issue in Dynamic reporting when using **Display on selected rows** option (CAMP-55895)


## Release 24.2 - 2024 Summer Release (LA) {#summer-24}

### Improvement {#summer-24-rn-improvements}

**Migration to OAuth Server-to-Server credential**

Starting this version, with the Service Account (JWT) credential being deprecated by Adobe, Campaign outbound integrations with Adobe solutions and apps now rely on OAuth Server-to-Server credential. Adobe will perform the JWT to OAuth migration for your outbound integrations, such as Campaign-Analytics integration or Experience Cloud Triggers integration.
    
If you have implemented inbound integrations with Campaign, and if you are using [Campaign APIs](../../api/using/get-started-apis.md), you must migrate your Technical Account as detailed in [this documentation](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/){target="_blank"}. Existing Service Account (JWT) credentials will stop working on **January 27, 2025**. 

### Fixes {#summer-24-rn-fixes}

* Fixed an issue which caused the workflow scheduler to start before scheduled time. (CAMP-55412)
* Fixed an issue which caused an error when duplicating custom fields in transactional push notifications. (CAMP-54459)
* Fixed issues which affected the usability of the time and date scheduler for In-App messaging. (CAMP-54495)
* Fixed an issue which caused tracking to not work when utilizing the Custom Tracking Alias Feature and the entire link is dynamic. (CAMP-56044)
* Fixed an issue which caused a limited number of templates to show up when using search to find specific templates. (CAMP-55273)
* Added the following languages to the preferred language drop-down list: en_kz (English - Kazakhstan) and en_ua (English - Ukraine). (CAMP-55336)
* Fixed an issue which caused the time adjustment buttons to not work in scheduler settings. (CAMP-53602)
* Fixed several user interface issues regarding the time adjustment bar in scheduler settings. (CAMP-55291)
