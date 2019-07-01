---
title: About tracked URLs
seo-title: About tracked URLs
description: About tracked URLs
seo-description: Learn how to manage all the URLs of your content that                 will be tracked.
page-status-flag: never-activated
uuid: dfe5146b-5256-431c-87b3-3c54817eba36
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: managing-links
discoiquuid: d9b0b3c2-874b-4cb4-bce9-c0194a19f25f

internal: n
snippet: y
---

# About tracked URLs{#about-tracked-urls}

Adobe Campaign enables you to track the behavior of your recipients when they click a URL included in an email. For more on tracking, see [this section](../../sending/using/tracking-messages.md#about-tracking).

The **[!UICONTROL Links]** icon in the action bar automatically displays the list of all the URLs of your content that will be tracked.

![](assets/des_links.png)

>[!NOTE]
>
>Tracking is activated by default. This functionality is only available for emails, if tracking has been activated in Adobe Campaign. For more on the tracking parameters, refer to [this section](../../administration/using/configuring-email-channel.md#tracking-parameters).

The URL, category, label, and tracking type of each link can be modified from this list. To edit a link, click the corresponding pencil icon.

![](assets/des_links_tracking.png)

For each tracked URL, you can set tracking mode to one of these values:

* **Tracked**: activates tracking on this URL.
* **Mirror page**: considers this URL is a mirror page URL.
* **Never**: never activates tracking of this URL. This information is saved: if the URL appears again in a future message, its tracking is automatically deactivated.
* **Opt-out**: considers this URL as an opt-out or unsubscription URL.

![](assets/des_link_tracking_type.png)

You can also deactivate or activate tracking for each URL.

>[!NOTE]
>
>By default in Adobe Campaign, all content URLs are tracked except **Mirror page URL** and **Unsubscription** link.

You can regroup your URLs by editing the **[!UICONTROL Category]** field, depending on the URLs used in the message. These categories can be displayed reports, as for example in [URLs and click streams](../../reporting/using/urls-and-click-streams.md).

![](assets/des_link_tracking_category.png)

When building a report, from the **[!UICONTROL Components]** tab, select **[!UICONTROL Dimension]** and scroll down the list to access the tracking components. For example, drag and drop **[!UICONTROL Tracking URL Category]** into the workspace to display results according to the tracking category of each clicked URL.

![](assets/des_link_tracking_report.png)

For more on building customized reports, see [this section](../../reporting/using/about-dynamic-reports.md).
