---
title: Breakdown by domains
description: With the Breakdown by domains out-of-the-box report, learn about the performance data of your deliveries depending on each of your customer's domain.
audience: reporting
content-type: reference
topic-tags: list-of-reports
context-tags: deliveryDomainBreakdownReport,main;campaignDomainBreakdownReport,main;programDomainBreakdownReport,main
feature: Reporting
role: Leader
level: Intermediate
exl-id: 513d74ae-10c0-4d41-a7d1-8ed655e1a2d1
TQID: https://experienceleague.adobe.com/25Ci4GFEJHIO3Ed2BTBF2qUmD4LKh3jwUC56K8JZgzA
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
role_v2:
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
---
# Breakdown by domains{#breakdown-by-domains}

This report contains the performance data for each domain represented in the audience for an email delivery. If it is a campaign or program report, the performance data is available for multiple audiences. This data allows you to analyze the behavior of each domain in reaction to specific events. For example, link display, URL on denylist, etc.

![](assets/delivery_reports_6.png)

The table **Broadcast statistics** contains the available data for possible errors encountered with each domain, such as:

* **Processed/sent**: The number of emails sent.
* **Delivered**: The number of emails delivered.
* **Bounces + Errors**: The number of messages that could not be delivered.
* **Hard bounce**: The total number of permanent errors, such as a wrong email address.
* **Soft bounce**: The total number of temporary errors, such as a full inbox.

The second table, **Tracking statistics**, contains the available data for recipient reactivity to delivery, such as:

* **Delivered**: The number of emails delivered
* **Open**: The number of times a message was opened in a delivery.
* **Click**: The number of times content was clicked in a delivery.
* **Unsubscribed**: The number of clicks on the subscription link.
* **Mirror Page**: The number of clicks on the mirror page link.
* **On denylist**: The number of recipients who have declared an email as spam or junk. [Learn more](../../audiences/using/about-opt-in-and-opt-out-in-campaign.md)
