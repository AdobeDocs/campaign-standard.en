---
title: Configuring the Campaign-Target integration
seo-title: Configuring the Campaign-Target integration
description: Configuring the Campaign-Target integration
seo-description: Learn how to configure the Adobe Target integration to start using dynamic content in Adobe Campaign.
page-status-flag: never-activated
uuid: a65a888d-bf49-47ec-a7d2-7245ac7fe41d
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/integrating/using/configuring-the-campaign-target-integration
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-target
discoiquuid: 4623478b-0a66-4796-9d72-f1aa858af86b
isreadyforlocalization: false
navTitle: Configuring the Campaign-Target integration
publishexternaldate: 2018-11-20
sha1: c2d4991fe1aa296244e531ac8257e4dbbf29c5c1
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
