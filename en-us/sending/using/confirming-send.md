---
title: Confirming send
seo-title: Confirming send
description: Confirming send
seo-description: Learn how to finalize the message preparation.
uuid: ceba74cb-c49b-4d2a-a119-fe5dbd57e43d
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/sending/using/confirming-send
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-30T04 53 55.477-0400
cq-lastreplicated: 2018-07-23T06 02 24.540-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: sending-and-tracking-messages
cq-template: /apps/help/templates/article-3
discoiquuid: 171085d8-0c01-4d1c-8a67-ae683799848b
firstPublishExternalDate: 2018-07-23T06:02:24.492-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 01 19.690-0400
jcr-createdby: admin
jcr-description: Confirming send
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T06:02:24.492-0400
lochandoffdate: 2018-07-30T04 53 55.477-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Confirming send
publishexternaldate: 2018-07-23T06 02 24.492-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/sending/using/confirming-send.html
sha1: 97ae329ac9e2670b0aae633fac4996c44fb0bcd3
topicBrowsingSortDate: 2018-07-23T06:02:24.492-0400
index: y
internal: n
snippet: y
---

# Confirming send

Confirming send

Once you have finished preparing your messages and the approval steps have been carried out, you can send them. For more on messages preparation, refer to [Preparing the send](../../sending/using/preparing-the-send.md).

Only users with the **Start deliveries** role can confirm send. For more on this, refer to the [List of roles](../../administration/using/list-of-roles.md) section.

Users without this role will see the following message: 

![](assets/confirm_delivery_2.png)

To send your delivery, click the **Confirm send** button found in the message's action bar.

![](assets/confirm_delivery.png)

You will be asked to finalize the send definitively by clicking the **OK** button.

![](assets/confirm_delivery1.png)

The message is being sent.

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

The delivery can be viewed in the history of one of the client profiles that makes up part of the delivery's audience. See [Integrated customer profile](../../audiences/using/integrated-customer-profile.md).

Once a delivery is sent, you can track the behavior of its recipients, and monitor it in order to measure its impact. For more on this, refer to these sections:

* [Tracking messages](../../sending/using/tracking-messages.md)
* [Monitoring a delivery](../../sending/using/monitoring-a-delivery.md)

