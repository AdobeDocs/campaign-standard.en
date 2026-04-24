---
title: Get started with dynamic reports
description: With dynamic reports, drag and drop variables and dimensions into your freeform environment and analyze the success of your campaigns.
audience: reporting
content-type: reference
topic-tags: about-reporting
feature: Reporting
role: Leader
level: Beginner
exl-id: fc3b28f3-63f6-4edc-923d-c7eb7925d1b7
TQID: https://experienceleague.adobe.com/L392oFEzYUkSajzO3Gi7gjWLmDrpbOhW24k1OXFmoRc
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
feature_v2:
  - id: a075b2c1-7748-4328-b7f6-343aa314616a
    internal-label: Campaigns
  - id: c309ee4e-82e4-4f7e-b608-ef345678c34e
    internal-label: Dynamic reporting
  - id: c5474392-5419-4296-9e41-f6f4ce4f6e9b
    internal-label: Administration
subfeature_v2:
  - id: ca3c1dd6-bdd2-41a9-bc5a-e35f5cca9e63
    internal-label: Application settings
role_v2:
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Get started with dynamic reports {#about-dynamic-reports}

Dynamic Reporting provides fully customizable and real-time reports. It adds access to profile data, enabling demographic analysis by profile dimensions such as gender, city and age in addition to functional email campaign data like opens and clicks. With the drag-and-drop interface, you can explore data, determine how your email campaigns performed against your most important customer segments and measure their impact on recipients.

>[!NOTE]
>
>Only users with administration rights or with organizational units set to **All** can create or save a new report. For more on this, refer to this [section](../../administration/using/users-management.md).

## Accessing dynamic reports {#accessing-dynamic-reports}

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

## Dynamic reporting usage agreement {#dynamic-reporting-usage-agreement}

The Dynamic reporting usage agreement's purpose is to function as a pop-up consent for data processing. By default, the agreement is only visible and can only be accepted or declined by users assigned with administration rights.

Three options are available:

* **[!UICONTROL Ask me later]**: By clicking **Ask me later**, the window will stop showing for 24 hours. Until you accept or decline the agreement, the profile dimensions will not appear in your reports and your customers' Personal identification information will not be collected or sent.
* **[!UICONTROL Accept]**: By accepting this agreement, you authorize Adobe Campaign to collect your customers' Personal identification information and to transfer them to the reporting or data center.
* **[!UICONTROL Decline]**: By declining the agreement, the profile dimensions will not appear in your reports and your customers' Personal identification information will not be collected or sent. Note that in this case externalID will still be collected and used to identify end-users.

The table below displays what happens after accepting with this agreement depending on your region.

|  |Dynamic reporting|Microsoft Dynamics 365 connector|
|---|---|---|
|Americas & APAC (Asia Pacific)| **Feature available**. <br>All out-of-the-box (i.e. city, country/region, state, gender and segments on the age basis) & custom profiles information pushed into the US reporting center. For more information on profile dimensions, refer to this [page](../../reporting/using/list-of-components.md) |**Feature available**. <br>All out-of-the-box & custom profiles fields and Adobe Campaign Standard event fields are processed in the US data center.|
|EMEA (Europe Middle East & Africa)|**Feature available**. <br>All out-of-the-box (i.e. city, country/region, state, gender and segments on the age basis) & custom profiles information pushed into the EMEA reporting center. For more information on profile dimensions, refer to this [page](../../reporting/using/list-of-components.md)|**Feature available.** <br>All out-of-the-box & custom profiles fields and Adobe Campaign Standard event fields processed in the EMEA data center. <br>**[!UICONTROL Control data]** which contains Adobe I/O registration data and IDs of customer end-user events sent and stored in the US data center.|

The table below displays what happens after declining this agreement depending on your region. Note that even if you decline this agreement, reporting on deliveries and Microsoft Dynamics 365 integration will still be available.

|  Region |Dynamic reporting|Microsoft Dynamics 365 connector|
|---|---|---|
|Americas & APAC (Asia Pacific)|**Feature available**. <br> No out-of-the-box & custom profiles information pushed into the US reporting center with the exception of ExternalID.|**Feature available**. <br>No out-of-the-box or custom profile fields sent to the US data center with the exception of External ID and Recipient ID. <br>All Adobe Campaign Standard event fields processed in the US data center with the exception of mirror page ID. <br>For more information on Microsoft Dynamics 365 integration, refer to this [page](../../integrating/using/d365-acs-get-started.md).|
|EMEA (Europe Middle East & Africa)|**Feature available**. <br>No out-of-the-box & custom profiles information pushed into the EMEA reporting center with the exception of ExternalID.|**Feature available.** <br>No out-of-the-box or custom profile fields sent to the EMEA data center with the exception of External ID and Recipient ID. <br>All Adobe Campaign Standard event fields processed in the EMEA data center with the exception of mirror page ID.  <br>**[!UICONTROL Control data]** which contains Adobe I/O registration data and IDs of customer end-user events sent and stored in the US data center.<br>For more information on Microsoft Dynamics 365 integration, refer to this [page](../../integrating/using/d365-acs-get-started.md).|

This choice is not final, you can always change it by selecting **[!UICONTROL Enable PII data to be transferred to US region to use reporting on Profile data]** in **[!UICONTROL Administration]** > **[!UICONTROL Application Settings]** > **[!UICONTROL Options]**.

The value can be changed at any time. The value 1 corresponds to **[!UICONTROL Ask me later]**, 2 **[!UICONTROL Decline]** and 3 **[!UICONTROL Accept]**.

![](assets/pii_window_2.png)
