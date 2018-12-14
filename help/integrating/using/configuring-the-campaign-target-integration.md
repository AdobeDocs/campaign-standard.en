---
title: Configuring the Campaign-Target integration
seo-title: Configuring the Campaign-Target integration
description: Configuring the Campaign-Target integration
seo-description: Learn how to configure the Adobe Target integration to start using dynamic content in Adobe Campaign.
page-status-flag: never-activated
uuid: a2fe9cd6-e488-4443-a1cb-fda8e5d8d224
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-target
discoiquuid: 4b7cce95-3ea6-460a-be3a-5ed3ca44ee86
isreadyforlocalization: true
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
