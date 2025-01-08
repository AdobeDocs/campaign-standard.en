---
title: Release Notes 2024
description: This page lists all 2024 releases of Adobe Campaign Standard
feature: Overview
role: User
level: Beginner
exl-id: 26616ecc-a009-485c-b13d-d4e0c23969f2
---
# Release Notes 2024 {#release-notes-2024}


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


## Release 24.1 - 2024 Winter Release {#winter-24}

### Improvements {#e-rn-improvements}

* **Android Push Notifications** - Adobe Campaign Standard 24.1 uses the HTTP v1 APIs to send Android Push Notification Messages, to ensure compatibility with upcoming FCM changes. Learn more in [this technote](../../administration/using/push-technote.md).

* **iOS Push Notifications** - Adobe Campaign Standard 24.1 now supports p8 authentication certificates for iOS push notifications. Your implementation must be adapted to activate these changes. Learn more in [this technote](../../administration/using/push-technote.md). 

* **One-Click List-Unsubscribe** - Starting on June 1, 2024, Google and Yahoo! will be requiring senders to comply with One-Click List-Unsubscribe. Campaign now supports this capability out-of-the-box. Learn more in [this section](../../administration/using/configuring-email-channel.md#list-of-email-smtp-parameters).

* **Infrastructure** - The Postgres database has been upgraded from version 11.22 to version 12.17.

* **CTA tracking** - When the users open and click on a personalized URL, the resolved personalized URL is now tracked instead of the coded personalized URL. This change is not enabled by default. To have it enabled on your Campaign instance, contact your Adobe representative.

* **Personalization fields drop down** - When creating transactional email message templates in Adobe Experience Manager, you can now select personalization fields from a dropdown list. This change is not enabled by default. To have it enabled on your Campaign instance, contact your Adobe representative.

### Fixes {#e-rn-fixes}

* Fixed an issue which was preventing the bounced email addresses from being removed from quarantine after 30 days. (CAMP-52977)
* Fixed an issue which stopped the Delivery Alerting workflow with the following error: `division by zero`. (CAMP-49786)
