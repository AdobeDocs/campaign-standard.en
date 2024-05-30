---
title: Latest Release
description: This page details content of the latest Campaign Standard release
feature: Overview
role: User
level: Beginner
exl-id: e1f55a9b-be51-4f57-8719-fed7efc89113
---

# Latest Release{#latest-release}

<!--
![Control Panel](assets/do-not-localize/cp-icon.png) **New Control Panel release**. [Learn more](https://experienceleague.adobe.com/docs/control-panel/using/release-notes.html){target="_blank"}.-->

## Release 24.1 - 2024 Winter Release {#winter-24}

### Improvements {#e-rn-improvements}

* **Android Push Notifications** - Adobe Campaign Standard 24.1 uses the HTTP v1 APIs to send Android Push Notification Messages, to ensure compatibility with upcoming FCM changes. Learn more in [this technote](../../administration/using/push-technote.md).

* **iOS Push Notifications** - Adobe Campaign Standard 24.1 now supports p8 authentication certificates for iOS push notifications. Your implementation must be adapted to activate these changes. Learn more in [this technote](../../administration/using/push-technote.md). 

**One-Click List-Unsubscribe** - Starting on June 1, 2024, Google and Yahoo! will be requiring senders to comply with One-Click List-Unsubscribe. Campaign now supports this capability out-of-the-box. Learn more in [this section](../../administration/using/configuring-email-channel.md#list-of-email-smtp-parameters).

* **Infrastructure** - The Postgres database has been upgraded from version 11.22 to version 12.17.

* **CTA tracking** - When the users open and click on a personalized URL, the resolved personalized URL is now tracked instead of the coded personalized URL. This change is not enabled by default. To have it enabled on your Campaign instance, contact your Adobe representative.

* **Personalization fields drop down** - When creating transactional email message templates in Adobe Experience Manager, you can now select personalization fields from a dropdown list. This change is not enabled by default. To have it enabled on your Campaign instance, contact your Adobe representative.

### Fixes {#e-rn-fixes}

* Fixed an issue which was preventing the bounced email addresses from being removed from quarantine after 30 days. (CAMP-52977)
* Fixed an issue which stopped the Delivery Alerting workflow with the following error: `division by zero`. (CAMP-49786)

