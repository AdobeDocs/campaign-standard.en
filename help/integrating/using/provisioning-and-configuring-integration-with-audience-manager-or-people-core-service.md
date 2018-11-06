---
title: Provisioning and configuring integration with Audience Manager or People core service
seo-title: Provisioning and configuring integration with Audience Manager or People core service
description: Provisioning and configuring integration with Audience Manager or People core service
seo-description: Learn how to configure the Audience Manager / People core service integration to start sharing audiences or segments with the different Adobe Experience Cloud solutions. 
uuid: c3bf2deb-90d3-49a3-905f-b70110d1ec17
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/integrating/using/provisioning-and-configuring-integration-with-audience-manager-or-people-core-service
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-27T03 26 49.168-0400
cq-lastreplicated: 2018-07-23T05 59 40.425-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-audience-manager-or-people-core-service
cq-template: /apps/help/templates/article-3
discoiquuid: 4ed6f299-8d6d-4596-8784-7ea04c6b5b46
firstPublishExternalDate: 2018-07-23T05:59:40.372-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 56.412-0400
jcr-createdby: admin
jcr-description: Provisioning and configuring integration with Audience Manager or People core service
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T05:59:40.372-0400
lochandoffdate: 2018-07-27T03 26 49.167-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Provisioning and configuring integration with Audience Manager or People core service
publishexternaldate: 2018-07-23T05 59 40.372-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/integrating/using/provisioning-and-configuring-integration-with-audience-manager-or-people-core-service.html
sha1: cf2f8e54192b389d0229fa950c0ed946ed290c52
topicBrowsingSortDate: 2018-07-23T05:59:40.372-0400
index: y
internal: n
snippet: y
---

# Provisioning and configuring integration with Audience Manager or People core service

Provisioning and configuring integration with Audience Manager or People core service

The provisioning and configuring of Audience Manager and People core in Adobe Campaign take two steps: [Submitting request to Adobe](../../integrating/using/provisioning-and-configuring-integration-with-audience-manager-or-people-core-service.md#submitting-request-to-adobe) then [Configuring the integration in Adobe Campaign](../../integrating/using/provisioning-and-configuring-integration-with-audience-manager-or-people-core-service.md#configuring-the-integration-in-adobe-campaign).

## Submitting request to Adobe

Audience Manager (AAM) or People core service integration lets you import and export audiences or segments in Adobe Campaign.

This integration must first be configured. To request provisioning of this integration, write an email to [Digital-Request@adobe.com](mailto:Digital-Request@adobe.com) with the following information:

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Request Type:</strong><br /> </td> 
   <td> Configure AAM/People core service-Campaign Integration </td> 
  </tr> 
  <tr> 
   <td> <strong>Organization Name:</strong><br /> </td> 
   <td> Your organization name </td> 
  </tr> 
  <tr> 
   <td> <strong>IMS Org ID</strong><br /> </td> 
   <td> Your IMS Org ID* </td> 
  </tr> 
  <tr> 
   <td> <strong>Environment:</strong><br /> </td> 
   <td> Example: Production </td> 
  </tr> 
  <tr> 
   <td> <strong>AAM or People Service</strong><br /> </td> 
   <td> Example: Adobe Audience Manager </td> 
  </tr> 
  <tr> 
   <td> <strong>Declared ID or Visitor ID</strong><br /> </td> 
   <td> Example: Declared ID </td> 
  </tr> 
  <tr> 
   <td> <strong>Additional Information</strong><br /> </td> 
   <td> Any useful information or comment that you may have </td> 
  </tr> 
 </tbody> 
</table>

&#42; You can find your IMS Org ID on the Experience Cloud, in the **Administration** menu. It is also provided when you first connect to the Adobe Experience Cloud.

## Configuring the integration in Adobe Campaign

After submitting this request, Adobe will proceed to the provisioning of the integration for you and contact you to provide details and information that you have to finalize the configuration:

* [Step 1: Configure or check the external accounts in Adobe Campaign](../../integrating/using/provisioning-and-configuring-integration-with-audience-manager-or-people-core-service.md#step-1--configure-or-check-the-external-accounts-in-adobe-campaign)
* [Step 2: Configure the Data Sources](../../integrating/using/provisioning-and-configuring-integration-with-audience-manager-or-people-core-service.md#step-2--configure-the-data-sources)
* [Step 3: Configure Campaign Tracking server](../../integrating/using/provisioning-and-configuring-integration-with-audience-manager-or-people-core-service.md#step-3--configure-campaign-tracking-server)
* [Step 4: Configure the Visitor ID Service](../../integrating/using/provisioning-and-configuring-integration-with-audience-manager-or-people-core-service.md#step-4--configure-the-visitor-id-service)

### Step 1: Configure or check the external accounts in Adobe Campaign

We first need to configure or check the external accounts in Adobe Campaign. These accounts should have been configured by Adobe and the necessary information should have been communicated to you.

To do so:

1. From the advanced menu, select **Administration > Application settings > External accounts**.

   Select one of the following external accounts available for this integration: 

   ![](assets/integration_aam_1.png)

1. Enter **Receiver server** in following format 
1. Enter the **AWS Access Key ID**, **Secret Access Key** and **AWS Region**.

Your external accounts are now configured for this integration.

### Step 2: Configure the Data Sources

The two following data sources are created inside Audience manager: Adobe Campaign (MID) and Adobe Campaign (DeclaredId). At the same time, these two data sources are available in Adobe Campaign:

* **Recipient - Visitor ID (Defaultdatasources)**: This is an out-of-the-box data source configured by default for Visitor ID. Segments created from Campaign will be part of this data source.
* **Declared ID** data source: This data source needs to be created and mapped with the **DeclaredId** data source definition from Audience Manager.

To configure the **Recipient - Visitor ID (Defaultdatasources)** data source:

1. In **Administration** > **Application settings** > **Shared Data Sources**, select **Recipient - Visitor ID (Defaultdatasources)**.

   ![](assets/integration_aam_2.png)

1. Choose **Adobe Campaign** in the **Data Source/ Alias** drop-down.
1. Enter the **AAM Destination ID** provided by Adobe.

   ![](assets/integration_aam_3.png)

1. In the **Reconciliation process** category, we advise you not to change the reconciliation criteria and always use the **Visitor ID**.
1. Click **Save**.

To create the **Declared ID** data source:

1. In **Administration** > **Application settings** > **Shared Data Sources**, click the **Create** button.
1. Edit the **Label** of your data source.
1. In the **Data Source/ Alias** drop-down, choose the Data Source corresponding to the **DeclaredID** data source from Audience Manager. 
1. Configure your data source by entering the **Data Source / Alias** and **AAM Destination ID** provided by Adobe.
1. Set the **Reconciliation process** as needed.
1. Click **Save**.

>[!NOTE]
>
>The **AAM Destination ID** field is not required if you are configuring the shared data source for the [Campaign-Triggers integration](../../integrating/using/configuring-triggers-in-experience-cloud.md). **Priority** is only needed when configuring the Triggers - Campaign integration. Priority decides which Data Source will be configured first. Priority can be any number such as 1 or 100. The higher the priority, the higher the preference during reconciliation.

### Step 3: Configure Campaign Tracking server

For the configuration of the integration with People Core service or Audience manager, we also need to configure Campaign Tracking server.

Here, you need to make sure the Campaign Tracking Server is registered on the domain (CNAME). You can find more information about domain name delegation in [this article](https://docs.campaign.adobe.com/doc/AC/en/technicalResources/Technotes/AdobeCampaign_Deliverability_Sub_Domain_Delegation.pdf).

### Step 4: Configure the Visitor ID Service

In the case that your Visitor ID service has never been configured on your web properties or websites, refer to the following [document](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-setup-aam-analytics.html) to learn how to configure your service or the following [video](https://helpx.adobe.com/marketing-cloud/how-to/email-marketing.html#step-two) .

Your configuration and provisioning are finalized, the integration can now be used to import and export audiences or segments.
