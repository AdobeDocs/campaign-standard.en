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
# Early release notes {#new-release}

This page describes new features, improvements and fixes included in the next Campaign Standard release.

>[!CAUTION]
>
> This content is subject to changes without prior notice until the stage environments upgrade date. Learn more in the [release planning page](../../rn/using/release-planning.md).
>

## Release 22.1 - February 2022 {#feb-2022}


**What's new?**


<table> 
<thead> 
<tr> 
<th> <strong>Security update for Apache Log4j Security Vulnerabilities</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
<td>
<p>Following the update to Apache log4j v2.17.0 release in December 2021, to ensure our customers are not impacted by possible unintended effects of introducing further change to the system outside of our normal release schedule, we have made the update internally and are getting it ready for deployment with this release.</p>
</td> 
</tr> 
</tbody> 
</table>

**Security fixes**

* New URL signature mechanism for tracking included in this release. The previous mechanism had been disabled to prevent an issue that was causing some valid, signed tracking links to be incorrectly blocked after being modified by third-party security tools. (CAMP-48983)
* Reinforce security to access application and server configuration files: JavaScript file access APIs security are now restricted to sandbox directories. (CAMP-49411)

**Improvements**

* Improved processing of reporting data to avoid over loading the system. (CAMP-47578)

**Patches**

* 
