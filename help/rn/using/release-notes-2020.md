---
title: Release Notes 2020
description: This page lists all 2020 releases of Adobe Campaign Standard.
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

# Release Notes 2020{#release-notes-2020}

[Release Planning](https://helpx.adobe.com/campaign/kb/acs-release-planning.html) &#124; [Control Panel releases](https://docs.adobe.com/content/help/en/control-panel/using/release-notes.html) &#124; [Documentation Updates](../../rn/using/documentation-updates.md) &#124; [Previous Release Notes](../../rn/using/release-notes-2019.md) &#124; [Deprecated Features](https://helpx.adobe.com/campaign/kb/acs-deprecated-and-removed-features.html)

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
    <p>For more information, refer to the <a href="../../sending/using/testing-messages-using-target.md">detailed documentation</a> and the <a href="https://docs.adobe.com/content/help/en/campaign-standard-learn/tutorials/communication-channels/email/profile-substitution.html">tutorial video</a>. </p>
   </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>New capabilities will be released in Campaign Control Panel in April, including Google TXT record management, Database space monitoring and email alerting. For more on these features, refer to the [Control Panel Release Note](https://docs.adobe.com/content/help/en/control-panel/using/release-notes.html).

**Improvements**

* Transactional messaging user experience has been enhanced and the interface consistency was improved. [Read more](../../channels/using/about-transactional-messaging.md)
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
>Adobe Experience Platform features in Campaign Standard are currently in beta, which may be subject to frequent updates without notice. Refer to the detailed documentation: [Experience Platform Data Connector](../../administration/using/aep-about-data-connector.md), [Audience Destinations](../../audiences/using/aep-about-audience-destinations-service.md)

* In workflow logs, every 10 minutes, Campaign now displays the number of records already processed by the job that is currently running.
* Fixed an issue that could occur when importing an Adobe Experience Platform profile that had been deleted from the database.
* Fixed an issue in workflow logs, that could display an incorrect result for the total number of imported records.

**Patches**

* Fixed an issue with the **Enrichment** workflow activity that could occur when adding spaces in the **Alias** field which then created a new row item. (CAMP-39229)
* Fixed an issue where every test profile could be targeted when sending a proof message.
* Fixed an issue that occurred after unpublishing and deleting an event configuration. [Read more](../../administration/using/configuring-transactional-messaging.md#deleting-an-event)
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
    <p>Please note this capability is only available to customers hosted on Azure. For more information about this capability and conditions to activate it, refer to the <a href="../../developing/using/aep-about-data-connector.md">detailed documentation</a> and the <a href="https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/adobe-experience-platform-data-connector/understanding-the-adobe-experience-platform-data-connector.html">how-to video</a>.</p>
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
    <p>Please note this capability is only available to customers hosted on Azure. For more information about this capability and conditions to activate it, refer to the <a href="../../audiences/using/aep-about-audience-destinations-service.md">detailed documentation</a> and the <a href="https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/profiles-and-audiences/audience-destinations/audience-destinations-overview.html">how-to video</a>. </p>
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
* Adobe Creative SDK has been decommissioned. It is now deprecated in Campaign Standard. See the [Deprecated and removed features](https://helpx.adobe.com/campaign/kb/acs-deprecated-and-removed-features.html) page.


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
* Fixed an issue that prevented In-app messages from being sent when adding a test profile to the delivery.
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
