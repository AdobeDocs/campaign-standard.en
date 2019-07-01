---
title: About dynamic reports
seo-title: About dynamic reports
description: About dynamic reports
seo-description: With dynamic reports, drag and drop variables and dimensions into your freeform environment and analyze the success of your campaigns.
page-status-flag: never-activated
uuid: a84a18bd-4e33-466e-a6ce-d7008fe12746
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: reporting
content-type: reference
topic-tags: about-reporting
discoiquuid: bbb41c38-12c1-4625-85d5-69627e2f4b39

internal: n
snippet: y
---

# About dynamic reports{#about-dynamic-reports}

>[!NOTE]
>
>Only users with administration rights or with organizational units set to **All** can create or save a new report. For more on this, refer to this [section](../../administration/using/types-of-users.md).

## Accessing dynamic reports {#accessing-dynamic-reports}

![](assets/dynamic_report_intro.png)

Thanks to its drag and drop menu and customizable visualizations, the dynamic reports feature allows you to combine dimensions, metrics and time range in any combination, with unlimited breakdowns and comparisons.

Adobe Campaign's dynamic reports is designed to be a flexible freeform environment where you can explore data. The workspace offers a set of real-time reports to monitor deliveries, campaigns, and programs and measure their impact on recipients.

Reports can be accessed:

* From the home page by selecting **[!UICONTROL Reports]** tab in the top bar or the **[!UICONTROL Reports]** card to access reports for all deliveries.

  ![](assets/campaign_reports_access.png)

* In each program, campaign, and message, from the **Reports** button by clicking **Dynamic Reports** to only view the reports specific to the delivery.

  ![](assets/campaign_reports_description.png)

Certain reports cannot be available immediately after a delivery, depending on the time it takes to collect and process information.

Dynamic reports are divided into two categories:

* **Templates**, which can be modified by copying them using the **Save as** option (**Project > Save As..**) in the template.
* **Custom reports** (identified in blue), which can be directly created by clicking the **Create New Project** button on the **Reports** home page.

>[!NOTE]
>
>Data are filtered depending of your organizational units.

![](assets/dynamic_report_overview.png)

**Related topics:**

* [Report list](../../reporting/using/defining-the-report-period.md)
* [Organizational units](../../administration/using/organizational-units.md)
* [Dynamic reports](https://helpx.adobe.com/campaign/kt/acs/using/acs-creating-a-dynamic-report-feature-video-use.html) video

## Dynamic reporting usage agreement {#dynamic-reporting-usage-agreement}

Dynamic reports allow you to filter your report based on profile data with the profile dimensions.

The profile dimensions can only be displayed and used in your reports after accepting the Dynamic reporting usage agreement. By default, the agreement is only visible and can only be accepted or declined by users assigned with administration rights.

This agreement allows the transfer and storage in the United States of the following profile data: city, country/region, state, gender and segments on the age basis.

By accepting this agreement, every European and non-European data will be transferred to the United States.

![](assets/pii_window.png)

Three options are available:

* **[!UICONTROL Ask me later]**: By clicking Ask me later, the window will stop showing for 24 hours.
* **[!UICONTROL Accept]**: By accepting this agreement, you authorize Adobe Campaign to collect your customers' Personal identification information and to transfer them to the United States.
* **[!UICONTROL Decline]**: By declining the agreement, the profile dimensions will not appear in your reports and your customers' Personal identification information will not be collected or sent.

This choice is not final, you can always change it by selecting **[!UICONTROL Enable PII data to be transferred to US region to use reporting on Profile data]** in **[!UICONTROL Administration]** > **[!UICONTROL Application Settings]** > **[!UICONTROL Options]**.

The value can be changed at any time. The value -1 corresponds to **[!UICONTROL Ask me later]**, 1 **[!UICONTROL Accept]** and 0 **[!UICONTROL Decline]**.

![](assets/pii_window_2.png)

