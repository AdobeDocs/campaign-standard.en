---
title: Release Notes
seo-title: Release Notes
description: Release Notes
seo-description: This page lists all recent releases of Adobe Campaign Standard.
page-status-flag: never-activated
uuid: 1cf2e40c-beca-43db-8261-a1820ee86ad3
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: rn
content-type: reference
topic-tags: campaign-standard-releases
discoiquuid: 5c7bfb74-4002-4ffe-87e8-bddb41d34b41

internal: n
snippet: y
---

# Release Notes{#release-notes}

Looking for a specific release of Adobe Campaign Standard?

Each release comes with new features and patches. Click on a release to view its content. Consult the [Release Planning](https://helpx.adobe.com/campaign/kb/acs-release-planning.html) to find out when the next release will happen.

View the latest [documentation updates](../../rn/using/documentation-updates.md) for Adobe Campaign Standard. If you're looking for a previous release, consult these pages: [2018 Release Notes](../../rn/using/release-notes-2018.md), [2017 Release Notes](../../rn/using/release-notes-2017.md), [2015-2016 Release Notes](../../rn/using/release-notes-2015-2016.md). Also consult the list of [Deprecated and Removed Features](https://helpx.adobe.com/campaign/kb/acs-deprecated-and-removed-features.html).

## Release 19.3 - July 2019 {#release-19-3---july-2019}

### What's new? {#what-s-new-3}

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Microsoft Dynamics 365 connector<br /> </td> 
   <td> <p>Activate your CRM data on cross-channel communication. Pass on contacts from Microsoft Dynamics 365 to Adobe Campaign, and share campaign performance data (sends, opens, clicks, and bounces) back from Adobe Campaign to Microsoft Dynamics 365.</p><p>For more information, refer to the <a href="https://helpx.adobe.com/campaign/kb/acs-ms-dynamics.html">detailed documentation</a> and the <a href="https://helpx.adobe.com/campaign/kt/acs/using/acs-ms-dynamics-crm-connector-tutorial.html">how-to video</a>.</p></td> 
  </tr> 
  <tr> 
   <td> External API (Public Beta)<br /> </td> 
   <td> <p>We’ve added a new activity to extend the workflow capabilities and give users the ability to communicate with external systems that offer web APIs. The External API activity allows you to bring data into a workflow from an external system via a REST API call. The REST endpoints can be a Customer management system, an Adobe I/O Runtime or an Experience Cloud REST endpoint (Data Platform, Target, Analytics, Campaign, etc). This data will then be used for segmentation and personalization.</p><p>This capability is a public beta feature. </p><p>For more information, refer to the <a href="../../automating/using/externalAPI.md">detailed documentation</a>.</p></td> 
  </tr> 
  <tr> 
   <td> Report on workflow segment<br /> </td> 
   <td> <p>This feature allows marketers to breakdown their delivery performance by segment code. When you create a workflow then use a segmentation activity to assign segments to the delivery population, these segments now go into the same delivery. This allows you to display the opens/clicks statistics based on segments in a single delivery. </p><p>For more information, refer to the <a href="../../reporting/using/creating-a-report-workflow-segment.md">detailed documentation</a>.</p></td> 
  </tr> 
  <tr> 
   <td> New Location Service integration with Campaign<br /> </td> 
   <td> <p>Through the integration with Adobe Analytics for Mobile, you can now use Adobe Campaign to send location-based marketing messages to your mobile application's subscribers via the Experience Platform SDK. For more information, refer to the <a href="../../integrating/using/configuring-campaign-points-of-interest-data-integration.md">detailed documentation</a>.</p></td> 
  </tr> 
 </tbody> 
</table>

### Security enhancements {#security-enhancements-2}

### Email Designer enhancements {#email-designer-enhancements}

* XX

### Other improvements {#other-improvements-3}

* The reporting feature has been improved for a better experience. To use this feature, you need to accept the Dynamic Reporting Usage Agreement.
* In workflows, a new option has been added to preview the next ten executions of a workflow. For more on this, refer to the [detailed documentation](../../automating/using/scheduler.md).
* In the Scheduler activity, a new option allows you to select a specific day of a specific week for monthly deliveries. For more on this, refer to the [detailed documentation](../../automating/using/scheduler.md).
* When creating recurring deliveries with no aggregation period, the delivery dashboard now allows you to request confirmation before the delivery is sent. For more on this, refer to the [detailed documentation](../../sending/using/confirming-the-send.md).
* You can now personalize a delivery’s label with events variables that have been declared into the workflow’s external signal activity. For more on this, refer to the [detailed documentation](../../automating/using/calling-a-workflow-with-external-parameters.md).
* A warning has been added in custom resource configuration screens. We recommend using 30 characters maximum for custom resource IDs. This also applies to custom resource fields, keys, indexes and links.
* Fixed an issue which could lead to an erroneous publication error message after login.
* The GDPR delete query has been improved for better performance. (CAMP-33504)

### Other changes {#other-changes-2}

* XX

### Patches {#patches-3}

* Fixed an issue which could cause GDPR Access requests to fail.
* Fixed an issue which could lead to triggers being discarded when multiple triggers were received for a unique profile.
* Fixed a configuration issue with the Campaign and Assets Core Service integration which could prevent you from selecting a shared asset in an email.

## Release 19.2.7 - July 2019 {#release-19-2-7---july-2019}

### Improvements {#improvements-2}

* The GDPR delete query has been improved for better performance.
* Fixed an issue which could cause web crashes after the 19.2 upgrade. (CAMP-34862)
* Fixed an issue which could prevent non-administrator users from saving or scheduling reports. (CAMP-31133)
* Fixed an issue when using "|" as the date separator in the Load file workflow activity. (CAMP-34706)

## Release 19.2.4 - June 2019 {#release-19-2-4---june-2019}

### Email Designer {#email-designer-2}

* Fixed an issue which prevented users from editing fragments when empty style tags were used in the HTML. This is a follow-up fix for CAMP-33778 in 19.2.3.

## Release 19.2.3 - June 2019 {#release-19-2-3---june-2019}

### Email Designer {#email-designer-1}

Introduced a series of improvements and fixes to optimize fragments in the 19.2 release. Newly created fragments will work seamlessly. Fragments that were previously built have been grayed-out and need to be migrated to the new format. To do so, click on each fragment and validate its migration to the new format. We recommend that you test a few fragments before migrating them all.

* Fixed an issue which prevented users from editing a fragment after unlocking it. This was affecting existing fragments when updating to 19.2. (CAMP-33778)
* Fixed an issue when using dynamic content. Extra spaces were added in the HTML.

### Other improvements {#other-improvements-2}

* Fixed an issue which could prevent SMS sending from resuming after a disconnection of the SMS connector.
* Fixed an issue which could close SMPP connections when TLS was enabled.
* Fixed an issue which could close SMPP connections when TLS was enabled.
* The “Launch_URL_Campaign” option has been added in Campaign to manage properties of mobile applications created with Adobe Experience Platform Mobile SDK.
* Fixed an error that led to the Sandbox environment option being unchecked after uploading the certificate of a newly created mobile property and exiting the mobile application property page.
* Fixed an issue which prevented you from enriching a transactional message content with information from the Service resource. (CAMP-33707)
* Fixed an issue in Blacklist landing pages that occurred when trying to unsubscribe profiles from a service.

## Release 19.2 - May 2019 {#release-19-2---may-2019}

### What's new? {#what-s-new-}

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
   <td> <p>To help increase efficiency in your work as an Admin user, you can easily monitor capacity and manage settings of your instances (starting with SFTP servers management).</p><p>For more information, refer to the <a href="https://helpx.adobe.com/campaign/kb/control-panel.html">detailed documentation</a> and the <a href="https://helpx.adobe.com/campaign/kt/acs/using/acs-control-panel-video-use.html">how-to video</a>.</p></td> 
  </tr> 
  <tr> 
   <td> Local notifications<br /> </td> 
   <td> <p>Local notification messaging allows you to inform your users when new data becomes available within their mobile applications, even without having access to the Internet or the mobile application running in the foreground. Local notifications are triggered by a mobile application on a particular time and depending on an event.</p><p>For more information, refer to the <a href="../../channels/using/customizing-an-in-app-message.md#customizing-a-local-notification-message-type">detailed documentation</a>.</p></td> 
  </tr> 
  <tr> 
   <td> Workflow enhancement - Add a payload to external signal activity<br /> </td> 
   <td> <p>Start a workflow with a payload when defined conditions are successfully met from another workflow or a REST API call to integrate with your external systems. This also includes a new <strong>test</strong> activity where you can run tests on this functionality.</p><p>For more information, refer to the <a href="../../automating/using/calling-a-workflow-with-external-parameters.md">detailed documentation</a> and the <a href="https://helpx.adobe.com/campaign/kt/acs/using/acs-external-signal-activity-feature-video-use.html">how-to video</a>.</p></td> 
  </tr> 
  <tr> 
   <td> Landing Pages enhancement - Google reCAPTCHA<br /> </td> 
   <td> <p>Leverage Google reCAPTCHA to prevent spam on your landing pages without requiring any action from your customers.</p><p>For more information, refer to the <a href="../../channels/using/designing-a-landing-page.md#setting-google-recaptcha">detailed documentation</a>.</p></td> 
  </tr> 
 </tbody> 
</table>

### Security enhancements {#security-enhancements}

* Fixed a potential clickjacking security issue in reporting workspace.

### Email Designer enhancements {#email-designer-enhancements}

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

### Transactional Messaging enhancements {#transactional-messaging-enhancements}

Several improvements have been added to the Transactional messaging channel in order to optimize operation and performance.

* The transactional message duration has been extended to make sure that all messages are sent before they expire, especially when retries are performed.
* Transactional messaging performance has been increased by distributing the load on different sending threads.
* The transactional messaging process has been optimized to be able to start in parallel multiple analysis of the same message. 
* Fixed an issue that could lead to inconsistent throughput and latency for transactional push notifications.
* Fixed an issue that displayed an incorrect target audience for transactional message execution deliveries.
* Fixed an issue that occurred when importing a package with an event configuration and the associated transactional message. For more on this, refer to the [detailed documentation](../../channels/using/about-transactional-messaging.md#exporting-and-importing-transactional-messages).
* Fixed an issue that deleted the collection data from the test profiles created for a transactional message containing product listings.

### Other changes {#other-changes}

* A new option has been added to the SMS external account. It enables to limit the maximum number of MTA processes that send SMS in order to better control the number of parallel connections. For more information, refer to the [SMS connector protocol and settings](https://helpx.adobe.com/campaign/kb/sms-connector-protocol-and-settings.html) technote.
* When publishing a resource with API extension, if the API has already been published, it is now automatically updated each time it is published again. Previously this action was manual and failing to update the API could break the profile or service resource of this API. For more on this, refer to the [detailed documentation](../../developing/using/updating-the-database-structure.md#publishing-a-resource-with-api-extension).
* Zip code dimension has been removed from Dynamic Reporting. We recommend using City, Country, State dimensions instead.
* The ‘First Launch’ Lifecycle event trigger for In-App messages has been removed.
* When exporting a package with security groups, it now contains the roles that are assigned to each group. (CAMP-32960)
* In the Load file activity, a new option lets you check that the columns of the file you are uploading match the column definition. For more information, refer to the [detailed documentation](../../automating/using/load-file.md). (CAMP-32229) 
* Workflows can now be started with a payload, allowing you to use and share external parameters between activities within the workflow. For more information, refer to the [detailed documentation](../../automating/using/calling-a-workflow-with-external-parameters.md). (CAMP-29412 & CAMP-29413)
* Campaign Standard APIs now let you update profiles' geographical and organizational units using a payload. For more information, refer to the [detailed documentation](https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html).
* Error messages when an object from the database is not accessible have been made clearer to understand.
* In the Extract file activity, Javascript capabilities have been updated when defining the name of a file to export. Only the formatDate function is now available for use in the Output field. For more information, refer to the [detailed documentation](../../automating/using/extract-file.md).
* Auto sequence ID generation has been improved for custom resources. Primary keys for new custom resources are now in 64 bits by default.
* The custom resource publication test mode has been improved. A warning message is now displayed to users if the last custom resource publication failed and is not fixed. After a custom resource publication failure, you can rollback to last working version. For more information, refer to the [detailed documentation](../../developing/using/updating-the-database-structure.md#publishing-a-custom-resource).
* A new option was added in the Transfer file activity. It allows you to sort the files when using the File download action, in SFTP mode. For more information, refer to the [detailed documentation](../../automating/using/transfer-file.md). (CAMP-33109)

### Patches {#patches}

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

### Email Designer enhancements {#email-designer-enhancements-1}

* Fixed an issue which prevented a template from being modified after saving it.
* Fixed various issues when using a previously created template in an email.
* Fixed an issue which prevented components from being hidden in imported templates.

### Other improvements {#other-improvements}

* Fixed an error when viewing typology rules. (CAMP-32059 & CAMP-31849)
* Fixed an issue which prevented typology rules from being edited. (CAMP-31750)
* Fixed an issue with the inMail process which could stop unexpectedly. (CAMP-31238)

## Release 19.1 - February 2019 {#release-19-1---february-2019}

### What's new? {#what-s-new--1}

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
   <td> <p>This release contains the integration of Adobe Campaign with the GA versions of Android and iOS extensions for Adobe Campaign Standard in Adobe Experience Platform Launch and Mobile SDKs. These extensions support push messaging, in-app messaging, and mobile app profile updates.</p><p> For more information, refer to the <a href="../../administration/using/about-typology-rules.md#typology-rules">detailed documentation</a>.</p> </td> 
  </tr> 
  <tr> 
   <td> Mobile In-App Messaging<br /> </td> 
   <td> <p>This release contains the GA version of In-App channel in Campaign. From a functional standpoint, the most notable additions to the Beta release are Dynamic reports for In-App channel and secure handshake between Mobile SDK and MCIAS (Marketing Cloud In-App Messaging Service that serves the In-App rules to the SDK). Secure handshake ensures that your users' PII data does not fall into malicious hands as well as enables you to maintain users' privacy on a shared device by clearing out message cache every time the user logs out.</p><p>For more information, refer to the <a href="../../channels/using/about-in-app-messaging.md">detailed documentation</a> and the dedicated <a href="https://helpx.adobe.com/campaign/kt/acs/using/acs-in-app-message-tutorial.html">In-App tutorial</a>.</p> </td> 
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

### Security enhancements {#security-enhancements-1}

* The generated landing page HTML code has been updated to prevent search engine indexing.

### Email Designer enhancements {#email-designer-enhancements-2}

* A set of four best-in-class responsive email templates designed by Behance artists is now available.

  For more information, refer to the [detailed documentation](../../start/using/about-templates.md#content-templates).

* Our new on-boarding experience will help you start email creation faster and give you easier access to documentation and tutorials.

  For more information, refer to the [detailed documentation](../../designing/using/about-email-content-design.md#email-designer-home-page).

* You now have the flexibility to configure the number of columns and width based on your needs.

  For more information, refer to the [detailed documentation](../../designing/using/defining-the-email-structure.md#editing-the-email-structure).

* When editing in mobile view, you can hide certain components just in mobile display for effective usage of space.

  For more information, refer to the [detailed documentation](../../designing/using/about-email-content-design.md#switching-to-mobile-view).

* You can now add custom social channels to your email template on top of the ones that are already available.
* Fixed an issue that prevented to scroll down the structure menu when using more than 18 structures. (CAMP-31173)
* Fixed an issue that displayed the preheader on top of the content when forwarding an email containing a preheader sent with Adobe Campaign. (CAMP-30736)
* Fixed an issue that prevented the subject line from being updated when clicking the **Refresh AEM content** option after modifying the subject in Adobe Experience Manager. (CAMP-29984)
* Fixed several issues that prevented the use of dynamic images from Adobe Target.
* Fixed an issue that prevented the preview from being updated when retrieving content at preparation time if the content had been previously imported from a URL.
* The YouTube icon has been added to the **Social** content component.
* The **List** view has been added for content components and fragments displayed in the Email Designer palette.

### Other improvements {#other-improvements-1}

* Adobe Campaign is now fully FCM compliant for both SDK V4 and AEP SDK Apps.
* Adobe Campaign supports Push notifications on Wear OS by Android as well as watchOS by Apple.
* Warning and error messages that may display when navigating in the interface have been made clearer and easier to understand. 
* You can now add to the profiles list columns related to opt-in and opt-out ("No longer contact …" fields).
* The Time zone drop-down list in the Profile creation screen has been moved from the Address section to the upper-section of the interface. 
* You can now add separators when configuring custom resource screens, allowing you to organize your fields into categories.

  For more information, refer to the [detailed documentation](../../developing/using/configuring-the-screen-definition.md#defining-the-detail-screen-configuration).

### Other changes {#other-changes-1}

* Adobe Campaign and Adobe Experience Cloud will drop support for Microsoft Internet Explorer 11 starting Spring 2019, and Campaign Standard 19.2 release. Please switch to Microsoft Edge or another supported browser. See [Deprecated and removed features](https://helpx.adobe.com/campaign/kb/acs-deprecated-and-removed-features.html) page.
* The **Country code** field from the Profile resource has been renamed to **Country/Region code**.

### Patches {#patches-1}

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

### What's new? {#what-s-new--2}

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
     <li> The ability to <a href="../../designing/using/importing-content-from-a-url.md#retrieving-content-from-a-url-automatically-at-preparation-time">retrieve content from a URL automatically at preparation time</a> </li> 
     <li> Fully compliant <a href="../../start/using/about-templates.md#content-templates">out-of-the box content templates</a>. </li> 
    </ul> 
    <p>For more information, refer to the <a href="../../designing/using/about-email-content-design.md">detailed documentation</a> and the <a href="https://helpx.adobe.com/campaign/kt/acs/using/acs-email-designer-tutorial.html">how-to video</a>. Improvements and fixes are listed below.</p><p>As a consequence, the legacy email content editor is now deprecated. For more information, refer to this <a href="https://helpx.adobe.com/campaign/kb/acs-deprecated-and-removed-features.html">page</a>.</p> </td> 
  </tr> 
  <tr> 
   <td> Product Listings in Transactional Emails<br /> </td> 
   <td> <p>You can now reference one or more product collections in a transactional email message. For example, you can automatically send a cart abandonment email listing all the products that were in the user’s cart with an image, price, and link to each product.</p><p>For more information, refer to the <a href="../../channels/using/event-transactional-messages.md#using-product-listings-in-a-transactional-message">detailed documentation</a> and the <a href="https://helpx.adobe.com/campaign/kt/acs/using/acs-product-listings-in-transactional-emails-feature-video-setup.html">how-to video</a>.</p> </td> 
  </tr> 
  <tr> 
   <td> Mobile View in the Email Designer<br /> </td> 
   <td> <p>You can now switch to a dedicated mobile view when editing email content. This allows you to fine-tune the responsive design of an email by separately editing all style options for mobile display, such as adapting margins, smaller font size, different background color, and so on.</p><p> For more information, refer to the <a href="../../designing/using/about-email-content-design.md#switching-to-mobile-view">detailed documentation</a>.</p> </td> 
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

### Improvements {#improvements}

* A new option in the Load data activity now lets you apply a post-processing stage to the file containing the rejected records (ex. Zip format compression). (CAMP-24521)
* A new option in the Update data activity now allows you to configure the maximum batch size for the data to upload. (CAMP-28400)
* Improved profiles' address state selection. When selecting a country, the "State" drop-down list is now automatically updated with relevant states values. (CAMP-28874)
* A new option in the Extract file activity now prevents from generating a file if the inbound transition is empty. This avoids creating and uploading empty files on SFTP servers.
* The Delivery summary report has been improved. 
* The list of available countries when defining a profile's address has been enriched. (CAMP-26707)
* An error message is now displayed when trying to import a built-in workflow.

### Email Designer {#email-designer}

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

### Patches {#patches-2}

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
* Fixed an issue that prevented blacklisted SMS numbers from being excluded in an SMS message. (CAMP-28898)
* Fixed an issue which could prevent SMPP providers from being notified in case of an error while processing incoming messages. (CAMP-29804)
* Fixed an issue which allowed external accounts with associated deliveries to be deleted. (CAMP-29738)
* The sending throughput has been improved and stabilized for SMS messages.
* Fixed an issue which prevented the "~" character from being used in an SMS message. (CAMP-29172)
* Fixed an issue in deliveries with the Send time optimization option. (CAMP-29231)

