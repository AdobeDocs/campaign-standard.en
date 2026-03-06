---
title: Release Notes 2025
description: This page lists all 2025 releases of Adobe Campaign Standard
feature: Overview
role: User
level: Beginner
exl-id: e1f55a9b-be51-4f57-8719-fed7efc89114
---
# Release Notes 2025 {#release-notes-2025}

## Release 25.2 - 2025 Summer Release {#summer-25}

### Security fixes {#summer-25-security}

* This release brings security fixes.
* This release comes with the following security upgrade: PostgreSQL 14.18, migration from CentOS to Rocky for Azure instances.

### Other fixes {#summer-25-fixes}

* Improved handling of sequence exhaustion to enhance system reliability. (CAMP-57281)
* General product stabilization updates. (CAMP-57339)
* Improved Dynamic Reporting for better robustness and reduced data mismatches. (CAMP-58157)
* Fixed an issue where drop-down menus did not wrap text correctly. (CAMP-57360)
* Updated reporting functionality to prevent users from querying data older than 2 years. (CAMP-59262)

## Release 25.1.2 {#25.1.2}

### Security fixes {#25.1.2-security}

* This release brings security fixes.
* This release comes with the following security upgrade: Apache Tomcat has been upgraded to v10.1.36.

### Other fixes {#25.1.2-fixes}

* Fixed a token parsing issue that could prevent users from logging in via IMS. (CAMP-57337)
* The auto sequence ID generation mechanism has been improved to enhance system reliability. (CAMP-57281)

## Release 25.1 - 2025 Winter Release {#winter-25}

### Security fixes {#winter-25-security}

* This release brings security fixes.
* This release comes with the following security upgrade: Apache Tomcat has been upgraded to v10.1.33.

### Other fixes {#winter-25-fixes}

 
* Fixed the 'Data Schema' URL in subscription summary screen (CAMP-56168, CAMP-56296)
* Fixed an issue to bypass the fatigue rules when the **Message to be sent immediately** option is used (CAMP-56866, CAMP-57033)
* Fixed a duplicate problem in templates (CAMP-56340)
* Fixed a tracking regression when dynamic URLs were used in Adobe Experience Manager templates (CAMP-51932)
* Fixed a performance issue on the billing process (CAMP-56796)
* Fixed an HTML encoding issue with the `>` character on JSSP web pages (CAMP-56497)
* Fixed an issue in Dynamic reporting when using **Display on selected rows** option (CAMP-55895)

