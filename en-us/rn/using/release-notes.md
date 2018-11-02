---
title: Release Notes
seo-title: Release Notes
description: Release Notes
seo-description: This page lists all 2017 and 2018 releases of Adobe Campaign Standard.
uuid: 9d0b21b0-70d1-48d4-a40c-ef719a7a97a7
content-encoding: UTF-8
aemsrcnodepath: /content/help/en/campaign/standard/rn/using/release-notes
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-08-01T05 09 54.209-0400
cq-lastmodifiedby: beneat
cq-lastreplicated: 2018-08-01T05 09 54.243-0400
cq-lastreplicatedby: beneat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: rn
content-type: reference
topic-tags: campaign-standard-releases
cq-template: /apps/help/templates/article-3
discoiquuid: b46e575d-d311-47fa-909f-b849b5bf0be9
firstPublishExternalDate: 2018-07-23T06:03:01.202-0400
firstpublishinternaldate: 2018-07-27T13 20 42.288-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-02-28T08 01 06.081-0500
jcr-createdby: admin
jcr-description: Release Notes
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-08-01T05:09:54.204-0400
lastpublishinternaldate: 2018-08-01T05 09 54.204-0400
lochandoffdate: 2018-07-30T04 51 22.154-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: beneat@adobe.com
moreHelpPaths: /content/help/en/campaign/standard/rn/morehelp/campaign-standard-releases;/content/help/en/campaign/standard/rn/morehelp/campaign-standard-releases
navTitle: Release Notes
publishexternaldate: 2018-08-01T05 09 54.204-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/rn/using/release-notes.html
publishinternaldate: 2018-08-01T05 09 54.204-0400
publishinternalurl: https //helpx-internal.corp.adobe.com/content/help/en/campaign/standard/rn/using/release-notes.html
sha1: 4073af6a48b021bfa9d61b9709809887a5dd9827
topicBrowsingSortDate: 2018-08-01T05:09:54.204-0400
index: y
internal: n
snippet: y
---

# Release Notes

Release Notes

Looking for a specific 2017-2018 release of Adobe Campaign Standard?

Each release comes with new features and patches. Click on a release to view its content.

View the latest [documentation updates](../../rn/using/documentation-updates.md) for Adobe Campaign Standard. If you're looking for a previous release, consult this [page](../../rn/using/previous-release-notes.md).

## v18.7 - July 2018 release

### What's new?

<table> 
 <thead> 
  <tr> 
   <th>Functionality<br /> </th> 
   <th>Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>High priority flag for Android push notifications<br /> </td> 
   <td>High priority flag for Android - Enable delivering a push notification with high priority for Android apps which causes the sleeping device to wake up and run some limited processing. Note that default priority is Normal which may delay the message delivery to save battery.<br /> For more information, refer to the <a href="../../channels/using/customizing-a-push-notification.md#change-the-notification-behavior-for-android">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td>Typology filter for mobile app subscribers<br /> </td> 
   <td>Support subscriptions in typology filter - When specifying the filtering criteria for a typology rule, application subscriptions can be selected as the filtering and targeting dimensions, providing the ability to filter on attributes for users with or without a profile.<br /> For more information, refer to the <a href="../../administration/using/about-typology-rules.md#typology-rules">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td>Automated content import from a URL during message preparation<br /> </td> 
   <td>It is now possible to import email content from a URL during the preparation phase. For recurring email deliveries, the latest HTML content is retrieved each time the message is prepared ensuring the content is always up-to-date at the time the email is sent. This feature also lets you create a scheduled delivery with content from a URL even if the content is not ready yet.<br /> For more information, refer to the <a href="../../designing/using/importing-content-from-a-url.md#retrieving-content-from-a-url-automatically-at-preparation-time">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td>Campaign release notification message<br /> </td> 
   <td>A pop-up message now appears when a user logs in after the instance has been upgraded to a new version. The message indicates the version number and includes a link to the release notes. You can choose to hide the message until the next release.<br /> </td> 
  </tr> 
  <tr> 
   <td>User management</td> 
   <td>The geographical unit capability is now unavailable for new Campaign Standard instances, as well as existing instances with no geographical units created, starting 18.7 release.<br /> For more information, refer to this <a href="https://helpx.adobe.com/campaign/kb/acs-deprecated-and-removed-features.html">page</a>.</td> 
  </tr> 
 </tbody> 
</table>

### Improvements

* The Adobe Campaign and Adobe Target integration now allows you to leverage Target’s [Permissions](https://marketing.adobe.com/resources/help/en_US/target/target/properties-overview.html) feature. When including a dynamic image from Adobe Target in an email, you can now specify a Target Property (at_property code).
* Custom resources that have an owncopy link to the profiles resource are now taken into account by GDPR Privacy access/delete requests. For 1 cardinality simple links and N cardinality collection links, you need to select "Deleting/Duplicating the target record implies deleting/duplicating the records referenced by the link" in the custom resource. For 0 or 1 cardinality simple links, select "Deleting/Duplicating the record implies deleting/duplicating the target record referenced by the link”.

### Other changes

* Report sharing time out has been increased from one to four minutes to avoid any time out error.
* When editing the content of an email, the new Creative Designer opens by default. If you wish, you can still go back to the default content editor at any time after saving your changes. For more on this, refer to the [detailed documentation](../../designing/using/about-email-content-design.md).
* In the Creative Designer, a new content component can now be added into an email: the carousel. For more on this, refer to the [detailed documentation](../../designing/using/defining-the-email-structure.md#about-content-components).
* In a transactional message hot click report, when you click the **Change profile** button, now only the test profiles linked to the event that you defined for your transactional message are listed.

### Patches

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

## v18.6 - June 2018 release

### Improvements

* The **History** API has been added to Adobe.IO. It allows you to access information related to a profile's marketing history: number of touchpoints, sent deliveries, mirror page URL etc. For more on this, refer to the [dedicated use case](https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#how-to-retrieve-the-mirror-page-for-a-delivery-sent-to-a-profile) .
* The **Database cleanup** technical workflow has been optimized in order to ensure better performance for database backup.
* The Creative Designer for Email is now also available in French and German.

### Other changes

* A **Compute stats** button has been added in the **Deployment** window of sent deliveries. It allows you to retrieve the latest KPIs, for example if the results from the sending take too long to update or have not been taken into account. For more on this, refer to this [section](../../sending/using/confirming-send.md). 
* In the **Update for deliverability** out-of-the-box technical workflow, functional administrators can now define the number of consecutive errors to ignore in the **Update rules** javascript activity. By default, the field value is set to 0, which means that all errors will be ignored.
* The SQL generated when managing unit access restriction conditions has been optimized.
* The **Update** activity now allows you to add, update or delete data related to subscriptions (nms:appSubscriptionRcp table). 
* The **Update delivery execution** technical workflow has been divided into two workflows in order to optimize performance: - **Update delivery execution**: updates the delivery's tracking. It is started every 10 minutes by default. **Update delivery indicators**: updates the delivery's KPI's, it is started every hour by default. For more on technical workflows, refer to this [section](../../administration/using/technical-workflows.md#list-of-technical-workflows).
* When a delivery is sending messages, the status in the **Deployment** section can now have two values: **Sending**: the messages are being sent. **Sending (retry)**: a retry pass is in progress. 
* Users with the **Delivery preparation** role are now able to send proofs. (CAMP-24313)
* The **Enable TLS over SMPP** option has been added to the **SMS routing via SMPP** external account. For more on this refer to this [section](../../administration/using/configuring-sms-channel.md#defining-an-sms-routing).

### Patches

* Fixed an issue which could prevent emails from being sent when including a dynamic image from Adobe Target (CAMP-24848). 
* Fixed an issue with the **Privacy Access/Delete Request** technical workflows, which did not complete if any of the requests failed.
* Fixed an issue which prevented the Privacy Core service from receiving request status updates from Campaign. 
* Fixed an issue which could prevent the **Import shared audience** technical workflow from working properly (CAMP-25465).
* Fixed an issue which prevented Campaign privacy requests from being marked as completed in the Core Privacy Service.
* Fixed an issue which could prevent certain users from logging in to Campaign Standard through IMS authentication when the Adobe ID was too long. (CAMP-24095)
* Fixed an issue in the Creative Designer that could occur when removing content modules. (CAMP-25242)
* Fixed an issue when using push notifications fatigue rules for subscribers with no profile in the database. (CAMP-25344)
* Fixed an issue which could display an error message when accessing deliveries exclusion logs. (CAMP-24724)
* Fixed an issue which prevented proofs from being prepared in instances with extended sending logs. 
* Fixed two issues that could occur when publishing custom resources with the **Sending log** extension activated. 
* Fixed an issue that could occur with delivery duration not taken into account in recurring deliveries. 
* Fixed an issue that could occur when sorting data in the **Client data** menu, for custom resources with more than 100K records. (CAMP-24308)
* Fixed an issue with custom profile dimensions which were not taken into account when using the search function in Dynamic reports. 
* Fixed an issue with the display of international data for Account levels in Dynamic reports.
* It is now possible to create a service without a subscription or unsubscription confirmation message.

## v18.5 - May 2018 release

### What's new?

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
   <td> Adobe Campaign now provides the ability to receive detailed feedback (sending logs et exclusion logs) on push messages from the providers (APNS/GCM) via MCPNS.<br /> For more information, refer to the <a href="../../channels/using/creating-and-sending-a-push-notification.md#sending-and-tracking-notifications">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Delivery logs extension<br /> </td> 
   <td> Delivery logs extension allows you to extend sending logs with profile data and segment code coming from workflows. This information can then be used in Dynamic Reports, and lets you keep a snapshot of some information at the sending time of a delivery.<br /> There are 2 more use cases :<br /> <li> Export extended broadlogs with "frozen" data: As a marketer, I would like to export all the profiles where segment code equals "A" (coming from the workflow engine). </li> <li> Segmentation on "frozen" data: As a marketer, I would like to <strong>retarget</strong> all profiles who have won 1000 loyalty points since the last sending or where segment code was equal to “A”. </li> For more information, refer to the <a href="../../developing/using/step-2--configure-the-resource-data-structure.md#defining-sending-logs-extension">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Dynamic reporting with Custom profile data<br /> </td> 
   <td> This feature allows you to create and manage reports based on custom profile data created during the profile resource extension. You can breakdown reports by profile attribute such as loyalty program, preferred channel, etc.<br /> For more information, refer to the <a href="../../developing/using/step-2--configure-the-resource-data-structure.md#defining-sending-logs-extension">detailed documentation</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Improvements

* Overall memory and CPU usage of the application has been enhanced

### Other changes

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

### Patches

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

## v18.4 - April 2018 release

### Patches

#### Platform

* Fixed an error that could prevent from correctly processing GDPR access or delete requests. This behavior has been observed in some rare cases where the extracted data was containing one of the following characters: & < > " '.

#### Emails, SMS messages and direct mail

* Fixed an issue could lead to KPIs being overwritten with wrong values if the broadlog synchronization took more than an hour.

#### Workflows

* Improved memory management and optimized performances in workflows.

#### Reporting

* KPI sharing workflow now retrieves delivery values for the last 2 months instead of the last 6 months. Fixed an issue with KPI sharing external account showing truncated dates.
* Fixed an issue which could lead to certain messages not being taken into account in **Sent**, **Delivered** and **Bounce**metrics.
* Fixed an error which occurred when the chosen time range in the **Delivery Summary Report** was too long.

#### Custom resources

* Fixed an error which caused custom resource preparation to fail.

## v18.3 - March 2018 release

### New capabilities

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
   <td> GDPR is the European Union’s (EU) new privacy law that harmonizes and modernizes data protection requirements going into effect on May 25, 2018. GDPR applies to Adobe Campaign customers who hold data for Data Subjects residing in the EU.<br /> In addition to the privacy capabilities already available in Adobe Campaign (including consent management, data retention settings, and user roles), we are taking this opportunity in our role as Data Processor to include additional capabilities, to help facilitate your readiness as Data Controller for certain GDPR requests:<br /> <li> Right to Access: allows the Data Subject to receive a copy of his/her personal data captured by Data Controllers, potentially including data stored in Adobe Campaign. </li> <li> Right to Delete: entitles the Data Subject to have his/her personal data captured by Data Controllers erased, potentially including data stored in Adobe Campaign. </li> For more information, refer to the <a href="https://docs.campaign.adobe.com/doc/standard/getting_started/en/ACS_GDPR.html">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Creative Designer for Email (Beta)<br /> </td> 
   <td> Adobe Campaign's new Creative Designer offers a fully integrated creation experience in Campaign, enabling the quick and effortless visual creation of captivating, individually personalized emails without the need to script a single line of code. Through its powerful drag and drop interface, the Creative Designer helps scale email creation whether users start from a blank slate, or leverage existing content Fragments or templates. <br /> Key capabilities include:<br /> <li> Visually design and create fully personalized, responsive emails through a drag and drop interface, augmented by native Creative Cloud integrations </li> <li> Create and save an email content template &amp; leverage saved templates to help scale email creation </li> <li> Create and save content Fragments (such as a header, footer, article, etc.) to streamline content creation and ensure brand consistency </li> <li> Seamlessly switch between creating in the drag &amp; drop interface and directly editing HTML of an email at the click of a button </li> The Creative Designer for Email is only available in English.<br /> For more information, refer to the <a href="../../designing/using/about-email-content-design.md#using-the-creative-designer">detailed documentation</a> and watch this <a href="https://www.youtube.com/watch?time_continue=1&amp;v=5S_6A4fsfms">video</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Multilingual Push Deliveries<br /> </td> 
   <td> The same simple multilingual interface, that already exists on the Email and SMS channels, has been added to the Push channel helping you engage customers no matter their preferred language.<br /> This capability offers a scalable and automatic solution for customers who manage Push campaigns spanning multiple regions and want to target users in their preferred language. It allows you to upload all lingual variants through a templated spreadsheet to a single Push delivery, in one click. Adobe Campaign then performs an automatic segmentation based on users' language preference, helping to reduce the redundancies by simplify workflows and reporting.<br /> For more information, refer to the <a href="../../channels/using/creating-a-multilingual-push-notification.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Use of Custom Resources in Transactional Messaging<br /> </td> 
   <td> In addition to out-of-the-box fields, transactional messaging now allows you to use custom resources to enrich the content of your messages.<br /> For example:<br /> <li> Leverage custom fields as a reconciliation criteria to match a transactional message to a profile </li> <li> Leverage full profiles, services and linked data to further personalize transactional messages </li> For more information, refer to the <a href="../../administration/using/configuring-transactional-messaging.md">detailed documentation</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches

#### Platform

* Fixed an issue that prevented from exporting more than 5000 records from a list.
* Fixed an issue when exporting data to files named with personalization fields.

#### Emails, SMS messages and direct mail

* Fixed an issue which caused multi-part SMS to be truncated because the size of parts were calculated in characters instead of bytes.
* Added an option which allows the **Delivered** or **Bounces + Errors** KPIs to be updated in real time after sending your delivery. They are directly recalculated from the SR (Status Report) received from the provider.
* Fixed an issue with the calendar widget in the delivery scheduler.
* Fixed a display issue when opening a target for a second time in a sent delivery.
* Fixed an issue which led to an error message requesting a start date, when creating an email template with a delayed sending date.
* Fixed an issue that could cause image rendering issues when editing the content of a delivery.
* Fixed an issue with proofs when duplicating a campaign.
* Fixed an issue that led to an error message when accessing a campaign template via the navigation bar, after adding a delivery to the workflow.
* Fixed an issue that could prevent the winner of an A/B test email to be automatically selected, leading to the email not being sent. This behavior could occur if the delivery was in **retryInProgress** state.
* Fixed an issue that could lead to an error message appearing when re-opening the parameters of an A/B test email.

#### Audiences &amp; queries

* Fixed an issue that prevented from accessing data and setting up queries for recipients replicated from Adobe Campaign Classic to Standard.
* Fixed an issue that occurred when using a filter type field in the query editor, after using the **Count** or **Preview** buttons.

#### Workflows

* The **Billing** workflow has been optimized to improve the delivery preparation delay.
* Fixed an issue that prevented population data from being displayed in an outbound transition when using a recurring delivery activity.
* Fixed an issue that prevented reject records from being displayed in a transition after an **Update data** activity.
* Fixed an issue which could cause the **deliverabilityUpdate** technical workflow to fail.

#### Integrations

* Fixed an issue that prevented international characters from being correctly sent to Adobe Analytics.
* Assets should now load faster when trying to insert an image from your Experience Cloud asset library in a message.
* Fixed an issue that could prevent the asset selection window from being closed in some cases.
* From a datasource detail, you can now directly access its related workflow to check the workflow’s state.
* You can now update the Triggers schema directly when defining or editing a trigger event. With this change, you no longer have to unpublish the trigger and create another one.

#### Transactional messages

* Fixed an error with transactional message template when the delivery resource was extended.
* It is now possible to delete transactional messages.

## v18.2 - February 2018 release

### New capabilities

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
   <td> The new <strong>Enrichment</strong> workflow activity allows you to leverage the inbound transitions and complete the output transition with additional data. If you target profiles, the enrichment activity allows you to enrich the profiles information with additional data that is not stored in the database (coming from an imported file, for example).<br /> For more information, refer to the <a href="../../automating/using/enrichment.md">detailed documentation</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches

#### Platform

* The top bar of Adobe Campaign's interface has been updated with the new Experience Cloud menu.
* Fixed an issue which prevented the link to **Offers** from being displayed in the solution dropdown list.

#### Emails, SMS messages and direct mail

* The delivery preparation phase has been enhanced to improve performance.
* Fixed several issues that could cause tracking logs to be corrupted in some niche situations.
* Fixed a contact date update issue that occurred when the contact date was changed between delivery preparation and confirmation. Now, when you change the contact date after the preparation, you are required to prepare the delivery again before being able to confirm the send. See the [detailed documentation](../../sending/using/preparing-the-send.md)

#### Push notifications

* Fixed an error that prevented some personalization fields from working in iOS push notifications.
* Fixed an error which displayed the click and open rates as 0% in the push notification dashboard.

#### Reports

* Fixed an error that showed the report list as empty in some browsers.
* Fixed an error that occurred in the **Report sharing** technical workflow just before its expiration limit was reached.

#### Workflows

* Fixed an issue which prevented activities from being accessible after drag and dropping them.
* Fixed an issue that could cause the order of output transitions of a **Segmentation** activity to change in some situations.
* Fixed an error occurring when reading an audience containing an enumeration type field and that had previously been saved from a workflow
* Fixed an issue causing the **Request confirmation before sending messages** option to remain checked even after unchecking it when defining the scheduling properties of a delivery created in a workflow.
* Automatic removal of duplicate rows (DISTINCT clause) can now be disabled in **Query** activities, via a new option located in the **Additional data** tab. Disabling this option is recommended when defining many (more than 100) additional elements, for performance reasons.

#### Integrations

* Some improvements were made to the **Data sources** configuration screen.

### Known issues

We recommend that you do not use Internet Explorer version 11 because of possible display issues.

Some issues might occur when using contextual help links from Campaign interface. They will be fixed in 18.3.

## v18.1 - January 2018 release

### New capabilities

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
   <td> Push Message Preview - Preview push notifications on iOS and Android devices from within the push notification content editor to see exactly what your recipients will see before testing or executing the delivery.<br /> For more information, refer to the <a href="../../channels/using/creating-and-sending-a-push-notification.md#previewing-the-notification">detailed documentation</a>.<br /> Content Available - When apps are not opened over longer periods of time, their data can become outdated. This results in the data having to be updated or replaced at the moment a user finally opens the app, which can cause delays in using the app. With the added support of Content Available, Adobe Campaign users can wake up their app to refresh its data in the background when delivering a push notification, enabling greater consistency and control over a user’s in-app experience.<br /> Mutable Content - With the added support of Mutable Content, Adobe Campaign users can now leverage their mobile app extensions to further modify the content or presentation of arriving push notifications sent from Adobe Campaign. For example, users can leverage Mutable Content to: <br /> <li> decrypt data that was delivered in an encrypted format </li> <li> download images or other media files and add them as attachments to a notification </li> <li> change the body or title text of a notification </li> <li> add a thread identifier to a notification </li> For more information on Content Available and Mutable Content, refer to the <a href="../../channels/using/customizing-a-push-notification.md#change-the-notification-behavior-for-ios">detailed documentation</a>.<br /> <strong>Warning:</strong> these updates on push notifications require customers to upgrade their mobile applications. Refer to <a href="https://docs.campaign.adobe.com/doc/AC/en/technicalResources/Technotes/AdobeCampaign-UnderstandingACSPushNotificationsPayloadStructure.pdf">this technote</a> for more information.<br /> </td> 
  </tr> 
  <tr> 
   <td> Time-zone optimized deliveries<br /> </td> 
   <td> Schedule recurring Email, SMS, and Push notifications to be delivered at a specific day/time in every recipients’ time zone ensuring that your messages are delivered at the right time without setting up multiple deliveries. <br /> For more information, refer to the <a href="../../automating/using/scheduler.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> API Signal activity triggering<br /> </td> 
   <td> It is now possible to trigger a signal activity for your workflows directly from Adobe Campaign Standard API.<br /> For more information, refer to the <a class="anchorLink" href="https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#triggering-a-signal-activity" target="_blank">detailed documentation</a> .<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches

#### Platform

* The profile search has been optimized to improve performance. 
* The internal identifier of default security groups is now in read-only mode for standard users.

#### Emails, SMS messages and direct mail

* Fixed a display issue which occurred when inserting emojis into the content of your deliveries. 
* Fixed an issue which allowed the user to access sending logs when the delivery was still in edition.
* The **Scheduler** activity now allows you to send your deliveries depending on the recipient's time zone.
* SMS: The option **Store incoming MO** in the database has been added to external accounts. When checked, all incoming SMS will be stored into the **inSMS** table.
* SMS: Services are now attached to an event instead of a transactional template.
* SMS: The default SMTP connection timeout has been reduced to 30 seconds.

#### Push notifications

* Fixed an error that prevented push notification deliveries from being stopped.
* Added an option in push notification advanced options to wake up the application with a push notification.
* Added a pause button for the push notification preview video.
* The push notification preview is now available for different devices such as iPhone, Android, tablets.

  all channels

#### Reports

* Fixed an error which displayed rates over 100%.
* Fixed an issue that prevented users from downloading reports in CSV.
* Added a new **Report** item in the homepage.

#### Workflows

* Fixed an issue which led to an error message when using additional data in a query and adding aliases containing spaces. The non-alphanumeric characters are now replaced by "_".
* Fixed an issue where the technical workflow calculating KPIs could be stopped by default in some cases.

#### Profiles and audiences

* Fixed an error that occurred when adding multiple filters in an audience's query.
* Fixed a display issue that occurred when changing a profile's picture.
* Added a tooltip displaying the exact result number after counting the population of a query.
* Fixed an issue that could prevent a user from selecting an audience or closing the audience picker window.
* The list of available functions in the expression editor has been updated. The **FormatCurrency** and **ConvertCurrency** functions have been removed.

## v17.10 - October 2017 release

### New capabilities

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Fatigue Management<br /> </td> 
   <td> Fatigue Management allows you to create fatigue rules to manage over-communication with profiles. Fatigue rules are easily built, but are extremely flexible with capabilities such as counting messages across multiple channels (including transactional messages), only counting specific deliveries, or applying rules to specific profiles.<br /> For more information, refer to the <a href="../../administration/using/fatigue-rules.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Content creation: Import from a URL<br /> </td> 
   <td> Import from a URL enables you to quickly retrieve your creative content from a website to build emails for any delivery. Additionally, you can streamline your creative process by enabling third parties to share content directly through a URL. Imported content can be flexibly used as part of a single delivery or at the template level ensuring brand consistency for all related campaigns whether they be workflow-based or transactional messages, and include A/B or multivariate testing. Import from a URL automatically converts and tracks all links to monitor email performance through Dynamic Reporting.<br /> For more information, refer to the <a href="../../designing/using/importing-content-from-a-url.md">detailed documentation</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches

#### Platform

* Fixed an issue that could prevent large zipped files from being correctly unzipped.
* Security in brand management has been improved. Modifying a brand's name and sender address is now reserved for Adobe technical administrators.
* To improve security, user generated content (images, mirror pages, landing pages, etc.) cannot be served by the adobe.com domain anymore. It is now mandatory that you use your own domain to handle these resources, via the use of branding.
* Fixed an interface issue when displaying and filtering marketing activities.
* Fixed an issue which prevented subscription date fields from being updated with a POST Rest API call.

#### Emails, SMS messages and direct mail

* Fixed an issue that could prevent from targeting a list type audience in a message, causing the preparation to fail.
* Missing languages added in the multilingual email delivery capabilities.
* The content thumbnail, displayed on the delivery dashboard, is now automatically updated when the user modifies content and saves.
* Fixed a timezone related issue that prevented a delivery from being opened.

#### Push notifications

* When configuring the push notification channel, the push provider platform for iOS should be **apns** and for Android **gcm**.
* Fixed an error that prevented iOS mobile app from being added in the Adobe Campaign interface.
* Push notifications are now supported on both GCM and FCM-enabled Android mobile applications.
* Fixed an error that prevented content from being saved when duplicating a push notification template.
* It is now possible to create or update a profile from the Adobe Campaign database by reconciling mobile application users' data.
* Adobe Campaign now prioritizes processing the transactional push notifications over standard push notifications.

#### Reports

* Fixed an issue that prevented the hot click percentages from being displayed in the email content.
* Fixed an issue with the blacklist metric which was counted as a hard bounce instead of a bounce.
* Fixed an issue that led to negative counts being displayed in summary data.
* Fixed an issue that counted profiles in the wrong age segment.
* The soft and hard bounce calculation formulas have changed.

#### Workflows

* Fixed an issue in the **Load file** activity that could lead to errors after manually adding and removing columns in the activity.
* The **deliverabilityUpdate** technical workflow is now scheduled to run at 2am, server time.
* Fixed a security issue that allowed to perform a list export without the export role.
* Fixed an issue with the **Reconciliation** activity. 
* Fixed an issue with the use of wildcard characters in the **File Transfer** activity.

#### Profiles and audiences

* Fixed an issue that could prevent a condition of a query from being correctly taken into account in some specific cases, leading to erroneous results.
* Fixed an issue that could prevent profiles from being accessed if they were targeted in a message that was prepared but never sent and expired.

#### Integrations

* Fixed an issue that could prevent some Data Sources created for Triggers from correctly showing up and being selected.

#### Custom resources

* Fixed an issue that occurred in list screens where custom resource rows could be displayed without any data. 
* Fixed an issue that prevented boolean type fields with 'False' value from being displayed in custom resources.

## v17.9 - September 2017 release

### New capabilities

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Library of Email templates<br /> </td> 
   <td> Introducing eighteen brand-new, responsive templates designed in two beautiful themes - Astro and Feather. These customizable templates are industry agnostic, and ready to be used right away. Templates include content for a variety of use cases to get your email marketing campaigns designed and delivered more quickly, efficiently and more beautifully than ever before.<br /> For more information, refer to the <a href="../../start/using/about-templates.md#content-templates">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Dynamic Reporting with Profile Data<br /> </td> 
   <td> Dynamic Reporting provides fully customizable and real-time business reports. With this release, a powerful enhancement to Dynamic Reporting adds access to profile data, enabling demographic analysis by profile dimensions such as gender, city, zip code and age in addition to functional email campaign data like opens and clicks. With the same easy-to-use drag-and-drop interface, determining how your email campaign performed against your most important customer segments is easier than ever.<br /> For more information, refer to the <a href="../../reporting/using/about-dynamic-reports.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Mass Subscription with Origin &amp; Date<br /> </td> 
   <td> With this Mass Subscription enhancement, you are now able to store subscription information (origin and date) directly in the Adobe Campaign Standard database through the Subscription Services activity in a workflow.<br /> For more information, refer to the <a href="../../automating/using/subscription-services.md">detailed documentation</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches

#### Platform

* Some customers need to be able to leverage an ID coming from Adobe Campaign Standard as they don't manage a unique key to identify their own records. This ID (**ACS ID**) can be exported as well as used as a reconciliation key while updating the data. For more information, refer to the [detailed documentation](../../developing/using/generating-a-unique-id-for-profiles-and-custom-resources.md).
* The FTP protocol is being deprecated. You should now use SFTP instead. In order to not block existing implementations, existing configurations on FTP will still work as before but the option will not be showing for new activities.

#### Emails, SMS messages and direct mail

* It is now possible to create new alerting criteria to use them in delivery alerting notifications. For more information, refer to the [detailed documentation](../../sending/using/receiving-alerts-when-failures-happen.md#creating-a-delivery-alerting-criterion).
* The delivery alerting notifications have a new design and the delivery alerting dashboard user experience has been improved.
* Now when a routing external account is disabled, a warning is displayed in the impacted deliveries (email, SMS and push) and the **Preview** button is hidden in these deliveries.
* Fixed an issue that caused an error in the preview of an A/B test on the email content when dynamic text was enabled in the subject line.

#### Transactional messages

* It is now possible to define when you want to send a follow-up message, for example 3 days after a transactional message was sent. For more information, refer to the [detailed documentation](../../channels/using/follow-up-messages.md#sending-a-follow-up-message).
* It is now possible to define the date from when the transactional messages linked to an event should be sent.
* Fixed an issue that caused an SQL error when executing a workflow containing a follow-up message after deleting profiles linked to received and processed events.
* Fixed an error that prevented to delete a profile linked to an event.
* Fixed an issue that could prevent the redirection of tracked links from working.
* Fixed an issue which prevented you from disable tracking for certain links in an email or SMS message.

#### Reports

* The **Hot clicks** report has been improved. Also, it is now possible to display hot clicks according to each conditional content that was defined in a delivery and to display hot clicks for each execution of recurring deliveries or transactional messages. For more information, refer to the [detailed documentation](../../sending/using/receiving-alerts-when-failures-happen.md#creating-a-delivery-alerting-criterion).
* Fixed an issue which prevented the quarantine metric from retrieving correct data.
* A new preset time frame has been added to the calendar widget.
* The [dynamic report metrics](../../reporting/using/indicator-calculation.md) and the [campaigns' KPIs](../../sending/using/confirming-send.md) (displayed on the dashboard of sent messages) have been aligned for more coherence.
* Fixed an issue that could cause pipelined to crash on debian 7.

#### Workflows

* Fixed an issue that could prevent the imported file retention from working.

#### Integrations

* eVars and events are now supported for the Analytics & Campaign integration.
* When sending an email with the content of the abandoned cart, the payload parameter for elements removed from cart is now optional.

#### Profiles and audiences

* Adobe Campaign now provides a report that displays the number of active profiles. This report is only informative, it doesn't have a direct impact on billing. For more information, refer to the [detailed documentation](../../audiences/using/active-profiles.md).
* Fixed an issue that prevented profiles from being subscribed to a service when using the Profiles and Services API.

## v17.7 - July 2017 release

### New capabilities

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Multilingual email and SMS deliveries<br /> </td> 
   <td> Define and execute multilingual Email &amp; SMS deliveries through a single delivery based on your automatically segmented customers' preferred language. Report on the performance of every delivery down to the language and individual levels.<br /> More and more companies are faced with the challenge of delivering content in multiple languages as they grow at home and abroad. As such, streamlining localized message delivery is a key part of an effective customer communication strategy for multinational companies; companies in countries with multiple languages; and companies who want to further personalize their content at the lingual level no matter where customers reside. For more information, refer to the <a href="../../channels/using/creating-a-multilingual-email.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Adobe Campaign Notifications<br /> </td> 
   <td> Receive notifications regarding important system activities directly within Adobe Campaign Standard. You will be notified, for example, on the progress of your on-going deliveries or when a workflow is in error.<br /> Real-time notifications keep relevant stakeholders informed and provide users with the ability to immediately and directly act on activity notifications from within the application. The result for teams is advanced agility, efficiency and smoother execution of campaigns. For more information, refer to the <a href="../../administration/using/adobe-campaign-notifications.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Delivery Alerting<br /> </td> 
   <td> In addition to viewing notifications directly in Adobe Campaign Standard, Adobe Campaign now also provides an email alerting system to trigger email alerts to users or external stakeholders of important system activities. Create, manage, and receive customizable alerts and dashboards to keep track of delivery successes or failures.<br /> Adobe Campaign Delivery Alerting boosts efficiency by keeping all involved Adobe Campaign users in a company automatically informed about the delivery execution status, via email and dashboard. For more information, refer to the <a href="../../sending/using/receiving-alerts-when-failures-happen.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Encrypted Declared ID in Datasources<br /> </td> 
   <td> Send Email and SMS triggers without the need for an existing profile in Campaign by using encrypted contact information (email address or phone number) as a Declared ID. Because Encrypted Declared IDs can be decoded by Adobe Campaign Standard, Campaign can now create new marketable profiles when receiving audiences from other Experience Cloud solutions containing previously unknown contacts.<br /> Target customers and unknown prospects in real-time through both email &amp; SMS to improve loyalty in your existing customer base and acquire new customers respectively. Make the most of your first-party cookie data (from Adobe Audience Manager*) once prospects authenticate and leverage those insights in Adobe Campaign. <br /> *Adobe Audience Manager is required. For more information, refer to the <a href="../../integrating/using/about-campaign-audience-manager-or-people-core-service-integration.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> KPI sharing from Campaign to Analytics<br /> </td> 
   <td> Share campaign data with Adobe Analytics to measure email marketing metrics from Campaign alongside other marketing and advertising efforts through conversion, unifying pre- and post-click behavior.<br /> Track overall performance directly and uncover synergies with external programs in Analytics. Apply your learning from this consolidated view back into your campaigns; ultimately improving open, click-through and conversion rates boosting revenue and overall campaign performance. <br /> Adobe Analytics is required. For more information, refer to the <a href="../../integrating/using/about-campaign-analytics-integration.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Direct Mail Channel - Return To Sender<br /> </td> 
   <td> Flat file exchanges with Direct Mail providers incorporating Return to Sender information are now supported. This enhancement to the Direct Mail channel allows corresponding postal addresses to be excluded from future communications.<br /> This enables marketers to be notified of an incorrect address and engage with the customer through other channels or to encourage him to update his postal address. This also reduces the number of wasted marketing dollars as marketers avoid sending mail to incorrect addresses. <br /> Direct Mail is available as an add-on channel. For more information, refer to the <a href="../../channels/using/return-to-sender.md">detailed documentation</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches

#### General

* Fixed an issue which let any user export lists. Now only users with the **Export** role are allowed to.

#### Emails, SMS messages and direct mail

* Fixed an issue with the **updateDeliveryExecInfo** workflow that set the **To deliver** indicator to 0 for SMS deliveries.
* In the **Advanced parameters** of the delivery template’s properties, the **Routing** drop-down list now only displays external accounts corresponding to the template message type. For example, an email delivery template only displays email external accounts.
* Fixed an issue with the **Text** preferred email format defined for test profiles.
* Fixed an issue that led to a Javascript error in when selecting the default time zone in the schedule definition screen of a delivery.
* Fixed an issue which prevented traps from appearing in the sending logs.
* In the template selection screen of the delivery creation wizard, follow-up and A/B test templates are now hidden by default. For more information, refer to the [detailed documention](../../channels/using/creating-an-email.md).
* Fixed an issue which let any user send deliveries. Now only users with the **Start deliveries** role are allowed to. For more information, refer to the [detailed documention](../../sending/using/confirming-send.md).

#### Push notifications

* Fixed an issue with the **Campaign Tracking Endpoint** URL that prevented reporting.
* Fixed an issue that prevented the push notification title to be displayed on Android devices.
* Fixed an issue that prevented the push notification to be displayed on iOS devices when the push notification contained only a title (and nothing in the body of the message).
* Fixed an issue that forced media attachment URLs in a delivery to be tracked, which prevented videos and pictures from being embedded in the delivery. The tracking of URLs of the type mediaAttachmentURL is now deactivated by default for push notifications.

#### Reports

* Corrected an issue where values appeared different between charts and table.
* Corrected an issue that displayed push notification values as email values. 
* Fixed an issue that showed values as unknown when a delivery was created outside of a campaign. 
* Corrected an issue that showed SMS report data as mobile application data.

#### Workflows

* You can now filter workflow logs (period of time and text search). For more information, refer to the [detailed documention](../../automating/using/executing-a-workflow.md#monitoring).
* An option is now available in worflow deliveries to deactivate the confirmation before the send.
* Fixed an issue which prevented you from setting an outbound transition in the creation wizard of recurring delivery.
* Fixed an issue that occurred when using a workflow query activity based on a custom resource field with an enumeration that had a lot of values

## v17.5 - May 2017 release

### New capabilities

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Direct mail<br /> </td> 
   <td> Break through the digital barrier and connect to the physical world with Adobe Campaign Standard’s first offline channel, Direct Mail. This feature allows you to personalize and generate the file required by direct mail providers as part of your cross-channel campaigns. Leverage Direct Mail to re-engage customers or to enhance the customer experience with a compelling tactile touchpoint driving customers to your app, website or store.<br /> For more information, refer to the <a href="../../channels/using/about-direct-mail.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Email BCC<br /> </td> 
   <td> Email BCC enables the saving of unique email messages sent to individual recipients, thus allowing the brand to archive those messages. By adding a BCC email address to all emails, Adobe Campaign Standard customers can keep an exact copy of each email with this feature. This is a common legal requirement for the financial services industry and is helpful in assisting customer service centers in resolving conflicts in real time.<br /> For more information, refer to the <a href="../../administration/using/configuring-email-channel.md#email-bcc">detailed documentation</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches

#### Interface updates

* In the top bar, the **Timeline** link has been removed and replaced with a link to **Programs & Campaigns**.

#### Emails and SMS messages

* Fixed an issue which displayed the wrong color for the **Retry in progress** delivery status. The color was gray instead of blue.

#### Workflows

* Fixed an issue that occurred when changing the action to perform in a **Transfer file** activity.

#### Reports

* The **Spam** and **Spam rate** indicator calculations have been changed.
* The **Bounce** metrics have been improved for a more accurate result.

#### Push notifications

* Fixed an issue which prevented you from clicking on a push event in a profile's marketing history.
* The use of push notifications in workflows has been improved.

## v17.4 - April 2017 release

### New capabilities

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Enhanced Image edition capabilities with the Creative SDK<br /> </td> 
   <td> You now have access to a complete set of features powered by the Creative SDK to enhance your images directly in the content editor when editing emails or landing pages.<br /> This feature does not require the acquisition of additional Creative Cloud solutions.<br /> For more information, refer to the <a href="../../designing/using/modifying-images-with-the-adobe-creative-sdk.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Transactional push notifications<br /> </td> 
   <td> The Mobile application channel has been added to Adobe Campaign's transactional messaging capabilities. Three channels are now supported for transactional messages: email, SMS and push notifications.<br /> For more information, refer to the <a href="../../channels/using/transactional-push-notifications.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Recurring push notifications<br /> </td> 
   <td> You can now configure recurring push notifications in a workflow. You can use recurring push notifications in situations where your customers expect periodic updates like weekly reminders to check out new content or promotions.<br /> For more information, refer to the <a href="../../automating/using/mobile-app-delivery.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Amazon Simple Storage Service (S3) connector<br /> </td> 
   <td> The Amazon Simple Storage Service (S3) connector can now be used to import or export data to Adobe Campaign. It can be set up in a workflow activity. The configuration is done in an external account.<br /> For more information, refer to the <a href="../../administration/using/external-accounts.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Dreamweaver integration live<br /> </td> 
   <td> The integration between Adobe Campaign and Dreamweaver is now live. It now works with the official last released version of Dreamweaver (17.0.2).<br /> This requires the installation of Adobe Campaign Integration extension from here: <a href="http://adobe.ly/acdw_addon">http://adobe.ly/acdw_addon</a><br /> For more information, refer to this <a href="http://docs.campaign.adobe.com/doc/standard/en/Videos/ACS_Dreamweaver.mp4">video</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches

#### Platform

* Fixed a memory consumption issue.

#### Emails and SMS messages

* Fixed an issue where content could not be properly synchronized with the latest changes when previewing a message.
* Fixed an issue which prevented an MX or Domain email processing rule from being created or deleted.
* Fixed an issue that could prevent you from sending emails with multiple aliases.
* Fixed an issue that prevented trap delivery logs from appearing in the sending logs of the delivery.
* Fixed an issue that led to an error when displaying the tracked URLs of a delivery with no URL in its content.
* Fixed an issue that prevented an image's size attributes from being correctly applied in the sent message.

#### Transactional messages

* The rtEventHistoId field is no longer exposed as a personalization field in a transactional message template.

#### Landing pages

* We have optimized the **by email** filter used in landing pages to reconcile new subscribers with database profiles.
* Fixed an issue which displayed free text inputs instead of check boxes when using boolean fields in a form configuration.
* Fixed an issue that prevented landing page thumbnails from being generated.

#### Workflows

* Fixed a display error when editing an **End** or **External Signal** activity (on Safari only).
* Improved the error message displayed when editing a **Read Audience** activity containing an erroneous audience.
* Fixed an issue that could lead to an SQL error when executing a subscription activity.

#### Integrations

* Points of Interest data: fixed an error that occurred when counting location subscribers.

#### Audiences and queries

* Fixed an issue that prevented sum and average aggregates from being used on a collection in the query editor.
* Fixed an issue that could prevent the query editor from being reloaded after changing the filter’s resource.

#### Reports

* Fixed an issue that prevented Open rate metrics to be correctly calculated when selecting multiple rows in a table.
* Fixed an error that only showed metrics as integer values. Metrics can now be displayed with decimals.

#### Push notifications

* Fixed an issue where an error message was not displayed when creating an Android application linked to a mobile app that had failed being created on MCPNS.
* Fixed an issue that allowed a user to add sounds to a silent notification.

## v17.2 - March 2017 release

### New capabilities

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Dynamic reporting<br /> </td> 
   <td> Dynamic Reporting provides a new generation of fully customizable and real-time business reports. Based on visual dynamic pivot tables and graphics, this feature lets you drag and drop variables and dimensions to analyze the efficiency and effectiveness of your marketing campaigns. Dynamic reporting also enables you to create your own business reports from scratch and save them for later use.<br /> For more information, refer to the <a href="../../reporting/using/about-dynamic-reports.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Dreamweaver integration (Labs)<br /> </td> 
   <td> With the Adobe Campaign and Dreamweaver integration, you now have an integrated process for creating email campaigns with Adobe solutions.<br /> You can edit Adobe Campaign emails in Dreamweaver and have the content seamlessly synchronized between both solutions.<br /> For the initial release, the integration is available as a "Labs" feature and works only with Dreamweaver Pre Release Beta. If you want to activate it, please contact AC-DW-integration@adobe.com.<br /> For more information, refer to this <a href="http://docs.campaign.adobe.com/doc/standard/en/Videos/ACS_Dreamweaver.mp4">video</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Manual send time optimization<br /> </td> 
   <td> You can now manually define a custom sending time per recipient - at the delivery level or using a workflow. <br /> Two new options are available: <br /> <li> All recipients receive the message with their time zone taken into account. </li> <li> Each recipient receives the message at a computed date and time defined by a formula. </li> For more information, refer to the <a href="../../sending/using/optimizing-the-sending-time.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Push notifications New capabilities<br /> </td> 
   <td> The push notification channel has been enhanced with several new capabilities:<br /> <li> New authoring interface </li> <li> Silent notifications </li> <li> Interactive push </li> <li> Rich content support </li> <li> Payload size calculator </li> For more information, refer to the <a href="../../channels/using/about-push-notifications.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Workflows: new Signal activity<br /> </td> 
   <td> Trigger a workflow from another workflow using the new <strong>Signal</strong> activity.<br /> With the ability to start one workflow from another, you can now support more complex customer journeys. You can better monitor the customer journeys and react in case there are issues.<br /> Several workflow activities have been updated:<br /> <li> <strong>End</strong> activity: a new tab allows you to specify a workflow to trigger after this activity has been executed. </li> <li> <strong>Update data</strong> activity: use the new empty outbound transition to add an <strong>End</strong> activity that triggers another workflow. Empty outbound transitions do not carry any data and do not consume unnecessary space on the system </li> For more information, refer to the <a href="../../automating/using/external-signal.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Workflows: new Read audience activity<br /> </td> 
   <td> Start your targeting process with an existing audience that you can easily select and refine in one activity.<br /> For more information, refer to the <a href="../../automating/using/read-audience.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Points of Interest data<br /> </td> 
   <td> Points of Interest data integrates Adobe Campaign with Adobe Analytics for Mobile. A brand can collect data from users' mobile locations - called <strong>Points of Interest</strong> - when users open the brand's app. This enables the brand to leverage Adobe Campaign workflows in order to send personalized messages based on the users’ locations. This channel leverages the Mobile core service’s SDK.<br /> Please note that using this feature requires Analytics for Mobile, which is a paid solution.<br /> For more information, refer to the <a href="../../integrating/using/about-campaign-points-of-interest-data-integration.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> REST APIs<br /> </td> 
   <td> Resources linked at any level to the profiles or services resources are now available in the API.<br /> For more information, refer to the <a href="../../developing/using/step-5--update-the-database-structure.md#publishing-a-resource-with-api-extension">detailed documentation</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches

#### General

* It is now possible to add profile data when exporting delivery logs.

#### Emails and SMS messages

* Fixed an issue causing the **Request confirmation before sending messages** option to remain selected even after unchecking it and saving the delivery.
* Fixed an issue that could prevent unpublishing transactional emails.
* Fixed an issue where content could not be properly synchronized with the latest changes before previewing a delivery.

#### Landing pages

* Fixed an error that prevented a user from editing when clicking in the content of a landing page.

#### Workflows

* Fixed an issue that could prevent from reading the content of the reject transition of a **Load file** activity.
* Fixed an issue that prevented swapped columns to be properly taken into account when configuring a **Load file** activity.

## v17.1 - January 2017 release

### New capabilities

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Log export for external reporting<br /> </td> 
   <td> Export logs such as delivery and tracking logs to process them in your preferred reporting or BI tools. You can use simple workflows with incremental queries to automate regular exports of new logs.<br /> In addition to the log resources availability from the resource picker, enhancements were made to the <a href="../../automating/using/incremental-query.md">Incremental query</a> and <a href="../../automating/using/extract-file.md">Extract file</a> activities:<br /> <li> <strong>Incremental query</strong> now allows you to use a date field to retrieve new or updated data. Previously, all results from earlier executions were automatically excluded, even if they were updated since the last execution. </li> <li> <strong>Extract file</strong> can now export labels for enumeration values instead of IDs. </li> These activities are available to administrators with access to all geo and org units.<br /> For more information on exporting logs, refer to the <a href="../../automating/using/exporting-logs.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Marketing capabilities for transactional messages<br /> </td> 
   <td> Marketers can now send transactional messages based on customer marketing profiles. This allows them to:<br /> <li> Apply marketing typology rules such as <strong>Blacklisted address</strong>. </li> <li> Include the unsubscription link within the messages. </li> <li> Add the transactional messages to the global delivery reporting. </li> <li> Leverage the transactional messages in the customer journey. </li> For more information, refer to the <a href="../../channels/using/profile-transactional-messages.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Transactional Messaging API<br /> </td> 
   <td> The Transactional Messaging API is now available through <a href="https://docs.campaign.adobe.com/doc/standard/en/adobeio.html">adobe.io</a>, making it easier to use and to monitor:<br /> <li> You can benefit from the adobe.io platform reporting and monitoring capabilites. </li> <li> Authentication is now carried out using the adobe.io token based authentication instead of IP whitelisting, making the security process simpler. </li> <li> All APIs are now integrated on a single platform, making it simpler than ever to add transactional messaging capabilities to your integration if you already support the Profile and Services API. </li> </td> 
  </tr> 
 </tbody> 
</table>

### Patches

#### General

* The **Access authorization** options have returned to the landing page properties.
* Fixed an issue that may have caused an old image to be rendered instead of the correct image. This occurred if the source image had been updated in the content definition of a delivery or landing page.
* Fixed an issue that prevented users from editing certain fields in an existing SFTP external account.
* Fixed several UI issues. For example, users can now edit profile attributes and save modifications without experiencing problems with the UI.

#### Emails and SMS messages

* Fixed an issue pertaining to delivery templates with HTML content that contains a

#### Push notifications

* Fixed an issue that may have prevented postback from an application to the Adobe Campaign server.
* Fixed an issue that may have prevented **Play a sound** and **Custom fields** to be taken into account for Android.
* Fixed an issue that may have caused an extra escaping character to be added to Unicode characters used for Emojis.
* When a subscriber's registration token becomes blacklisted, the corresponding status is now immediately updated in the application's list of subscribers in Adobe Campaign.

#### Workflows

* Fixed an issue that may have prevented previews of queries on event resources (e.g. rtEvent).
* The reject file generated by a **Load file** activity can now be retrieved in its outbound transition and processed in the next activity. For example, upload the reject file via an SFTP server using **Transfer file**.
* Fixed an issue that may have prevented a user from limiting the population of a segment if **Temporary resource** was selected in the **General** tab of **Segmentation**.
* **Scheduler** activities can no longer be set to trigger a workflow more than once every 10 minutes.
* Fixed an issue that may have prevented **Use common columns** from working properly in an **Union** activity.

#### Integrations

* Fixed an issue that may have caused an error when deploying an event trigger in Adobe Campaign. This error occurred when the "Likelihood to Return in 30 Days" metadata had been added to the Abandonment trigger in Adobe Marketing Cloud.
* Fixed an issue that may have caused the technical workflow to clear the Target Dimension field when importing audiences from People core service. Subsequent queries could not retrieve the imported audiences.
* Fixed an issue that may have caused the **Save audience** activity of a workflow to fail when the option **Share in Adobe Marketing Cloud** was checked.
