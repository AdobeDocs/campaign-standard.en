---
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
<p>Apache log4j has fixed the reported vulnerabilities in Apache log4j v2.17.1 release. Adobe Campaign Standard uses Apache log4j and in this release is including this latest Apache log4j v2.17.1 </p>
</td> 
</tr> 
</tbody> 
</table>

**Security fixes**

* New URL signature mechanism for tracking included in this release. The previous mechanism had been disabled to prevent an issue that was causing some valid, signed tracking links to be incorrectly blocked after being modified by third-party security tools. (CAMP-48983)

**Improvements**

* Improved processing of reporting data to avoid over loading the system. (CAMP-47578)
* After sending your In-App messages, you can now choose to deactivate your delivery. This allows you to delete your delivery without losing any reporting data. (CAMP-48469)
* To prevent any issue, users can no longer use the same name for a custom table column as the one used for the automatic Primary Key in the database, `"<dataType><resourceName>Id"`. (CAMP-49358)
* You can now monitor your delivery and track job logs with the new **Job history** drop-down from your messages' dashboard. (CAMP-49840)
* Improved stability and database health, by reducing dead tuples, when large number of messages are sent across all channels over the time. (CAMP-49755, CAMP-49792, CAMP-49849)
* To ensure database connections are refreshed automatically in case of database crash or restart, improvements have been implemented in Campaign Mail Transfer Agent (MTA). (CAMP-48063)


**Patches**

* Fixed an issue with the **Send report now** option in Dynamic reports: the PDF generation jobs failed with deliveries including multi-variants. (CAMP-49120)
* Fixed an issue that prevented users to refresh or unlink Adobe Experience Manager (AEM) content from their Adobe Campaign Standard deliveries when a duplicated content in AEM shared the same key (cq:uuid). (CAMP-49161)
* Fixed an error when accessing an instance where pages were not loading, deliveries could not be opened or any pending modifications could not be saved. (CAMP-50195)
* Fixed an issue that prevented Delivery alerting criteria to be opened if the field **Delivery filter** applied by this criterion was not filled. (CAMP-49093)
* Fixed an issue when editing the **Secondary** button in In-App deliveries that prevented changes to be taken into account. (CAMP-50250)
* Fixed an error in Japanese instances that prevented users to choose Several times a day as **Execution frequency** in the **Scheduler** activity. (CAMP-50247)
* Fixed an issue when working in a Japanese user interface which displayed an error message when selecting a time in a Scheduler activity. (CAMP-49289)
* Fixed an error with push notification reports that displayed dismissed push notifications as **Open** instead of **Impression**. (CAMP-45980)
* Fixed an issue which could lead to errors when opening a report. (CAMP-49222)
* Fixed an issue which could lead to the email preparation failing after deleting a link to AEM content. (CAMP-49877)
* To solve various issues, the retry mechanism has been improved for deliveries including content imported from a URL. [Learn more](../../designing/using/using-existing-content.md#retrieving-content-from-a-url-automatically-at-preparation-time) (CAMP-48888)
* Fixed an issue which occurred after creating a new filter in a custom resource, then using it as a reconciliation key in a landing page. If the custom resource was published again, the filter was removed from the list of available reconciliation keys for the landing page. (CAMP-49516)
* Fixed an issue in landing pages when using dynamic conditions with checkboxes. (CAMP-48604)
* Fixed an issue that occurred in a **Query** activity when using the “On or before October” filter condition. When working from an instance set to a European timezone, the selected month for the filter showed September instead of October, due to an issue when converting the timezone. (CAMP-48602)
* To optimize deliverability, Adobe Campaign now sends emails using 7-bit encoding instead of 8-bit. This prevents intermediate relays from invalidating the DKIM signature which could affect the authenticity of the messages. (CAMP-49016)
* Performances when duplicating audiences have been enhanced in order to avoid any issue when working with large audiences. (CAMP-49639)
* Fixed an issue which could prevent a custom filter from displaying the correct results when used into a **Query** activity. (CAMP-49417)
* Fixed an error that displayed an error message when trying to use a fragment in a delivery with a comma in its name. The issue has been resolved, commas can now be used in fragments’ names. (CAMP-49216)


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
<p>For more information refer to the <a href="../../start/using/interface-description.md#top-bar">detailed documentation</a>.
</p>
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
<p>For more information, refer to the <a href="../../administration/using/audit.md">detailed documentation</a>.</p>
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
<p>For more information refer to the <a href="../../automating/using/managing-execution-options.md">detailed documentation</a>.</p>
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
* A new consistency check in custom resources publication prevents users from creating duplicate indexes, which causes publication to fail. An improved error message asks the user to rename the index if needed. [Learn more](../../developing/using/updating-the-database-structure.md#publishing-a-custom-resource)

**Other changes**

* Adobe Experience Platform Data Connector and Audience Destinations service are now deprecated with Campaign Standard. If you are using these capabilities, you need to move to Adobe Sources and Destinations and adapt your implementation. [Learn more](../../integrating/using/get-started-sources-destinations.md)
* Deprecated and removed features are listed in [this page](deprecated-features.md).
* A new 'StringAgg' aggregate function has been introduced to concatenate the values of a string type column. (CAMP-47077) [Learn more](../../automating/using/list-of-functions.md#aggregates)
* The **Update delivery indicators** (updateDeliveryIndicators) technical workflow has been improved for better performance.
* In-App messaging templates are now available for all languages supported in Campaign Standard.
* Delivery preparation time has been optimized for transactional messages by reducing the number of calls to the tracking server during delivery analysis.
* A new alert message informs users of a high bounce rate.
* Improved log error messages and warnings to make debugging easier when the tracking logs failed to be correctly retrieved. (CAMP-48939, CAMP-47360)
* You can now fully personalize URLs, including the domain name. [Learn more](../../designing/using/personalization.md#personalizing-urls)

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
