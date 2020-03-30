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

[Click here](http://amc-mkt-prod1-t.adobe-campaign.com/lp/LP25?service=%40rZ5cqp2DgNzrgz0alKPInakNbPSTeJYozZYnS7Wbs802u4GlISkHZX4omtK00nAU6xzZ6luEWQzr7kQ9pkCwJYumWkU) to subscribe to release notifications and get details about latest Adobe Experience Cloud releases straight in your inbox.

## Release 20.2 - March 2020 {#release-20-2---march-2020}

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