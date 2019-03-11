---
title: Release Notes 2017
seo-title: Release Notes 2017
description: Release Notes 2017
seo-description: This page lists all 2017 releases of Adobe Campaign Standard.
uuid: 682d94ee-94db-4ad4-b744-ed033c942eb1
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: rn
content-type: reference
topic-tags: campaign-standard-releases
discoiquuid: 110d3a9f-ef2b-4d48-81d7-ae7664aa36bd
index: y
internal: n
snippet: y
---

# Release Notes 2017{#release-notes}

Release Notes 2017

Looking for a specific 2017 release of Adobe Campaign Standard?

Each release comes with new features and patches. Click on a release to view its content.

View the latest [documentation updates](../../rn/using/documentation-updates.md) for Adobe Campaign Standard. If you're looking for a newer release, consult this [page](../../rn/using/release-notes.md).

## Release 17.10 - October 2017 {#release-17-10---october-2017}

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
   <td> Fatigue Management<br /> </td> 
   <td> Fatigue Management allows you to create fatigue rules to manage over-communication with profiles. Fatigue rules are easily built, but are extremely flexible with capabilities such as counting messages across multiple channels (including transactional messages), only counting specific deliveries, or applying rules to specific profiles.<br /> For more information, refer to the <a href="../../administration/using/fatigue-rules.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Content creation: Import from a URL<br /> </td> 
   <td> Import from a URL enables you to quickly retrieve your creative content from a website to build emails for any delivery. Additionally, you can streamline your creative process by enabling third parties to share content directly through a URL. Imported content can be flexibly used as part of a single delivery or at the template level ensuring brand consistency for all related campaigns whether they be workflow-based or transactional messages, and include A/B or multivariate testing. Import from a URL automatically converts and tracks all links to monitor email performance through Dynamic Reporting.<br /> For more information, refer to the <a href="../../designing/using/importing-content-from-a-url.md">detailed documentation</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches {#patches}

#### Platform {#platform}

* Fixed an issue that could prevent large zipped files from being correctly unzipped.
* Security in brand management has been improved. Modifying a brand's name and sender address is now reserved for Adobe technical administrators.
* To improve security, user generated content (images, mirror pages, landing pages, etc.) cannot be served by the adobe.com domain anymore. It is now mandatory that you use your own domain to handle these resources, via the use of branding.
* Fixed an interface issue when displaying and filtering marketing activities.
* Fixed an issue which prevented subscription date fields from being updated with a POST Rest API call.

#### Emails, SMS messages and direct mail {#emails--sms-messages-and-direct-mail}

* Fixed an issue that could prevent from targeting a list type audience in a message, causing the preparation to fail.
* Missing languages added in the multilingual email delivery capabilities.
* The content thumbnail, displayed on the delivery dashboard, is now automatically updated when the user modifies content and saves.
* Fixed a timezone related issue that prevented a delivery from being opened.

#### Push notifications {#push-notifications}

* When configuring the push notification channel, the push provider platform for iOS should be **apns** and for Android **gcm**.
* Fixed an error that prevented iOS mobile app from being added in the Adobe Campaign interface.
* Push notifications are now supported on both GCM and FCM-enabled Android mobile applications.
* Fixed an error that prevented content from being saved when duplicating a push notification template.
* It is now possible to create or update a profile from the Adobe Campaign database by reconciling mobile application users' data.
* Adobe Campaign now prioritizes processing the transactional push notifications over standard push notifications.

#### Reports {#reports}

* Fixed an issue that prevented the hot click percentages from being displayed in the email content.
* Fixed an issue with the blacklist metric which was counted as a hard bounce instead of a bounce.
* Fixed an issue that led to negative counts being displayed in summary data.
* Fixed an issue that counted profiles in the wrong age segment.
* The soft and hard bounce calculation formulas have changed.

#### Workflows {#workflows}

* Fixed an issue in the **[!UICONTROL Load file]** activity that could lead to errors after manually adding and removing columns in the activity.
* The **[!UICONTROL deliverabilityUpdate]** technical workflow is now scheduled to run at 2am, server time.
* Fixed a security issue that allowed to perform a list export without the export role.
* Fixed an issue with the **[!UICONTROL Reconciliation]** activity. 
* Fixed an issue with the use of wildcard characters in the **[!UICONTROL File Transfer]** activity.

#### Profiles and audiences {#profiles-and-audiences}

* Fixed an issue that could prevent a condition of a query from being correctly taken into account in some specific cases, leading to erroneous results.
* Fixed an issue that could prevent profiles from being accessed if they were targeted in a message that was prepared but never sent and expired.

#### Integrations {#integrations}

* Fixed an issue that could prevent some Data Sources created for Triggers from correctly showing up and being selected.

#### Custom resources {#custom-resources}

* Fixed an issue that occurred in list screens where custom resource rows could be displayed without any data. 
* Fixed an issue that prevented boolean type fields with 'False' value from being displayed in custom resources.

## Release 17.9 - September 2017 {#release-17-9---september-2017}

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

### Patches {#patches-1}

#### Platform {#platform-1}

* Some customers need to be able to leverage an ID coming from Adobe Campaign Standard as they don't manage a unique key to identify their own records. This ID (**ACS ID**) can be exported as well as used as a reconciliation key while updating the data. For more information, refer to the [detailed documentation](../../developing/using/configuring-the-resource-s-data-structure.md#generating-a-unique-id-for-profiles-and-custom-resources).
* The FTP protocol is being deprecated. You should now use SFTP instead. In order to not block existing implementations, existing configurations on FTP will still work as before but the option will not be showing for new activities.

#### Emails, SMS messages and direct mail {#emails--sms-messages-and-direct-mail-1}

* It is now possible to create new alerting criteria to use them in delivery alerting notifications. For more information, refer to the [detailed documentation](../../sending/using/receiving-alerts-when-failures-happen.md#creating-a-delivery-alerting-criterion).
* The delivery alerting notifications have a new design and the delivery alerting dashboard user experience has been improved.
* Now when a routing external account is disabled, a warning is displayed in the impacted deliveries (email, SMS and push) and the **Preview** button is hidden in these deliveries.
* Fixed an issue that caused an error in the preview of an A/B test on the email content when dynamic text was enabled in the subject line.

#### Transactional messages {#transactional-messages}

* It is now possible to define when you want to send a follow-up message, for example 3 days after a transactional message was sent. For more information, refer to the [detailed documentation](../../channels/using/follow-up-messages.md#sending-a-follow-up-message).
* It is now possible to define the date from when the transactional messages linked to an event should be sent.
* Fixed an issue that caused an SQL error when executing a workflow containing a follow-up message after deleting profiles linked to received and processed events.
* Fixed an error that prevented to delete a profile linked to an event.
* Fixed an issue that could prevent the redirection of tracked links from working.
* Fixed an issue which prevented you from disable tracking for certain links in an email or SMS message.

#### Reports {#reports-1}

* The **Hot clicks** report has been improved. Also, it is now possible to display hot clicks according to each conditional content that was defined in a delivery and to display hot clicks for each execution of recurring deliveries or transactional messages. For more information, refer to the [detailed documentation](../../sending/using/receiving-alerts-when-failures-happen.md#creating-a-delivery-alerting-criterion).
* Fixed an issue which prevented the quarantine metric from retrieving correct data.
* A new preset time frame has been added to the calendar widget.
* The [dynamic report metrics](../../reporting/using/indicator-calculation.md) and the [campaigns' KPIs](../../sending/using/confirming-the-send.md) (displayed on the dashboard of sent messages) have been aligned for more coherence.
* Fixed an issue that could cause pipelined to crash on debian 7.

#### Workflows {#workflows-1}

* Fixed an issue that could prevent the imported file retention from working.

#### Integrations {#integrations-1}

* eVars and events are now supported for the Analytics & Campaign integration.
* When sending an email with the content of the abandoned cart, the payload parameter for elements removed from cart is now optional.

#### Profiles and audiences {#profiles-and-audiences-1}

* Adobe Campaign now provides a report that displays the number of active profiles. This report is only informative, it doesn't have a direct impact on billing. For more information, refer to the [detailed documentation](../../audiences/using/active-profiles.md).
* Fixed an issue that prevented profiles from being subscribed to a service when using the Profiles and Services API.

## Release 17.7 - July 2017 {#release-17-7---july-2017}

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
   <td> Multilingual email and SMS deliveries<br /> </td> 
   <td> Define and execute multilingual Email &amp; SMS deliveries through a single delivery based on your automatically segmented customers' preferred language. Report on the performance of every delivery down to the language and individual levels.<br /> More and more companies are faced with the challenge of delivering content in multiple languages as they grow at home and abroad. As such, streamlining localized message delivery is a key part of an effective customer communication strategy for multinational companies; companies in countries with multiple languages; and companies who want to further personalize their content at the lingual level no matter where customers reside. For more information, refer to the <a href="../../channels/using/creating-a-multilingual-email.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Adobe Campaign Notifications<br /> </td> 
   <td> Receive notifications regarding important system activities directly within Adobe Campaign Standard. You will be notified, for example, on the progress of your on-going deliveries or when a workflow is in error.<br /> Real-time notifications keep relevant stakeholders informed and provide users with the ability to immediately and directly act on activity notifications from within the application. The result for teams is advanced agility, efficiency and smoother execution of campaigns. For more information, refer to the <a href="../../administration/using/sending-internal-notifications.md">detailed documentation</a>.<br /> </td> 
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

### Patches {#patches-2}

#### General {#general}

* Fixed an issue which let any user export lists. Now only users with the **[!UICONTROL Export]** role are allowed to.

#### Emails, SMS messages and direct mail {#emails--sms-messages-and-direct-mail-2}

* Fixed an issue with the **updateDeliveryExecInfo** workflow that set the **To deliver** indicator to 0 for SMS deliveries.
* In the **Advanced parameters** of the delivery template’s properties, the **Routing** drop-down list now only displays external accounts corresponding to the template message type. For example, an email delivery template only displays email external accounts.
* Fixed an issue with the **[!UICONTROL Text]** preferred email format defined for test profiles.
* Fixed an issue that led to a Javascript error in when selecting the default time zone in the schedule definition screen of a delivery.
* Fixed an issue which prevented traps from appearing in the sending logs.
* In the template selection screen of the delivery creation wizard, follow-up and A/B test templates are now hidden by default. For more information, refer to the [detailed documention](../../channels/using/creating-an-email.md).
* Fixed an issue which let any user send deliveries. Now only users with the **[!UICONTROL Start deliveries]** role are allowed to. For more information, refer to the [detailed documention](../../sending/using/confirming-the-send.md).

#### Push notifications {#push-notifications-1}

* Fixed an issue with the **Campaign Tracking Endpoint** URL that prevented reporting.
* Fixed an issue that prevented the push notification title to be displayed on Android devices.
* Fixed an issue that prevented the push notification to be displayed on iOS devices when the push notification contained only a title (and nothing in the body of the message).
* Fixed an issue that forced media attachment URLs in a delivery to be tracked, which prevented videos and pictures from being embedded in the delivery. The tracking of URLs of the type mediaAttachmentURL is now deactivated by default for push notifications.

#### Reports {#reports-2}

* Corrected an issue where values appeared different between charts and table.
* Corrected an issue that displayed push notification values as email values. 
* Fixed an issue that showed values as unknown when a delivery was created outside of a campaign. 
* Corrected an issue that showed SMS report data as mobile application data.

#### Workflows {#workflows-2}

* You can now filter workflow logs (period of time and text search). For more information, refer to the [detailed documention](../../automating/using/executing-a-workflow.md#monitoring).
* An option is now available in workflow deliveries to deactivate the confirmation before the send.
* Fixed an issue which prevented you from setting an outbound transition in the creation wizard of recurring delivery.
* Fixed an issue that occurred when using a workflow query activity based on a custom resource field with an enumeration that had a lot of values

## Release 17.5 - May 2017 {#release-17-5---may-2017}

### New capabilities {#new-capabilities-3}

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

### Patches {#patches-3}

#### Interface updates {#interface-updates}

* In the top bar, the **[!UICONTROL Timeline]** link has been removed and replaced with a link to **[!UICONTROL Programs & Campaigns]** .

#### Emails and SMS messages {#emails-and-sms-messages}

* Fixed an issue which displayed the wrong color for the **[!UICONTROL Retry in progress]** delivery status. The color was gray instead of blue.

#### Workflows {#workflows-3}

* Fixed an issue that occurred when changing the action to perform in a **[!UICONTROL Transfer file]** activity.

#### Reports {#reports-3}

* The **[!UICONTROL Spam]** and **[!UICONTROL Spam rate]** indicator calculations have been changed.
* The **[!UICONTROL Bounce]** metrics have been improved for a more accurate result.

#### Push notifications {#push-notifications-2}

* Fixed an issue which prevented you from clicking on a push event in a profile's marketing history.
* The use of push notifications in workflows has been improved.

## Release 17.4 - April 2017 {#release-17-4---april-2017}

### New capabilities {#new-capabilities-4}

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
   <td> You can now configure recurring push notifications in a workflow. You can use recurring push notifications in situations where your customers expect periodic updates like weekly reminders to check out new content or promotions.<br /> For more information, refer to the <a href="../../automating/using/push-notification-delivery.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Amazon Simple Storage Service (S3) connector<br /> </td> 
   <td> The Amazon Simple Storage Service (S3) connector can now be used to import or export data to Adobe Campaign. It can be set up in a workflow activity. The configuration is done in an external account.<br /> For more information, refer to the <a href="../../administration/using/external-accounts.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Dreamweaver integration live<br /> </td> 
   <td> The integration between Adobe Campaign and Dreamweaver is now live. It now works with the official last released version of Dreamweaver (17.0.2).<br /> This requires the installation of Adobe Campaign Integration extension from here: <a href="http://adobe.ly/acdw_addon">http://adobe.ly/acdw_addon</a><br /> For more information, refer to this <a href="https://helpx.adobe.com/campaign/kt/acs/using/acs-dreamweaver-integration-feature-video-use.html">video</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches {#patches-4}

#### Platform {#platform-2}

* Fixed a memory consumption issue.

#### Emails and SMS messages {#emails-and-sms-messages-1}

* Fixed an issue where content could not be properly synchronized with the latest changes when previewing a message.
* Fixed an issue which prevented an MX or Domain email processing rule from being created or deleted.
* Fixed an issue that could prevent you from sending emails with multiple aliases.
* Fixed an issue that prevented trap delivery logs from appearing in the sending logs of the delivery.
* Fixed an issue that led to an error when displaying the tracked URLs of a delivery with no URL in its content.
* Fixed an issue that prevented an image's size attributes from being correctly applied in the sent message.

#### Transactional messages {#transactional-messages-1}

* The rtEventHistoId field is no longer exposed as a personalization field in a transactional message template.

#### Landing pages {#landing-pages}

* We have optimized the **[!UICONTROL by email]** filter used in landing pages to reconcile new subscribers with database profiles.
* Fixed an issue which displayed free text inputs instead of check boxes when using boolean fields in a form configuration.
* Fixed an issue that prevented landing page thumbnails from being generated.

#### Workflows {#workflows-4}

* Fixed a display error when editing an **[!UICONTROL End]** or **[!UICONTROL External Signal]** activity (on Safari only).
* Improved the error message displayed when editing a **[!UICONTROL Read Audience]** activity containing an erroneous audience.
* Fixed an issue that could lead to an SQL error when executing a subscription activity.

#### Integrations {#integrations-2}

* Points of Interest data: fixed an error that occurred when counting location subscribers.

#### Audiences and queries {#audiences-and-queries}

* Fixed an issue that prevented sum and average aggregates from being used on a collection in the query editor.
* Fixed an issue that could prevent the query editor from being reloaded after changing the filter’s resource.

#### Reports {#reports-4}

* Fixed an issue that prevented Open rate metrics to be correctly calculated when selecting multiple rows in a table.
* Fixed an error that only showed metrics as integer values. Metrics can now be displayed with decimals.

#### Push notifications {#push-notifications-3}

* Fixed an issue where an error message was not displayed when creating an Android application linked to a mobile app that had failed being created on MCPNS.
* Fixed an issue that allowed a user to add sounds to a silent notification.

## Release 17.2 - March 2017 {#release-17-2---march-2017}

### New capabilities {#new-capabilities-5}

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
   <td> With the Adobe Campaign and Dreamweaver integration, you now have an integrated process for creating email campaigns with Adobe solutions.<br /> You can edit Adobe Campaign emails in Dreamweaver and have the content seamlessly synchronized between both solutions.<br /> For the initial release, the integration is available as a "Labs" feature and works only with Dreamweaver Pre Release Beta. If you want to activate it, please contact AC-DW-integration@adobe.com.<br /> For more information, refer to this <a href="https://helpx.adobe.com/campaign/kt/acs/using/acs-dreamweaver-integration-feature-video-use.html">video</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Manual send time optimization<br /> </td> 
   <td> You can now manually define a custom sending time per recipient - at the delivery level or using a workflow. <br /> Two new options are available: <br /> <ul><li> All recipients receive the message with their time zone taken into account. </li> <li> Each recipient receives the message at a computed date and time defined by a formula. </li></ul> For more information, refer to the <a href="../../sending/using/optimizing-the-sending-time.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Push notifications New capabilities<br /> </td> 
   <td> The push notification channel has been enhanced with several new capabilities:<br /> <ul><li> New authoring interface </li> <li> Silent notifications </li> <li> Interactive push </li> <li> Rich content support </li> <li> Payload size calculator </li></ul> For more information, refer to the <a href="../../channels/using/about-push-notifications.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Workflows: new Signal activity<br /> </td> 
   <td> Trigger a workflow from another workflow using the new <span class="uicontrol">Signal</span> activity.<br /> With the ability to start one workflow from another, you can now support more complex customer journeys. You can better monitor the customer journeys and react in case there are issues.<br /> Several workflow activities have been updated:<br /><ul> <li> <span class="uicontrol">End</span> activity: a new tab allows you to specify a workflow to trigger after this activity has been executed. </li> <li> <span class="uicontrol">Update data</span> activity: use the new empty outbound transition to add an <strong>End</strong> activity that triggers another workflow. Empty outbound transitions do not carry any data and do not consume unnecessary space on the system </li></ul> For more information, refer to the <a href="../../automating/using/external-signal.md">detailed documentation</a>.<br /> </td> 
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
   <td> Resources linked at any level to the profiles or services resources are now available in the API.<br /> For more information, refer to the <a href="../../developing/using/updating-the-database-structure.md#publishing-a-resource-with-api-extension">detailed documentation</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches {#patches-5}

#### General {#general-1}

* It is now possible to add profile data when exporting delivery logs.

#### Emails and SMS messages {#emails-and-sms-messages-2}

* Fixed an issue causing the **[!UICONTROL Request confirmation before sending messages]** option to remain selected even after unchecking it and saving the delivery.
* Fixed an issue that could prevent unpublishing transactional emails.
* Fixed an issue where content could not be properly synchronized with the latest changes before previewing a delivery.

#### Landing pages {#landing-pages-1}

* Fixed an error that prevented a user from editing when clicking in the content of a landing page.

#### Workflows {#workflows-5}

* Fixed an issue that could prevent from reading the content of the reject transition of a **[!UICONTROL Load file]** activity.
* Fixed an issue that prevented swapped columns to be properly taken into account when configuring a **[!UICONTROL Load file]** activity.

## Release 17.1 - January 2017 {#release-17-1---january-2017}

### New capabilities {#new-capabilities-6}

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
   <td> Export logs such as delivery and tracking logs to process them in your preferred reporting or BI tools. You can use simple workflows with incremental queries to automate regular exports of new logs.<br /> In addition to the log resources availability from the resource picker, enhancements were made to the <a href="../../automating/using/incremental-query.md">Incremental query</a> and <a href="../../automating/using/extract-file.md">Extract file</a> activities:<br /> <ul><li> <span class="uicontrol">Incremental query</span> now allows you to use a date field to retrieve new or updated data. Previously, all results from earlier executions were automatically excluded, even if they were updated since the last execution. </li> <li> <span class="uicontrol">Extract file</span> can now export labels for enumeration values instead of IDs. </li></ul> These activities are available to administrators with access to all geo and org units.<br /> For more information on exporting logs, refer to the <a href="../../automating/using/exporting-logs.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Marketing capabilities for transactional messages<br /> </td> 
   <td> Marketers can now send transactional messages based on customer marketing profiles. This allows them to:<br /> <ul><li> Apply marketing typology rules such as <span class="uicontrol">Blacklisted address</span> . </li> <li> Include the unsubscription link within the messages. </li> <li> Add the transactional messages to the global delivery reporting. </li> <li> Leverage the transactional messages in the customer journey. </li></ul> For more information, refer to the <a href="../../channels/using/profile-transactional-messages.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Transactional Messaging API<br /> </td> 
   <td> The Transactional Messaging API is now available through <a href="https://docs.campaign.adobe.com/doc/standard/en/adobeio.html">adobe.io</a>, making it easier to use and to monitor:<br /> <li> You can benefit from the adobe.io platform reporting and monitoring capabilites. </li> <li> Authentication is now carried out using the adobe.io token based authentication instead of IP whitelisting, making the security process simpler. </li> <li> All APIs are now integrated on a single platform, making it simpler than ever to add transactional messaging capabilities to your integration if you already support the Profile and Services API. </li></ul> </td> 
  </tr> 
 </tbody> 
</table>

### Patches {#patches-6}

#### General {#general-2}

* The **[!UICONTROL Access authorization]** options have returned to the landing page properties.
* Fixed an issue that may have caused an old image to be rendered instead of the correct image. This occurred if the source image had been updated in the content definition of a delivery or landing page.
* Fixed an issue that prevented users from editing certain fields in an existing SFTP external account.
* Fixed several UI issues. For example, users can now edit profile attributes and save modifications without experiencing problems with the UI.

#### Emails and SMS messages {#emails-and-sms-messages-3}

* Fixed an issue pertaining to delivery templates with HTML content that contains a

#### Push notifications {#push-notifications-4}

* Fixed an issue that may have prevented postback from an application to the Adobe Campaign server.
* Fixed an issue that may have prevented **[!UICONTROL Play a sound]** and **[!UICONTROL Custom fields]** to be taken into account for Android.
* Fixed an issue that may have caused an extra escaping character to be added to Unicode characters used for Emojis.
* When a subscriber's registration token becomes blacklisted, the corresponding status is now immediately updated in the application's list of subscribers in Adobe Campaign.

#### Workflows {#workflows-6}

* Fixed an issue that may have prevented previews of queries on event resources (e.g. rtEvent).
* The reject file generated by a **[!UICONTROL Load file]** activity can now be retrieved in its outbound transition and processed in the next activity. For example, upload the reject file via an SFTP server using **[!UICONTROL Transfer file]** .
* Fixed an issue that may have prevented a user from limiting the population of a segment if **[!UICONTROL Temporary resource]** was selected in the **[!UICONTROL General]** tab of **[!UICONTROL Segmentation]** .
* **[!UICONTROL Scheduler]** activities can no longer be set to trigger a workflow more than once every 10 minutes.
* Fixed an issue that may have prevented **[!UICONTROL Use common columns]** from working properly in an **[!UICONTROL Union]** activity.

#### Integrations {#integrations-3}

* Fixed an issue that may have caused an error when deploying an event trigger in Adobe Campaign. This error occurred when the "Likelihood to Return in 30 Days" metadata had been added to the Abandonment trigger in Adobe Marketing Cloud.
* Fixed an issue that may have caused the technical workflow to clear the Target Dimension field when importing audiences from People core service. Subsequent queries could not retrieve the imported audiences.
* Fixed an issue that may have caused the **[!UICONTROL Save audience]** activity of a workflow to fail when the option **[!UICONTROL Share in Adobe Marketing Cloud]** was checked.

