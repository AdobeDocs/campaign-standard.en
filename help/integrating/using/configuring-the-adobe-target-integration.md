---
title: Configuring the Adobe Target integration
seo-title: Configuring the Adobe Target integration
description: Configuring the Adobe Target integration
seo-description: Learn how to configure the Adobe Target integration to start using dynamic content in Adobe Campaign.
page-status-flag: never-activated
uuid: 5a7a0e25-424b-4689-8815-adab74fba2a7
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/integrating/using/configuring-the-adobe-target-integration
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-01-10T15 24 02.585-0500
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: adobe-target-integration
cq-template: /apps/help/templates/article-3
discoiquuid: 255779fa-a41b-4c44-8b4e-fac3a7fa0ff3
firstPublishExternalDate: 2018-01-10T15:24:02.579-0500
herogradient: light
jcr-created: 2018-01-11T19 02 07.831-0500
jcr-createdby: admin
jcr-description: Configuring the Adobe Target integration
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-01-10T15:24:02.579-0500
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Configuring the Adobe Target integration
publishexternaldate: 2018-01-10T15 24 02.579-0500
publishExternalURL: https://helpx.adobe.com/campaign/standard/integrating/using/configuring-the-adobe-target-integration.html
sha1: 934a5eb14fff8f01ab2dda95376b7aa4bd346db6
topicBrowsingSortDate: 2018-01-10T15:24:02.579-0500
index: y
internal: n
snippet: y
---

# Configuring the Adobe Target integration

Configuring the Adobe Target integration

The integration between Adobe Campaign and Adobe Target lets you insert dynamic content in your delivery.

A configuration is first needed in Adobe Campaign to use the integration functionalities with Adobe Target and must be managed by the functional administrator.

The following elements are needed for this procedure:

* An Adobe Marketing Cloud tenant
* An Adobe Target tenant
* An Adobe Target rawbox specified to establish the connection with Adobe Campaign

1. From the advanced menu, via the Adobe Campaign logo in the top left corner, select **Administration** > **Application settings** > **Options**.
1. To configure the server and tenant options for Adobe Target, fill in the following fields accordingly:

    * **TNT_TenantName**: name of the Adobe Target tenant. This value corresponds to the name of the Adobe Target **Client**.
    * **TNT_EdgeServer**: Adobe Target server used for integration. This option is already provided by default. This value corresponds to the Adobe Target **Server Domain**, followed by the **/m2** value. For example: **tt.omtrdc.net/m2**.

   ![](assets/tar_options.png)

Your users can now add dynamic images in a delivery with Adobe Target.
