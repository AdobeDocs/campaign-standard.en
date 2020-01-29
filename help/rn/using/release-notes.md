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
   <td> <p>The Adobe Experience Platform Data Connector is now integrated with Adobe Campaign Standard, allowing you to make your data available on Adobe Experience Platform by mapping XTK data (data ingested in Campaign) to Experience Data Model (XDM) data on Adobe Experience Platform. </p>
    <p>For more information, refer to the <a href="XXX">detailed documentation</a> and the <a href="XXX">how-to video</a>.</p>
    <p>Note: the Adobe Experience Platform Data Connector is currently in beta, which may be subject to frequent updates without notice. Customers are required to be hosted on Azure (currently in beta for North America only) to access these capabilities. Please reach out to Adobe Customer Care if you would like access.</p>
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
   <td> <p>Transactional messaging can now be managed by the Adobe Campaign Enhanced MTA, which provides an upgraded sending infrastructure allowing for improved deliverability, throughput, and bounce handling.</p>
    <p>For more information, refer to the <a href="https://helpx.adobe.com/campaign/kb/campaign-enhanced-mta.html">detailed documentation</a>.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

<table> 
 <thead> 
  <tr> 
   <th> <strong>Audience Destinations service (public beta)</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>The Audience Destinations service is now integrated with Adobe Campaign Standard, allowing you to build highly targeted audiences based on large, complex datasets and share these segments near real-time with other Adobe Experience Cloud solutions.</p>
    <p>For more information, refer to the <a href="XXX">detailed documentation</a> and the <a href="XXX">how-to video</a>.</p>
    <p>Note: the Audience Destinations service is currently in beta, which may be subject to frequent updates without notice. Customers are required to be hosted on Azure (currently in beta for North America only) to access these capabilities. Please reach out to Adobe Customer Care if you would like access.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

**Improvements**

* Campaign Standard APIs now allow you to perform pagination when using large tables, by adding the _forcePagination=true parameter to your call UR. [Read more](https://docs.adobe.com/content/help/en/campaign-standard/using/working-with-apis/global-concepts/additional-operations/pagination.html)

* The Delivery log ID (which is a unique identifier for each log) is now available in the Delivery logs and Tracking logs resources for all targeting dimensions. This enables to identify sending or tracking logs when exporting for example.

**Email Designer enhancements**

* Fixed an issue with containing elements to allow text resize without loss of functionality.
* Fixed an issue with accessibility ensuring that alternative text is available for images.
* Fixed an issue with the auto Calendar pop-up to allow users to dismiss content that appears on hover in marketing activities.
* Fixed an issue with accessibility ensuring that instructive text is placed at the beginning of the Audiences form.
* Fixed an issue when clicking on change content in the wizard of the deprecated content editor.
* Fixed an issue where headers are not aligned with the content on the Service Summary report. (CAMP-38103)

**Other changes**

* XXX

**Patches**

* Fixed an issue in the **[!UICONTROL External API]** activity that displayed the **[!UICONTROL Confirm]** button even when * no data was modified.
* The "Deliveries with preparation failed"  filter now takes into account the deliveries creation date rather than the last modification date. 
* Fixed an issue when using an **[!UICONTROL Union]** activity on queries with different target dimensions. The transition data only showed records from the main set's targeting dimension.  (CAMP-36831)
* Fixed an issue that could lead to an error when using a **[!UICONTROL]**Reconciiliation activity in specific contexts, for example with two inbound activities, one of them being an exclusion activity. (CAMP-37490)
* Fixed performance issues that could occur when selecting and updating test profiles. (CAMP-37976)
* Fixed an issue that could display error pages when subscribing or unsubscribing via landing pages.  (CAMP-37771) 
* Fixed an issue that occured when uploading content in zip format, with PNG files referenced in the HTML with their extension in capital letters. (CAMP-37913)* 