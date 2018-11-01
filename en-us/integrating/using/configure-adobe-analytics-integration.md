---
title: Configure Adobe Analytics integration
seo-title: Configure Adobe Analytics integration
description: Configure Adobe Analytics integration
seo-description: Learn how to configure the Adobe Analytics integration to start measuring the success of your email deliveries.
page-status-flag: never-activated
uuid: abacb39b-caa3-457e-9c32-1e5c3d69e071
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/integrating/using/configure-adobe-analytics-integration
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-01-10T15 24 08.000-0500
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: adobe-analytics-integration
cq-template: /apps/help/templates/article-3
discoiquuid: 0bc46e04-dcbf-4556-ae3e-73e4d933d2d1
firstPublishExternalDate: 2018-01-10T15:24:07.987-0500
herogradient: light
jcr-created: 2018-01-11T19 01 49.038-0500
jcr-createdby: admin
jcr-description: Configure Adobe Analytics integration
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-01-10T15:24:07.987-0500
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Configure Adobe Analytics integration
publishexternaldate: 2018-01-10T15 24 07.987-0500
publishExternalURL: https://helpx.adobe.com/campaign/standard/integrating/using/configure-adobe-analytics-integration.html
sha1: 7e139d43ded0ab981ee89ae23b443dd8b04ac4b4
topicBrowsingSortDate: 2018-01-10T15:24:07.987-0500
index: y
internal: n
snippet: y
---

# Configure Adobe Analytics integration

Configure Adobe Analytics integration

This integration allows you to share your Key Performance Indicator data directly from Adobe Campaign to Adobe Analytics Standard or Premium.

To start the integration between Adobe Campaign Standard and Adobe Analytics, you first need to configure the external account linked to Adobe Analytics.

External accounts and technical workflows can only be managed by the functional administrator of the platform.

1. From the advanced menu, via the Adobe Campaign logo, select **Administration > Application settings > External accounts**.
1. Select the **Share KPIs with Adobe Analytics** external account.

   ![](assets/analytics_2.png)

1. Specify your **Web services user name** and **Web services share secret** in the **Connection** field.

   These parameters can be found in Analytics by selecting **Admin > Company settings > Web services**.

   ![](assets/analytics_1.png)

1. Click the **Refresh report suites** button.
1. Select in the **Analytics default report suite** drop-down the Adobe Analytics report suite you want to enrich with Adobe Campaign data.

   Your external account is now ready and linked with Adobe Analytics. You can disable it at any time by checking the **Enabled** box.

   ![](assets/analytics.png)

The **Share KPIs with Adobe Analytics** technical workflow will now automatically launch and can be viewed from the advanced menu by selecting **Administration > Application settings > Workflow**. This technical workflow will automatically execute every 15 minutes and will push up to 6 months old data in Adobe Analytics.

![](assets/analytics_3.png)

Your data are now available in Adobe Analytics.

**Related topics:**

* [External accounts](../../administration/using/external-accounts.md)
* [Technical workflows](../../administration/using/technical-workflows.md)
* [Share KPIs for integrated Campaign reporting](https://helpx.adobe.com/marketing-cloud/how-to/email-marketing.html) video

