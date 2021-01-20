---
solution: Campaign Standard
product: campaign
title: Latest Release
description: This page details content of the latest Campaign Standard release
audience: rn
content-type: reference
topic-tags: campaign-standard-releases

---

# Latest Release{#latest-release}

[Release Planning](../../rn/using/release-planning.md) &#124; [Control Panel releases](https://docs.adobe.com/content/help/en/control-panel/using/release-notes.html) &#124; [Documentation Updates](../../rn/using/documentation-updates.md) &#124; [Previous Release Notes](../../rn/using/release-notes-2020.md) &#124; [Deprecated Features](../../rn/using/deprecated-features.md)

## Release 21.1 - January 2021 {#release-21-1---january-2021}

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
<li>All categories of events are captured: Delays, Delivered, To Sent, Unsubscribe (Link, List), Feedback (Spam Complaints, Async events).</li>
<li>Calculation of Sent/ Delivered indicators is now based on real-time feedback from the Enhanced MTA for improved accuracy and reactivity.</li>
<li>EFS solves the problem of synchronous bounces reporting delays and takes 80% of load off from the inMail process.</li>
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
<p>The integration with Adobe Experience Manager has been improved: you can now import multilingual content more easily from Adobe Experience Manager. Adobe Campaign Standard now automatically detects language variants from Adobe Experience Manager content. 
</p>
<p>For more information refer to the <a href="../../integrating/using/creating-multilingual-email-aem.md">detailed documentation</a>.
</p>
</td> 
</tr> 
</tbody> 
</table>

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

**Improvements**

* Microsoft Dynamics 365 integration has been enhanced with a dedicated self-service integration app and an improved implementation process.

* Fixed an issue that caused deliveries to run very slowly because of certain processes. This was due to incorrect units defined for several parameters (milliseconds instead of seconds for example).

* Fixed an issue when the Mobile SDK sent an open tracking request based on the condition that deliveryId/MessageID is not null. This would result in 404 errors for deliveries with tracking disabled. An additional variable (acsDeliveryTracking) with information on the tracking status of the delivery is now sent in the payload. This variable can have two values on or off depending on the set tracking status. [Learn more](../../administration/using/push-tracking.md)

* An improvement has been made to facilitate troubleshooting when encountering issues with the Transactional messaging process.

* The Profiles list now allows you to search for records based on one of these fields: email, first name, last name or custom fields that have been added in advanced filtering when extending the profile resource. This feature is also available in Campaign Standard APIs using the filterType parameter. [Learn more](../../audiences/using/integrated-customer-profile.md)

* A parameter has been adjusted to the number of containers running the Transactional messaging database pooling process. This allows the load to be uniformly distributed across all the containers that are used and reach optimal performance.

* A new function (GetOption) is now available in activities using event variables after calling a workflow with external parameters. It allows you to return the value of a specified function. [Learn more](../../automating/using/customizing-workflow-external-parameters.md)

* A new technical option has been added. It allows Campaign Standard to check if there is enough physical memory available on your system before starting a workflow. If the amount of memory is below 5120 Mb, the workflow execution will be delayed until the system memory reaches this threshold. Note that this option is read-only and cannot be modified.

**Other changes**

* Changed an error to a warning during message preparation, when the limit of 100 content downloads per rolling hour is reached. A warning is now displayed when the limit is reached, which allows to proceed with delivery.

* A new delivery mapping (mapRtEventAppSubRcp) is now available for transactional push messages targeting profiles. The delivery, exclusion and tracking logs for these deliveries will now be available in the broadLogAppSubRcp, excludeLogAppSubRcp and trackingLogAppSubRcp tables. This solves an issue which caused delivery analysis to fail when sending a transactional push message using the Profile target dimension.

* When enriching a transactional message content, the links are not retrieved anymore when fetching data from the Profile table, which reduces latency during message preparation and avoids empty profile data due to an incorrect relation defined with the profile table.

* The instance technical configuration has been optimized to ensure stability. (CAMP-45681)

* Session management has been improved to optimize memory. (CAMP-45901, CAMP-46767)

* The **Transfer file** activity now generates an additional variable (filesCount) that contains the number of uploaded or downloaded files. (CAMP-45842) [Learn more](../../automating/using/transfer-file.md#output-variables)

* The SMS connector can now send multiple optional parameters with each message.

* Fixed an issue that prevented users with the DATA MODEL role from publishing delivery log extensions. This operation will now be available for the DATA MODEL role. (CAMP-46604)

* Fixed an issue in workflows that could occur when copy-pasting a **Deduplication** activity that had been executed once and that leveraged a temporary resource. Once duplicated, the activity's resource was automatically set to empty, leading to issues in other activities of the workflow. Once pasted, the activity's resource will now remain the same, in order for the error to be triggered as soon as possible rather than later in the workflow. (CAMP-46903)

* The error message that displayed when trying to publish a resource targeting a custom resource that does not exist anymore has been made clearer. (CAMP-46893)
 
* The following languages have been added to the Preferred language list: Indonesian - Indonesia (in-id), English – Sweden (en-se), English – Asia Pacific (en-ap), English - Japan (en-jp), Spanish – Latin America (es-la). (CAMP-46351)

* The picker for profiles selection when testing a landing page will now use the profilBase resource instead of profile to prevent timeout.

* The SMPP log format has been improved.

* Optional parameters to cryptString and decryptString JS functions have been added to match Adobe Campaign Classic API's.

* You can now modify the default validity date of SMS transactional messages.

* Improved warning or error messages in delivery preparation logs.

* Improved error logs when trying to connect to IMS.

* You can now further filter the Delivery and Campaign dimensions using the search bar in Dynamic reporting.

* The transactional SMS message validity date can now be defined by the value set for the expiration parameter in the Transactional Messages API. (CAMP-36600)

* In Dynamic reporting, the **Delivery summary** built-in report was showing incorrect data for the unsubscribed rate metric. A new metric named **Unique unsubscription** has been added to fix this. (CAMP-46445)

**Patches**

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
* Fixed an issue where Push notification preparation was taking too much time to be completed. This was caused by a missing index on the transient working tables.
* Fixed an error which could occur when using the **Dimension to reconciliate** option in a **Reconciliation** activity in a workflow if a relation was already defined between a custom resource and a profile resource.
* Fixed an issue which occurred when adding links through a **Reconciliation** or **Enrichment** activity. Chosen links were not displayed in the output transition.
* Fixed an issue when using a **Segmentation** activity with recurring deliveries in a workflow which caused the delivery to be sent to the wrong audience. (CAMP-46275)
* Fixed an error where custom resources publication failed when trying to extend the Profile resource to create custom profile dimensions for Dynamic reporting. (CAMP-46266)
* Fixed an error which occurred when adding a link to a File import table. After adding an **Enrichment** activity to the **File import** activity, the link previously configured disappeared. (CAMP-46557)
* Fixed an issue when using custom resources linked to Profile data where the display order in the Detail configuration screen was changed when saving. (CAMP-46312)
* Fixed an issue which could prevent you from displayed data in dynamic reporting due to deliveries based on a custom delivery mapping.
* Fixed an error which could prevent you from selecting a collection with an incorrect resource target in a workflow query activity.  
* Fixed an issue which could cause the InMail process to validate hard bounces incorrectly.
* Fixed an error which occurred when opening a profile screen due to a link error.
* Fixed an issue which could prevent you from deleting GDPR data from the cleanup workflow.
* Fixed an error which occurred when the scheduling configuration was manually updated with tye keyboard in email delivery schedule parameters.
*  Fixed an issue which could prevent you from editing a profile due to incorrect parameters in the Organizational unit.
* Fixed an issue which let the Service extension field empty and impossible to set in the Email properties, even if it was set in the delivery template.
* Fixed an issue which could result in proofs taking longer to be processed. (CAMP-45048)
* Fixed an issue which could prevent you from sorting columns in a profile overview screen.
* Fixed a thumbnail generation issue which could occur on Azure in email variants containing Chinese characters. (CAMP-47152)
* Fixed a regression introduced in 20.4 which could lead to incorrect open rates for Gmail due to the filtering of tracking events received from Gmail accounts. (CAMP-46504)
* Fixed an issue which could prevent you from importing HTML content into a transactional message template. (CAMP-47318)
* Fixed an issue that could slow down the display of the renderings in the Email rendering report. (CAMP-46226)
* Fixed an issue which could prevent you from publishing custom resources configured with a List-type element in the screen definition. (CAMP-47217)
* Fixed an issue in the Creative Designer which prevented line dividers from rendering correctly in Microsoft Outlook when placed at the top of the email content. (CAMP-46294)
* Fixed an issue that caused the KPIs reconciliation with Adobe Analytics technical workflow to get stuck. (CAMP-46576) 
