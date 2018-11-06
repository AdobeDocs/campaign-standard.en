---
title: Integrating with Experience Manager
seo-title: Integrating with Experience Manager
description: Integrating with Experience Manager
seo-description: With the Adobe Experience Manager integration, you can create content directly in AEM and use it later on in Adobe Campaign.
uuid: 5ffed55d-b25f-467f-8c96-2c0f71f93c0f
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/integrating/using/integrating-with-experience-manager
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-27T03 26 21.292-0400
cq-lastmodifiedby: mancini
cq-lastreplicated: 2018-07-23T05 59 25.597-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-experience-manager
cq-template: /apps/help/templates/article-3
discoiquuid: 90025eeb-6573-4682-9d8d-b563a12ab85a
firstPublishExternalDate: 2018-07-23T05:59:25.488-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 38.293-0400
jcr-createdby: admin
jcr-description: Integrating with Experience Manager
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T05:59:25.488-0400
lochandoffdate: 2018-07-27T03 26 21.290-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
moreHelpPaths: /content/help/en/campaign/standard/integrating/morehelp/working-with-campaign-and-experience-manager;/content/help/en/campaign/standard/integrating/morehelp/working-with-campaign-and-experience-manager
navTitle: Integrating with Experience Manager
publishexternaldate: 2018-07-23T05 59 25.488-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/integrating/using/integrating-with-experience-manager.html
sha1: 79aea449c908726ea3bdfc0234e28013a9e99754
topicBrowsingSortDate: 2018-07-23T05:59:25.488-0400
index: y
internal: n
snippet: y
---

# Integrating with Experience Manager

Integrating with Experience Manager

This integration between Adobe Campaign Standard and Adobe Experience Manager allows you to use content created in Adobe Experience Manager in your Adobe Campaign emails.

You can therefore make the most of the Adobe Experience Manager content editing functionalities as well as Adobe Campaign's delivery and data management capabilities.

>[!NOTE]
>
>You cannot perform A/B tests for contents imported from Adobe Experience Manager.

Adobe Campaign Standard is compatible with Adobe Experience Manager 6.1, 6.2, 6.3 and 6.4. The following sections present an overview of the actions you can execute. For more information, refer to the sections dedicated to [configuration](https://helpx.adobe.com/experience-manager/6-4/sites/administering/using/campaignstandard.html) and the [use](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/campaign.html) of the integration.

## Prerequisites

You should make sure you have the following elements beforehand:

* An Adobe Experience Manager **authoring** instance
* An Adobe Experience Manager **publishing** instance
* An Adobe Campaign instance

## Use case

To create an email content in Adobe Experience Manager:

1. Create an email content using a template created specifically for Adobe Campaign.
1. In the content properties, select the **Cloud Service** corresponding to your Adobe Campaign instance.
1. Edit the content by inserting text, images, personalization, etc.
1. Validate the content.

For more information, refer to the [detailed documentation](https://docs.adobe.com/docs/en/aem/6-2/author/personalization/adobe-campaign/campaign.html).

![](assets/aem_content.png)

To retrieve the content in Adobe Campaign:

1. Create an email based on an Adobe Experience Manager type content template.
1. Link a content created with Adobe Experience Manager using the Adobe Campaign email content definition screen.

![](assets/aem_linked_content.png)

## Configuration

To use these two solutions together, you must configure them to connect to one another.

1. Configure Adobe Campaign. To do this:

    * Configure an Adobe Experience Manager type external account.
    * Configure the **AEMResourceTypeFilter** option, which recognizes the content types created in Adobe Experience Manager for Adobe Campaign.
    * Create an email template specifying that it is Adobe Experience Manager content and link the previously created external account to this template.

1. Configure Adobe Experience Manager. To do this:

    * Configure the replication between the Adobe Experience Manager authoring and publishing instances.
    * Connect Adobe Experience Manager to Adobe Campaign by configuring a dedicated **Cloud Service**.

