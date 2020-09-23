---
title: Latest Release
description: This page details content of the latest Campaign Standard release
page-status-flag: never-activated
uuid: 1cf2e40c-beca-43db-8261-a1820ee86ad3
contentOwner: vignes
products: SG_CAMPAIGN/STANDARD
audience: rn
content-type: reference
topic-tags: campaign-standard-releases
discoiquuid: 5c7bfb74-4002-4ffe-87e8-bddb41d34b41

internal: n
snippet: y
---

# Latest Release{#latest-release}

[Release Planning](../../rn/using/release-planning.md) &#124; [Control Panel releases](https://docs.adobe.com/content/help/en/control-panel/using/release-notes.html) &#124; [Documentation Updates](../../rn/using/documentation-updates.md) &#124; [Previous Release Notes](../../rn/using/release-notes-2020.md) &#124; [Deprecated Features](../../rn/using/deprecated-features.md)

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
<p>For more information refer to the <a href="../../sending/using/control-group.md">detailed documentation</a> and <a href="https://docs.adobe.com/content/help/en/campaign-standard-learn/tutorials/communication-channels/email/control-groups.html">how-to video</a>.
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
     <li> <strong>Predictive Engagement Scoring</strong>  - Intelligently identifies customers' preferred level of engagement to better target and personalize messages to increase conversions and retention. Watch the <a href="https://docs.adobe.com/content/help/en/campaign-standard-learn/tutorials/communication-channels/email/journey-ai/predictive-engagement-scoring.html">how-to video</a>.</li> 
     <li> <strong>Predictive Send Time Optimization</strong>  - Predicts the best time to send emails to each individual in a campaign to maximize engagement rates and improve email campaign ROI. Watch the <a href="https://docs.adobe.com/content/help/en/campaign-standard-learn/tutorials/communication-channels/email/journey-ai/predictive-send-time-optimization.html">how-to video</a>.</li>
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
* A **new delivery mapping** (mapRtEventAppSubRcp) is now available for transactional push messages targeting profiles. The delivery, exclusion and tracking logs for these deliveries will now be available in the broadLogAppSubRcp, excludeLogAppSubRcp and trackingLogAppSubRcp tables. This solves an issue which caused delivery analysis to fail when sending a transactional push message using the **Profile** target dimension.
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
* New filters have been added to the list of transactional events. They allow you to filter the event configurations according to their status, as well as the last time an event was received.
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

