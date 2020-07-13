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

[Release Planning](../../rn/using/release-planning.md) &#124; [Control Panel releases](https://docs.adobe.com/content/help/en/control-panel/using/release-notes.html) &#124; [Documentation Updates](../../rn/using/documentation-updates.md) &#124; [Previous Release Notes](../../rn/using/release-notes-2020.md) &#124; [Deprecated Features](../../rn/using/deprecated-features.md)

![](assets/do-not-localize/cp-icon.png) **New Control Panel June release** with Active profiles monitoring, Subdomain deliverability audit and GPG keys management. [Learn more](https://docs.adobe.com/content/help/en/control-panel/using/release-notes.html).

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
<p>Refer to the <a href="https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/privacy/privacy-overview.html">how-to video</a>.</p>
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
<p>For more information, refer to the <a href="../../automating/using/external-api.md">detailed documentation</a> and the <a href="https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/managing-processes-and-data/data-management-activities/external-api-activity.html">how-to video</a>.</p>
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

* Activation of Adobe [Experience Platform Audiences](../../automating/using/aep-targeting-audiences.md) from the **Read audience** activity has been improved to provide better performance and stability. Moreover, workflow logs have been made clearer and more detailed regarding activation jobs, allowing easier monitoring and troubleshooting when reading Adobe Experience Platform audiences.

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


![](assets/do-not-localize/cp-icon.png) **New Control Panel May release** with Certificate renewal for CNAME subdomains. [Learn more](https://docs.adobe.com/content/help/en/control-panel/using/release-notes.html).
