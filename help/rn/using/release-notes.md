---
solution: Campaign Standard
product: campaign
title: Latest Release
description: This page details content of the latest Campaign Standard release
audience: rn
content-type: reference
topic-tags: campaign-standard-releases

feature: Overview
role: User
level: Beginner
exl-id: e1f55a9b-be51-4f57-8719-fed7efc89113
---

# Latest Release{#latest-release}

## Release 21.3 - September 2021 {#release-21-3---sept-2021}

New features, improvements and fixes included in the latest Campaign Standard release are listed below. 

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

**Security improvements**

* Security has been enhanced for protection against SSRF attacks. (CAMP-47836)
* The list of users is now restricted to administrators only. (CAMP-47260)
* Environment variables can no longer be used as part of parameter expansion in a URL. (CAMP-47268)

**Improvements**

* When creating a recurring delivery in a workflow, linked to an Adobe Experience Manager content, content approval status is now checked before sending.
* Database connection limit is now aligned with the Campaign package to avoid connection errors.
* Added a consistency check while creating indexes in custom resources and improved the error messages.

**Other changes**

* Adobe Experience Platform Data Connector and Audience Destinations service are now deprecated with Campaign Standard. If you are using these capabilities, you need to move to Adobe Sources and Destinations and adapt your implementation. [Learn more](../../integrating/using/get-started-sources-destinations.md)
* Deprecated and removed features are listed in [this page](deprecated-features.md).
* A new 'StringAgg' aggregate function has been introduced to concatenate the values of a string type column. (CAMP-47077)
* The **Update delivery indicators** (updateDeliveryIndicators) technical workflow has been improved for better performance.
* In-App messaging templates are now available for all languages supported in Campaign Standard.
* Delivery preparation time has been optimized for transactional messages by reducing the number of calls to the tracking server during delivery analysis.
* A new alert message informs users of a high bounce rate.
* Improved log error messages and warnings to make debugging easier when the tracking logs failed to be correctly retrieved. (CAMP-48939, CAMP-47360)
* You can now fully personalize URLs, including the domain name.

**Patches**

* Fixed a timeout error when importing email content from a URL. (CAMP-49054)
* Fixed an error (-69) caused by an end of session, when accessing a bookmarked URL or refreshing a page from the browser. (CAMP-49003, CAMP-48930, CAMP-48894)
* Fixed an issue when synchronizing rules from the legacy deliverability server to the new deliverability server. (CAMP-48923)
* Fixed an issue when loading an email template with HTML tags in the Email Designer. (CAMP-48243)
* Fixed an error where Adobe Experience Manager content was not loading when creating transactional messages with the Email designer. (CAMP-49075)
* Fixed an issue in the interface where too much padding was added between the top bar and the content.
* Fixed an issue with transactional messages which could lead to a publication error when using Campaign content blocks in Adobe Experience Manager content. (CAMP-49233)
* Fixed an issue which could lead to an error message when the authentication failed. The user is now redirected to the login page.
* Fixed a token display issue which could prevent users from editing or sharing a report.
* Fixed an issue during the publication of a custom resource using a filter expression with 1-n table relationships. (CAMP-48740)
* Fixed a date formatting issue that prevented delivery contact dates from being retrieved in workflow transitions. (CAMP-48871)
* Fixed an issue that prevented the extension of sending logs during the creation of a custom profile dimension.
* Fixed an issue that could cause deliveries with multiple language variants to fail. From now on, if a user deletes the default language variant, another language variant must be set as the default one before creating languages copies. (CAMP-48235)
* Fixed an issue that caused email messages to show extra white spaces in Outlook if the user had selected the **Only show on mobile devices** option when designing the message. (CAMP-48902)
* Fixed an issue that caused the last execution date of the incremental query activity field to be missing from the **Processed Data** tab after running the incremental query workflow. (CAMP-48879)
* Fixed an issue that prevented you from properly defining a dynamic segment code in the **Segmentation** workflow activity. (CAMP-48727)
* Fixed an error that randomly occurred when trying to save a workflow after editing it. (CAMP-48695)
* Fixed an issue that prevented you from publishing custom resources due to a trigger's data schema remaining even after the trigger's deletion. (CAMP-48523)
* Fixed an issue that prevented the feedback loop requests from being honored, because the InMail process was not able to retrieve the delivery logs to update. (CAMP-48705)
* Fixed an issue that prevented you from properly defining the exclusion options in the **Exclusion** workflow activity.(CAMP-48355)
* Fixed an issue that occurred when enrichment activities in workflows involved subscriptions to or unsubscriptions from a service. This issue led to crashing. 
* Fixed an issue that could prevent workflows from running.
* Fixed an issue that could prevent users from renaming or deleting out-of-the box security groups from the user interface.
* Fixed an issue that could prevent users from deleting an incomplete event publication job.
* Fixed an issue where the database cleanup workflow which was failing with an error. (CAMP-49097)
