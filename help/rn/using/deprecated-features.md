---
solution: Campaign Standard
product: campaign
title: Campaign Standard Deprecated and Removed Features
description: This page lists deprecated and removed features of Adobe Campaign Standard.
audience: rn
content-type: reference
topic-tags: campaign-standard-deprecated-features

---

# Deprecated and Removed Features {#deprecated-and-removed-features}

Adobe constantly evaluates product capabilities to identify older features that should be replaced with more modern alternatives to improve overall customer value, always under careful consideration of backward compatibility.

To communicate the impending removal/replacement of Campaign Standard capabilities, the following rules apply:

* Announcement of deprecation comes first. While deprecated capabilities can still be available for existing users, they will not be further enhanced, nor documented. 
* Removal of deprecated capabilities will occur in the following release at the earliest. Actual target date for removal is announced in this page. 

This process gives customers at least one release cycle to adapt their implementation to a new version or successor of a deprecated capability, before actual removal. 

>[!NOTE]
>Adobe Campaign Standard releases and new capabilities are listed in the [Release Notes](../../rn/using/release-notes.md).


## Deprecated Features {#deprecated-features}

This section lists features and capabilities that have been marked as deprecated with latest Campaign Standard releases. 

Generally, features that are planned to be removed in a future release are set to deprecated first, with an alternative provided. These features and capabilities are either no longer available for new Campaign Standard customers, or should not be used for any new implementation. They are also removed from product documentation.

Customers are advised to review if they make use of the feature/capability in their current deployment, and make plans to change their implementation to use the alternative provided. Please refer to the target removal version to plan your environment and project updates accordingly.

<table> 
 <thead> 
 <tr> 
   <th> <strong>Predictive Subject Line</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p> Starting December 1st, Predictive Subject Line capability is deprecated.</p><br/>
   <p>We suggest you leverage AI-powered email capabilities to analyze and predict open rates, optimal send times, and probable churn based on historical engagement metrics. <a href="https://experienceleague.adobe.com/docs/campaign-standard/using/testing-and-sending/preparing-and-testing-messages/predictive.html">Learn more</a></p></br>
     <p>
     <em>Target removal: Campaign 21.1 release</em></p>
     </td> 
  </tr> 
  <tr> 
   <th> <strong>Push Notifications with SDK v4</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p> Starting 20.1 release, SDK v4 is deprecated. <a href="https://aep-sdks.gitbook.io/docs/version-4-sdk-end-of-support-faq">Learn more</a>.</p><br/>
   <p>The <a href="https://aep-sdks.gitbook.io/docs/">Adobe Experience Platform Mobile SDK</a> (previously referred to as v5) will exclusively support upcoming Adobe Experience Cloud features and functionality.</p></br>
     <p>
     <em>Target removal date: August 31, 2021</em></p>
     </td> 
  </tr> 
 </tbody> 
</table>
<table> 
 <thead> 
  <tr> 
   <th> <strong>Privacy requests - Campaign API and interface</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>Starting Campaign 19.4 release, the use of the Campaign API and interface for access and delete requests is deprecated. The 2-step profile deletion will not be available. Use  <a href="https://www.adobe.io/apis/experiencecloud/gdpr.html">Adobe Privacy Core Service</a>.</p></br>
   <p>See also <a href="https://experienceleague.adobe.com/docs/campaign-standard/using/getting-started/privacy/privacy-requests.html?lang=en">Managing Privacy requests</a>.</p>
  <p> 
  <em>Target removal date: 2021</em></p>
   </td> 
  </tr> 
 </tbody> 
</table>

<table> 
 <thead> 
  <tr> 
   <th> <strong>Email Design - Legacy email editor</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>Starting Campaign 19.0 release, the legacy email editor is deprecated. Use <a href="https://experienceleague.adobe.com/docs/campaign-standard/using/designing-content/designing-content-in-adobe-campaign.html">Campaign Email Designer</a> to create and personalize your email content. </p></br>
   <p>Read out <a href="https://experienceleague.adobe.com/docs/campaign-standard/using/designing-content/building-email-content/using-existing-content.html">this section</a> to learn how to adapt your email templates for the new editor.</p></br>
  <p> 
  <em>Target removal date: end of 2021</em></p>
   </td> 
  </tr> 
 </tbody> 
</table>

<table> 
 <thead> 
  <tr> 
   <th> <strong>Users & Security - Geographical units</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>Starting 18.7 release, Geographical units are deprecated. Organizational and Geographical units are identical constructs in Campaign. Users should use Organizational units alone to build their user permission/data access hierarchy. <a href="https://helpx.adobe.com/campaign/standard/administration/using/organizational-units.html">Learn more</a>. Please note that new Campaign Standard instances, as well as existing instances with no geographical units created, cannot have this capability implemented starting 18.7 release.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

## Removed Features {#removed-features}

This section lists features and capabilities that have been removed from Campaign Standard.

<table> 
 <thead> 
  <tr> 
   <th> <strong>Propensity Score with Experience Cloud Triggers</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>The <b>Propensity Score</b> has been decommissioned from Adobe Experience Cloud Triggers. As a consequence, this option has been removed from Adobe Campaign Standard. To avoid any outdated values of Propensity score in the Enrichment schemas, we recommend updating schemas to retrieve the latest changes and republishing existing Triggers. For more information, refer to <a href="https://experienceleague.adobe.com/docs/campaign-standard/using/integrating-with-adobe-cloud/working-with-campaign-and-triggers/using-triggers-in-campaign.html"> Publishing a trigger in Campaign </a>.
</p></br>
   </td> 
  </tr> 
 </tbody> 
</table>

<table> 
 <thead> 
  <tr> 
   <th> <strong>Creative SDK for Campaign Standard</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>[!DNL Adobe Creative SDK] has been decommissioned. As a consequence, image edition powered by [!DNL Creative SDK] in Campaign Standard emails is no longer available starting Campaign 20.2 release.</p></br>
   </td> 
  </tr> 
 </tbody> 
</table>

## End of compatibility {#end-of-compatibility}

<table> 
 <thead> 
  <tr> 
   <th> <strong>Microsoft Internet Explorer 11</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>Adobe Campaign and Adobe Experience Cloud has dropped support for Microsoft Internet Explorer 11 starting Spring 2019, and Campaign 19.2 release. Please switch to Microsoft Edge or another supported browser. <a href="https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/about-configuration-guidelines.html">Learn more</a>.</p>
   </td> 
  </tr> 
 </tbody> 
</table>
