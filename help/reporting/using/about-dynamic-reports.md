---
title: About dynamic reports
seo-title: About dynamic reports
description: About dynamic reports
seo-description: With dynamic reports, drag and drop variables and dimensions into your freeform environment and analyze the success of your campaigns.
uuid: a068ff0a-0571-438a-b588-4f266bdb68d1
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/reporting/using/about-dynamic-reports
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-17T07 15 21.368-0400
cq-lastmodifiedby: mancini
cq-lastreplicated: 2018-09-11T08 43 16.331-0400
cq-lastreplicatedby: beneat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: reporting
content-type: reference
topic-tags: about-reporting
cq-template: /apps/help/templates/article-3
discoiquuid: f742dc8a-1c61-4b23-93f5-c52c54b16993
firstPublishExternalDate: 2018-09-07T14:59:50.868-0400
firstpublishinternaldate: 2018-09-11T08 43 16.310-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 23.599-0400
jcr-createdby: admin
jcr-description: About dynamic reports
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-11T08:43:16.310-0400
lastpublishinternaldate: 2018-09-11T08 43 16.310-0400
lochandoffdate: 2018-09-17T07 15 21.368-0400
loclangtag: locales fr;locales de
lr-lastreplicatedby: beneat@adobe.com
moreHelpPaths: /content/help/en/campaign/standard/reporting/morehelp/about-reporting;/content/help/en/campaign/standard/reporting/morehelp/about-reporting
navTitle: About dynamic reports
publishexternaldate: 2018-09-11T08 43 16.310-0400
publishExternalURL: "https://helpx.adobe.com/campaign/standard/reporting/using/about-dynamic-reports.html"
publishinternaldate: 2018-09-11T08 43 16.310-0400
publishinternalurl: https //helpx-internal.corp.adobe.com/content/help/en/campaign/standard/reporting/using/about-dynamic-reports.html
sha1: 78e9210a541f04241d5ae9b371b92b3c02f4b91e
topicBrowsingSortDate: 2018-09-11T08:43:16.310-0400
index: y
internal: n
snippet: y
---

# About dynamic reports{#about-dynamic-reports}

About dynamic reports

>[!NOTE]
>
>Only users with administration rights or with organizational and geographical units set to **All** can create or save a new report. For more on this, refer to this [section](../../administration/using/about-access-management.md#main-pars_text_27).

## Accessing dynamic reports {#accessing-dynamic-reports}

![](assets/dynamic_report_intro.png)

Thanks to its drag and drop menu and customizable visualizations, the dynamic reports feature allows you to combine dimensions, metrics and time range in any combination, with unlimited breakdowns and comparisons.

Adobe Campaign's dynamic reports is designed to be a flexible freeform environment where you can explore data. The workspace offers a set of real-time reports to monitor deliveries, campaigns, and programs and measure their impact on recipients.

Reports can be accessed:

* From the home page by selecting **Reports** tab in the top bar or the **Reports** card to access reports for all deliveries.

  ![](assets/campaign_reports_access.png)

* In each program, campaign, and message, from the **Reports** button by clicking **Dynamic Reports** to only view the reports specific to the delivery.

  ![](assets/campaign_reports_description.png)

Certain reports cannot be available immediately after a delivery, depending on the time it takes to collect and process information.

Dynamic reports are divided into two categories:

* **Templates**, which can be modified by copying them using the **Save as** option (**Project > Save As..**) in the template.
* **Custom reports** (identified in blue), which can be directly created by clicking the **Create New Project** button on the **Reports** home page.

>[!NOTE]
>
>Data are filtered depending of your geographical and organizational units.

![](assets/dynamic_report_overview.png)

**Related topics:**

* [Report list](../../reporting/using/defining-the-report-period.md)
* [Organizational and geographical units](../../administration/using/organizational-and-geographical-units.md)
* [Dynamic reports](http://docs.campaign.adobe.com/doc/standard/en/GST_Tutorials_How-to_videos.html) video

## Dynamic reporting usage agreement {#dynamic-reporting-usage-agreement}

Dynamic reports allow you to filter your report based on profile data with the profile dimensions.

The profile dimensions can only be displayed and used in your reports after accepting the Dynamic reporting usage agreement. By default, the agreement is only visible and can only be accepted or declined by users assigned with administration rights.

This agreement allows the transfer and storage in the United States of the following profile data: city, country, state, zip code, gender and segments on the age basis.

By accepting this agreement, every European and non-European data will be transferred to the United States.

![](assets/PII_window.png)

Three options are available:

* **Ask me later**: By clicking Ask me later, the window will stop showing for 24 hours.
* **Accept**: By accepting this agreement, you authorize Adobe Campaign to collect your customers' Personal identification information and to transfer them to the United States.
* **Decline**: By declining the agreement, the profile dimensions will not appear in your reports and your customers' Personal identification information will not be collected or sent.

This choice is not final, you can always change it by selecting **Enable PII data to be transferred to US region to use reporting on Profile data** in **Administration** > **Application Settings** > **Options**.

The value can be changed at any time. The value -1 corresponds to **Ask me later**, 1 **Accept** and 0 **Decline**.

![](assets/PII_window_2.png)

