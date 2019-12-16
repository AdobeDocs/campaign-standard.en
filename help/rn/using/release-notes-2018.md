---
title: Release Notes 2018
description: This page lists all 2018 releases of Adobe Campaign Standard.
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

# Release Notes 2018{#release-notes}

Looking for a specific 2018 release of Adobe Campaign Standard?

Each release comes with new features and patches. Click on a release to view its content.

View the latest [documentation updates](../../rn/using/documentation-updates.md) for Adobe Campaign Standard. If you're looking for a newer release, consult this [page](../../rn/using/release-notes.md).

## Release 18.9 - September 2018 {#release-18-9---september-2018}

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
   <td> In-App messaging (beta)<br /> </td> 
   <td> In-App messaging allows you to engage Mobile App users more effectively by providing contextual interaction and enabling you to reach users who may have opted out of Push notifications. Use In-app messaging in tandem with Push notifications to create a highly personalized and relevant experience. This leads to better conversion and retention of your App users.<br /> For more information, refer to the <a href="../../channels/using/about-in-app-messaging.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Adobe Launch integration for mobile apps (beta)<br /> </td> 
   <td> Adobe Launch integration with Adobe Campaign now simplifies and automates the process of Mobile App Property activation in Campaign using the Mobile SDK V5.<br /> For more information, refer to the <a href="https://helpx.adobe.com/campaign/kb/configuring-app-sdk.html">detailed documentation</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Improvements {#improvements}

* Adobe Campaign Standard now supports version 4 of Amazon S3 API.

### Other changes {#other-changes}

* In the broadlogs, there is now a distinction between the maximum number of connections and the maximum number of messages per hour. When the limits are reached, it is then possible to know why the throughput is limited. Previously, the same message (‘quota met’) applied to both cases.
* When configuring a mobile application in Campaign, the user can now know if the iOS certificate and Android server key have been successfully uploaded and their expiration date.

  For more on this, refer to the detailed documentation on how to configure a mobile application using [SDK V4](https://helpx.adobe.com/campaign/kb/configuring-app-sdkv4.html ) and [SDK V5](https://helpx.adobe.com/campaign/kb/configuring-app-sdk.html). 

* Target users on a specific Mobile App by selecting a Mobile App while defining the Campaign properties. This feature is for both Push and In-App Messaging channels.

  For more information, refer to the [detailed documentation](../../channels/using/preparing-and-sending-a-push-notification.md#preparing-the-notification).

* When selecting a content block using the Creative Designer interface, all the content blocks from the list are now loaded and displayed. (CAMP-27311)

  For more on this, refer to the [detailed documentation](../../designing/using/personalization.md#adding-a-content-block).

### Patches {#patches}

* Fixed an issue that showed a discrepancy in the log counts between the email dashboard and the email summary report for transactional emails. (CAMP-28237
* Fixed an issue in workflows that could display an error message when importing a file through a File transfer activity. (CAMP-27435)
* Fixed an issue with landing pages containing more that 25 services, that led services to be randomly deselected in the form. (CAMP-26572)
* Fixed an issue in workflows that prevented from configuring external accounts with a SFTP URL when using the File transfer activity. (CAMP-26475)
* Fixed an issue that prevented services summary report from being updated. (CAMP-26301)
* Fixed an issue in workflows when using an Enrichment activity, that prevented a custom field from displaying the correct date. (CAMP-26242)
* Fixed an issue that prevented service subscription dates from being updated when imported through a file import.
* Fixed an error with the load file activity that prevented workflows from importing files (CAMP-27068).
* Fixed an issue that displayed the wrong number of subscriptions in the Service summary reports (CAMP-25587).
* Fixed an issue of data discrepancy between Adobe Analytics and Adobe Campaign reports. (CAMP-25393)
* Fixed an issue which could prevent a limited access user from logging in. (CAMP-27381)
* Fixed an issue which could prevent the list of Adobe Experience Manager contents from being displayed when editing an email using the Creative Designer. (CAMP-27181)
* Fixed an issue that could prevent the Creative Designer from opening, causing an error. (CAMP-27304)
* Fixed an issue that prevented the drag and drop from working correctly in the Creative Designer when using Internet Explorer 11.
* Fixed an issue that caused pictures uploaded from a camera and shot in portrait mode to display in an unwanted rotated position.
* Fixed an issue that displayed unclear selection information when using the query editor interface in the Creative Designer.
* Fixed an issue that prevented from correctly duplicating an element when using the query editor interface in the Creative Designer.
* Fixed an issue that kept delivering SMS messages to blacklisted recipients even though they had been unsubscribed through an automatic reply. (CAMP-27128)
* Fixed an issue that prevented displaying the errors that caused the **Database Cleanup** workflow to fail. (CAMP-26876)
* Fixed an issue which could prevent the deletion of custom fields in a push notification definition. (CAMP-25588)

## Release 18.7 - July 2018 {#release-18-7---july-2018}

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
   <td> High priority flag for Android push notifications<br /> </td> 
   <td> High priority flag for Android - Enable delivering a push notification with high priority for Android apps which causes the sleeping device to wake up and run some limited processing. Note that default priority is Normal which may delay the message delivery to save battery. <br /> For more information, refer to the <a href="../../channels/using/customizing-a-push-notification.md#change-the-notification-behavior-for-android">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Typology filter for mobile app subscribers<br /> </td> 
   <td> Support subscriptions in typology filter - When specifying the filtering criteria for a typology rule, application subscriptions can be selected as the filtering and targeting dimensions, providing the ability to filter on attributes for users with or without a profile. <br /> For more information, refer to the <a href="../../administration/using/about-typology-rules.md#typology-rules">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Automated content import from a URL during message preparation<br /> </td> 
   <td> It is now possible to import email content from a URL during the preparation phase. For recurring email deliveries, the latest HTML content is retrieved each time the message is prepared ensuring the content is always up-to-date at the time the email is sent. This feature also lets you create a scheduled delivery with content from a URL even if the content is not ready yet.<br /> For more information, refer to the <a href="../../designing/using/using-existing-content.md#retrieving-content-from-a-url-automatically-at-preparation-time">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Campaign release notification message<br /> </td> 
   <td> A pop-up message now appears when a user logs in after the instance has been upgraded to a new version. The message indicates the version number and includes a link to the release notes. You can choose to hide the message until the next release. <br /> </td> 
  </tr> 
  <tr> 
   <td> User management<br /> </td> 
   <td> The geographical unit capability is now unavailable for new Campaign Standard instances, as well as existing instances with no geographical units created, starting 18.7 release.<br /> For more information, refer to this <a href="https://helpx.adobe.com/campaign/kb/acs-deprecated-and-removed-features.html">page</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Improvements {#improvements-1}

* The Adobe Campaign and Adobe Target integration now allows you to leverage Target’s [Permissions](https://marketing.adobe.com/resources/help/en_US/target/target/properties-overview.html) feature. When including a dynamic image from Adobe Target in an email, you can now specify a Target Property (at_property code).
* Custom resources that have an owncopy link to the profiles resource are now taken into account by GDPR Privacy access/delete requests. For 1 cardinality simple links and N cardinality collection links, you need to select "Deleting/Duplicating the target record implies deleting/duplicating the records referenced by the link" in the custom resource. For 0 or 1 cardinality simple links, select "Deleting/Duplicating the record implies deleting/duplicating the target record referenced by the link”.

### Other changes {#other-changes-1}

* Report sharing time out has been increased from one to four minutes to avoid any time out error.
* When editing the content of an email, the new Creative Designer opens by default. If you wish, you can still go back to the default content editor at any time after saving your changes. For more on this, refer to the [detailed documentation](../../designing/using/overview.md).
* In the Creative Designer, a new content component can now be added into an email: the carousel. For more on this, refer to the [detailed documentation](../../designing/using/designing-from-scratch.md#about-content-components).
* In a transactional message hot click report, when you click the **Change profile** button, now only the test profiles linked to the event that you defined for your transactional message are listed.

### Patches {#patches-1}

* Fixed an issue with the byEmail query filter which failed to return any results. (CAMP-23420)
* Fixed an issue which allowed a standard user to access certain features or screens restricted to administrators (/rest/head/&#42; endpoints, transactional messaging screens, profiles and audiences import screens). 
* Fixed an issue which prevented GDPR Privacy delete requests from processing custom resources if their name started by a number.
* Fixed an error that prevented the Save Audience activity from sharing application subscribers in Adobe Experience Cloud.
* Fixed an issue with the File Transfer activity that could occur when the file name contained blank spaces. (CAMP-25936)
* Fixed an issue that could occur when using the reconnection button after a session expires. (CAMP-25560)
* Fixed an issue that could lead to exclusions when sending deliveries with time zone optimization associated to fatigues rules. (CAMP-25425)
* Fixed an issue when using the API GDPR feature, that could prevent from deleting data with a 0-1 type link.
* Fixed an issue that could lead to an error message when cancelling the edition of a fatigue typology rule.
* Fixed an issue that could occur when previewing a delivery content after it had been edited.
* Fixed an issue that could occur when processing CSV zip files while using the Decompression option.
* Fixed an issue in the Creative Designer which resulted in unwanted color font and formatting when changing some text with inbuilt styling to a link or when editing that link. (CAMP-26001)
* Fixed an issue that prevented the hot click report to display the percentages for each condition in deliveries containing dynamic content. Previously, only the clicks on the default variant were displayed.

## Release 18.6 - June 2018 {#release-18-6---june-2018}

### Improvements {#improvements-2}

* The **[!UICONTROL History]** API has been added to Adobe.IO. It allows you to access information related to a profile's marketing history: number of touchpoints, sent deliveries, mirror page URL etc. For more on this, refer to the [dedicated use case](../../api/using/interacting-with-marketing-history.md) .
* The **[!UICONTROL Database cleanup]** technical workflow has been optimized in order to ensure better performance for database backup.
* The Creative Designer for Email is now also available in French and German.

### Other changes {#other-changes-2}

* A **[!UICONTROL Compute stats]** button has been added in the **[!UICONTROL Deployment]** window of sent deliveries. It allows you to retrieve the latest KPIs, for example if the results from the sending take too long to update or have not been taken into account. For more on this, refer to this [section](../../sending/using/confirming-the-send.md). 
* In the **Update for deliverability** out-of-the-box technical workflow, functional administrators can now define the number of consecutive errors to ignore in the **Update rules** javascript activity. By default, the field value is set to 0, which means that all errors will be ignored.
* The SQL generated when managing unit access restriction conditions has been optimized.
* The **[!UICONTROL Update]** activity now allows you to add, update or delete data related to subscriptions (nms:appSubscriptionRcp table). 
* The **[!UICONTROL Update delivery execution]** technical workflow has been divided into two workflows in order to optimize performance: - **[!UICONTROL Update delivery execution]**: updates the delivery's tracking. It is started every 10 minutes by default. **[!UICONTROL Update delivery indicators]**: updates the delivery's KPI's, it is started every hour by default. For more on technical workflows, refer to this [section](../../administration/using/technical-workflows.md#list-of-technical-workflows).
* When a delivery is sending messages, the status in the **[!UICONTROL Deployment]** section can now have two values: **[!UICONTROL Sending]**: the messages are being sent. **[!UICONTROL Sending (retry)]**: a retry pass is in progress. 
* Users with the **[!UICONTROL Delivery preparation]** role are now able to send proofs. (CAMP-24313)
* The **Enable TLS over SMPP** option has been added to the **SMS routing via SMPP** external account. For more on this refer to this [section](../../administration/using/configuring-sms-channel.md#defining-an-sms-routing).

### Patches {#patches-2}

* Fixed an issue which could prevent emails from being sent when including a dynamic image from Adobe Target (CAMP-24848). 
* Fixed an issue with the **[!UICONTROL Privacy Access/Delete Request]** technical workflows, which did not complete if any of the requests failed.
* Fixed an issue which prevented the Privacy Core service from receiving request status updates from Campaign. 
* Fixed an issue which could prevent the **[!UICONTROL Import shared audience]** technical workflow from working properly (CAMP-25465).
* Fixed an issue which prevented Campaign privacy requests from being marked as completed in the Core Privacy Service.
* Fixed an issue which could prevent certain users from logging in to Campaign Standard through IMS authentication when the Adobe ID was too long. (CAMP-24095)
* Fixed an issue in the Creative Designer that could occur when removing content modules. (CAMP-25242)
* Fixed an issue when using push notifications fatigue rules for subscribers with no profile in the database. (CAMP-25344)
* Fixed an issue which could display an error message when accessing deliveries exclusion logs. (CAMP-24724)
* Fixed an issue which prevented proofs from being prepared in instances with extended sending logs. 
* Fixed two issues that could occur when publishing custom resources with the **[!UICONTROL Sending log]** extension activated. 
* Fixed an issue that could occur with delivery duration not taken into account in recurring deliveries. 
* Fixed an issue that could occur when sorting data in the **[!UICONTROL Client data]** menu, for custom resources with more than 100K records. (CAMP-24308)
* Fixed an issue with custom profile dimensions which were not taken into account when using the search function in Dynamic reports. 
* Fixed an issue with the display of international data for Account levels in Dynamic reports.
* It is now possible to create a service without a subscription or unsubscription confirmation message.

## Release 18.5 - May 2018 {#release-18-5---may-2018}

### What's new? {#what-s-new--2}

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> GDPR: Core Service Integration<br /> </td> 
   <td> Privacy Core Service Integration allows you to automate your GDPR requests in a multi-solution context through a single JSON API call. <br /> GDPR requests pushed from the Privacy Core Service to all Experience Cloud solutions are now automatically handled by Campaign. <br /> For more information, refer to the <a href="https://docs.campaign.adobe.com/doc/standard/getting_started/en/ACS_GDPR.html">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Push improvements - detailed delivery feedback<br /> </td> 
   <td> Adobe Campaign now provides the ability to receive detailed feedback (sending logs et exclusion logs) on push messages from the providers (APNS/GCM) via MCPNS.<br /> For more information, refer to the <a href="../../channels/using/preparing-and-sending-a-push-notification.md#sending-the-notification">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Delivery logs extension<br /> </td> 
   <td> Delivery logs extension allows you to extend sending logs with profile data and segment code coming from workflows. This information can then be used in Dynamic Reports, and lets you keep a snapshot of some information at the sending time of a delivery.<br /> There are 2 more use cases :<br /> 
    <ul> 
     <li> Export extended broadlogs with "frozen" data: As a marketer, I would like to export all the profiles where segment code equals "A" (coming from the workflow engine). </li> 
     <li> Segmentation on "frozen" data: As a marketer, I would like to <strong>retarget</strong> all profiles who have won 1000 loyalty points since the last sending or where segment code was equal to "A". </li> 
    </ul> For more information, refer to the <a href="../../developing/using/configuring-the-resource-s-data-structure.md#defining-sending-logs-extension">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Dynamic reporting with Custom profile data<br /> </td> 
   <td> This feature allows you to create and manage reports based on custom profile data created during the profile resource extension. You can breakdown reports by profile attribute such as loyalty program, preferred channel, etc.<br /> For more information, refer to the <a href="../../developing/using/configuring-the-resource-s-data-structure.md#defining-sending-logs-extension">detailed documentation</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Improvements {#improvements-3}

* Overall memory and CPU usage of the application has been enhanced

### Other changes {#other-changes-3}

* The Read Audience workflow activity can now read Experience Cloud audiences. Previously, this activity could only read Query and List audiences. Refer to the [detailed documentation](../../automating/using/read-audience.md). (CAMP-23623)
* The identifier of the default Shared data source is now in read only mode and can no longer be changed. Changing this identifier could lead to some issues when sharing audiences with the Experience Cloud.
* Importing audiences from Audience Manager now works with split files. Previously, only the last file of the segment was imported by the importSharedAudience technical workflow. 
* AWS S3 external accounts now support regions and the version 4 authentication mechanism. Refer to the [detailed documentation](../../administration/using/external-accounts.md).
* The Asset selection window should now load faster and allow to select an asset then exit the window without any issue.
* The properties and structure of technical workflows can now be modified by users with administration rights and belonging to the "All" organizational and geographical units.
* Enhancements have been made in the Segmentation activity interface when creating new segments: The Limitation tab now appears directly after adding a limitation. New segments' names are now incremented ("Segment 1", "Segment 2", etc.). 
* A "nextProcessingDate" field is added to the Workflow resource. This field is only visible via REST API calls, it allows you to visualize workflows next processing dates. 
* The "sourceId" field is now exposed in the tracking logs resource (nms:trackingLog).
* "Total opens" and "Total clicks" values can now be exported in a flat file via a workflow. (CAMP-24186) 
* "English - Danmark" is now available in the Preferred languages list in profiles. (CAMP-23728) 
* When using a Segmentation activity with an Additional data (targetData) link, a message now informs you that the data is not available outside the workflow. This message displays when clicking on the Count or Preview button from the Segmentation activity. (CAMP-23651) 
* Enhancements have been made to optimize disk space used by workflows: (CAMP-21979): The files processed by the "Load file" activity are now deleted by default. An option allows you to keep them for specific needs. When a workflow is deleted, its dedicated folder is automatically suppressed from the server directory.

### Patches {#patches-3}

* Fixed an issue where some raw reporting events did not have associated tracking events because the eventDate field was not properly populated.
* Fixed an issue that prevented personalized fields to show in the preview window of a push notification delivery.
* Fixed an issue that prevented the text from word-wrapping the message body of a push notification in the preview window.
* Fixed an issue when sending a reccuring delivery from a workflow when the main target is empty.
* Fixed an issue which prevented from accessing a target mapping if it is linked to an unexisting schema.
* Fixed an issue that could occur when importing a zip file via a File load activity. (CAMP-24309) 
* Fixed an issue which led to a PostgreSQL error when sending a recurring delivery. (CAMP-23613) 
* Fixed an issue which displayed an error message when sending a REST API request with an empty JSON attribute. (CAMP-23506) 
* Fixed an issue in profiles which set to capitals the characters following the "ß" character. (CAMP-23136) 
* Fixed an issue when sending deliveries used with personalization or dynamic content block's eligibility condition while using attributes from a linked schema of profile. (CAMP-22751) 
* Fixed an issue which prevented from deleting services. (CAMP-22050) 
* Fixed an issue that prevented from changing the Country or State values in a Test profile. (CAMP-20426) 
* Fixed an issue which could prevent the Creative Designer from loading. (CAMP-24573) 
* Fixed an issue which removed characters added after personalization fields in the email subject. (CAMP-24113)

## Release 18.4 - April 2018 {#release-18-4---april-2018}

### Patches {#patches-4}

#### Platform {#platform}

* Fixed an error that could prevent from correctly processing GDPR access or delete requests. This behavior has been observed in some rare cases where the extracted data was containing one of the following characters: & < > " '.

#### Emails, SMS messages and direct mail {#emails--sms-messages-and-direct-mail}

* Fixed an issue could lead to KPIs being overwritten with wrong values if the broadlog synchronization took more than an hour.

#### Workflows {#workflows}

* Improved memory management and optimized performances in workflows.

#### Reporting {#reporting}

* KPI sharing workflow now retrieves delivery values for the last 2 months instead of the last 6 months. Fixed an issue with KPI sharing external account showing truncated dates.
* Fixed an issue which could lead to certain messages not being taken into account in **Sent**, **Delivered** and **Bounce**metrics.
* Fixed an error which occurred when the chosen time range in the **Delivery Summary Report** was too long.

#### Custom resources {#custom-resources}

* Fixed an error which caused custom resource preparation to fail.

## Release 18.3 - March 2018 {#release-18-3---march-2018}

### New capabilities {#new-capabilities}

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> EU General Data Protection Regulation (GDPR)<br /> </td> 
   <td> GDPR is the European Union’s (EU) new privacy law that harmonizes and modernizes data protection requirements going into effect on May 25, 2018. GDPR applies to Adobe Campaign customers who hold data for Data Subjects residing in the EU.<br /> In addition to the privacy capabilities already available in Adobe Campaign (including consent management, data retention settings, and user roles), we are taking this opportunity in our role as Data Processor to include additional capabilities, to help facilitate your readiness as Data Controller for certain GDPR requests:<br /> 
    <ul> 
     <li> Right to Access: allows the Data Subject to receive a copy of his/her personal data captured by Data Controllers, potentially including data stored in Adobe Campaign. </li> 
     <li> Right to Delete: entitles the Data Subject to have his/her personal data captured by Data Controllers erased, potentially including data stored in Adobe Campaign. </li> 
    </ul> For more information, refer to the <a href="https://docs.campaign.adobe.com/doc/standard/getting_started/en/ACS_GDPR.html">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Creative Designer for Email (Beta)<br /> </td> 
   <td> Adobe Campaign's new Creative Designer offers a fully integrated creation experience in Campaign, enabling the quick and effortless visual creation of captivating, individually personalized emails without the need to script a single line of code. Through its powerful drag and drop interface, the Creative Designer helps scale email creation whether users start from a blank slate, or leverage existing content Fragments or templates. <br /> Key capabilities include:<br /> 
    <ul> 
     <li> Visually design and create fully personalized, responsive emails through a drag and drop interface, augmented by native Creative Cloud integrations </li> 
     <li> Create and save an email content template &amp; leverage saved templates to help scale email creation </li> 
     <li> Create and save content Fragments (such as a header, footer, article, etc.) to streamline content creation and ensure brand consistency </li> 
     <li> Seamlessly switch between creating in the drag &amp; drop interface and directly editing HTML of an email at the click of a button </li> 
    </ul> The Creative Designer for Email is only available in English.<br /> For more information, refer to the <a href="../../designing/using/overview.md">detailed documentation</a> and watch this <a href="https://www.youtube.com/watch?time_continue=1&amp;v=5S_6A4fsfms">video</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Multilingual Push Deliveries<br /> </td> 
   <td> The same simple multilingual interface, that already exists on the Email and SMS channels, has been added to the Push channel helping you engage customers no matter their preferred language.<br /> This capability offers a scalable and automatic solution for customers who manage Push campaigns spanning multiple regions and want to target users in their preferred language. It allows you to upload all lingual variants through a templated spreadsheet to a single Push delivery, in one click. Adobe Campaign then performs an automatic segmentation based on users' language preference, helping to reduce the redundancies by simplify workflows and reporting.<br /> For more information, refer to the <a href="../../channels/using/creating-a-multilingual-push-notification.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Use of Custom Resources in Transactional Messaging<br /> </td> 
   <td> In addition to out-of-the-box fields, transactional messaging now allows you to use custom resources to enrich the content of your messages.<br /> For example:<br /> 
    <ul> 
     <li> Leverage custom fields as a reconciliation criteria to match a transactional message to a profile </li> 
     <li> Leverage full profiles, services and linked data to further personalize transactional messages </li> 
    </ul> For more information, refer to the <a href="../../administration/using/configuring-transactional-messaging.md">detailed documentation</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches {#patches-5}

#### Platform {#platform-1}

* Fixed an issue that prevented from exporting more than 5000 records from a list.
* Fixed an issue when exporting data to files named with personalization fields.

#### Emails, SMS messages and direct mail {#emails--sms-messages-and-direct-mail-1}

* Fixed an issue which caused multi-part SMS to be truncated because the size of parts were calculated in characters instead of bytes.
* Added an option which allows the **[!UICONTROL Delivered]** or **[!UICONTROL Bounces + Errors]** KPIs to be updated in real time after sending your delivery. They are directly recalculated from the SR (Status Report) received from the provider.
* Fixed an issue with the calendar widget in the delivery scheduler.
* Fixed a display issue when opening a target for a second time in a sent delivery.
* Fixed an issue which led to an error message requesting a start date, when creating an email template with a delayed sending date.
* Fixed an issue that could cause image rendering issues when editing the content of a delivery.
* Fixed an issue with proofs when duplicating a campaign.
* Fixed an issue that led to an error message when accessing a campaign template via the navigation bar, after adding a delivery to the workflow.
* Fixed an issue that could prevent the winner of an A/B test email to be automatically selected, leading to the email not being sent. This behavior could occur if the delivery was in **[!UICONTROL retryInProgress]** state.
* Fixed an issue that could lead to an error message appearing when re-opening the parameters of an A/B test email.

#### Audiences &amp; queries {#audiences-e-queries}

* Fixed an issue that prevented from accessing data and setting up queries for recipients replicated from Adobe Campaign Classic to Standard.
* Fixed an issue that occurred when using a filter type field in the query editor, after using the **Count** or **Preview** buttons.

#### Workflows {#workflows-1}

* The **Billing** workflow has been optimized to improve the delivery preparation delay.
* Fixed an issue that prevented population data from being displayed in an outbound transition when using a recurring delivery activity.
* Fixed an issue that prevented reject records from being displayed in a transition after an **Update data** activity.
* Fixed an issue which could cause the **deliverabilityUpdate** technical workflow to fail.

#### Integrations {#integrations}

* Fixed an issue that prevented international characters from being correctly sent to Adobe Analytics.
* Assets should now load faster when trying to insert an image from your Experience Cloud asset library in a message.
* Fixed an issue that could prevent the asset selection window from being closed in some cases.
* From a datasource detail, you can now directly access its related workflow to check the workflow’s state.
* You can now update the Triggers schema directly when defining or editing a trigger event. With this change, you no longer have to unpublish the trigger and create another one.

#### Transactional messages {#transactional-messages}

* Fixed an error with transactional message template when the delivery resource was extended.
* It is now possible to delete transactional messages.

## Release 18.2 - February 2018 {#release-18-2---february-2018}

### New capabilities {#new-capabilities-1}

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Subscription - subscribe or unsubscribe a list of profiles to multiple services<br /> </td> 
   <td> The <strong>Subscription Services</strong> workflow activity now allows you to subscribe or unsubscribe a list of profiles to multiple services. In your workflow, import a file containing the profiles, and for each profile, the operation type and the service. The <strong>Subscription Services</strong> activity will be able to use this information and handle dynamically all your profiles subscriptions and unsubscriptions at once.<br /> For more information, refer to the <a href="../../automating/using/subscription-services.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Enrichment activity - enrich data based on previous transitions<br /> </td> 
   <td> The new <span class="uicontrol">Enrichment</span> workflow activity allows you to leverage the inbound transitions and complete the output transition with additional data. If you target profiles, the enrichment activity allows you to enrich the profiles information with additional data that is not stored in the database (coming from an imported file, for example).<br /> For more information, refer to the <a href="../../automating/using/enrichment.md">detailed documentation</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches {#patches-6}

#### Platform {#platform-2}

* The top bar of Adobe Campaign's interface has been updated with the new Experience Cloud menu.
* Fixed an issue which prevented the link to **[!UICONTROL Offers]** from being displayed in the solution dropdown list.

#### Emails, SMS messages and direct mail {#emails--sms-messages-and-direct-mail-2}

* The delivery preparation phase has been enhanced to improve performance.
* Fixed several issues that could cause tracking logs to be corrupted in some niche situations.
* Fixed a contact date update issue that occurred when the contact date was changed between delivery preparation and confirmation. Now, when you change the contact date after the preparation, you are required to prepare the delivery again before being able to confirm the send. See the [detailed documentation](../../sending/using/preparing-the-send.md).

#### Push notifications {#push-notifications}

* Fixed an error that prevented some personalization fields from working in iOS push notifications.
* Fixed an error which displayed the click and open rates as 0% in the push notification dashboard.

#### Reports {#reports}

* Fixed an error that showed the report list as empty in some browsers.
* Fixed an error that occurred in the **[!UICONTROL Report sharing]** technical workflow just before its expiration limit was reached.

#### Workflows {#workflows-2}

* Fixed an issue which prevented activities from being accessible after drag and dropping them.
* Fixed an issue that could cause the order of output transitions of a **[!UICONTROL Segmentation]** activity to change in some situations.
* Fixed an error occurring when reading an audience containing an enumeration type field and that had previously been saved from a workflow
* Fixed an issue causing the **[!UICONTROL Request confirmation before sending messages]** option to remain checked even after unchecking it when defining the scheduling properties of a delivery created in a workflow.
* Automatic removal of duplicate rows (DISTINCT clause) can now be disabled in **[!UICONTROL Query]** activities, via a new option located in the **[!UICONTROL Additional data]** tab. Disabling this option is recommended when defining many (more than 100) additional elements, for performance reasons.

#### Integrations {#integrations-1}

* Some improvements were made to the **[!UICONTROL Data sources]** configuration screen.

### Known issues {#known-issues}

We recommend that you do not use Internet Explorer version 11 because of possible display issues.

Some issues might occur when using contextual help links from Campaign interface. They will be fixed in 18.3.

## Release 18.1 - January 2018 {#release-18-1---january-2018}

### New capabilities {#new-capabilities-2}

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Reporting for Fatigue Management<br /> </td> 
   <td> Reporting for Fatigue Management is a dedicated, configurable report displaying the impact fatigue rules have on deliveries across the Email, Push, SMS, and Direct Mail channels within a specified date range before send. With the added insight of being able to quickly see all conflicting campaigns in a single view, marketers are able to plan marketing campaigns according to set the fatigue rules more effectively, and prioritize communications.<br /> For more information, refer to the <a href="../../administration/using/fatigue-rules.md#viewing-the-fatigue-rule-summary-report">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Report sharing<br /> </td> 
   <td> Report Sharing allows you to share your reports with Adobe Campaign users as an email attachment including on an automated recurring basis. Users who receive recurring reports have the ability to unsubscribe from these communications via a dedicated link in each email.<br /> For more information, refer to the <a href="../../reporting/using/reporting-interface.md#share-tab">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Push New capabilities<br /> </td> 
   <td> Push Message Preview - Preview push notifications on iOS and Android devices from within the push notification content editor to see exactly what your recipients will see before testing or executing the delivery.<br /> For more information, refer to the <a href="../../channels/using/preparing-and-sending-a-push-notification.md#preparing-the-notification">detailed documentation</a>.<br /> Content Available - When apps are not opened over longer periods of time, their data can become outdated. This results in the data having to be updated or replaced at the moment a user finally opens the app, which can cause delays in using the app. With the added support of Content Available, Adobe Campaign users can wake up their app to refresh its data in the background when delivering a push notification, enabling greater consistency and control over a user’s in-app experience.<br /> Mutable Content - With the added support of Mutable Content, Adobe Campaign users can now leverage their mobile app extensions to further modify the content or presentation of arriving push notifications sent from Adobe Campaign. For example, users can leverage Mutable Content to: <br /> 
    <ul> 
     <li> decrypt data that was delivered in an encrypted format </li> 
     <li> download images or other media files and add them as attachments to a notification </li> 
     <li> change the body or title text of a notification </li> 
     <li> add a thread identifier to a notification </li> 
    </ul> For more information on Content Available and Mutable Content, refer to the <a href="../../channels/using/customizing-a-push-notification.md#change-the-notification-behavior-for-ios">detailed documentation</a>.<br /> <strong>Warning:</strong> these updates on push notifications require customers to upgrade their mobile applications. Refer to <a href="https://helpx.adobe.com/campaign/kb/understanding-campaign-standard-push-notifications-payload-struc.html">this technote</a> for more information.<br /> </td> 
  </tr> 
  <tr> 
   <td> Time-zone optimized deliveries<br /> </td> 
   <td> Schedule recurring Email, SMS, and Push notifications to be delivered at a specific day/time in every recipients’ time zone ensuring that your messages are delivered at the right time without setting up multiple deliveries. <br /> For more information, refer to the <a href="../../automating/using/scheduler.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> API Signal activity triggering<br /> </td> 
   <td> It is now possible to trigger a signal activity for your workflows directly from Adobe Campaign Standard API.<br /> For more information, refer to the <a class="anchorLink" href="../../api/using/triggering-a-signal-activity.md">detailed documentation</a> .<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches {#patches-7}

#### Platform {#platform-3}

* The profile search has been optimized to improve performance. 
* The internal identifier of default security groups is now in read-only mode for standard users.

#### Emails, SMS messages and direct mail {#emails--sms-messages-and-direct-mail-3}

* Fixed a display issue which occurred when inserting emojis into the content of your deliveries. 
* Fixed an issue which allowed the user to access sending logs when the delivery was still in edition.
* The **[!UICONTROL Scheduler]** activity now allows you to send your deliveries depending on the recipient's time zone.
* SMS: The option **[!UICONTROL Store incoming MO]** in the database has been added to external accounts. When checked, all incoming SMS will be stored into the **inSMS** table.
* SMS: Services are now attached to an event instead of a transactional template.
* SMS: The default SMTP connection timeout has been reduced to 30 seconds.

#### Push notifications {#push-notifications-1}

* Fixed an error that prevented push notification deliveries from being stopped.
* Added an option in push notification advanced options to wake up the application with a push notification.
* Added a pause button for the push notification preview video.
* The push notification preview is now available for different devices such as iPhone, Android, tablets.

  all channels

#### Reports {#reports-1}

* Fixed an error which displayed rates over 100%.
* Fixed an issue that prevented users from downloading reports in CSV.
* Added a new **[!UICONTROL Report]** item in the homepage.

#### Workflows {#workflows-3}

* Fixed an issue which led to an error message when using additional data in a query and adding aliases containing spaces. The non-alphanumeric characters are now replaced by "_".
* Fixed an issue where the technical workflow calculating KPIs could be stopped by default in some cases.

#### Profiles and audiences {#profiles-and-audiences}

* Fixed an error that occurred when adding multiple filters in an audience's query.
* Fixed a display issue that occurred when changing a profile's picture.
* Added a tooltip displaying the exact result number after counting the population of a query.
* Fixed an issue that could prevent a user from selecting an audience or closing the audience picker window.
* The list of available functions in the expression editor has been updated. The **FormatCurrency** and **ConvertCurrency** functions have been removed.

