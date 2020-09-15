---
title: Release Notes 2019
description: This page lists all 2019 releases of Adobe Campaign Standard.
page-status-flag: never-activated
uuid: 99f92a54-4b3d-48b9-b08d-e98b24e75f62
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: rn
content-type: reference
topic-tags: campaign-standard-releases
discoiquuid: e54f8305-7e32-4193-8e5a-b5d87b03038c

internal: n
snippet: y
---

# Release Notes 2019{#release-notes-2019}

[Release Planning](https://helpx.adobe.com/campaign/kb/acs-release-planning.html) &#124; [Control Panel releases](https://docs.adobe.com/content/help/en/control-panel/using/release-notes.html) &#124; [Documentation Updates](../../rn/using/documentation-updates.md) &#124; [Latest Release Notes](../../rn/using/release-notes.md) &#124; [Deprecated Features](https://helpx.adobe.com/campaign/kb/acs-deprecated-and-removed-features.html)

## Release 19.4 - December 2019 {#release-19-4---october-2019}

**What's new?**

<table> 
 <thead> 
  <tr> 
   <th> <strong>California Consumer Privacy Act (CCPA)</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>CCPA is the State of California's new privacy law hat harmonizes and modernizes data protection requirements going into effect on Jan 01, 2020. CCPA applies to Adobe Campaign customers who hold data for Data Subjects residing in California.</p>
   <p>In addition to the privacy capabilities already available in Adobe Campaign (including consent management, data retention settings, and user roles), we are taking this opportunity to include additional capabilities, to help facilitate your readiness for CCPA:</p>
   <ul>
    <li>Right to Access and Right to Delete: we are leveraging the capabilities that were added for GDPR. <a href="https://helpx.adobe.com/content/help/en/campaign/kb/acs-privacy.html#righttoaccess">Learn more</a> </li>
    <li><p>When creating a Privacy request, the regulation type (GDPR or CCPA) has been added in the Privacy Core Service. This method is the one you should use for all access and delete requests. The use of the Campaign API and interface for access and delete requests is deprecated.  See the <a href="https://helpx.adobe.com/campaign/kb/acs-deprecated-and-removed-features.html">Deprecated and Removed Features article</a>.</p></li>
    <li>A <strong>CCPA Opt-Out</strong> field has been added to the Profiles resource to allow Adobe Campaign users to track whether a consumer has opted-out for the sale of Personal Information. <a href="https://helpx.adobe.com/content/help/en/campaign/kb/acs-privacy.html#ccpa">Learn more</a>.</li>
  </ul>
    <p>Refer to the <a href="https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/privacy/privacy-overview.html">how-to video</a>.</p>
</td> 
  </tr> 
 </tbody> 
</table>

<table> 
 <thead> 
  <tr> 
   <th> <strong>Microsoft Dynamics 365 integration (GA)</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> 
    <p>The integration between Adobe Campaign Standard and Microsoft Dynamics 365 is now available. You’ll be able to transfer your contact and custom entity records from Dynamics 365 to Campaign, and get email event data back from Campaign to Dynamics 365 for better sales/marketing alignment.</p>
    <p>Refer to the <a href="../../integrating/using/working-with-campaign-standard-and-microsoft-dynamics-365.md">detailed documentation</a> to set this integration up and view the <a href="https://docs.adobe.com/content/help/en/campaign-standard/using/integrating-with-adobe-cloud/campaign-and-microsoft-dynamics-365/working-with-campaign-standard-and-microsoft-dynamics-365.html">how-to video</a>.</p>
  </td>
  </tr> 
 </tbody> 
</table>

**Improvements**

* The consent pop-up for Dynamic reporting has been updated to include Adobe Campaign Standard and Microsoft Dynamics 365 integration. By accepting the terms, profile data will be included when using the Adobe Campaign Standard / Microsoft Dynamics 365 integration and Dynamic Reporting. [Read more](../../reporting/using/about-dynamic-reports.md#dynamic-reporting-usage-agreement) (CAMP-29766)
* Fixed an issue which displayed incorrect contact dates when receiving delivery alerts. 
* When a transactional message event is submitted with an unknown context parameter, Campaign now returns a “400” error message instead of “500". (CAMP-28632)
* A new **Exclude proof** segment has been added in Dynamic reporting. This segment is now selected by default to filter your reports. [Read more](../../reporting/using/list-of-components-.md#segments)
* The **Message expiration** option has been added to push notification. It allows you to specify an expiration date where the message will no longer be sent by Apple (APNS) or Android (FCM). [Read more](../../channels/using/customizing-a-push-notification.md#add-expiration-date)
* Improvements have been made to the **Load file** activity: workflow logs have been made clearer and more detailed about the error that occurs when a file fails to load. The outbound transition generated when activating the **Keep the rejects in a file** option has been renamed **Rejects**. [Read more](../../automating/using/load-file.md)
* Multilingual related logs have been added to the sending logs to better understand sending failures due to missing languages in the uploaded CSV files.

**Security enhancements**

* Fixed an issue, when deleting a quanrantined profile's information via a privacy request, which removed all data except the email address in the quarantine list. 
* Security has been enhanced for protection against injections in email headers.
* Security has been enhanced for protection against SSRF attacks where xtk expressions can be used (email HTML, text content and subject, SMS and push notification content).

**Email Designer enhancements**

* Fixed an issue which prevented unsubscription, subscription and landing page links from being tracked when inserted in an email. (CAMP-37809)
* Fixed an issue which could lead to errors when creating a new email and selecting a template. (CAMP-38000)
* When editing a link using the Email Designer, you can now use the **Underline link** option. Also, a **Target** property has been added with the default value set to **None**. [Read more](../../designing/using/styles.md#about-styling-links)
* Fixed a color issue on links in text components in the body of an email. (CAMP-37330)
* Fixed an issue which prevented associated links from being removed when deleting an image. (CAMP-37234)
* Fixed an issue which prevented saving modifications on the **Order** settings of dynamic content in a condition. (CAMP-36883)
* Fixed an issue when searching landing pages. The search has been extended from the 50 first created to all the database. (CAMP-36839)
* Fixed an issue when saving modifications on the email sender in the **From: Name** field. (CAMP-36606)
* The carousel component compatibility warning has been modified to reflect supported email clients.
* Fixed a display issue on mobile. The height attribute is now always set to “height: auto” when adding or uploading a new image in an email. (CAMP-35497)
* Fixed an issue which left style and meta tags in the HTML when deleting a fragment from a structure component. (CAMP-35390)
* Fixed an issue with fragments when updating reusable content. (CAMP-35186)
* Fixed an issue when displaying mobile only conditional content in emails. (CAMP-35155)
* Fixed an issue which randomly displayed zero width non-breaking spaces. (CAMP-35116)
* Fixed an issue with the position of buttons in the **Save as fragment** dialog box.
* Fixed a preview issue when adding an HTML tag in an image title and alternative text. 
* Fixed an issue when editing, in the Email designer, links created in emails from the legacy editor.
* Fixed an issue which left duplicated style tags in the content.
* Fixed an issue with the date format when inserting a personalization field in an email. 
* Fixed a saving issue when switching from HTML mode to plain text.
* Fixed an issue when clicking the lock and unlock option which added margin values in the inline style property panel.
* Fixed an issue with the size of mobile preview for better rendering.
* Fixed an issue with the size of buttons in templates and fragments.
* Fixed an issue with the size of images when inserted in a button component.

**Other changes**

* The default time range for which data is shown on the delivery KPI pages and on the Dynamic Reporting page has been aligned to prevent discrepancy in reporting results. (CAMP-35148)
* An error message has been added in logs when the application certificate is expired. 
* The payload calculation preview now includes custom field size to prevent push notification failures. (CAMP-35303)
* The name of the **Rejects file** in the **Load file** activity can now be personalized in the same was as in the **File export** activity.
* All custom entities that are not linked to any out-of-the-box entity can now be accessed via the API.
* Improved database performance on large resources. 
* The descriptions of some errors occurring when sending SMS messages have been made clearer. (CAMP-36558) 
* An error message now displays when executing a workflow's **Scheduler** activity that is connected to itself, either directly or through several activities, as this could lead to the instance's workflow server being stuck.
* Improvements have been made to help troubleshoot transactional messaging: the "Data" link has been renamed "Last transactional events" in the event configuration screen, it now lists the received events sorted in a descending order. Also, a new transactional event status has been created: "targetingFailed". When the transactional messaging module fails to enrich a link that is used for message targeting, the transactional event will now be in this new state (instead of the "routingFailed" status).
* Improvements have been made to the interface when restricting landing page access to specific geographical or organizational units. The purpose is to warn that the landing page may be subject to visibility conditions: the selection of a geographical and organizational unit when creating a landing page is now mandatory. A banner with related information now displays once a unit is selected. The error message that displays when testing the landing page has been made clearer.
* In Campaign Standard APIs, custom keys cannot be modified using a PATCH operation if the key value is different from the origin key, or if you are using your own business key as URI instead of the one provided by Adobe.
* The "Albanian - Macedonia" language has been added to the preferred language drop-down list. (CAMP-35396)

**Patches**

* Fixed an issue that prevented scheduled reports from being sorted or searched.
* Fixed an issue with Triggers rules which caused the AND and OR rules to be mixed up. 
* Fixed an issue that displayed the Mobile property as Deleted in Launch. (CAMP-35382)
* Fixed an issue which prevented Adobe Launch mobile properties from being synchronized in Adobe Campaign. (CAMP-35411, CAMP-35089, CAMP-35014, CAMP-35487)
* Fixed an issue where transactional push messages failed when events were enriched with profile data. (CAMP-34385)
* Fixed an issue with mobile properties not syncing on multiple environments. (CAMP-37060)
* Fixed an issue when selecting, in a push notification, a template using a contact date formula. (CAMP-35300)
* Fixed an issue which could cause the message sending service to crash. (CAMP-35287)
* Fixed an issue with recurring direct mails which were all defined with the first event date. (CAMP-35139)
* Fixed an issue with newly extended **Profiles** custom resources which were not available for queries. (CAMP-35119)
* Fixed the **Repair database structure** mode for instances with Sharding configuration activated. (CAMP-35118)
* Fixed an issue which led to an SQL log error when adding aggregate data on broadlogs. (CAMP-35034)
* Fixed an issue with transitions when creating a **Segmentation** activity. (CAMP-35033)
* Fixed an issue in the **Query** activity which prevented the **encryption_aescbcDecrypt** function from decrypting the **encryption_aescbcEncrypt** function. (CAMP-34952)
* Fixed an issue which could prevent the **Tracking logs** from being displayed in deliveries. (CAMP-34855)
* Fixed an issue, when using a **Send time optimization** custom date formula, which could prevent push notifications from being sent due to errors with the workflow's additional data. (CAMP-30336)
* Fixed an issue that could prevent custom resources from being published. (CAMP-37425)
* Fixed an issue that prevented Admin users from modifying import packages.  (CAMP-37176)
* Fixed an issue in workflows that prevented proofs from being sent, if the delivery activity was connected to an empty **Read audience** activity. (CAMP-37164)
* Fixed an issue that prevented custom resources from being imported into a new environment. (CAMP-36506)
* Fixed an issue in hot click reports that could lead to percentages being hidden by images (CAMP-36407)
* Fixed an issue that occurred when trying to export a delivery description field. (CAMP-35467)
* Fixed an issue that could leave the state of a delivery as "Start pending” although the delivery was finished. (CAMP-35355)
* Fixed an issue that prevented workflow logs from being displayed after enabling, then disabling SQL logs.

## Release 19.3 - July 2019 {#release-19-3---july-2019}

**What's new?**

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> External API Activity (Public Beta)<br /> </td> 
   <td> <p>For deeper personalization, External API Activity allows you to bring data from external systems into a workflow via a REST API call. The REST endpoints can be a customer management system, Adobe I/O Runtime or Adobe Experience Cloud REST endpoint (e.g. Data Platform, Target, Analytics, Campaign).</p><p>This capability is currently in public beta.</p><p>For more information, refer to the <a href="../../automating/using/external-api.md">detailed documentation</a> and the <a href="https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/managing-processes-and-data/data-management-activities/external-api-activity.html">how-to video</a>.</p></td> 
  </tr> 
  <tr> 
   <td> Report on workflow segment<br /> </td> 
   <td> <p>This feature allows marketers to break down their delivery performance by segment code. When you create a workflow and use a segmentation activity to assign segments to the delivery population, these segments can now go into the same delivery. This allows you to display the opens/clicks statistics based on multiple segments within a single delivery.</p><p>For more information, refer to the <a href="../../reporting/using/creating-a-report-workflow-segment.md">detailed documentation</a> and the <a href="https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/reporting/report-on-workflow-segments.html">how-to video</a>.</p></td>
  </tr> 
 </tbody> 
</table>

**Security enhancements**

* Fixed a security issue to prevent denial of service (DoS) attacks on invalid requests to get images. (CAMP-33454)

**Email Designer enhancements**

* Fixed an issue that added additional HTML style tags to an HTML template each time a component was added, which could dramatically increase the template’s size. (CAMP-34694)
* Fixed an issue that could prevent some right top toolbar menu options from being available. (CAMP-34577)
* Fixed an issue that occurred when the Mirror page URL content block was inserted into an email content. (CAMP-34779)
* Fixed an issue that occurred when using JSPP code in an email, making it difficult to edit the content. (CAMP-34574)
* Fixed an issue that resulted in images truncated on top when a hyperlink was added to them. (CAMP-34382)
* Fixed a display issue when using the Email Designer with Firefox. (CAMP-34364)
* Fixed several issues that occurred with the Advanced mode when defining dynamic content in an email. (CAMP-34351, CAMP-34333, CAMP-34331)
* Fixed several issues that occurred with the dynamic content rule editor (CAMP-34304, CAMP-34303).
* Fixed an issue that could prevent the Link field from being displayed in the Email Designer Settings pane (CAMP-33749).
* Fixed an issue with the YouTube icon that was oversized in sent emails. (CAMP-33726)
* Fixed a security issue that made the mirror page content editable. (CAMP-33691)
* Fixed an issue that broke the HTML output when using the greater than symbol in dynamic content. (CAMP-33688)
* Fixed an issue that occurred on using the Undo option when editing text in the Email Designer. (CAMP-32565)
* Fixed an issue that created extra tags when undoing styles instead of removing them. (CAMP-32359)
* You can now define if each component used in an email will be shown only on desktop devices or only on mobile devices.
* You can now set the width and height of a Social content component.
* Fixed an issue that prevented dynamic content old source code from being removed after deleting that dynamic content.
* Fixed an issue that could prevent the subject of an email from being updated after it was modified.
* Fixed an issue that prevented a n:n column structure from being selected once dropped into the workspace.
* Fixed an issue that made the thumbnail of the message appear blurred in the email dashboard.
* Fixed an issue that prevented the background from being correctly displayed for emails received in Outlook.
* Fixed some sorting issues on the Email Designer home page.
* Fixed an issue that occurred on duplicating variants when using dynamic content.
* Some unwanted fields were removed from the Email Designer Settings pane.

**Other improvements**

* Through the integration with Adobe Experience Platform Location Services, Adobe Campaign is now compatible to send location-based marketing messages to your mobile application's subscribers via the Experience Platform SDK. For more information, refer to the [detailed documentation](../../integrating/using/configuring-campaign-points-of-interest-data-integration.md).
* The reporting feature has been improved for a better experience. To use this feature, you need to accept the Dynamic Reporting Usage Agreement. For more on this, refer to the [detailed documentation](../../reporting/using/about-dynamic-reports.md#dynamic-reporting-usage-agreement).
* In workflows, a new option has been added to preview the next ten executions of a workflow. For more on this, refer to the [detailed documentation](../../automating/using/scheduler.md).
* In the Scheduler activity, a new option allows you to select a specific day of a specific week for monthly deliveries. For more on this, refer to the [detailed documentation](../../automating/using/scheduler.md).
* When creating recurring deliveries with no aggregation period, the delivery dashboard now allows you to request confirmation before the delivery is sent. For more on this, refer to the [detailed documentation](../../sending/using/confirming-the-send.md).
* You can now personalize a delivery’s label with event variables that have been declared in the workflow’s external signal activity. For more on this, refer to the [detailed documentation](../../automating/using/calling-a-workflow-with-external-parameters.md).
* The GDPR delete query has been improved for better performance. (CAMP-33504)
* The "ftp" option was removed from the external account configuration interface. (CAMP-34472)
* You can now enable and disable the SMTP test mode option for each email message. For more on this, refer to the [detailed documentation](../../administration/using/configuring-email-channel.md#smtp-test-mode). (CAMP-34602)

**Other changes**

* A warning was added in the delivery properties interface. It specifies that deliveries are prepared based on their aggregation period and thaw to call the workflow multiple times a day, you should make sure they don't have any period. (CAMP-34393)
* A warning has been added in custom resource configuration screens. We recommend using 30 characters maximum for custom resource IDs. This also applies to custom resource fields, keys, indexes and links.
* A message now appears when trying to delete a transactional message that is used by a landing page as a confirmation message.
* A warning now appears in workflows logs when an activity has been running for more than 6 hours. This does not apply to Push notification, Delivery, Signal, Start, End, Fork , AND-joint, Schedule, and Wait activities.
* A warning now appears in workflows logs when you reach the maximum number of workflows that are simultaneously running.
* Workflows that have been in pause or fail status for more than 7 days are now stopped in order to consume less disk space. The cleaning task is displayed in the workflow logs.
* When using a "Transfer file" activity, an error is now logged if the file size exceeds the available disk space.
* The Redirect to destination URL action can no longer be selected for the secondary button in In-App messages.

**Patches**

* Fixed an issue which could cause GDPR access requests to fail.
* Fixed an issue which could lead to triggers being discarded when multiple triggers were received for a unique profile.
* Fixed an issue which could lead to an erroneous custom resource publication error message after login.
* Fixed an issue which displayed a blank page when creating or extending a custom resource.
* Fixed an issue which prevented an audience with appSubscriptionrcp as the targeting dimension from being available for targeting in a mobile delivery.
* Fixed an error which prevented hard bounces email addresses from being put in quarantine. (CAMP-24587)
* Fixed an issue which occurred when adding a typology rule, then deleting it before saving the typology. (CAMP-32789)
* Fixed an issue that could prevent landing page content from being displayed when disabling dynamic content. (CAMP-32924)
* Fixed an issue with recurring deliveries which occurred when using personalization on a primary delivery's attributes. (CAMP-32983)
* Fixed an issue in workflows which prevented from reading results from a transition containing incoming SMS messages data. (CAMP-33134)
* Fixed an issue in workflows which occurred when combining fork and exclusion activities to create audiences. (CAMP-33401)
* Fixed an issue that could prevent mirror page content from being displayed, and proof messages from being sent for recurring deliveries. (CAMP-33413)
* Fixed an issue leading to an error when using a Union activity between profiles and audiences. This issue was caused by an incompatibility of the identification keys in input transitions. (CAMP-33713)
* Fixed an issue in the Test activities which prevented the "recCount" expression from using the correct syntax when double-clicking it. (CAMP-33756)
* Fixed an issue that could lead to an error message when opening the Billing technical workflow logs. (CAMP-34313)
* Fixed an issue in landing pages that could occur when configuring checkbox fields with subscriptions. (CAMP-34369)
* Fixed an issue that occurred when configuring a list and adding the "icon" field to it. (CAMP-34585)
* Fixed an issue which prevented from using the "|" and "%" symbols as date or time separators in Load file workflow activities. (CAMP-34706)
* Fixed an issue which occurred when using visibility conditions with checkboxes in landing pages. (CAMP-34802)
* Fixed an issue in the Enrichment activity that prevented fields from displaying in the "Additional data" tab, if the filtering dimension was set to tracking logs and the target dimension to profile.
* Fixed an issue that led to an error message when exporting a "workflowTemplate" resource.
* Fixed an issue when creating a new profile, which prevented the "Country/Region code" field from being saved if it was selected from the dialog box.
* Fixed several issues that occurred when using the Direct Mail import template (updateQuarantinesDeliveryLogsDirectMail).
* Fixed an issue related to the Assets on Demand integration.
* Fixed an issue that occurred when zooming in on the Timeline view. (CAMP-33628)
* Fixed an issue that prevented proofs from being instantly sent for email messages with a scheduled date and time. (CAMP-33723)
* Fixed an issue related to transactional messaging that generated error logs when a user logged out. (CAMP-31698)
* Fixed an error that could occur on specific environments when scheduling an email message.
* Fixed an issue that caused the Update delivery execution workflow to fail.
* Fixed a security issue that broke the email content when the subject contained multiple lines.


## Release 19.2.7 - July 2019 {#release-19-2-7---july-2019}

**Improvements**

* The GDPR delete query has been improved for better performance.
* Fixed an issue which could cause web crashes after the 19.2 upgrade. (CAMP-34862)
* Fixed an issue which could prevent non-administrator users from saving or scheduling reports. (CAMP-31133)
* Fixed an issue when using "|" as the date separator in the Load file workflow activity. (CAMP-34706)

## Release 19.2.4 - June 2019 {#release-19-2-4---june-2019}

**Email Designer**

* Fixed an issue which prevented users from editing fragments when empty style tags were used in the HTML. This is a follow-up fix for CAMP-33778 in 19.2.3.

## Release 19.2.3 - June 2019 {#release-19-2-3---june-2019}

**Email Designer**

Introduced a series of improvements and fixes to optimize fragments in the 19.2 release. Newly created fragments will work seamlessly. Fragments that were previously built have been grayed-out and need to be migrated to the new format. To do so, click on each fragment and validate its migration to the new format. We recommend that you test a few fragments before migrating them all.

* Fixed an issue which prevented users from editing a fragment after unlocking it. This was affecting existing fragments when updating to 19.2. (CAMP-33778)
* Fixed an issue when using dynamic content. Extra spaces were added in the HTML.

**Other improvements**

* Fixed an issue which could prevent SMS sending from resuming after a disconnection of the SMS connector.
* Fixed an issue which could close SMPP connections when TLS was enabled.
* Fixed an issue which could close SMPP connections when TLS was enabled.
* The “Launch_URL_Campaign” option has been added in Campaign to manage properties of mobile applications created with Adobe Experience Platform Mobile SDK.
* Fixed an error that led to the Sandbox environment option being unchecked after uploading the certificate of a newly created mobile property and exiting the mobile application property page.
* Fixed an issue which prevented you from enriching a transactional message content with information from the Service resource. (CAMP-33707)
* Fixed an issue in the denylist landing pages that occurred when trying to unsubscribe profiles from a service.

## Release 19.2 - May 2019 {#release-19-2---may-2019}

**What's new?**

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Control Panel<br /> </td> 
   <td> <p>To help increase efficiency in your work as an Admin user, you can easily monitor capacity and manage settings of your instances (starting with SFTP servers management).</p><p>For more information, refer to the <a href="https://docs.adobe.com/content/help/en/control-panel/using/control-panel-home.html">detailed documentation</a> and the <a href="https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/control-panel-overview.html">how-to video</a>.</p></td> 
  </tr> 
  <tr> 
   <td> Local notifications<br /> </td> 
   <td> <p>Local notification messaging allows you to inform your users when new data becomes available within their mobile applications, even without having access to the Internet or the mobile application running in the foreground. Local notifications are triggered by a mobile application on a particular time and depending on an event.</p><p>For more information, refer to the <a href="../../channels/using/customizing-an-in-app-message.md#customizing-a-local-notification-message-type">detailed documentation</a>.</p></td> 
  </tr> 
  <tr> 
   <td> Workflow enhancement - Add a payload to external signal activity<br /> </td> 
   <td> <p>Start a workflow with a payload when defined conditions are successfully met from another workflow or a REST API call to integrate with your external systems. This also includes a new <strong>test</strong> activity where you can run tests on this functionality.</p><p>For more information, refer to the <a href="../../automating/using/calling-a-workflow-with-external-parameters.md">detailed documentation</a> and the <a href="https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/managing-processes-and-data/execution-activities/external-signal-activity.html">how-to video</a>.</p></td> 
  </tr> 
  <tr> 
   <td> Landing Pages enhancement - Google reCAPTCHA<br /> </td> 
   <td> <p>Leverage Google reCAPTCHA to prevent spam on your landing pages without requiring any action from your customers.</p><p>For more information, refer to the <a href="../../channels/using/configuring-landing-page.md#setting-google-recaptcha">detailed documentation</a>.</p></td> 
  </tr> 
 </tbody> 
</table>

**Security enhancements**

* Fixed a potential clickjacking security issue in reporting workspace.

**Email Designer enhancements**

* Fixed an issue that occurred when duplicating fragments and trying to use them in the Email Designer. (CAMP-33193)
* Fixed an issue that created unwanted spaces when using inline elements in the Email Designer interface. (CAMP-32163)
* Fixed an issue that deleted some additional HTML tag attributes added by the user after saving email content in the Email Designer. (CAMP-32162)
* Fixed an issue that displayed a Microsoft Office tag in the Email Designer HTML mode even after removing it. (CAMP-32141)
* If you created an email using a previous version of the Email Designer, upon opening this email content, a pop-up window now prompts the user to update to the latest version. (CAMP-31529)
* Fixed an issue that could distort images from an email created with the Email Designer when delivered to some messaging clients. (CAMP-31407)
* Fixed an issue that prevented some elements such as lists or buttons from being correctly displayed in plain text mode when created in HTML mode. (CAMP-32582, CAMP-32542)
* Fixed an issue that prevented displaying more than 50 organizational units in a content template or fragment properties. (CAMP-32932)
* Fixed an issue with the viewport background color when receiving an email created with the Email Designer on Outlook. (CAMP-31402)
* Fixed an issue that could prevent email contents created with the Email Designer from being responsive when opened in Outlook. (CAMP-31400)
* Fixed an issue that prevented dynamic content from working properly when used in an email subject. (CAMP-32837)
* Fixed an issue related to the email subject that was not properly escaped.
* Fixed an issue that prevented fragments from being loaded in the Email Designer left palette.
* Fixed an issue that prevented fragments created during email content edition from being displayed in the Email Designer left palette when refreshing the fragment list.
* Fixed several issues that occurred while using dynamic content in an email.
* Fixed an issue that occurred with the color picker when trying to define a color using RGB values.
* Fixed an issue that prevented the mirror page from being responsive when receiving the email on a mobile.

**Transactional Messaging enhancements**

Several improvements have been added to the Transactional messaging channel in order to optimize operation and performance.

* The transactional message duration has been extended to make sure that all messages are sent before they expire, especially when retries are performed.
* Transactional messaging performance has been increased by distributing the load on different sending threads.
* The transactional messaging process has been optimized to be able to start in parallel multiple analysis of the same message. 
* Fixed an issue that could lead to inconsistent throughput and latency for transactional push notifications.
* Fixed an issue that displayed an incorrect target audience for transactional message execution deliveries.
* Fixed an issue that occurred when importing a package with an event configuration and the associated transactional message. For more on this, refer to the [detailed documentation](../../channels/using/getting-started-with-transactional-msg.md#exporting-and-importing-transactional-messages).
* Fixed an issue that deleted the collection data from the test profiles created for a transactional message containing product listings.

**Other changes**

* A new option has been added to the SMS external account. It enables to limit the maximum number of MTA processes that send SMS in order to better control the number of parallel connections. For more information, refer to the [SMS connector protocol and settings](https://helpx.adobe.com/campaign/kb/sms-connector-protocol-and-settings.html) technote.
* When publishing a resource with API extension, if the API has already been published, it is now automatically updated each time it is published again. Previously this action was manual and failing to update the API could break the profile or service resource of this API. For more on this, refer to the [detailed documentation](../../developing/using/updating-the-database-structure.md#publishing-a-resource-with-api-extension).
* Zip code dimension has been removed from Dynamic Reporting. We recommend using City, Country, State dimensions instead.
* The ‘First Launch’ Lifecycle event trigger for In-App messages has been removed.
* When exporting a package with security groups, it now contains the roles that are assigned to each group. (CAMP-32960)
* In the Load file activity, a new option lets you check that the columns of the file you are uploading match the column definition. For more information, refer to the [detailed documentation](../../automating/using/load-file.md). (CAMP-32229) 
* Workflows can now be started with a payload, allowing you to use and share external parameters between activities within the workflow. For more information, refer to the [detailed documentation](../../automating/using/calling-a-workflow-with-external-parameters.md). (CAMP-29412 & CAMP-29413)
* Campaign Standard APIs now let you update profiles' geographical and organizational units using a payload. For more information, refer to the [detailed documentation](../../api/using/get-started-apis.md).
* Error messages when an object from the database is not accessible have been made clearer to understand.
* In the Extract file activity, Javascript capabilities have been updated when defining the name of a file to export. Only the formatDate function is now available for use in the Output field. For more information, refer to the [detailed documentation](../../automating/using/extract-file.md).
* Auto sequence ID generation has been improved for custom resources. Primary keys for new custom resources are now in 64 bits by default.
* The custom resource publication test mode has been improved. A warning message is now displayed to users if the last custom resource publication failed and is not fixed. After a custom resource publication failure, you can rollback to last working version. For more information, refer to the [detailed documentation](../../developing/using/updating-the-database-structure.md#publishing-a-custom-resource).
* A new option was added in the Transfer file activity. It allows you to sort the files when using the File download action, in SFTP mode. For more information, refer to the [detailed documentation](../../automating/using/transfer-file.md). (CAMP-33109)

**Patches**

* Fixed an issue that could cause memory leak to the MTA when SMS settings were reloaded.
* Fixed an issue that could prevent publishing database updates in repair mode.
* Fixed an issue that caused discrepancy between Adobe Analytics Reports and Adobe Campaign Dynamic Reporting. (CAMP-25393) 
* Fixed an error which caused the Report sharing workflow to fail.
* Fixed an error that prevented users from sending In-App messages with just Media URL.
* Fixed an issue that displayed a mobile app even if its certificate was not uploaded to the instance. 
* Fixed an error that prevented personalization fields from working when using the **Target all users of a Mobile app** template. 
* New Campaign Standard instances were provisioned. (CAMP-32635 & CAMP-32344)
* Fixed an error that prevented the customization of date formula in a workflow. (CAMP-30336)
* Fixed an issue when defining a custom date formula that could prevent the "Additional data" and "Segment code" fields from being available in the drop-down list. (CAMP-32383)
* Fixed an issue that could prevent the "Transfer file" and "Extract file" activities from finding the files rejects if they were encrypted. (CAMP-32377)
* Fixed an issue in APIs that could prevent the lineCount filter from rendering the exact total count. (CAMP-31424)
* Fixed an issue in landing pages that could prevent input fields from showing the updated value once it had been modified. (CAMP-31401) 
* Fixed an issue which could lead a signal activity to activate unexpectedly. 
* Fixed an issue which could prevent email preview from displaying when the audience is empty.
* Fixed an issue in the “Extract file” activity that could generate a file while the "Do not generate a file if the inbound transition is empty" option was activated. 
* Fixed an issue that led the Deliverability workflow to turn off if it did not finish successfully. 
* Fixed an issue which could prevent users from saving or scheduling reports. (CAMP-31133)

## Release 19.1.3 - March 2019 {#release-19-1-3---march-2019}

**Email Designer enhancements**

* Fixed an issue which prevented a template from being modified after saving it.
* Fixed various issues when using a previously created template in an email.
* Fixed an issue which prevented components from being hidden in imported templates.

**Other improvements**

* Fixed an error when viewing typology rules. (CAMP-32059 & CAMP-31849)
* Fixed an issue which prevented typology rules from being edited. (CAMP-31750)
* Fixed an issue with the inMail process which could stop unexpectedly. (CAMP-31238)

## Release 19.1 - February 2019 {#release-19-1---february-2019}

**What's new?**

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Push channel Reporting improvements<br /> </td> 
   <td> <p>Several enhancements have been added to Push channel reporting to allow you to measure user engagement more intuitively. With this release, we are expanding the list of Push channel metrics to three different metrics: Impressions, Clicks, Opens (App Open) to help you measure and analyze users’ interaction with Push notifications more effectively. Along with this, we are also standardizing the definition and implementation of these metrics. The Push notification built-in report has also been improved with commonly used visualizations and metrics.</p><p> For more information, refer to the <a href="../../reporting/using/push-notification-report.md">detailed documentation</a>.</p> </td> 
  </tr> 
  <tr> 
   <td> Launch integration for Mobile App<br /> </td> 
   <td> <p>This release contains the integration of Adobe Campaign with the GA versions of Android and iOS extensions for Adobe Campaign Standard in Adobe Experience Platform Launch and Mobile SDKs. These extensions support push messaging, in-app messaging, and mobile app profile updates.</p><p> For more information, refer to the <a href="https://helpx.adobe.com/campaign/kb/configuring-app-sdk.html">detailed documentation</a>.</p> </td> 
  </tr> 
  <tr> 
   <td> Mobile In-App Messaging<br /> </td> 
   <td> <p>This release contains the GA version of In-App channel in Campaign. From a functional standpoint, the most notable additions to the Beta release are Dynamic reports for In-App channel and secure handshake between Mobile SDK and MCIAS (Marketing Cloud In-App Messaging Service that serves the In-App rules to the SDK). Secure handshake ensures that your users' PII data does not fall into malicious hands as well as enables you to maintain users' privacy on a shared device by clearing out message cache every time the user logs out.</p><p>For more information, refer to the <a href="../../channels/using/about-in-app-messaging.md">detailed documentation</a> and the dedicated <a href="https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/communication-channels/mobile/in-app/in-app-message-overview.html">In-App tutorial</a>.</p> </td> 
  </tr> 
  <tr> 
   <td> Workflow enhancements<br /> </td> 
   <td> <p>The following workflow capabilities have been added:</p> 
    <ul> 
     <li> You can now copy-paste activities within a workflow or another workflow from the same Campaign instance. This way, you can easily duplicate an entire workflow or specific activities, and keep the settings that were initially defined. For more information, refer to the <a href="../../automating/using/workflow-interface.md#duplicating-workflow-activities">detailed documentation</a>. (CAMP-20014) </li> 
     <li> When using the <strong>Load file</strong> activity, you can now add a timestamp to the name of the file containing the rejected records. For more information, refer to the <a href="../../automating/using/load-file.md#configuration">detailed documentation</a>. </li> 
     <li> <strong>Query</strong> and <strong>Segmentation</strong> activities now let you enable an outbound transition if the activities retrieve no data. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

**Security enhancements**

* The generated landing page HTML code has been updated to prevent search engine indexing.

**Email Designer enhancements**

* A set of four best-in-class responsive email templates designed by Behance artists is now available.

  For more information, refer to the [detailed documentation](../../designing/using/using-reusable-content.md#content-templates).

* Our new on-boarding experience will help you start email creation faster and give you easier access to documentation and tutorials.

  For more information, refer to the [detailed documentation](../../designing/using/designing-content-in-adobe-campaign.md#email-designer-home-page).

* You now have the flexibility to configure the number of columns and width based on your needs.

  For more information, refer to the [detailed documentation](../../designing/using/designing-from-scratch.md#defining-the-email-structure).

* When editing in mobile view, you can hide certain components just in mobile display for effective usage of space.

  For more information, refer to the [detailed documentation](../../designing/using/plain-text-html-modes.md#switching-to-mobile-view).

* You can now add custom social channels to your email template on top of the ones that are already available.
* Fixed an issue that prevented to scroll down the structure menu when using more than 18 structures. (CAMP-31173)
* Fixed an issue that displayed the preheader on top of the content when forwarding an email containing a preheader sent with Adobe Campaign. (CAMP-30736)
* Fixed an issue that prevented the subject line from being updated when clicking the **Refresh AEM content** option after modifying the subject in Adobe Experience Manager. (CAMP-29984)
* Fixed several issues that prevented the use of dynamic images from Adobe Target.
* Fixed an issue that prevented the preview from being updated when retrieving content at preparation time if the content had been previously imported from a URL.
* The YouTube icon has been added to the **Social** content component.
* The **List** view has been added for content components and fragments displayed in the Email Designer palette.

**Other improvements**

* Adobe Campaign is now fully FCM compliant for both SDK V4 and AEP SDK Apps.
* Adobe Campaign supports Push notifications on Wear OS by Android as well as watchOS by Apple.
* Warning and error messages that may display when navigating in the interface have been made clearer and easier to understand. 
* You can now add to the profiles list columns related to opt-in and opt-out ("No longer contact …" fields).
* The Time zone drop-down list in the Profile creation screen has been moved from the Address section to the upper-section of the interface. 
* You can now add separators when configuring custom resource screens, allowing you to organize your fields into categories.

  For more information, refer to the [detailed documentation](../../developing/using/configuring-the-screen-definition.md#defining-the-detail-screen-configuration).

**Other changes**

* Adobe Campaign and Adobe Experience Cloud will drop support for Microsoft Internet Explorer 11 starting Spring 2019, and Campaign Standard 19.2 release. Please switch to Microsoft Edge or another supported browser. See [Deprecated and removed features](https://helpx.adobe.com/campaign/kb/acs-deprecated-and-removed-features.html) page.
* The **Country code** field from the Profile resource has been renamed to **Country/Region code**.

**Patches**

* Fixed an issue that prevented the message from being sent when adding a test profile to an email transactional message. (CAMP-29854)
* Fixed an issue that slowed down message sending from other channels if sending was low for one channel when message sending from all channels was triggered simultaneously.
* Fixed an issue that caused the MTA to start sending SMS messages when the external account connection was not yet established.
* Fixed an issue that occurred with the Scheduler activity execution frequency and start time. (CAMP-30745) 
* Fixed an issue that could occur with PKEY generation when using extended profile resources. (CAMP-30285) 
* Fixed an issue that could occur with calendar day based Fatigue rules. (CAMP-30136) 
* Fixed an issue that could occur when trying to access custom resources with names ending with "Base". (CAMP-30109) 
* Fixed an issue that prevented from using a PATCH call to subscribe a profile to a service. (CAMP-29728) 
* Fixed an issue that could corrupt a workflow when importing an XML file through the Load File activity. (CAMP-29208 and CAMP-28205) 
* Fixed an issue when linking custom resources which could prevent reverse cardinality links to be generated. (CAMP-30476)
* Fixed an issue that prevented from extending delivery logs when using the segment code only. 
* Fixed an issue which could duplicate rows when using the File transfer activity in workflows.
* Fixed an issue which prevented scheduled reports from being sent at the chosen time. 
* Fixed an issue which caused discrepancy between the "To deliver" and "Sent" KPIs for an In-App delivery in a workflow. 
* Fixed an issue that prevented tracking from working for an In-App message authored with a custom HTML.
* Fixed an issue that prevented In-App delivery content from being saved when used in a workflow. 
* Fixed an issue that prevented mobile applications from being displayed for administrators. 
* Fixed an issue which caused the Deliverability Update technical workflow to fail. (CAMP-26387) 
* Fixed an issue which caused discrepancy between the profiles targeted while creating an In-App delivery and the ones displayed in the delivery dashboard. (CAMP-28722)
* Fixed an issue with the Campaign and Assets Core Service integration which could prevent you from selecting a shared asset in an email.

## Release 19.0 - January 2019 {#release-19-0---january-2019}

**What's new?**

<table> 
 <colgroup><col style="width: 30%"><col style="width: 70%"></colgroup>
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Email Designer General Availability<br /> </td> 
   <td> <p>The new intuitive Email Designer (formerly known as Creative Designer) has moved to GA. It now supports all the features from the legacy content editor, including:</p> 
    <ul> 
     <li> The use of <a href="../../integrating/using/adding-target-dynamic-content.md">dynamic images from Adobe Target</a> </li> 
     <li> The ability to <a href="../../designing/using/using-existing-content.md#retrieving-content-from-a-url-automatically-at-preparation-time">retrieve content from a URL automatically at preparation time</a> </li> 
     <li> Fully compliant <a href="../../designing/using/using-reusable-content.md#content-templates">out-of-the box content templates</a>. </li> 
    </ul> 
    <p>For more information, refer to the <a href="../../designing/using/designing-content-in-adobe-campaign.md">detailed documentation</a> and the <a href="https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/designing-content/email-designer/email-designer-overview.html">how-to video</a>. Improvements and fixes are listed below.</p><p>As a consequence, the legacy email content editor is now deprecated. For more information, refer to this <a href="https://helpx.adobe.com/campaign/kb/acs-deprecated-and-removed-features.html">page</a>.</p> </td> 
  </tr> 
  <tr> 
   <td> Product Listings in Transactional Emails<br /> </td> 
   <td> <p>You can now reference one or more product collections in a transactional email message. For example, you can automatically send a cart abandonment email listing all the products that were in the user’s cart with an image, price, and link to each product.</p><p>For more information, refer to the <a href="../../channels/using/event-transactional-messages.md#using-product-listings-in-a-transactional-message">detailed documentation</a> and the <a href="https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/designing-content/product-listings-in-transactional-email.html">how-to video</a>.</p> </td> 
  </tr> 
  <tr> 
   <td> Mobile View in the Email Designer<br /> </td> 
   <td> <p>You can now switch to a dedicated mobile view when editing email content. This allows you to fine-tune the responsive design of an email by separately editing all style options for mobile display, such as adapting margins, smaller font size, different background color, and so on.</p><p> For more information, refer to the <a href="../../designing/using/plain-text-html-modes.md#switching-to-mobile-view">detailed documentation</a>.</p> </td> 
  </tr> 
  <tr> 
   <td> In-App Messaging Beta Improvements<br /> </td> 
   <td> <p>The In-App Messaging Beta feature has been enhanced with the following capabilities:</p> 
    <ul> 
     <li> In-App Beta channel is GDPR compliant </li> 
     <li> Integration with Analytics APIs to populate Triggers dropdowns </li> 
     <li> Intuitive look and description of delivery templates </li> 
     <li> Enhancements to authoring interface from usability standpoint </li> 
    </ul> <p>For more information, refer to the <a href="../../channels/using/about-in-app-messaging.md">detailed documentation</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

**Improvements**

* A new option in the Load data activity now lets you apply a post-processing stage to the file containing the rejected records (ex. Zip format compression). (CAMP-24521)
* A new option in the Update data activity now allows you to configure the maximum batch size for the data to upload. (CAMP-28400)
* Improved profiles' address state selection. When selecting a country, the "State" drop-down list is now automatically updated with relevant states values. (CAMP-28874)
* A new option in the Extract file activity now prevents from generating a file if the inbound transition is empty. This avoids creating and uploading empty files on SFTP servers.
* The Delivery summary report has been improved. 
* The list of available countries when defining a profile's address has been enriched. (CAMP-26707)
* An error message is now displayed when trying to import a built-in workflow.

**Email Designer**

* Fixed an issue that enabled the geographical unit capability on an email template or a content fragment created with the Email Designer, even though this capability was disabled in Adobe Campaign, which made the template or fragment unavailable when trying to access it again. (CAMP-28174)
* Fixed an issue that prevented Dynamic content conditions to be saved when editing content with the Email Designer. (CAMP-27905)
* Fixed an issue that removed the HTML version from the email content after editing the plain text version of a message and breaking HTML synchronization in the Email Designer. (CAMP-28507)
* Fixed an issue that prevented the Email Designer interface to open when using Internet Explorer 11. (CAMP-28273)
* Fixed an issue that distorted the Microsoft Outlook rendering of style settings applied to buttons with the Email Designer.
* Fixed an issue in the Email Designer that made editable a URL from a content fragment used in an email, which was not expected as the fragment is locked by default.
* Fixed an issue that prevented the Email Designer divider component to be displayed in Microsoft Office.
* Fixed an issue which caused a page freeze on certain Internet browsers when viewing a content synchronized from AEM using the legacy email content editor. (CAMP-29068)
* Fixed an error that occurred when clicking any image in an email when using the legacy email content editor. (CAMP-30424)
* Fixed an issue that prevented the newly created fragments to be displayed when editing an email with the Email Designer. (CAMP-29928)
* Fixed an issue that prevented button text to be displayed properly in emails created with the Email Designer and received using Outlook webmail client.
* It is now possible to create profile transactional messages using the Email Designer. (CAMP-28900)
* Fixed an error in the Email Designer that made the content editable when retrieving content from a URL automatically at preparation time, whereas it should be locked.

**Patches**

* Fixed an issue that showed incorrect delivery logs in Dynamic reporting. (CAMP-23446)
* Fixed an issue that could affect the numbers on the bounce Summary report (CAMP-28703)
* Fixed an issue with the Campaign and Assets Core Service integration which could prevent assets from being displayed when selecting **[!UICONTROL Image shared from Adobe Experience Cloud]** in an email (CAMP-28732).
* Fixed an issue that prevented SMS messages containing the ‘œ’ character to be sent even though transliteration was authorized in the SMPP external account. (CAMP-29041)
* Fixed an issue that could display duplicate records when using a Segmentation activity in workflows. (CAMP-28743) 
* Fixed an issue which prevented from deleting one of the value mappings on a column in a workflow activity. (CAMP-28708)
* Fixed an issue in the File transfer activity, when using wildcards with the "Test to see if file exists" option. (CAMP-28977)
* Fixed an issue in the File Transfer activity that could occur when updating external account settings. (CAMP-28894)
* Fixed an issue with custom filters in the query editor when using the "Email is not empty" condition. (CAMP-28741)
* Fixed an issue that could occur when exporting custom resource tables with more than 100k records. (CAMP-28150)
* Fixed an issue that prevented to delete transactional messages linked to triggers. (CAMP-28385)
* Removed passwords that were insecurely displayed in some SMS logs.
* Fixed an issue that caused the connections to the SMPP simulator to fail due to empty password sent by Adobe Campaign.
* Fixed an issue that prevented sending campaigns when SMS connections are unstable.
* Fixed an issue that displayed deleted deliveries in Dynamic reporting.
* Fixed an issue that could prevent from retrieving additional data from delivery logs, tracking logs and exclude logs tables, when using an Enrichment activity in a workflow.
* Fixed an issue with GDPR delete requests that could occur when using a "N cardinality collection link" link type and the "Deleting the target record implies deleting records references by the link" option.
* Fixed an issue with report sharing.
* Fixed an issue which could lead to throughput issues when sending a push notification. 
* Fixed an issue with direct mail output files missing fields.
* Fixed an issue which allowed users to modify built-in workflows.
* Fixed an issue when creating a campaign based on a campaign template including a workflow with a configured extract activity. (CAMP-29198)
* Fixed an issue with the File extraction activity which prevented from using the same expression for several elements. (CAMP-29182)
* Fixed an issue, in the query editor, with the join condition between broadlog and tracking log for rtEvent. (CAMP-28780)
* Fixed an issue which prevented modifications to the "Specific action" landing page option from being saved. (CAMP-29422)
* Fixed an issue which prevented from exporting an event's payload in a workflow. (CAMP-29029)
* Fixed an issue that prevented SMS numbers on the denylist from being excluded in an SMS message. (CAMP-28898)
* Fixed an issue which could prevent SMPP providers from being notified in case of an error while processing incoming messages. (CAMP-29804)
* Fixed an issue which allowed external accounts with associated deliveries to be deleted. (CAMP-29738)
* The sending throughput has been improved and stabilized for SMS messages.
* Fixed an issue which prevented the "~" character from being used in an SMS message. (CAMP-29172)
* Fixed an issue in deliveries with the Send time optimization option. (CAMP-29231)

