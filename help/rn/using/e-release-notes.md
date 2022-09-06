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
>

## Release 22.3 - Fall/Winter 2022 {#e-rn-2022}

### Improvement{#e-rn-improvements}

**Accessibility**

Campaign Standard 22.3 comes with accessibility fixes and improvements which facilitate users to navigate and get the most out of Adobe Campaign.

These capabilities are released in Limited Availability and rolled out to a set of customers only. To have these improvements enabled on your Campaign environment(s), contact your Adobe representative.

### Security update{#e-rn-security}

This release comes with the following security upgrade: Apache Tomcat has been upgraded from v7.0 to v8.0.

### Fixes{#e-rn-fixes}

* Fixed an issue with scheduled reports, which were triggered an hour prior to the scheduled timing. (CAMP-51502)
* Fixed an issue on the Delivery indicators in the Delivery dashboard which did not match Sending Logs (nms:broadLogRcp). (CAMP-51127)
* Fixed an issue which prevented custom resources extension with ACS Connector (Prime Offering). (CAMP-51033)
* Improved the publication process for Privacy requests responses to avoid delay. (CAMP-50613)