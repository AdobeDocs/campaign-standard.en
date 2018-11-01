---
title: Bounce summary
seo-title: Bounce summary
description: Bounce summary
seo-description: With the Bounce summary out-of-the-box report, learn about the status of your sent campaigns and errors they may have encountered.
uuid: f59124f4-63a4-46bb-b694-c7589a9dabc0
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/reporting/using/bounce-summary
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-27T03 26 40.765-0400
cq-lastreplicated: 2018-07-23T06 00 14.754-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: reporting
content-type: reference
topic-tags: list-of-reports
cq-template: /apps/help/templates/article-3
discoiquuid: d836b6e2-c136-467b-babf-a495d999ea01
firstPublishExternalDate: 2018-07-23T06:00:14.715-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 37.395-0400
jcr-createdby: admin
jcr-description: Bounce summary
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T06:00:14.715-0400
lochandoffdate: 2018-07-27T03 26 40.764-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Bounce summary
publishexternaldate: 2018-07-23T06 00 14.715-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/reporting/using/bounce-summary.html
sha1: 1589103219286027f4be58e2184b0517ceeb06fe
topicBrowsingSortDate: 2018-07-23T06:00:14.715-0400
index: y
internal: n
snippet: y
---

# Bounce summary

Bounce summary

This report details the overall hard and soft errors encountered during deliveries as well as the automatic processing of bounces.

![](assets/campaign_reports_bounces.png)

Each table is represented by summary numbers and charts. You can change how the details are shown in their respective visualization settings.

**Flop 5 repartition** lists the five deliveries with the highest number of quarantines:

The **Bounce reasons** table contains the available data for the types of errors that caused bounces for each delivery:

* **User unknown**: The type of error generated when a delivery is sent to an invalid email address.
* **Invalid domain**: The type of error generated when a delivery is sent to an email address whose domain is wrong or no longer exists.
* **Unreachable**: The type of error encountered in the message delivery string. For example, SMTP relay incident, domain temporarily unreachable, etc. 
* **Account disabled**: The type of error generated when a delivery is sent to an email address that no longer exists.
* **Mailbox full**: The type of error generated when the recipient's inbox is full. There are five attempts to deliver the message before this error is generated.
* **Not connected**: The type of error generated when the recipient's mobile phone is off or it is not connected to a network at the time the message is sent.

  >[!NOTE]
  >
  >This type of error only concerns deliveries on mobile channels.

* **Refused**: The type of error generated when an address is refused by the Internet service provider (ISP). For example, when a security rule has been applied by anti-Spam software.

The **Domain repartition** table displays the overall problems encountered during the deliveries according to the recipient domain.
