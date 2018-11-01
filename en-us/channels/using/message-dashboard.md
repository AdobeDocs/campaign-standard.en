---
title: Message dashboard
seo-title: Message dashboard
description: Message dashboard
seo-description: Discover what the message dashboard is made up of, including the action bar and the various functional blocks.
uuid: 17b4bdf3-50fa-4216-85c5-f52ee87d3f5c
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/channels/using/message-dashboard
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-30T04 53 47.223-0400
cq-lastreplicated: 2018-07-23T06 02 39.048-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: about-communication-channels
cq-template: /apps/help/templates/article-3
discoiquuid: dde5db50-cc54-4b74-899e-f6d5a9339b5d
firstPublishExternalDate: 2018-07-23T06:02:38.973-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 01 16.792-0400
jcr-createdby: admin
jcr-description: Message dashboard
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T06:02:38.973-0400
lochandoffdate: 2018-07-30T04 53 47.223-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Message dashboard
publishexternaldate: 2018-07-23T06 02 38.973-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/channels/using/message-dashboard.html
sha1: 22f504a2ca478995ba60d4b8c6a1191b02f37bb3
topicBrowsingSortDate: 2018-07-23T06:02:38.973-0400
index: y
internal: n
snippet: y
---

# Message dashboard

Message dashboard

The message dashboard is a workspace made up of different icons - regrouped into an action bar - and various functional blocks that allow you to establish your message's parameters and send it. These elements are presented hereafter.

![](assets/delivery_dashboard_2.png)

## <p>Gray bar</p>

The gray bar regroups various icons linked to your message.

* **Summary**: shows/hides the main information regarding the message.
* **Edit properties**: lets you edit the message's advanced parameters.
* **Reports**: gives you access to the reports relating to the message.

**Related topics**

* [Configuring channels](../../administration/using/about-channel-configuration.md)
* [Accessing reports](../../reporting/using/about-dynamic-reports.md)

## <p>Action bar</p>

The action bar has different icons that allow you to interact with your message.

![](assets/delivery_dashboard_4.png)

Depending on the parameters that have been set up and the progress made, certain icons may not be available.

* **Show proofs**: shows/hides the list of proofs that have been sent, if they exist. This button is only enabled once you have sent proofs.

  For more on proofs, see [Managing test profiles and sending proofs](../../sending/using/managing-test-profiles-and-sending-proofs.md).

* **Send a test**: lets you select the approval mode to use: **Email rendering**, **Proof** or both for an email. For more on test profiles, see [Sending proofs](../../sending/using/managing-test-profiles-and-sending-proofs.md#sending-proofs).

  This button is only enabled once you have established test profiles.

  >[!NOTE]
  >
  >For an SMS message, there is no other choice: it is automatically a **Proof**.

* **Prepare send**: starts to prepare the send. The **Deployment** block appears and displays the result of the preparation. This button only appears once the target has been entered. You can stop preparation at any time using the corresponding button.

  For more on message preparation, [Preparing the send](../../sending/using/preparing-the-send.md).

* **Confirm send**: confirms sending the message. The sending statistics appear in the **Deployment** block. This button only appears after the send has been prepared. You can stop or pause the send at any time using the **Stop send** and **Pause** buttons.

  For more on confirming sending, see [Sending messages](../../sending/using/confirming-send.md).

## <p>Blocks</p>

The main screen is made up of different blocks. Click inside a block to access the corresponding parameter screen:

![](assets/delivery_dashboard_3.png)

* **Deployment**: allows you to track the progress of the message preparation or send. Click the button found in the lower right section of this block to access the send and analysis logs. This block only appears once the send has been prepared. For more on this. See [Confirming send](../../sending/using/confirming-send.md).
* **Audience**: allows you to establish the message's main target as well as the test profiles. See [Creating audiences](../../audiences/using/creating-audiences.md).
* **Schedule**: allows you to specify the date on which your message will be sent. See [Scheduling](../../sending/using/about-scheduling-messages.md).
* **Content**: allows you to define the message's content and preview it. See [Defining content](../../designing/using/designing-content-in-adobe-campaign.md).

