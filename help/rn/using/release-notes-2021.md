---
title: Release Notes 2021
description: This page lists all 2021 releases of Adobe Campaign Standard.
audience: rn
content-type: reference
topic-tags: campaign-standard-releases
feature: Overview
role: User
level: Beginner
exl-id: 225c65cc-2964-4b71-84a9-30fcd22d75bf
---
# Release Notes 2021{#release-notes-2021}

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
* Proof and trap profiles have now been excluded from delivery performance calculation in Dynamic Reports. (CAMP-47338)

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


## Release 21.2 - June 2021 {#release-21-2---june-2021}

New features, improvements and fixes included in the next Campaign Standard release are listed below. New features, improvements and fixes included in this Campaign Standard release are listed below.

**Improvements**

* When designing a landing page, you can now add a mandatory checkbox that profiles are required to select before submitting the form. For more information refer to the [detailed documentation](../../channels/using/managing-landing-page-form-data.md#agreement-checkbox).

* For the Triggers integration, the error message displayed when there is no reconciliation data coming in the trigger payload has been improved: "Alias data missing from payload".

* Performance to retrieve push notifications from the queue has been improved.

**Other changes**

* The URL signature mechanism for tracking links has been disabled to prevent an issue that was causing some valid, signed tracking links to be incorrectly blocked after being modified by third-party security tools.

* In multi-variant deliveries, users can no longer create language copies if the default variant has been deleted. A message is now displayed during language copy creation. (CAMP-48235)

* The 2-step profile deletion process (deprecated starting Campaign 19.4 release) is now disabled by default. Previously it had to be manually disabled from the Campaign interface before using the Privacy Core Service. Not doing so would cause Delete requests to remain in pending state without completing.

* In Dynamic reports, the **Exclude Proof** segment has been removed. (CAMP-46161)

* A new warning message has been added to inform the user when an iOS certificate is uploaded without the platformPrincipal value in the Campaign application.

* The maximum size of an email is now set to 100 MB by default. This limit enables to prevent any error that could indefinitely increase the size of an email, which can lead to a system crash. (CAMP-47445) [Learn more](../../sending/using/design-and-personalize.md#email-size) 

* The Asset Core Service integration with the Email designer can now be used by Standard Users.  

* A new message has been added to confirm a successful migration from a v4 push application to a v5 push application.

* During JSONWeb Tokens creation to authenticate to the Campaign Standard API, the product profiles are now **considered**. This means that the organizational units and roles allocated to the security group (that matches the product profile on AdobeIO) will be applied to the IMS technical account needed for Campaign Standard Rest API calls. (CAMP-47479)

**Patches**

* Fixed an issue which prevented the expiry option for the batch process log table (**xtkjoblog**) table from being applied. This prevented the table from being correctly purged.

* Fixed an issue which prevented you from changing the order of filters in a **Segmentation** workflow activity. (CAMP-48357)

* Fixed a regression from 20.4 that could lead to deliveries failing with a null value error. (CAMP-48591)

* Fixed an issue which prevented you from sending a report through the **Share** > **Send Report Now** or **Send Report on Schedule** menu. (CAMP-47798)

* Fixed a regression which could lead to incorrect open rates for Gmail due to the filtering of tracking events received from Gmail accounts. (CAMP-46504)

* Fixed various issues causing data discrepancy between reports in Adobe Campaign Standard and reports in Adobe Analytics. (CAMP-47671, CAMP-47296)

* Fixed an issue that prevented you from accessing the delivery logs after preparation had failed. (CAMP-48296)

* Fixed an issue which could display an error message when trying to edit, delete or send a custom report. (CAMP-47789, CAMP-47798)

* Fixed an issue causing the APIs calls to fail when creating a new custom resource and enabling the **Do not synchronize** option. (CAMP-48014)

* Fixed an issue where custom resources with the **Do not synchronize** option enabled could reference a schema that had been redrafted or deleted. This issue was causing an error when publishing the custom resources.

* Fixed an SMS opt-out issue when using multiple short codes on the same external account.

* Fixed an issue which prevented you from accessing a new delivery alerting criterion ("the resource you are trying to access is unreachable") after publishing the database. (CAMP-48221)

* Fixed an issue where tracking logs were missing in some Campaign instances with Dynamic reporting. A new [technical workflow](../../administration/using/technical-workflows.md) has been added to restore these tracking logs. (CAMP-47885)

* Fixed an issue where no delivery data was displayed in Dynamic reports. Reports were set to 0. (CAMP-47480)

* Fixed an issue which prevented the Server JavaScript HTTP Client from connecting to external URL.

* Fixed an issue which reset an **Incremental query** activity after changing the internal name of the workflow. This occurred when a date field was used as incremental mode. (CAMP-47674)

* Fixed an issue which prevented the preview thumbnail from displaying in the delivery summary, when creating a multilingual email with the Adobe Experience Manager integration. This issue occurred when using the **Language copy creation** button to create the email variants. (CAMP-47810)

* Fixed an issue which prevented users from accessing the parent delivery from the Email or SMS child delivery. (CAMP-47986)

* Fixed an issue which could cause excess CPU and memory consumption when sending transactional messages via the REST API with a missing custom event. (CAMP-47147)

* Fixed an error with the Transactional Messaging API which sometimes prevented realtime messages from being sent.

* Fixed an issue where reports were not received after using the **Send report on schedule** option. (CAMP-48583, CAMP-47786)

* Fixed an issue where reports received after using the **Send report now option** were incomplete and missing data. (CAMP-48583)

* Fixed an issue with the Email Designer where an image's dimensions were narrowed down when uploading an image. (CAMP-47017)

* Fixed an issue which prevented every available Experience Manager template from being displayed when creating a delivery. (CAMP-48132)

* Fixed an error which prevented the Campaign link in the Summary page of a sent delivery from redirecting the users to the related campaign. (CAMP-48012)

* Fixed an issue in the Email Designer where the Asset Core Service integration kept failing when trying to select an asset. (CAMP-47446)

* Fixed an issue that blocked some Journey Orchestration deliveries due to Campaign not supporting timestamps with an exact value (i.e. ending with 00) sent by events from Journey Orchestration.

## Release 21.1 - February 2021 {#release-21-1---february-2021}

**What's new?**

<table> 
<thead> 
<tr> 
<th> <strong>Email Feedback Service</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
<td>
<p>Email Feedback Service (EFS) is a scalable service which captures feedback from the Enhanced MTA directly, thus improving reporting accuracy. This capability is released as a private beta and will be progressively available to all customers in future releases.</p>
<ul>
<li>All categories of feedback are now captured for complete and precise reporting.</li>
<li>Calculation of the <b>Delivered</b> indicator is now based on real-time feedback from the Enhanced MTA for improved accuracy and reactivity.</li>
<li>EFS solves the problem of delays with synchronous soft bounces reporting.</li>
</ul>
<p>For more information refer to the <a href="../../sending/using/confirming-the-send.md">detailed documentation</a>.
</p>
</td> 
</tr> 
</tbody> 
</table>

<table> 
<thead> 
<tr> 
<th> <strong>Adobe Experience Manager integration improvements</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
<td>
<p>Campaign integration with Adobe Experience Manager has been improved: you can now import multilingual content more easily from Adobe Experience Manager. <p>
<p>Adobe Campaign Standard now automatically detects language variants from Adobe Experience Manager content and allows for bulk variant import and creation, significantly simplifying the number of steps that a practitioner needs to go through to create a multilingual campaign based on Adobe Experience Manager content.</p>
<p>For more information refer to the <a href="../../integrating/using/creating-multilingual-email-aem.md">detailed documentation</a>.
</p>
</td> 
</tr> 
</tbody> 
</table>

<!--
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
<p>NOTE: This change will be progressively rolled out to all customer environments between Feb 10 and March 1st.
</p>
</td> 
</tr> 
</tbody> 
</table>
-->

**Improvements**

* **Microsoft Dynamics 365 integration** has been enhanced with a dedicated self-service integration app and an improved implementation process. [Learn more](../../integrating/using/d365-acs-get-started.md)

* An improvement has been made to facilitate troubleshooting when encountering issues with the Transactional messaging process. Adobe technical administrators can now use tracing on any process without restarting it.

* The **Profiles** list now allows you to search for records based on one of these fields: email, first name, last name or custom fields that have been added in advanced filtering when extending the profile resource. This feature is also available in Campaign Standard APIs using the filterType parameter. [Learn more](../../audiences/using/integrated-customer-profile.md)

* A parameter has been adjusted to the number of containers running the Transactional messaging database pooling process. This allows the load to be uniformly distributed across all the containers that are used and reach optimal performance.

* A new **GetOption** function is now available in activities using event variables after calling a workflow with external parameters. It allows you to return the value of a specified function. [Learn more](../../automating/using/customizing-workflow-external-parameters.md)

* A new option allows Campaign Standard to **check physical memory** availability on your system before starting a workflow. If the amount of memory is too low, the workflow execution will be delayed until the system memory reaches this threshold. This avoids further degradation of performance and mitigate the risk of an outage. The workflow will auto-resume once the load on the server comes down and the memory increases. Note that this option is read-only and cannot be modified. [Learn more](../../automating/using/best-practices-workflows.md#execution)

* A new process is available in Adobe Campaign Standard which allows you to migrate more easily from the legacy SDK v4 mobile application to **Adobe Experience Platform Mobile SDK**. Refer to [this page](../../administration/using/sdkv4-migration.md).

**Other changes**

* Changed an error to a warning during message preparation, when the limit of 100 content downloads per rolling hour is reached. A warning is now displayed when the limit is reached, which allows to proceed with delivery.

* When enriching a transactional message content, the links are not retrieved anymore when fetching data from the Profile table, which reduces latency during message preparation and avoids empty profile data due to an incorrect relation defined with the profile table.

* The instance technical configuration has been optimized to ensure stability. (CAMP-45681)

* Session management has been improved to optimize memory. (CAMP-45901, CAMP-46767)

* The **Transfer file** activity now generates an additional variable (filesCount) that contains the number of uploaded or downloaded files. (CAMP-45842) [Learn more](../../automating/using/transfer-file.md#output-variables)

* The SMS connector can now send multiple optional parameters with each message. [Learn more](../../administration/using/sms-protocol.md)

* Users with the DATAMODEL role can now publish delivery log extensions. (CAMP-46604)

* The error message that displayed when trying to publish a resource targeting a custom resource that does not exist anymore has been made clearer. (CAMP-46893)
 
* The following languages have been added to the **Preferred language** list: Indonesian - Indonesia (in-id), English – Sweden (en-se), English – Asia Pacific (en-ap), English - Japan (en-jp), Spanish – Latin America (es-la). (CAMP-46351)

* The picker for profiles selection when testing a landing page will now use the profilBase resource instead of profile to prevent timeout.

* The SMPP log format has been improved.

* Optional parameters to cryptString and decryptString JS functions have been added to match Adobe Campaign Standard API's.

* Improved warning or error messages in delivery preparation logs.

* Improved error logs when trying to connect to Adobe Identity Management Service (IMS).

* You can now further filter the **Delivery** and **Campaign** dimensions using the search bar in Dynamic reporting.

* The transactional SMS message validity date can now be defined by the value set for the expiration parameter in the Transactional Messages API. (CAMP-36600)

* In Dynamic reporting, the **Delivery summary** built-in report was showing incorrect data for the unsubscribed rate metric. A new metric named **Unique unsubscription** has been added to fix this. (CAMP-46445)

**Patches**

* Fixed an issue that caused deliveries to run very slowly because of certain processes. This was due to incorrect units defined for several parameters (milliseconds instead of seconds for example).

* Fixed an issue when the Mobile SDK sent an open tracking request based on the condition that deliveryId/MessageID is not null. This would result in 404 errors for deliveries with tracking disabled. An additional variable (acsDeliveryTracking) with information on the tracking status of the delivery is now sent in the payload. This variable can have two values on or off depending on the set tracking status. [Learn more](../../administration/using/push-tracking.md).

* Fixed an issue in workflows that could occur when copy-pasting a **Deduplication** activity that had been executed once and that leveraged a temporary resource. Once duplicated, the activity's resource was automatically set to empty, leading to issues in other activities of the workflow. Once pasted, the activity's resource will now remain the same, in order for the error to be triggered as soon as possible rather than later in the workflow. (CAMP-46903)

* Fixed issues which caused the delivery analysis to fail when sending a transactional push notification targeting profiles, by introducing a new [target mapping](../../administration/using/target-mappings-in-campaign.md): **Profile - Real-time event for Push** (*mapRtEventAppSubRcp*). The delivery, exclusion and tracking logs for [profile-based transactional push notifications](../../channels/using/transactional-push-notifications.md#transactional-push-notifications-targeting-a-profile) will now be stored in the *broadLogAppSubRcp*, *excludeLogAppSubRcp* and *trackingLogAppSubRcp* tables.

   >[!IMPORTANT]
   >
   >Due to this change, if you are using an existing profile-based push transactional notification (created before upgrading to Adobe Campaign 21.1), it is recommended you update the target mapping to the new one and publish the message again. See the steps detailed [here](../../channels/using/transactional-push-notifications.md#change-target-mapping). Using the previous target mapping **Profile - Real-time event** (*mapRtEventRcp*) may result in longer delivery preparation times and performance degradation.

* Fixed an issue which prevented delivery reports from running when 5000 rows were displayed.
* Fixed an issue with A/B testing which prevented content of variant B from being updated after the delivery template had been modified. (CAMP-45235)
* Fixed an issue that caused the Transactional messaging process to get stuck, preventing messages from being sent.
* Fixed an issue which could lead to navigation issues after clicking an internal link (for example when accessing the parent delivery from a proof summary screen).
* Fixed an issue which prevented all available Experience Manager content templates from displaying when creating a delivery. (CAMP-45990)
* Fixed an issue in workflows which could prevent failure messages from displaying in the delivery logs after adding the **Reason** column to the additional data tab. (CAMP-45139)
* Fixed an issue that could occur when two app subscription calls had the same Marketing Cloud ID ('duplicate key value violates unique constraint' error).
* Fixed an issue that could lead to slowness issues when drag and dropping activities into a workflow containing a large amount of **Query** and **Read audience** activities. (CAMP-44511)
* Fixed an error that could occur at the end of transactional message preparation, preventing redirection information from being uploaded to the tracking servers.
* Fixed an issue which could display error messages when trying to open import templates or past import jobs after having customized the workflow resource. (CAMP-46183)
* Fixed an issue that could prevent a **Read audience** activity from running if it was configured with a dynamic audience name. (CAMP-46047)
* Fixed an issue which prevented the **Export list** button from being displayed
* Fixed an issue which could lead to the failure of the **Reporting aggregates** workflow. (CAMP-45979)
* Fixed an issue when creating a custom resource with a custom composite key (text/date dynamic content).
* Fixed an issue that could prevent query transition data from being displayed. (CAMP-45669)
* Fixed memory consumption issues related to custom resource publication.
* Fixed an issue that occurred when configuring a delivery to be sent on a specific date. If the delivery was then set to be sent immediately once confirmed, the delivery preparation failed and the date specified initially was still taken into account. (CAMP-44107)
* Fixed an issue that could prevent transactional templates from being opened. (CAMP-47181)
* Fixed an issue in transactional message publication process which could lead to duplicate typologies and typology rules with names exceeding the allowed string size. (CAMP-47104)
* Fixed an issue in the **External API** activity that occurred when an input parameter returned a record that did not exist. (CAMP-47023)
* Fixed an issue that could prevent the SMPP connector from reconnecting.
* Fixed an issue that occurred in the **File transfer** activity when downloading a file containing a dot in its name. The characters following the dot were considered as the file's extension. (CAMP-46624)
* Fixed an issue that prevented database pooling from being performed, which caused transactional messages to be stuck in the router queue.
* Fixed an error that did not prevent the canceled delivery logs from being sent.
* Fixed an issue that could cause a workflow to fail when using an **AND-join** activity. The activity automatically changed the Primary set to the last transition wired to it, even if it visually showed the first wired transition. (CAMP-46900)
* Fixed an issue that could cause addresses that were successfully quarantined to have their status incorrectly set to Valid, thus removing them from quarantine.
* Fixed an issue that could prevent personalized fields from displaying if they contained special characters. (CAMP-46805)
* Fixed an issue that could prevent you from displaying a specific detailed view for a profile. This occurred if the profile resource had been extended with custom fields with the **Add a personalized fields section** option enabled.
* Fixed an issue that could return an error code 500 when sending transactional events. (CAMP-46811)
* Fixed an issue which could prevent you from receiving email scheduled reports. (CAMP-46891)
* Fixed an issue that occurred when linking a custom resource to the profile resource with a 1 cardinality simple link. When accessing a profile with the custom resource field empty, an error message is now displayed instead of an empty list.
* Fixed an issue when using profile substitution in a workflow where the page failed to load the delivery profiles when selecting the profile to replace. (CAMP-46522)
* Fixed a regression where the **Database Cleanup** technical workflow tried to drop expired delivery worktables resulting to the following errors: (CAMP-46536)

```
   PGS-220000 PostgreSQL error: ERROR: table ""wkdlv_24439460_data"" does not exist and WDB-200001 SQL statement 'DROP TABLE wkdlv_24448131_data' could not be executed.
```

* Fixed the following error which occurred in some cases when using custom filter on custom resources: (CAMP-46509)

```
   The 'profile/xxxx' field used in the filter 'xxxxx' does not exist in custom resource 'xxx'
```

* Fixed an issue where **Push notification preparation** was taking too much time to be completed. This was caused by a missing index on the transient working tables.
* Fixed an error which could occur when using the **Dimension to reconciliate** option in a **Reconciliation** activity in a workflow if a relation was already defined between a custom resource and a profile resource.
* Fixed an issue which occurred when adding links through a **Reconciliation** or **Enrichment** activity. Chosen links were not displayed in the output transition.
* Fixed an issue when using a **Segmentation** activity with recurring deliveries in a workflow which caused the delivery to be sent to the wrong audience. (CAMP-46275, CAMP-46470)
* Fixed an error where custom resources publication failed when trying to extend the Profile resource to create custom profile dimensions for Dynamic reporting. (CAMP-46266)
* Fixed an error which occurred when adding a link to a File import table. After adding an **Enrichment** activity to the **File import** activity, the link previously configured disappeared. (CAMP-46557)
* Fixed an issue when using custom resources linked to Profile data where the display order in the **Details** configuration screen was changed when saving. (CAMP-46312)
* Fixed an issue which could prevent you from displaying data in dynamic reporting due to deliveries based on a custom delivery mapping.
* Fixed an error which could prevent you from selecting a collection with an incorrect resource target in a workflow **Query** activity.  
* Fixed an issue which could cause the InMail process to validate hard bounces incorrectly.
* Fixed an error which occurred when opening a profile screen due to a link error.
* Fixed an issue which could prevent you from deleting GDPR data from the cleanup workflow.
* Fixed an error which occurred when the scheduling configuration was manually updated with the keyboard in email delivery schedule parameters.
*  Fixed an issue which could prevent you from editing a profile due to incorrect parameters in the Organizational unit.
* Fixed an issue which let the **Service** extension field empty and impossible to set in the **Email properties**, even if it was set in the delivery template.
* Fixed an issue which could result in proofs taking longer to be processed. (CAMP-45048)
* Fixed an issue which could prevent you from sorting columns in a profile overview screen.
* Fixed a thumbnail generation issue which could occur on Azure in email variants containing Chinese characters. (CAMP-47152)
* Fixed a regression introduced in Campaign 20.4 which could lead to incorrect open rates for Gmail due to the filtering of tracking events received from Gmail accounts. (CAMP-46504)
* Fixed an issue which could prevent you from importing HTML content into a transactional message template. (CAMP-47318)
* Fixed an issue that could slow down the display of the renderings in the **Email rendering report**. (CAMP-46226)
* Fixed an issue which could prevent you from publishing custom resources configured with a List-type element in the screen definition. (CAMP-47217)
* Fixed an issue in the Email Designer which prevented line dividers from rendering correctly in **Microsoft Outlook** when placed at the top of the email content. (CAMP-46294)
* Fixed an issue that caused the KPIs reconciliation with **Adobe Analytics** technical workflow to get stuck. (CAMP-46576) 
* Fixed an issue in the **Email Designer** that prevented fragments from being automatically displayed in search boxes when inserting content blocks. (CAMP-44205)
* Fixed an issue in the **Email Designer** that caused unwanted characters to be displayed in sent emails when using emojis in fragments. (CAMP-46621)
* Fixed regression introduced in 20.4 in the **Email Designer** impacting the Divider component, which resulted in additional line heights and image distorsions in content. (CAMP-46663)
* Fixed an issue that forced the out-of-the-box buttons to remain centered when the message was sent to an Outlook mailbox, even though these buttons were aligned to the right or left in **Email Designer**. (CAMP-46466) 
* Fixed an issue that prevented the list of test profiles from refreshing when searching profiles in the **Email Designer** preview. (CAMP-45265)
* Fixed an issue that prevented custom test profiles from displaying in the list when searching profiles in the **Email Designer** preview. (CAMP-45589)
* Fixed an issue that caused mismatching dates to be displayed when generating trend graphics from the **Delivery summary report**. (CAMP-45521)
