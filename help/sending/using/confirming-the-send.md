---
title: Confirming the send
seo-title: Confirming the send
description: Confirming the send
seo-description: Learn how to finalize the message preparation.
uuid: b877e701-5af9-48c0-a758-79e73106b222
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/sending/using/confirming-the-send
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-08T08 23 09.482-0400
cq-lastreplicated: 2018-09-07T15 11 27.652-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: sending-and-tracking-messages
cq-template: /apps/help/templates/article-3
discoiquuid: 3ad862d1-9b9b-4015-9b1f-c7533fe5784d
firstPublishExternalDate: 2018-09-07T15:11:27.467-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-11-06T09 43 32.032-0500
jcr-createdby: admin
jcr-description: Confirming the send
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T15:11:27.467-0400
lochandoffdate: 2018-09-08T08 23 09.482-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Confirming the send
publishexternaldate: 2018-09-07T15 11 27.467-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/sending/using/confirming-the-send.html
sha1: c2eca1e9da4284150c249d728df5bd6519d56580
topicBrowsingSortDate: 2018-09-07T15:11:27.467-0400
index: y
internal: n
snippet: y
---

# Confirming the send

Confirming the send

Once you have finished preparing your messages and the approval steps have been carried out, you can send them. For more on messages preparation, refer to [Preparing the send](../../sending/using/preparing-the-send.md).

Only users with the **Start deliveries** role can confirm send. For more on this, refer to the [List of roles](../../administration/using/list-of-roles.md) section.

Users without this role will see the following message: 

![](assets/confirm_delivery_2.png)

To send your delivery, click the **Confirm send** button found in the message's action bar.

![](assets/confirm_delivery.png)

You will be asked to finalize the send definitively by clicking the **OK** button.

![](assets/confirm_delivery1.png)

The message is being sent.

>[!NOTE]
>
>If the message is scheduled, it will be sent when sending time is reached. For more on scheduling messages, refer to [this section](../../sending/using/about-scheduling-messages.md).

The **Deployment** block shows the progress of the send.

Once the message is sent to the contacts, the **Deployment** zone shows your KPIs (Key Performance Indicator) data , including:

* The number of messages to deliver
* The number of messages sent
* The percentage of messages delivered
* The percentage of bounces and errors
* The percentage of open messages
* The percentage of clicks in the messages (for emails)

  >[!NOTE]
  >
  >The **Open rate** and **Click-through rate** are updated every hour.

![](assets/sending_delivery.png)

If the KPIs take too long to update or don't take into account the results from the sending logs, click the **Compute stats** button in the **Deployment** window.

![](assets/sending_delivery7.png)

The message can be viewed in the history of one of the client profiles that makes up part of the audience. See [Integrated customer profile](../../audiences/using/integrated-customer-profile.md).

Once a message is sent, you can track the behavior of its recipients, and monitor it in order to measure its impact. For more on this, refer to these sections:

* [Tracking messages](../../sending/using/tracking-messages.md)
* [Monitoring a delivery](../../sending/using/monitoring-a-delivery.md)

