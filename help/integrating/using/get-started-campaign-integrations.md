---
title: Get started with Campaign integrations
description: Use other Adobe solutions and combine their different capabilities with Campaign.
audience: integrating
content-type: reference
topic-tags: get-started-campaign-integrations

feature: Triggers
role: Data Architect
level: Intermediate
exl-id: ecf88c7d-6729-4b3a-85c4-60427bb57442
---
# About Campaign integrations{#get-started-campaign-integrations}

This section details the functional integrations available between the current version of Adobe Campaign and other solutions and services.

The different integrations presented below allow you to combine the delivery and advanced campaign management functionalities of Adobe Campaign with a set of solutions created to help you personalize your users' experience.

>[!NOTE]
>
> By default, Adobe Campaign is already linked to an Adobe Experience Cloud account.

Depending on your environment, other solutions can also be linked to Adobe Experience Cloud. They are linked as Organizations (also called Tenants).

An organization is the entity that enables an administrator to configure groups and users, and to control single sign-on in the Experience Cloud. The organization functions like a log-in company that spans all the Experience Cloud products and solutions. Most often, an organization is your company name. However, a company can have many organizations. User and organization management is detailed in the [Adobe Experience Cloud help portal](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/organizations.html).

If you would like to integrate data flows from other systems with Adobe Campaign, have a look at our [API documentation](../../api/using/get-started-apis.md).

>[!NOTE]
>
>Adobe Campaign Standard can also connect to Microsoft Dynamics 365 : this integration enables synchronization of all available Contact data in the CRM system, making all relevant Contact data available for campaign activities. For more on this integration, refer to [Working with Campaign and Dynamics 365](../../integrating/using/d365-acs-get-started.md).


<table> 
 <thead> 
  <tr> 
   <th> Solution<br /> </th> 
   <th> Use Case<br /> </th> 
   <th> Refer to<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Adobe Experience Manager<br /> </td> 
   <td> Allows you to create email contents or forms mapped to the Adobe Campaign database directly in Adobe Experience Manager.<br /> </td> 
   <td> 
     <a href="../../integrating/using/integrating-with-experience-manager.md">Work with Campaign and Experience Manager</a>, <a href="https://helpx.adobe.com/experience-manager/6-4/sites/administering/using/campaignstandard.html">Integrate Experience Manager and Campaign Standard</a>, <a href="https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/campaignstandard.html">Create an email with Experience Manager and Campaign</a> 
    </td> 
  </tr> 
  <tr> 
   <td> Adobe Target<br /> </td> 
   <td> Allows you to insert images that are dynamically computed by Adobe Target when an email created and sent by Adobe Campaign is opened.<br /> </td> 
   <td> 
    <a href="../../integrating/using/about-campaign-target-integration.md">Work with Campaign and Target</a>, <a href="https://experienceleague.adobe.com/docs/target/using/integrate/campaign-and-target.html">Integrate Campaign and Target</a>, <a href="https://helpx.adobe.com/marketing-cloud/how-to/email-marketing.html">Personalize Email Images in Real-Time</a> video (step 3)
    </td> 
  </tr> 
  <tr> 
   <td> Adobe Analytics<br /> </td> 
   <td> Allows you to track the success of your email deliveries directly in Adobe Analytics.<br /> </td> 
   <td> 
    <a href="../../integrating/using/about-campaign-analytics-integration.md">Share Campaign data with Analytics</a>, <a href="https://helpx.adobe.com/marketing-cloud/how-to/email-marketing.html">Share KPIs for integrated Campaign reporting</a> video (step 1)
    </td> 
  </tr> 
  <tr> 
   <td> Adobe Audience Manager and People core service (Profiles &amp; Audiences)<br /> </td> 
   <td> Allow you to exchange audiences with the different Adobe Experience Cloud applications that you use.<br /> </td> 
   <td> <a href="../../integrating/using/about-campaign-audience-manager-or-people-core-service-integration.md">People Core Service (Profiles &amp; Audiences)</a><br /> </td> 
  </tr> 
   <tr> 
   <td> Adobe Real-time Customer Data Platform (RTCDP)<br /> </td> 
   <td> The integration between Adobe Campaign and Adobe Real-time Customer Data Platform (RTCDP) allows you to share segments data and import audiences to Adobe Campaign.</td>
   <td><a href="../../integrating/using/get-started-sources-destinations.md">Get started with Sources and Destinations</a></td>
  </tr> 
  <tr> 
   <td> Adobe Asset core service and Assets On Demand<br /> </td> 
   <td> Allows you to insert assets from your Adobe Experience Cloud library into emails and landing pages created in Adobe Campaign.<br /> </td> 
   <td> <a href="../../integrating/using/working-with-campaign-and-assets-core-service.md">Assets Core Service</a> or Assets On Demand<br /> </td> 
  </tr> 
  <tr> 
   <td> Points of Interest (Analytics for Mobile)<br /> </td> 
   <td> Allows you to collect Points of Interest data from your mobile application's subscribers to send personalized marketing messages with Adobe Campaign.<br /> </td> 
   <td> <a href="../../integrating/using/about-campaign-points-of-interest-data-integration.md">Send location-based marketing messages with Campaign and Points of Interest data</a> (Analytics for Mobile)<br /> </td> 
  </tr> 
  <tr> 
   <td> Adobe Experience Cloud Triggers<br /> </td> 
   <td> Allows you to send personalized emails to your customers in Adobe Campaign as a reaction to specific behaviors that are tracked on your website by Adobe Analytics.<br /> </td> 
   <td> 
    <a href="../../integrating/using/about-adobe-experience-cloud-triggers.md">Use Experience Cloud Triggers in Campaign Standard</a>, <a href="../../integrating/using/abandonment-triggers-use-cases.md">Abandonment Triggers-Campaign use cases</a>, <a href="https://helpx.adobe.com/marketing-cloud/how-to/email-marketing.html">Trigger Remarketing Messages based on Site Activity</a> video (step 2)
    </td> 
  </tr> 
    <tr> 
   <td> Adobe Journey Orchestration<br /> </td> 
   <td> Allows to send emails, push notifications and SMS using the Adobe Campaign Standard’s Transactional Messaging capabilities in the context of Adobe Journey Orchestration, through an out-of-the-box action.<br /> </td> 
   <td> <a href="https://experienceleague.adobe.com/docs/journeys/using/action-journeys/working-with-adobe-campaign.html">Working with Adobe Journey Orchestration and Adobe Campaign Standard</a><br /> </td> 
  </tr> 
  <tr> 
   <td> Adobe Dreamweaver<br /> </td> 
   <td> Allows you to edit an email content from Dreamweaver and synchronize it with Adobe Campaign.<br /> </td> 
   <td> 
    <a href="https://experienceleague.adobe.com/docs/campaign-learn/campaign-standard-tutorials/designing-content/email-designer/dreamweaver-integration.html">Create personalized emails with Dreamweaver</a> video, <a href="https://helpx.adobe.com/dreamweaver/using/working-with-dreamweaver-and-campaign.html">Use Campaign extension for Dreamweaver</a> 
  </td> 
  </tr> 
  <tr> 
   <td> Adobe Experience Platform SDKs<br /> </td> 
   <td> Allows automation of the Mobile App Property activation process in Adobe Campaign using the Experience Platform SDKs.<br /> </td> 
   <td> <a href="https://helpx.adobe.com/campaign/kb/configuring-app-sdk.html">Configuring a mobile application using Experience Platform SDKs</a><br /> </td> 
  </tr> 
 </tbody> 
</table>
