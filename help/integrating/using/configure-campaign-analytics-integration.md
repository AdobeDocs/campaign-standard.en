---
title: Configure Campaign-Analytics integration
seo-title: Configure Campaign-Analytics integration
description: Configure Campaign-Analytics integration
seo-description: Learn how to configure the Adobe Analytics integration to start measuring the success of your email deliveries.
uuid: bfb35d88-33a3-42c7-9f6b-b16996734923
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/integrating/using/configure-campaign-analytics-integration
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-10T02 18 50.167-0400
cq-lastreplicated: 2018-09-07T15 04 11.865-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-analytics
cq-template: /apps/help/templates/article-3
discoiquuid: 6582c3d3-e61a-490a-8c27-5c2fd823e21e
firstPublishExternalDate: 2018-09-07T15:04:09.550-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 01 52.209-0400
jcr-createdby: admin
jcr-description: Configure Campaign-Analytics integration
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T15:04:09.550-0400
lochandoffdate: 2018-09-10T02 18 50.166-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Configure Campaign-Analytics integration
publishexternaldate: 2018-09-07T15 04 09.550-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/integrating/using/configure-campaign-analytics-integration.html
sha1: 0175b16e9363dfb73948a6b8813b616cc6d04c20
topicBrowsingSortDate: 2018-09-07T15:04:09.550-0400
index: y
internal: n
snippet: y
---

# Configure Campaign-Analytics integration{#configure-campaign-analytics-integration}

Configure Campaign-Analytics integration

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

