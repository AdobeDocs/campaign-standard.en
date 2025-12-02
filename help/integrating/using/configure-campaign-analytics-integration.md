---
title: Configure Campaign-Analytics integration
description: Learn how to configure the Adobe Analytics integration to start measuring the success of your email deliveries.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-analytics

feature: Triggers
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: a6748b4b-36c5-4961-a599-ace73a8504cc
---
# Configure Campaign-Analytics integration{#configure-campaign-analytics-integration}

This integration allows you to share your Key Performance Indicator data directly from Adobe Campaign to Adobe Analytics Standard or Premium.

To start the integration between Adobe Campaign Standard and Adobe Analytics, you first need to configure the external account linked to Adobe Analytics.

External accounts and technical workflows can only be managed by the functional administrator of the platform.

1. From the advanced menu, via the Adobe Campaign logo, select **[!UICONTROL Administration > Application settings > External accounts]**.
1. Select the **[!UICONTROL Share KPIs with Adobe Analytics]** external account.

   ![](assets/analytics_2.png)

1. Specify your **[!UICONTROL Web services user name]** and **[!UICONTROL Web services share secret]** in the **[!UICONTROL Connection]** field.

   These parameters can be found in Analytics by selecting **[!UICONTROL Admin > Company settings > Web services]**.

   ![](assets/analytics_1.png)

1. Click the **[!UICONTROL Refresh report suites]** button.
1. Select in the **[!UICONTROL Analytics default report suite]** drop-down the Adobe Analytics report suite you want to enrich with Adobe Campaign data.

   Your external account is now ready and linked with Adobe Analytics. You can disable it at any time by checking the **[!UICONTROL Enabled]** box.

   ![](assets/analytics.png)

The **[!UICONTROL Share KPIs with Adobe Analytics]** technical workflow will now automatically launch and can be viewed from the advanced menu by selecting **[!UICONTROL Administration > Application settings > Workflow]**. This technical workflow can retain up to 6 months old broadlogs. Note that this workflow is incremental and will push data from the previous day.

![](assets/analytics_3.png)

Your data are now available in Adobe Analytics.

**Related topics:**

* [External accounts](../../administration/using/external-accounts.md)
* [Technical workflows](../../administration/using/technical-workflows.md)
* [Share KPIs for integrated Campaign reporting](https://helpx.adobe.com/marketing-cloud/how-to/email-marketing.html) video
