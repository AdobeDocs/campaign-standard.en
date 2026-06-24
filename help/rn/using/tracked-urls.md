---
title: Tracked URLs signature issue
description: Tracked URLs signature issue
hide: true
exl-id: 8c2725a8-2c3a-448a-8c04-c0c2a5950574
TQID: https://experienceleague.adobe.com/6R8s1OkdU0TWD2Qo1DnI33T-FsiV4kVNkn942k0o5-Q
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
---
# Tracked URLs signature issue {#tracked-urls}

Following recent changes, tracked URLs sent by Campaign can fail. Some mailboxes can be more impacted than others, as some companies have specific security tools which can impact links and alter the URL signature mechanism.

As a consequence, Adobe decided to disable the signature mechanism for tracking links. This procedure fixes all tracking links.

Note that unsubscription links can fail as any other links, the frequency is variable from host to host but is less than 1%.

**Are you impacted?**

Some Campaign Standard users are impacted as the signature mechanism for tracking links in emails has been introduced in [Campaign Standard 20.4](release-notes-2020.md#release-20-4---october-2020) - October 2020 - and is enabled by default for all customers.

**How to update?**

Adobe will be working with you to update your configuration shortly. You will receive an email notification with your upgrade timeline.

**What is the impact?**

The maintenance requires a maximum of 25-minutes downtime and during this period all the deliveries, tracking links and API calls will not work.

Once the update is done, all links work as expected.

>[!NOTE]
>
>For any questions about these changes, contact [Adobe Customer Care](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html).
>

