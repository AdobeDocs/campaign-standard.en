---
title: Early Release Notes
description: Early Release Notes
feature: Overview
role: User
level: Beginner
hide: yes
hidefromtoc: yes
exl-id: 4b10eb63-3fea-438e-a1a7-25fbf7b0e5b0
---

# Early release notes {#e-new-release}

This page describes improvements and fixes included in the next Campaign Standard release.

>[!CAUTION]
>
> This content is subject to changes without prior notice until the stage environments upgrade date. Learn more in the [release planning page](../../rn/using/release-planning.md).

## Release 24.1 - 2024 Winter Release {#winter-24}

>[!AVAILABILITY]
>
>This release is only available for a set of organizations (Limited Availability). For more information, contact your Adobe representative.

### Improvements {#e-rn-improvements}

Adobe Campaign Standard 24.1 uses the HTTP v1 APIs to send Android Push Notification Messages, to ensure compatibility with upcoming FCM changes. Learn more in [this technote](../../administration/using/push-technote.md).

Adobe Campaign Standard 24.1 now supports p8 authentication certificates for iOS push notifications. Your implementation must be adapted to activate these changes. Learn more in [this technote](../../administration/using/push-technote.md). 


### Fixes {#e-rn-fixes}

* Fixed an issue which was preventing the bounced email addresses from being removed from quarantine after 30 days. (CAMP-52977)
* Fixed an issue which stopped the Delivery Alerting workflow with the following error: `division by zero`. (CAMP-49786)
