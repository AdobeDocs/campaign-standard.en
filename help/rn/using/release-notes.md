---
title: Latest Release
description: This page lists all recent releases of Adobe Campaign Standard.
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

# Latest Release{#latest-release}

[Release Planning](https://helpx.adobe.com/campaign/kb/acs-release-planning.html) &#124; [Control Panel releases](https://docs.adobe.com/content/help/en/control-panel/using/release-notes.html) &#124; [Documentation Updates](../../rn/using/documentation-updates.md) &#124; [Previous Release Notes](../../rn/using/release-notes-2019.md) &#124; [Deprecated Features](https://helpx.adobe.com/campaign/kb/acs-deprecated-and-removed-features.html)

## Release 20.1 - February 2020 {#release-20-1---february-2020}

**What's new?**


<table> 
 <thead> 
  <tr> 
   <th> <strong>Adobe Experience Platform Data Connector</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>
   The Adobe Experience Platform Data Connector is now integrated with Adobe Campaign Standard. You can make your Campaign data available on Adobe Experience Platform by mapping XTK data (data ingested in Campaign) to Adobe Experience Platform Data Model (XDM). </p>
    <p>For more information about this capability and conditions to activate it, refer to the <a href="../../administration/using/aep-about-data-connector.md">detailed documentation</a>.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

<table> 
 <thead> 
  <tr> 
   <th> <strong>Integration with Audience Destination service’ </strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>The Audience Destinations service is now integrated with Adobe Campaign Standard. You can build highly targeted audiences based on large, complex datasets and share these segments near real-time with other Adobe Experience Cloud solutions.</p>
    <p>For more information about this capability and conditions to activate it, refer to the <a href="../../audiences/using/aep-about-audience-destinations-service.md">detailed documentation</a>.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

<table> 
 <thead> 
  <tr> 
   <th> <strong>Campaign Enhanced MTA for transactional messaging</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>Transactional messages are now sent by the Adobe Campaign Enhanced MTA, which provides an upgraded sending infrastructure allowing for improved deliverability, throughput, and bounce handling.</p>
    <p>For more information, refer to the <a href="https://helpx.adobe.com/campaign/kb/campaign-enhanced-mta.html">detailed documentation</a>.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

**Improvements**

* Timezone management has been enhanced. You can now define a [specific timezone](../../automating/using/building-a-workflow.md) for an entire workflow. The selected timezone will apply to all the workflow's activities. Information about the timezone that has been configured for the operator or the server is now displayed in the interface (in logs, and after selecting a timezone). (CAMP-37672)

* Campaign Standard APIs now allow you to perform pagination when using large tables, by adding the `_forcePagination=true parameter` to your call URL. [Read more](../../api/using/pagination.md)

* The Delivery log ID (which is a unique identifier for each log) is now available in the Delivery logs and Tracking logs resources for all targeting dimensions. This enables to identify sending or tracking logs when exporting, for example.

**Email Designer enhancements**

* Fixed an issue which led to accessibility problems when resizing text in a container element.
* Added missing mandatory text instruction when creating an Audience.
* Fixed an issue which prevented users from dismissing the auto Calendar pop-up that appears on hover in marketing activities.
* Fixed an issue when clicking on the **Change content** button in the wizard of the legacy email editor.
* Fixed an issue which prevented headers from being aligned with the content on the Service Summary report. (CAMP-38103)
* Fixed an issue which prevented dynamic content variants from being deleted without affecting the rest of the subject line. (CAMP-40096)
* Fixed an A/B testing issue when using the B variant on the subject line. (CAMP-40327)
* Fixed an issue which prevented you from dragging and dropping files when using the Upload HTML import feature. (CAMP-39326)
* Fixed an issue which prevented you from copying and pasting text from a text editor. (CAMP-39028)
* Fixed an issue which prevented the word suggestions from being displayed. (CAMP-38970)
* Fixed an issue which prevented users from saving fragments. (ATU-2447)

**Other changes**

* The "Deliveries with preparation failed" filter now takes into account the deliveries' creation date rather than the last modification date. 
* The Organizational unit of the Administrators security group can no longer be changed.
* When creating a profile, the Organizational unit field must now be filled. 
* An Experience Cloud Trigger can now only be deleted if both the event and the transactional template that are linked to it are deleted.

**Patches**

* Fixed an issue in the **[!UICONTROL External API]** activity which displayed the **[!UICONTROL Confirm]** button even when no data was modified.
* Fixed an issue when using an **[!UICONTROL Union]** activity on queries with different target dimensions. The transition data only showed records from the main set's targeting dimension. (CAMP-36831)
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
* Fixed an issue which caused the enumeration value in a delivery template to default to a different one than the one configured. (CAMP-38388)
* Fixed an error with email bulk deliveries which displayed the deliveries' state as Pending and the Sent status as Finished. (CAMP-35355)
* Fixed an error which displayed the sender domain incorrectly in Dynamic reporting. (CAMP-33123)
* Fixed an issue which caused discrepancy in Unsubscription counts in Dynamic reporting. (CAMP-39949)
* Fixed an issue which prevented addresses from being displayed in the Sending logs screen when sending In-App messages.
* Fixed an issue which prevented SMS sending logs from being updated with the correct number of bounces. (CAMP-38395)
