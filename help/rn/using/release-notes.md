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

Adobe Campaign Standard 24.1 uses the HTTP v1 APIs to send Android Push Notification Messages, to ensure compatibility with upcoming FCM changes. Learn more in [this technote](../../administration/using/push-technote.md).

Adobe Campaign Standard 24.1 now supports p8 authentication certificates for iOS push notifications. Your implementation must be adapted to activate these changes. Learn more in [this technote](../../administration/using/push-technote.md). 

Starting on June 1, 2024, Google and Yahoo! will be requiring senders to comply with One-Click List-Unsubscribe. Campaign now supports this capability out-of-the-box. Learn more in [this section](../../administration/using/configuring-email-channel.md#list-of-email-smtp-parameters).

### Fixes {#e-rn-fixes}

* Fixed an issue which was preventing the bounced email addresses from being removed from quarantine after 30 days. (CAMP-52977)
* Fixed an issue which stopped the Delivery Alerting workflow with the following error: `division by zero`. (CAMP-49786)

