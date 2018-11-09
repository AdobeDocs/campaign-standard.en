---
title: Configuring the Campaign-Target integration
seo-title: Configuring the Campaign-Target integration
description: Configuring the Campaign-Target integration
seo-description: Learn how to configure the Adobe Target integration to start using dynamic content in Adobe Campaign.
uuid: c932d094-e745-4f52-930c-600e9e0d27ef
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/integrating/using/configuring-the-campaign-target-integration
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-10T02 18 41.760-0400
cq-lastreplicated: 2018-09-07T15 01 14.252-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-target
cq-template: /apps/help/templates/article-3
discoiquuid: e760679b-ac2d-48a0-a7bd-7340a7038a5c
firstPublishExternalDate: 2018-09-07T15:01:11.299-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 20.080-0400
jcr-createdby: admin
jcr-description: Configuring the Campaign-Target integration
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T15:01:11.299-0400
lochandoffdate: 2018-09-10T02 18 41.760-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Configuring the Campaign-Target integration
publishexternaldate: 2018-09-07T15 01 11.299-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/integrating/using/configuring-the-campaign-target-integration.html
sha1: a8779f56fc49464b110b73346930e9ae9a611cf5
topicBrowsingSortDate: 2018-09-07T15:01:11.299-0400
index: y
internal: n
snippet: y
---

# Configuring the Campaign-Target integration{#configuring-the-campaign-target-integration}

Configuring the Campaign-Target integration

The integration between Adobe Campaign and Adobe Target lets you insert dynamic content in your delivery.

A configuration is first needed in Adobe Campaign to use the integration functionalities with Adobe Target and must be managed by the functional administrator.

The following elements are needed for this procedure:

* An Adobe Experience Cloud tenant
* An Adobe Target tenant
* An Adobe Target rawbox specified to establish the connection with Adobe Campaign

1. From the advanced menu, via the Adobe Campaign logo in the top left corner, select **Administration** > **Application settings** > **Options**.
1. To configure the server and tenant options for Adobe Target, fill in the following fields accordingly:

    * **TNT_TenantName**: name of the Adobe Target tenant. This value corresponds to the name of the Adobe Target **Client**.
    * **TNT_EdgeServer**: Adobe Target server used for integration. This option is already provided by default. This value corresponds to the Adobe Target **Server Domain**, followed by the **/m2** value. For example: **tt.omtrdc.net/m2**.

   ![](assets/tar_options.png)

Your users can now add dynamic images in a delivery with Adobe Target.
