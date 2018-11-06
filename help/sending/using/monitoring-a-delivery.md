---
title: Monitoring a delivery
seo-title: Monitoring a delivery
description: Monitoring a delivery
seo-description: Discover how to monitor a delivery.
uuid: 40bbd1c4-e41d-46d6-9706-45ce69654c23
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/sending/using/monitoring-a-delivery
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-08T08 23 10.284-0400
cq-lastreplicated: 2018-09-07T15 11 33.438-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: monitoring-messages
cq-template: /apps/help/templates/article-3
discoiquuid: 4116796a-2427-4dea-bc8a-12753bbc646a
firstPublishExternalDate: 2018-09-07T15:11:33.175-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 01 45.621-0400
jcr-createdby: admin
jcr-description: Monitoring a delivery
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T15:11:33.175-0400
lochandoffdate: 2018-09-08T08 23 10.284-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Monitoring a delivery
publishexternaldate: 2018-09-07T15 11 33.175-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/sending/using/monitoring-a-delivery.html
sha1: 22d48e168468cb6d9448158b00d3aeda708927f8
topicBrowsingSortDate: 2018-09-07T15:11:33.175-0400
index: y
internal: n
snippet: y
---

# Monitoring a delivery

Monitoring a delivery

There are several ways to monitor a delivery and to measure its impact:

* **Message logs**: These logs can be accessed directly from the message dashboard. They show the detail of the sending, which target has been excluded and why, as well as the tracking information such as opens and clicks.

  To view the message logs, click the icon at the bottom right of the **Deployment** block.

  Several tabs contain information (if it exists) regarding the **Sending logs**, **Exclusion logs**, **Exclusion causes**, **Tracking logs** and **Tracked URLs**. See [Delivery logs](../../sending/using/monitoring-a-delivery.md#delivery-logs).

  ![](assets/sending_delivery1.png)

  The log contains all messages relating to the delivery and the proofs. Specific icons allow you to identify errors or warnings. For more on this, see [Approving messages](../../sending/using/previewing-messages.md).

  You can export the log by clicking the **Export list** button.

  ![](assets/sending_delivery2.png)

* **Delivery alerts**: To keep track of delivery successes or failures, Adobe Campaign provides an email alerting system that sends notifications to inform users of important system activities.
* **Reports**: From the message dashboard, you can access several reports for this specific message. You also have a **Reports** menu that allows you to access a complete list of built-in or custom reports that you can use to outline specific metrics related to your message or campaign.
* An administrator can also export logs in a separate file that can be processed in your own reporting or BI tools. For more on this, see [Exporting logs](../../automating/using/exporting-logs.md).

**Related topics:**

* [Receiving alerts when failures happen](../../sending/using/receiving-alerts-when-failures-happen.md)
* [Reports](../../reporting/using/about-dynamic-reports.md)

## Delivery logs

### Sending logs

The **Sending logs** tab offers a history of every occurrence of this delivery. The list of sent messages and their statuses is stored here. It allows you to view the delivery status for each recipient.

For each profile with a **Sent** status, the **Date** column shows when the message was sent.

![](assets/sending_delivery3.png)

### Exclusion logs

The **Exclusion logs** tab lists all the messages that have been excluded from the target sent and specifies the reason for the send failure.

![](assets/sending_delivery4.png)

### Exclusion causes

The **Exclusion causes** tab displays the volume (in number of messages) of messages that were excluded from the target send.

![](assets/sending_delivery5.png)

