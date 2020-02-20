---
title: Campaign Standard Deprecated and Removed Features
description: This page lists deprecated and removed features of Adobe Campaign Standard.
page-status-flag: never-activated
uuid: 
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: rn
content-type: reference
topic-tags: campaign-standard-deprecated-features
discoiquuid: 

internal: n
snippet: y
---

# Campaign Standard Deprecated and Removed Features {#deprecated-and-removed-features}

Adobe constantly evaluates product capabilities to identify older features that should be replaced with more modern alternatives to improve overall customer value, always under careful consideration of backward compatibility.

To communicate the impending removal/replacement of Campaign Standard capabilities, the following rules apply:

* Announcement of deprecation comes first. While deprecated capabilities can still be available for existing users, they will not be further enhanced, nor documented. 
* Removal of deprecated capabilities will occur in the following release at the earliest. Actual target date for removal is announced in this page. 

This process gives customers at least one release cycle to adapt their implementation to a new version or successor of a deprecated capability, before actual removal. 

>[!NOTE]
>Adobe Campaign Standard releases and new capabilities are listed in the [Release Notes](../../rn/using/release-notes.md).


## Deprecated Features {#deprecated-features}

This section lists features and capabilities that have been marked as deprecated with latest Campaign Standard releases. Generally, features that are planned to be removed in a future release are set to deprecated first, with an alternative provided. These features and capabilities are either no longer available for new Campaign Standard customers, or should not be used for any new implementation. They are also removed from product documentation.

Customers are advised to review if they make use of the feature/capability in their current deployment, and make plans to change their implementation to use the alternative provided. Please refer to the target removal date to plan your environment and project updates accordingly.

<table> 
 <thead> 
  <tr> 
   <th> Release<br /> </th> 
   <th> Features<br /> </th> 
   <th> Replacement<br /> </th> 
    <th> Target removal date<br /> </th>
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> 20.1<br /> </td> 
   <td> Push Notifications<br /> </td> 
    <td> The <a href="https://aep-sdks.gitbook.io/docs/version-4-sdk-end-of-support-faq">Adobe Experience Platform Mobile SDK</a> (previously referred to as v5) will exclusively support upcoming Adobe Experience Cloud features and functionality. <br /> </td> 
    <td> September 30, 2020<br /> </td> 
  </tr> 
  <tr> 
   <td> 20.1<br /> </td> 
   <td> Creative SDK for Campaign Standard<br /> </td> 
  <td> Adobe Creative SDK has been decommissioned. As a consequence, image edition powered by Creative SDK in Campaign Standard emails is now deprecated.<br /> </td>
  <td> March 2020 - Campaign 20.2 release<br /> </td> 
  </tr> 
  <tr> 
   <td> 19.4<br /> </td> 
   <td> Privacy requests - Campaign API and interface<br /> </td>
    <td> The use of the Campaign API and interface for access and delete requests is deprecated. Use the Privacy Core Service. <a href="https://www.adobe.io/apis/experiencecloud/gdpr.html">Learn more</a>. See also <a href="https://helpx.adobe.com/campaign/kb/acs-privacy.html">Privacy Management in Campaign Standard</a>.<br /> </td>
    <td> July 2020 - Campaign 20.5 release<br /> </td> 
  </tr>
  <tr> 
   <td> 19.0<br /> </td> 
   <td> Email Design - Legacy email editor<br /> </td>
    <td> The legacy email editor is now deprecated. Use the new Email Designer to create and personalize your email content. <a href="https://docs.adobe.com/content/help/en/campaign-standard/using/designing-content/designing-content-in-adobe-campaign.html">Learn more</a>. Read out <a href="https://docs.adobe.com/content/help/en/campaign-standard/using/designing-content/building-email-content/using-existing-content.html">this section</a> to learn how to adapt your email templates for the new editor.<br /> </td>
    <td> October 2020 - Campaign 20.6 release<br /> </td> 
  </tr>
  <tr> 
   <td> 18.7<br /> </td> 
   <td> Users & Security - Geographical units<br /> </td>
    <td> Organizational and Geographical units are identical constructs in Campaign. Users should use Organizational units alone to build their user permission/data access hierarchy. <a href="https://helpx.adobe.com/campaign/standard/administration/using/organizational-units.html">Learn more</a>. Please note that new Campaign Standard instances, as well as existing instances with no geographical units created, cannot have this capability implemented starting 18.7 release.<br /> </td>
    <td> N/A<br /> </td> 
  </tr> 
 </tbody> 
</table>

## End of compatibility {#end-of-compatibility}

<table> 
 <thead> 
  <tr> 
   <th> Release<br /> </th> 
   <th> Features<br /> </th> 
   <th> Replacement<br /> </th> 
 </tr> 
 </thead> 
 <tbody>
<tr> 
   <td> 19.2<br /> </td> 
   <td> Privacy requests - Campaign API and interface<br /> </td>
    <td> Adobe Campaign and Adobe Experience Cloud has dropped support for Microsoft Internet Explorer 11 starting Spring 2019, and Campaign 19.2 release. Please switch to Microsoft Edge or another supported browser.  <a href="Learn more">Learn more</a>.<br /> </td>
    <td><br /> </td> 
  </tr>
  </tbody> 
</table>
