---
title: Release Notes
seo-title: Release Notes
description: Release Notes
seo-description: This page lists all recent releases of Adobe Campaign Standard.
uuid: c967a05c-56eb-4fa1-8a4e-abbd683508ab
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: rn
content-type: reference
topic-tags: campaign-standard-releases
discoiquuid: bd3d18ea-7ca8-465c-9313-2c382571d1ce
index: y
internal: n
snippet: y
---

# Release Notes{#release-notes}

Release Notes

Looking for a specific release of Adobe Campaign Standard?

Each release comes with new features and patches. Click on a release to view its content.

View the latest [documentation updates](../../rn/using/documentation-updates.md) for Adobe Campaign Standard. If you're looking for a previous release, consult these pages: [2018 Release Notes](../../rn/using/release-notes-2018.md), [2017 Release Notes](../../rn/using/release-notes-2017.md), [2015-2016 Release Notes](../../rn/using/release-notes.md). Also consult the list of [Deprecated and Removed Features](https://helpx.adobe.com/campaign/kb/acs-deprecated-and-removed-features.html).

## Release 19.1 - February 2019 {#release-19-1---february-2019}

### What's new? {#what-s-new-}

<table> 
 <thead>
  <tr>
   <th>Functionality<br /> </th> 
   <th>Description<br /> </th> 
  </tr>
 </thead>
 <tbody>
  <tr>
   <td>Push channel Reporting improvements<br /> </td> 
   <td>Several enhancements have been added to Push channel reporting to allow you to measure user engagement more intuitively. With this release, we are expanding the list of Push channel metrics to three different metrics: Impressions, Clicks, Opens (App Open) to help you measure and analyze users’ interaction with Push notifications more effectively. Along with this, we are also standardizing the definition and implementation of these metrics. The Push notification built-in report has also been improved with commonly used visualizations and metrics.<br /> For more information, refer to the <a href="../../reporting/using/push-notification-report.md">detailed documentation</a>.<br /> </td> 
  </tr>
  <tr>
   <td>Launch integration for Mobile App<br /> </td> 
   <td>This release contains the integration of Adobe Campaign with the GA versions of Android and iOS extensions for Adobe Campaign Standard in Adobe Experience Platform Launch and Mobile SDKs. These extensions support push messaging, in-app messaging, and mobile app profile updates.<br /> For more information, refer to the <a href="../../administration/using/configuring-a-mobile-application.md#main-pars-header-49">detailed documentation</a>.<br /> </td> 
  </tr>
  <tr>
   <td>Mobile In-App Messaging<br /> </td> 
   <td>This release contains the GA version of In-App channel in Campaign. From a functional standpoint, the most notable additions to the Beta release are Dynamic reports for In-App channel and secure handshake between Mobile SDK and MCIAS (Marketing Cloud In-App Messaging Service that serves the In-App rules to the SDK). Secure handshake ensures that your users' PII data does not fall into malicious hands as well as enables you to maintain users' privacy on a shared device by clearing out message cache every time the user logs out.<br /> For more information, refer to the <a href="../../channels/using/about-in-app-messaging.md">detailed documentation</a> and the dedicated <a href="https://helpx.adobe.com/campaign/kt/acs/using/acs-in-app-message-tutorial.html">In-App tutorial</a>.<br /> </td> 
  </tr>
  <tr>
   <td>Workflow enhancements<br /> </td> 
   <td>The following workflow capabilities have been added:<br /> <li>You can now copy-paste activities within a workflow or another workflow from the same Campaign instance. This way, you can easily duplicate an entire workflow or specific activities, and keep the settings that were initially defined. For more information, refer to the <a href="../../automating/using/workflow-interface.md#duplicating-workflow-activities">detailed documentation</a>. (CAMP-20014)</li> <li>When using the <strong>Load file</strong> activity, you can now add a timestamp to the name of the file containing the rejected records. For more information, refer to the <a href="../../automating/using/load-file.md#configuration">detailed documentation</a>.</li> <li><strong>Query</strong> and <strong>Segmentation</strong> activities now let you enable an outbound transition if the activities retrieve no data.</li> </td> 
  </tr>
 </tbody>
</table>

### Security enhancements {#security-enhancements}

* The generated landing page HTML code has been updated to prevent search engine indexing.

### Email Designer enhancements {#email-designer-enhancements}

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

### Other improvements {#other-improvements}

* Adobe Campaign is now fully FCM compliant for both SDK V4 and AEP SDK Apps.
* Adobe Campaign supports Push notifications on Wear OS by Android as well as watchOS by Apple.
* Warning and error messages that may display when navigating in the interface have been made clearer and easier to understand. 
* You can now add to the profiles list columns related to opt-in and opt-out ("No longer contact …" fields).
* The Time zone drop-down list in the Profile creation screen has been moved from the Address section to the upper-section of the interface. 
* You can now add separators when configuring custom resource screens, allowing you to organize your fields into categories.

  For more information, refer to the [detailed documentation](../../developing/using/configuring-the-screen-definition.md#defining-the-detail-screen-configuration).

### Other changes {#other-changes}

* Adobe Campaign and Adobe Experience Cloud will drop support for Microsoft Internet Explorer 11 starting Spring 2019, and Campaign Standard 19.2 release. Please switch to Microsoft Edge or another supported browser. See [Deprecated and removed features](https://helpx.adobe.com/campaign/kb/acs-deprecated-and-removed-features.html) page.
* The **Country code** field from the Profile resource has been renamed to **Country/Region code**.

### Patches {#patches}

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
   <td> Email Designer General Availability<br /> </td> 
   <td> The new intuitive Email Designer (formerly known as Creative Designer) has moved to GA. It now supports all the features from the legacy content editor, including:<br /> <li> The use of <a href="../../integrating/using/adding-target-dynamic-content.md">dynamic images from Adobe Target</a> </li> <li> The ability to <a href="../../designing/using/importing-content-from-a-url.md#retrieving-content-from-a-url-automatically-at-preparation-time">retrieve content from a URL automatically at preparation time</a> </li> <li> Fully compliant <a href="../../start/using/about-templates.md#content-templates">out-of-the box content templates</a>. </li> For more information, refer to the <a href="../../designing/using/about-email-content-design.md">detailed documentation</a>. Improvements and fixes are listed below.<br /> As a consequence, the legacy email content editor is now deprecated. For more information, refer to this <a href="https://helpx.adobe.com/campaign/kb/acs-deprecated-and-removed-features.html">page</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Product Listings in Transactional Emails<br /> </td> 
   <td> You can now reference one or more product collections in a transactional email message. For example, you can automatically send a cart abandonment email listing all the products that were in the user’s cart with an image, price, and link to each product.<br /> For more information, refer to the <a href="../../channels/using/event-transactional-messages.md#using-product-listings-in-a-transactional-message">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Mobile View in the Email Designer<br /> </td> 
   <td> You can now switch to a dedicated mobile view when editing email content. This allows you to fine-tune the responsive design of an email by separately editing all style options for mobile display, such as adapting margins, smaller font size, different background color, and so on.<br /> For more information, refer to the <a href="../../designing/using/about-email-content-design.md#switching-to-mobile-view">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> In-App Messaging Beta Improvements<br /> </td> 
   <td> The In-App Messaging Beta feature has been enhanced with the following capabilities:<br /> <li> In-App Beta channel is GDPR compliant </li> <li> Integration with Analytics APIs to populate Triggers dropdowns </li> <li> Intuitive look and description of delivery templates </li> <li> Enhancements to authoring interface from usability standpoint </li> For more information, refer to the <a href="../../channels/using/about-in-app-messaging.md">detailed documentation</a>.<br /> </td> 
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

### Patches {#patches-1}

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

