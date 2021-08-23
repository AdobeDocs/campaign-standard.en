---
solution: Campaign Standard
product: campaign
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

## Release 21.3 - September 2021 {#release-21-3---sept-2021}


**What's new?**


<table> 
<thead> 
<tr> 
<th> <strong>Unified Experience Cloud interface</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
<td>
<p>Adobe Campaign header bar has been changed to unify and improve your experience across all Experience Cloud products and services. These changes are designed to make your life easier, including:</p>
<ul>
<li>Easier switching between your organizations or to a different application.</li>
<li>Improved User Help – Bringing the Experience League into the product, search results also include results from community forums and more video content, giving you easier access to more content to help get the most out of the application. We've also added a feedback mechanism right in the Help menu, making it easier to report issues or share your ideas.</li>
<li>Improved Notifications – Notifications drop-down now has two tabs: one for your own product notifications, and one for more global product announcements.</li>
</ul>
<!--<p>For more information refer to the <a href="../../start/using/interface-description.md#top-bar">detailed documentation</a>.
</p>-->
</td> 
</tr> 
</tbody> 
</table>

<table> 
<thead> 
<tr> 
<th> <strong>Audit Trail</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
<td>
<p>The new Audit Trail capability captures, in real-time, a comprehensive list of actions and events occurring within Adobe Campaign. It includes a self-serve way to access a history of data to help answer questions such as:</p>
<ul>
<li>What happened to this workflow, and who last updated it?</li>
<li>Who did the last changes?</li>
<li>What was the previous state?</li>
</ul>
<p>Adobe Campaign now audits creation, edition and deletion actions for: workflows, options, custom resources. Modifications of those items are also tracked.</p>
<!--<p>For more information refer to the <a href="../../administration/using/audit.md">detailed documentation</a>.
</p>-->
</td> 
</tr> 
</tbody> 
</table>


<table> 
<thead> 
<tr> 
<th> <strong>Workflow diagnostic mode</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
<td>
<p>You can now run Campaign workflows in diagnostic mode. This mode logs information to help troubleshooting execution issues. The whole execution plan is logged if a workflow query takes, by default, more than one minute.</p>
<!--<p>For more information refer to the <a href="../../administration/using/audit.md">detailed documentation</a>.
</p>-->
</td> 
</tr> 
</tbody> 
</table>

**Improvements**

* When creating a recurring delivery in a workflow, linked to an Adobe Experience Manager content, content approval status is now checked before sending.
* Database connection limit is now aligned with the Campaign package to avoid connection errors.
* Added a consistency check while creating indexes in custom resources and improved error message.

**Other changes**

* Adobe Experience Platform Data Connector and Audience Destinations service are now deprecated with Campaign Standard. If you are using these capabilities, you need to move to Adobe Sources and Destinations and adapt your implementation. [Learn more](../../integrating/using/get-started-sources-destinations.md)

    Deprecated and removed features are listed in [this page](deprecated-features.md).

**Patches**

* Fixed a timeout error when importing email content from a URL. (CAMP-49054)
* Fixed an error (-69) caused by end of session, when accessing a bookmarked URL or refreshing a page from the browser. (CAMP-49003, CAMP-48930, CAMP-48894)
* Fixed an issue when synchronizing rules from the legacy deliverability server to the new deliverability server. (CAMP-48923)
* Fixed an issue when loading an email template with HTML tags in the Email Designer. (CAMP-48243)
