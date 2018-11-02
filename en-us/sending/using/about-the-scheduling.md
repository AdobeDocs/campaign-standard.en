---
title: About the scheduling
seo-title: About the scheduling
description: About the scheduling
seo-description: Discover the scheduling feature.
page-status-flag: never-activated
uuid: 82072927-c06e-4b80-9ccd-64ebdab95e77
content-encoding: UTF-8
aemsrcnodepath: /content/help/en/campaign/standard/sending/using/about-the-scheduling
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-01-23T08 51 07.958-0500
cq-lastmodifiedby: simonetn
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: sheduling-messages
cq-template: /apps/help/templates/article-3
discoiquuid: 27e41592-4aff-4ed4-b307-1b3384c22a1e
firstPublishExternalDate: 2018-01-10T15:31:16.749-0500
herogradient: light
jcr-created: 2018-01-24T19 01 37.640-0500
jcr-createdby: admin
jcr-description: About the scheduling
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-01-23T08:51:07.951-0500
lr-lastreplicatedby: simonetn@adobe.com
moreHelpPaths: /content/help/en/campaign/standard/sending/morehelp/sheduling-messages;/content/help/en/campaign/standard/sending/morehelp/sheduling-messages
navTitle: About the scheduling
publishexternaldate: 2018-01-23T08 51 07.951-0500
publishExternalURL: https://helpx.adobe.com/campaign/standard/sending/using/about-the-scheduling.html
sha1: f4beb4c5bc9a509ee5e2721290ebd8090dfffbf9
topicBrowsingSortDate: 2018-01-23T08:51:07.951-0500
index: y
internal: n
snippet: y
---

# About the scheduling

About the scheduling

In the delivery dashboard, the **Schedule** block allows you to choose when you want to send the message.

![](assets/delivery_dashboard.png)

The **Schedule** screen has two options:

![](assets/delivery_planning.png)

* **Messages to be sent once confirmed**: The message is sent as soon as the send is confirmed. See [Confirming send](../../sending/using/confirming-send.md).
* **Messages to be sent automatically on the date specified below**: The message will be sent at a later date and time. Specify the **contact date** in the **Start sending from** field.

  You can prepare and confirm the send, but the messages will only be sent on the selected date and time.

  >[!CAUTION]
  >
  >Whenever making changes to a delivery’s schedule, be sure to re-prepare the delivery by clicking on the **Prepare** button before clicking **Confirm**.

  Preparing and confirming the send are presented in the [Preparing the send](../../sending/using/preparing-the-send.md) and [Confirming send](../../sending/using/confirming-send.md) sections.

  The **Time zone of the contact date** drop-down list allows you to modify the time zone that will be taken into account for the sending time.

  For example, if you enter 9:00 AM in the **Start sending from** field and if you select Brussels, Copenhagen, Madrid, Paris (GMT+1) in the **Time zone of the contact date** drop-down list, all recipients will receive the message at 9:00 AM Paris time. Therefore, a recipient located in Moscow (GMT+3) will receive the message at 11:00 AM Moscow time.

  >[!NOTE]
  >
  >The default time zone is the time zone the user is currently in.

  If you would like to manually confirm the send, check the **Request confirmation before sending messages** box. This option is enabled by default.

  >[!CAUTION]
  >
  >When duplicating a delivery, all scheduling settings are deleted. Unless you schedule a new contact date, the duplicated delivery will be sent as soon as the send is confirmed.

