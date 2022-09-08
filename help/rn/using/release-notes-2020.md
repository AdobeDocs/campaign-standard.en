---
title: Release Notes 2020
description: This page lists all 2020 releases of Adobe Campaign Standard.
audience: rn
content-type: reference
topic-tags: campaign-standard-releases
feature: Overview
role: User
level: Beginner
exl-id: b6cf7152-2200-43d7-8d0a-d65752bb2c9b
---
# Release Notes 2020{#release-notes-2020}

![](assets/do-not-localize/cp-icon.png) **New Control Panel June release** with Active profiles monitoring, Subdomain deliverability audit and GPG keys management. [Learn more](https://experienceleague.adobe.com/docs/control-panel/using/release-notes.html).

![](assets/do-not-localize/cp-icon.png) **New Control Panel October release** with domain configuration using CNAMEs and new database monitoring capabilities. [Learn more](https://experienceleague.adobe.com/docs/control-panel/using/release-notes.html).

## Release 20.4 - October 2020 {#release-20-4---october-2020}

**What's new?**

<table> 
<thead> 
<tr> 
<th> <strong>Control Groups</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
  <td> <p>You can now use <strong>Control groups</strong> to measure the impact of your campaigns by excluding a portion of their audience. You will then be able to compare the behavior of the target population which did receive the message with the behavior of contacts which were not targeted. Based on the sending logs, you can also target a control group in future campaigns.
</p>
<p>For more information refer to the <a href="../../sending/using/control-group.md">detailed documentation</a> and <a href="https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/communication-channels/email/control-groups.html">how-to video</a>.
</p>
</td> 
</tr> 
</tbody> 
</table>

<table> 
<thead> 
<tr> 
<th> <strong>External API - OAuth Support</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
  <td> <p>Adobe Campaign now supports OAuth for authentication in the <strong>External API</strong> workflow activity. This new capability opens up the ability for this activity to communicate with systems requiring OAuth support.
</p>
<p>For more information refer to the <a href="../../automating/using/external-api.md">detailed documentation</a>.
</p>
</td> 
</tr> 
</tbody> 
</table>

<table> 
<thead> 
<tr> 
<th> <strong>Journey AI integration</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
  <td> <p>We are excited to announce Journey AI for all Adobe Campaign Standard customers.</p>
  <p>Journey AI uses advanced Machine Learning (ML) to enable companies to optimize the design and delivery of customer journeys by predicting each individual’s engagement preference.</p>
  <P>Journey AI consists of two ML features:</p>
<ul> 
     <li> <strong>Predictive Engagement Scoring</strong>  - Intelligently identifies customers' preferred level of engagement to better target and personalize messages to increase conversions and retention. Watch the <a href="https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/communication-channels/email/journey-ai/predictive-engagement-scoring.html">how-to video</a>.</li> 
     <li> <strong>Predictive Send Time Optimization</strong>  - Predicts the best time to send emails to each individual in a campaign to maximize engagement rates and improve email campaign ROI. Watch the <a href="https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/communication-channels/email/journey-ai/predictive-send-time-optimization.html">how-to video</a>.</li>
    </ul>
  <p>If you want to learn how to get started with Journey AI, please review the <a href="../../sending/using/predictive.md">detailed documentation</a> and reach out to your Account Executive. Note that while Journey AI is available for free to existing Campaign customers, there is an implementation cost of approximately 50 hours.</p>
    </td> 
</tr> 
</tbody> 
</table>

**Improvements**

* **Privacy Management**: the **CCPA Opt-Out** field, which was available via the Campaign interface and API, is now also supported through the Privacy Core Service. This field allows Adobe Campaign users to track whether a consumer has opted-out for the sale of Personal Information. [Learn more](https://helpx.adobe.com/content/help/en/campaign/kb/acs-privacy.html#ccpa)
* **Workflow execution improvements** (beta): in the context of a global initiative around workflows, some major improvements have been developed to stabilize memory management, reduce latency and optimize the memory consumed by workflows during execution. These improvements are currently in beta, and only available to a set of customers. General availability is planned for early 2021.
* To improve security, Campaign now uses a **signature mechanism** for tracking links in emails.
* Mobile app configuration has been improved with **clearer error messages** when uploading iOS certificates or Android keys.
* **SMS error management** has been improved to prevent too many profiles from being added to the quarantine list. By default, SMS errors are now configured as soft errors instead of hard errors. Refer to [this page](https://helpx.adobe.com/campaign/kb/sms-connector-protocol-and-settings.html).

**Email Designer enhancements**

* We have improved the user experience in the Email Designer with the **new dynamic contextual help** which fully connects user interface and documentation, providing an easy access to the latest help content.
* Fixed an issue which removed line breaks in a message when editing its text version. (CAMP-44483)
* Fixed an issue which prevented the plain text version of an HTML template from being automatically generated and synchronized. (CAMP-44195)
* Fixed an issue that could occur when resizing images. Once the messages were sent, the images did not display properly in Microsoft Outlook. (CAMP-44656)
* Fixed an issue which occurred when inserting a button and setting its width to "auto". Once the message was sent, the content of the button was not displayed entirely. (CAMP-44560)
* Fixed an issue which occurred when uploading content from an attached HTML file. Once the message was sent to a Gmail address, the CSS was not applied, causing a rendering issue. (CAMP-44085)
* Fixed an issue which prevented content fragments previously used in a message from being updated when they were modified directly in the content template. (CAMP-43973)
* Fixed an issue with the **Fragments** search bar. When searching for an existing fragment, the search bar showed no result. (CAMP-44223)
* Fixed an issue with the **Content Blocks** and **Fragments** search bars. When using one of the search bars, results were only displayed if you clicked **Show More Results...**. (CAMP-44205)
* Fixed an issue which prevented padding between text and images from being applied in Microsoft Outlook. (CAMP-45370)
* Fixed an issue when duplicating a fragment. After duplicating the fragment, the original fragment had missing HTML lines. (CAMP-45207)
* Fixed an error which caused rendering issues in Microsoft Outlook. (CAMP-44749)
* Fixed an error which occurred when modifying the **Structure Component** padding in a delivery template. CSS tags did not carry over changes made to the padding causing a rendering issue. (CAMP-45381)
* Fixed an issue when uploading an image. The image's height was automatically set to 0 causing a rendering issue. (CAMP-45366)

**Other changes**

* Retry mechanisms have been added in case of error when trying to import an Experience Platform audience using a **Read audience** activity. (CAMP-43947, CAMP-43366)
* Organizational units are now automatically set to match the organizational unit of the user creating the profile or entity. Organizational units can no longer be removed and left empty.
* When publishing a custom resource, a confirmation pop-up is now displayed after preparation.
* The pop-up message which appears when a custom resource fails has been improved for better clarity.
* The expression editor in workflows has been improved to prevent execution errors. [New functions](../../automating/using/customizing-workflow-external-parameters.md) are available: they can be used in all the activities that allow you to use event variables after calling a workflow with external parameters. Additionally, a tooltip now displays in the expression editor with the function description. 
* [New filters](../../channels/using/configuring-transactional-event.md#searching-transactional-events) have been added to the list of transactional events. They allow you to filter the event configurations according to their status, as well as the last time an event was received.
* The logs displaying when exporting packages have been made more specific and detailed about the encountered errors in case of failure.
* After sending a message, you can now search, filter and export the list of [tracked URLs](../../sending/using/tracking-messages.md).
* Automatic [synchronization between Launch and Campaign](../../administration/using/configuring-a-mobile-application.md#aepsdk-workflow) is now GA and enabled by default.
* The size of workflow export packages has been optimized by removing the sending proof export.
* A new message has been added to display the size of the downloaded file in the **File transfer** activity.
* Error messages for invalid session tokens have been improved.
* A new mechanism now prevents tracking events from proxies from being added to tracking logs and reporting.
* A new warning message has been added to help debugging data management activities connected to a delivery activity.
* Labels in the reporting workspace have been improved.
* A new validation step has been added to prevent the deletion of technical objects in transactional messages.
* A new filter on delivery status has been added in the **Execution list** tab of a transactional message to improve troubleshooting.
* To improve performance and optimize execution time, unused indexes have been removed, based on usage stats of tables identified in preliminary analysis for 350+ customers. Impacted tables are: nmsaddressStatus, nmscampaign, nmsdelivery, nmslandingpage, nmsprogram, nmsrecipient, nmsseedmember, nmsservice, nmssubhistorcp, nmsaudience, xtkworkflow

**Patches**

* Fixed an issue which prevented you from using a destination link for Push notifications or In-App messaging when tracking was enabled.
* Fixed an issue where high priority in transactional messages was not respected in case of significant bulk delivery.
* Fixed an issue which could prevent you from assigning brands to a transactional email. Several error messages could display during the publication step. (CAMP-44988)
* Fixed an issue in the workflow user interface which could prevent information from being saved in fields requesting numeric values. (CAMP-44025)
* Fixed an issue which could display an error message when using a **Test** activity in an import template workflow. (CAMP-42910)
* Fixed an issue which occurred when using a **Read audience** activity containing an enumeration type field and connected to **Union** or **Enrichment** activities. (CAMP-42795)
* Fixed an issue in Dynamic reports when using the out-of-the-box segments to filter data in reports. (CAMP-42627)
* Fixed an issue which prevented you from setting a **Scheduler** activity to 12 AM. (CAMP-42674)
* Fixed an issue which could interrupt the sending of SMS messages when the SMPP connection was unstable. (CAMP-42789)
* Fixed an issue which prevented the **Stop preparation** button from displaying after refreshing the page. (CAMP-42721)
* Fixed an issue which prevented hot click reports percentages from displaying when importing content from a URL. (CAMP-44468)
* Fixed an issue which could display a timeout error when selecting a profile to use in the context of profile substitution. (CAMP-44746)
* Fixed an issue which could prevent instances from working after deploying custom resources containing incorrect link definitions. (CAMP-44406)
* Fixed an issue which created empty linked entities (typologies, brands, etc.) after copying and pasting a delivery into a campaign template. (CAMP-44765)
* Fixed an issue which prevented proofs from being sent due to an incorrect handling of delivery preparation tables in case of a database crash or a simple database restart on Azure.
* Fixed an issue which could prevent you from deleting links with Experience Manager content in a delivery configured with multilingual content. (CAMP-44029)
* Fixed an issue in dynamic reports that could display an error message when trying to filter dimensions.  (CAMP-43097)
* Fixed an issue which could display a blank screen when trying to access profiles on an instance configured with custom resources containing specific link definitions. (CAMP-41009)
* Fixed an issue in workflows that could occur when using an **Enrichment** activity with two input activities having both target resources linked together. (CAMP-42133)
* Fixed an issue causing import workflows to loop when using a **File transfer** activity. (CAMP-43754)
* Fixed an issue which led to duplicates not being taken into account when creating a profile with exported logs. (CAMP-45031)
* Fixed an issue causing data discrepancy between reports in Adobe Campaign and reports exported in PDF files. (CAMP-43010)
* Fixed an error which caused the direct mail delivery workflow to fail when using existing data fields in functions. (CAMP-42737)
* Fixed an issue when importing packages including transactional events and message templates. The import process stopped at 5%. (CAMP-42544)
* Fixed an issue which caused an error (Uncaught TypeError) after modifying the **Enrichment** activity and adding additional data in a workflow. (CAMP-41877)
* Fixed an error which prevented workflow deletion. Logs had to be purged in order to delete the workflow. (CAMP-44144)
* Fixed an error when creating a landing page with HTML code. Mandatory checkboxes were not recognized in Campaign and were not available in the published landing page. (CAMP-44181)
* Fixed an issue causing workflows to loop when using the **Wait** activity. (CAMP-43981)
* Fixed an issue when sending transactional messages which led to several email addresses being targeted multiple times in a same delivery. (CAMP-44202)
* Fixed an error when using profile substitution with targetData personalization. (CAMP-44996)
* Fixed an issue which caused the delivery preview to fail when exporting a delivery template in a package. (CAMP-44084)
* Fixed an issue which prevented proofs from being sent to test profiles when using custom target mappings. (CAMP-43701)
* Fixed an error which occurred in workflows when using the **Read Audience** activity and targeting an audience configured with a targeting dimension other than **Profile**.  (CAMP-41885)
* Fixed an issue which led to errors when the **updateEventsStatus** technical workflow was taking too much time retrieving event history (when the workflow was stopped). The unused "sumQueueTime" aggregate field has been removed from the workflow to solve the issue. (CAMP-43920)
* Fixed a memory issue when deploying custom resources. (CAMP-42909)
* Fixed an issue in transactional messaging when attributes were missing in collections. Now all missing attributes are defined with a default value and included in the payload. (CAMP-42882)
* Fixed an issue that could affect performance when querying real-time event delivery logs. (CAMP-42759)
* Fixed an error which occurred when using upper case file extensions with Shared assets. (CAMP-44159)
* Fixed an issue which displayed an error message when testing the connection to an external account before it was created. The **Test connection** button now displays only once the external account has been created.
* Fixed an issue that left messages as pending after the Enhanced MTA was restarted on instances configured with sharding.
* Fixed an issue that could lead the active profiles count to mismatch the effective number of sent deliveries.
* Fixed an issue that could lead to latency when searching for resources in the query editor in a workflow.
* Fixed an issue when selecting the **Specify the fields to be taken into account in the text search** option in a custom resource. If the field list was left empty, the custom resource publication failed.
* Fixed a performance issue when displaying the overview of custom resources with a large volume of data.
* Fixed an issue which prevented you from importing a delivery using profile substitutions.
* Fixed an issue when using profile substitution which prevented proofs from being sent immediately if the delivery was scheduled.
* Fixed an issue that occurred when uploading an Android key for a mobile application. The message that showed up after successfully uploading the key displayed the value of the former key.
* Fixed an issue which prevented you from creating test profiles from transactional messages after creating an event configuration with a collection containing no attribute.
* Fixed an issue that could prevent you from publishing custom resources after creating a new filter using an aggregate.
* Fixed an issue causing an incorrect tracking open rate for Gmail recipients caused by the Gmail image proxy.
* Fixed an issue causing Out Of Memory errors when importing a package.
* Fixed an issue which caused the Experience Manager unlink action to fail when the Experience Manager content included a path with a "%20" character.
* Fixed an error on labels when duplicating workflow activities.
* Fixed an issue with the transactional message picker in a landing page when the **Start sending message** option was selected.
* Fixed an issue with transactional messages or recurring deliveries which prevented the delivery status from being initialized with the right default value. Error logs have also been improved.
* Fixed an issue when extending the **Subscription to an application** (appSubscriptionRcp) schema with a profile link using a custom field. The index was not automatically created which could affect push sending time. (CAMP-41120)



## Release 20.3 - May 2020 {#release-20-3---may-2020}

**What's new?**

<table> 
<thead> 
<tr> 
<th> <strong>Thailand's Personal Data Protection Act (PDPA)</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
<td> <p>Thailand's Personal Data Protection Act (PDPA) is the new privacy law that harmonizes and modernizes data protection requirements for Thailand. This regulation applies to Adobe Campaign customers who hold data for Data Subjects residing in this country.</p>
<p>In addition to the privacy capabilities already available in Adobe Campaign (including consent management, data retention settings, and user roles), we are taking this opportunity to include additional capabilities, to help facilitate your readiness for PDPA:</p>
<ul>
<li>Right to Access and Right to Delete: we are leveraging the capabilities that were added for GDPR and CCPA. <a href="https://helpx.adobe.com/content/help/en/campaign/kb/acs-privacy.html#righttoaccess">Learn more</a> </li>
<li><p>When creating a Privacy request, the PDPA regulation type has been added in the Privacy Core Service. This method is the one you should use for all access and delete requests. The use of the Campaign API and interface for access and delete requests is deprecated.  See the <a href="../../rn/using/deprecated-features.md">Deprecated and Removed Features article</a>.</p></li>
</ul>
<p>Refer to the <a href="https://experienceleague.adobe.com/docs/campaign-learn/campaign-standard-tutorials/privacy/privacy-overview.html">how-to video</a>.</p>
</td> 
</tr> 
</tbody> 
</table>

<table> 
<thead> 
<tr> 
<th> <strong>External API Activity (GA)</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
  <td> <p>The <strong>External API</strong> activity is transitioning from beta to GA. This release brings additional flexibility to the JSON response body parser. You can now:</p>
<ul>
<li>parse a nested JSON with a maximum depth of 10 levels. </li>
<li>parse selected properties as leaf nodes from a JSON and flatten them into a single table row.</li>
<li>select and use an array object from a JSON without having to name the object "data" or have it be at the top level.</li>
</ul>
<p><strong>Caution:</strong> Customers will need to <strong>replace all beta External API activities</strong> with GA External API activities in their workflows.  Workflows that use the beta version of External API will stop working in 20.3.</p>
<p>For more information, refer to the <a href="../../automating/using/external-api.md">detailed documentation</a> and the <a href="https://experienceleague.adobe.com/docs/campaign-learn/campaign-standard-tutorials/managing-processes-and-data/data-management-activities/external-api-activity.html">how-to video</a>.</p>
</td> 
</tr> 
</tbody> 
</table>

**Additional capabilities** (starting July 13)
 
* **AI-Powered send time optimization and profile scoring** - You can now you can optimize the design and delivery of customer journeys to predict each individual's engagement preference. Powered by Journey AI, Adobe Campaign can analyze and predict open rates, optimal send times, and probable churn based on historical engagement metrics. [Learn more](../../sending/using/predictive.md)
* **Brazil’s new privacy regulation** - In addition to the privacy capabilities already available in Campaign, Adobe helps facilitate your readiness for Brazil’s Lei Geral de Proteçao de Datos (LGPD). When creating a Privacy request, the LGPD regulation has been added to Adobe Privacy Core Service. [Learn more](https://helpx.adobe.com/campaign/kb/campaign-privacy-overview.html)

**Improvements**

* The number of characters that can be used in the **Prefix** field to [test messages using targeted profiles](../../sending/using/testing-messages-using-target.md) has been increased from 32 to 500 characters. 
* The maximum number of real-time events that can be published on an instance has been increased from 350 to 2000. (CAMP-41608)
* The synchronization between Adobe Launch and Campaign Standard has been improved by using the syncWithLaunch technical workflow. This workflow enables automatic importing of all Adobe Launch mobile properties into Adobe Campaign Standard. For more information, refer to [this page](../../administration/using/technical-workflows.md).
  
  You will need to submit a ticket to Adobe Customer Care (either directly or through your Adobe contact) to have the syncWithLaunch technical workflow enabled in your Campaign instance. (CAMP-40082)

**Email Designer enhancements**

* The Email Designer can now handle a more flexible HTML formatting than strict W3C. (CAMP-42529)
* Fixed an issue with [clickable images](../../designing/using/links.md#inserting-a-link) to prevent links from being displayed next to the image in content blocks. (CAMP-41586)
* Fixed an issue preventing the redirection to a landing page when the [tracked URL](../../designing/using/links.md#about-tracked-urls) had a category added in the template. (CAMP-41537)
* Fixed an issue with buttons padding in Outlook.
* Fixed an issue causing HTML tags to appear in plain text.
* Content block search now displays server search results as well as preloaded results. (CAMP-41870)

**Other changes**

* The custom resource publication interface has been improved with clearer error messages.
* Unused delivery mappings have been removed from the interface.
* Unnecessary administrator roles have been removed from the interface.
* Checkboxes can now be mandatory in a landing page.
* When downloading the CSV file of a Dynamic report, the limit of 200 rows has been removed. You can now include every row of your report. (CAMP-40810)
* Added ES-US language in the list of out-of-the-box languages for multilingual emails. (CAMP-42279)
* Files downloaded with a Transfer File activity will now be deleted after X days, where X is determined by the **History in days** field under the **Execution** menu in the Workflow properties. [Read more](../../automating/using/managing-execution-options.md)

**Experience Platform integrations**

* Activation of Adobe [Experience Platform Audiences](../../integrating/using/aep-targeting-audiences.md) from the **Read audience** activity has been improved to provide better performance and stability. Moreover, workflow logs have been made clearer and more detailed regarding activation jobs, allowing easier monitoring and troubleshooting when reading Adobe Experience Platform audiences.

**Patches**

* Fixed an error which led to a ghost resource being created during the publication job of a custom resource.
* Fixed an issue that could prevent profiles' Marketing History from displaying if the Profile resource was extended with a custom resource. (CAMP-41009)
* Fixed an issue with out-of-the-box landing page templates which displayed their content in French when opening the editor. (CAMP-41639)
* Fixed an issue in push notifications with dynamic content that could prevent emojis from being displayed. (CAMP-40715)
* Fixed an issue in the **Deduplication** activity which could led to an incorrect segment code being assigned to one of the outbound complement transitions. (CAMP-41400)
* Fixed an error which prevented scheduled reports from being deleted. (CAMP-41302)
* Fixed an issue which caused discrepancy between the delivery dashboard and the **Delivery Summary** report. (CAMP-41145)
* Fixed an issue which led to a character overlap display issue in downloaded reports.
* Fixed an issue which prevented the preview of a delivery from working for proof substitution.
* Fixed an error when deleting custom fields of an In-App local notification.
* Fixed an issue which prevented the charIndex function from working with an **End** or **File transfer** activity in a workflow.
* Fixed an issue in workflows that could occur when using an **Enrichment** activity with two input activities including target resources having a link between them. (CAMP-42133)
* Fixed an issue that could prevent a workflow from running when using unknown functions. (CAMP-41873)
* Fixed an issue in workflows that could occur when creating audiences using several **Save audience** activities with complement outbound transitions. (CAMP-39992)
* Fixed an issue which caused data discrepancy when using personalization in transactional emails. (CAMP-41842)
* Fixed issues which occurred when deleting custom fields in push notification deliveries. (CAMP-37586)
* Fixed an error which prevented users from making changes to reports. (CAMP-42505)


![](assets/do-not-localize/cp-icon.png) **New Control Panel May release** with Certificate renewal for CNAME subdomains. [Learn more](https://experienceleague.adobe.com/docs/control-panel/using/release-notes.html).

## Release 20.2 - April 2020 {#release-20-2---april-2020}

**What's new?**

<table> 
 <thead> 
  <tr> 
   <th> <strong>Azure Blob Integration</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>The Azure Blob storage connector can now be used to import or export data to Adobe Campaign using a <strong>Transfer file</strong> workflow activity. </p>
    <p>For more information, refer to the <a href="../../administration/using/external-accounts.md#microsoft-azure-external-account">detailed documentation</a>.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

<table> 
 <thead> 
  <tr> 
   <th> <strong>Email testing using targeted profiles</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>In addition to test profiles, you can now test your emails on real targeted profiles. This allows you to get an exact representation of the message that the profile will receive: custom fields, dynamic and personalized information, including additional data from workflows, etc. </p>
    <p>For more information, refer to the <a href="../../sending/using/testing-messages-using-target.md">detailed documentation</a> and the <a href="https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/communication-channels/email/profile-substitution.html">tutorial video</a>. </p>
   </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>New capabilities will be released in Campaign Control Panel in April, including Google TXT record management, Database space monitoring and email alerting. For more on these features, refer to the [Control Panel Release Note](https://experienceleague.adobe.com/docs/control-panel/using/release-notes.html).

**Improvements**

* Transactional messaging user experience has been enhanced and the interface consistency was improved. [Read more](../../channels/using/getting-started-with-transactional-msg.md)
* Campaign Standard now allows you to send proofs to Test profiles using additional data from workflows.
* Guardrails for the External API activity have been updated. [Read more](../../automating/using/external-api.md)

**Email Designer enhancements**

* Fixed an issue affecting escaping when clicking multiple times on a personalized image. 
* Fixed an issue when duplicating dynamic text components which could lead to the wong line being duplicated. (CAMP-41249)
* Fixed an issue with padding in Outlook when defining padding at table level instead of div level. 
* Fixed an issue that caused the width of an image to be modified when switching to HTML mode. (CAMP-41116)
* Fixed an issue preventing the social media component from being accessible when providing alternative text to the icons. (CAMP-41345)
* Fixed an issue causing visible `<br>` tags to be displayed when using copy paste in the Email Designer.
* Fixed an issue causing HTML tags to be displayed in the email after switching from HTML content to Plain Text. (CAMP-41138)
* Fixed an issue preventing the rendering of buttons with only one border defined. 
* Fixed an issue in HTML indentation which caused the footer of emails to move leftwards in Microsoft Outlook. (CAMP-40987)
* Fixed an issue causing personalization fields targeting a collection attribute defined in HTML to be copied in the plain text content when switching to plain text mode. (CAMP-40365)
* Fixed an issue preventing links from being inserted on a text segment that is selected. (CAMP-41406)
* Fixed an issue that caused the date to be altered when selecting a timezone in the query editor. (CAMP-38277)

**Other changes**

* The **KPIs Reconciliation with Adobe Analytics** out-of-the-box workflow now runs until current date instead of running for a single day.
* The MCPNS doesn't support adding APNS and APNS-SANDBOX both as platforms in an app. After successfully adding the certificate in Adobe Campaign Standard, you are now no longer able to change your settings back since only one APNS platform (production or sandbox) can be added to the MCPNS app.

**Experience Platform integrations**

>[!NOTE]
>
>Adobe Experience Platform features in Campaign Standard are currently in beta, which may be subject to frequent updates without notice. Refer to the detailed documentation: [Experience Platform Data Connector](../../integrating/using/aep-about-data-connector.md), [Audience Destinations](../../integrating/using/aep-about-audience-destinations-service.md)

* In workflow logs, every 10 minutes, Campaign now displays the number of records already processed by the job that is currently running.
* Fixed an issue that could occur when importing an Adobe Experience Platform profile that had been deleted from the database.
* Fixed an issue in workflow logs, that could display an incorrect result for the total number of imported records.

**Patches**

* Fixed an issue with the **Enrichment** workflow activity that could occur when adding spaces in the **Alias** field which then created a new row item. (CAMP-39229)
* Fixed an issue where every test profile could be targeted when sending a proof message.
* Fixed an issue that occurred after unpublishing and deleting an event configuration. [Read more](../../channels/using/publishing-transactional-event.md#deleting-an-event)
* Fixed an issue where the **Save** button disappeared when making changes to workflows.
* Fixed an issue when deleting a privacy request manually in Campaign after it had been processed, which prevented data associated to the request from being deleted even after cleanup.
* Fixed an issue that could occur when previewing or sending messages that included special characters from Adobe Experience Manager.
* Fixed an issue that could occur in workflows when executing an activity with several inbound transitions.
* Fixed an issue which prevented standard users from using the 'Subscriptions to an application' as the target dimension in a workflow query or a delivery. (CAMP-37618)

## Release 20.1.4 - February 2020 {#release-20-1-4---february-2020}

* Fixed an issue when opening a **Read Audience** actvity on existing workflows. (CAMP-41002) 

## Release 20.1.3 - February 2020 {#release-20-1-3---february-2020}

* Fixed a regression issue introduced in 20.1 by CAMP-39273 for customers using the loophole. CAMP-39273 was reverted. 

## Release 20.1.2 - February 2020 {#release-20-1-2---february-2020}

**Email Designer enhancements**

* Fixed an issue which added an HTML tag element in an outdated fragment when patching it and then saving the content. (CAMP-40685)
* Fixed an issue which added a space when using dynamic content. (CAMP-40605)
* Fixed an issue when configuring a transactional email template. (CAMP-40604)

## Release 20.1 - February 2020 {#release-20-1---february-2020}

**What's new?**


<table> 
 <thead> 
  <tr> 
   <th> <strong>Adobe Experience Platform Data Connector (beta)</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>The Adobe Experience Platform Data Connector is now integrated with Adobe Campaign Standard. You can make your Campaign data available on Adobe Experience Platform by mapping XTK data (data ingested in Campaign) to Adobe Experience Platform Data Model (XDM). </p>
    <p>Please note this capability is only available to customers hosted on Azure. For more information about this capability and conditions to activate it, refer to the <a href="../../integrating/using/aep-about-data-connector.md">detailed documentation</a> and the <a href="https://experienceleague.adobe.com/docs/campaign-learn/campaign-standard-tutorials/administrating/adobe-experience-platform-data-connector/understanding-the-adobe-experience-platform-data-connector.html">how-to video</a>.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

<table> 
 <thead> 
  <tr> 
   <th> <strong>Audience Destinations (beta) </strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>Audience Destinations allows you to share segments from Adobe Experience Platform to Adobe Campaign.</p>
    <p>Please note this capability is only available to customers hosted on Azure. For more information about this capability and conditions to activate it, refer to the <a href="../../integrating/using/aep-about-audience-destinations-service.md">detailed documentation</a> and the <a href="https://experienceleague.adobe.com/docs/campaign-learn/campaign-standard-tutorials/profiles-and-audiences/audience-destinations/audience-destinations-overview.html">how-to video</a>. </p>
   </td> 
  </tr> 
 </tbody> 
</table>

**Improvements**

* Global availability of the enhanced MTA: messages (including transactional messages) are now sent by the Adobe Campaign Enhanced MTA, which provides an upgraded sending infrastructure allowing for improved deliverability, throughput, and bounce handling. [Read more](https://helpx.adobe.com/campaign/kb/campaign-enhanced-mta.html)

* Timezone management has been enhanced. You can now define a [specific timezone](../../automating/using/building-a-workflow.md) for an entire workflow. The selected timezone will apply to all the workflow's activities. Information about the timezone that has been configured for the operator or the server is now displayed in the interface (in logs, and after selecting a timezone). (CAMP-37672)

* Campaign Standard APIs now allow you to perform pagination when using large tables, by adding the `_forcePagination=true` parameter to your call URL. [Read more](../../api/using/pagination.md)

* The Delivery log ID (which is a unique identifier for each log) is now available in the Delivery logs and Tracking logs resources for all targeting dimensions. This enables to identify sending or tracking logs when exporting, for example. [Read more](../../automating/using/exporting-logs.md)

**Email Designer enhancements**

* Added missing mandatory text instructions when creating an Audience.
* Fixed an issue when clicking on the **Change content** button in the wizard of the legacy email editor.
* Fixed an issue which prevented headers from being aligned with the content on the Service Summary report. (CAMP-38103)
* Fixed an issue which prevented dynamic content variants from being deleted without affecting the rest of the subject line. (CAMP-40096)
* Fixed an A/B testing issue when using the B variant on the subject line. (CAMP-40327)
* Fixed an issue which prevented you from dragging and dropping files when using the Upload HTML import feature. (CAMP-39326)
* Fixed an issue which prevented you from copying and pasting text from a text editor. (CAMP-39028)
* Fixed an issue which prevented the word suggestions from being displayed. (CAMP-38970)
* Fixed an issue which prevented users from saving fragments. (ATU-2447)
* Fixed an issue preventing dynamic structures from being duplicated. (CAMP-38367)
* Fixed an issue preventing dynamic content to retain conditions when duplicated. (CAMP-39051)

**Other changes**

* The "Deliveries with preparation failed" filter now takes into account the deliveries' creation date rather than the last modification date.
* The Organizational unit of the Administrators security group can no longer be changed.
* When creating a profile, the Organizational unit field must now be filled.
* An Experience Cloud Trigger can now only be deleted if both the event and the transactional template that are linked to it are deleted.
* [!DNL Adobe Creative SDK] has been decommissioned. It is now deprecated in Campaign Standard. See the [Deprecated and removed features](../../rn/using/deprecated-features.md) page.


**Patches**

* Fixed an issue when performing a delete privacy request which prevented user data from being deleted in exclusion logs. (CAMP-39003)
* Fixed an issue which led to accessibility problems when resizing text in a container element.
* Fixed an issue which prevented users from dismissing the Calendar pop-up that appears on hover in marketing activities.
* Fixed an issue in the **[!UICONTROL External API]** activity which displayed the **[!UICONTROL Confirm]** button even when no data was modified.
* Fixed an issue when using a **[!UICONTROL Union]** activity on queries with different target dimensions. The transition data only showed records from the main set's targeting dimension. (CAMP-36831)
* Fixed an issue that could lead to an error when using a **[!UICONTROL Reconciliation]** activity in specific contexts, for example with two inbound activities, one of them being an exclusion activity. (CAMP-37490)
* Fixed performance issues that could occur when selecting and updating test profiles. (CAMP-37976)
* Fixed an issue that could display error pages when subscribing or unsubscribing via landing pages. (CAMP-37771) 
* Fixed an issue that occurred when uploading content in zip format, with PNG files referenced in the HTML with their extension in capital letters. (CAMP-37913)
* Fixed an issue that prevented In-App messages from being sent when adding a test profile to the delivery.
* Fixed an error with the External API workflow activity which failed when linked to enrichment activities.
* Fixed an issue which could cause the status of SMS messages to be displayed incorrectly.
* Fixed an issue with custom resources which caused duplicate entries to appear under different API endpoints.
* Fixed an issue which prevented landing pages from being available after publishing. (CAMP-38695)
* Fixed a bug which occurred when displaying data from an Intersection transition coming from two different resources. (CAMP-38974)
* Fixed an issue which caused the enumeration value in a delivery template to be set incorrectly. (CAMP-38388)
* Fixed an error with email bulk deliveries which displayed the deliveries' state as Pending and the Sent status as Finished. (CAMP-35355)
* Fixed an error which displayed the sender domain incorrectly in Dynamic reporting. (CAMP-33123)
* Fixed an issue which caused discrepancy in Unsubscription counts in Dynamic reporting. (CAMP-39949)
* Fixed an issue which prevented addresses from being displayed in the Sending logs screen when sending In-App messages.
* Fixed an issue which prevented SMS sending logs from being updated with the correct number of bounces. (CAMP-38395)
* Fixed a loophole which allowed the application subscription post calls to update the push notification tokens. (CAMP-39273)
