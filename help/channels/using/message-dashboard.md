---
title: Message dashboard
seo-title: Message dashboard
description: Message dashboard
seo-description: Discover what the message dashboard is made up of, including the action bar and the various functional blocks.
uuid: 648b9089-9608-4af5-9714-7d61181e8243
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/channels/using/message-dashboard
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-08T08 23 02.798-0400
cq-lastreplicated: 2018-09-07T15 11 32.541-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: about-communication-channels
cq-template: /apps/help/templates/article-3
discoiquuid: d49d24ea-9818-491f-9490-7d71bd0aeed1
firstPublishExternalDate: 2018-09-07T15:11:32.375-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 01 16.792-0400
jcr-createdby: admin
jcr-description: Message dashboard
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T15:11:32.375-0400
lochandoffdate: 2018-09-08T08 23 02.798-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Message dashboard
publishexternaldate: 2018-09-07T15 11 32.375-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/channels/using/message-dashboard.html
sha1: cd0b25a59af3b6fae94a74175207d2c2dfb619a8
topicBrowsingSortDate: 2018-09-07T15:11:32.375-0400
index: y
internal: n
snippet: y
---

# Message dashboard{#message-dashboard}

Message dashboard

The message dashboard is a workspace made up of different icons - regrouped into an action bar - and various functional blocks that allow you to establish your message's parameters and send it. These elements are presented hereafter.

![](assets/delivery_dashboard_2.png)

## Gray bar {#gray-bar}

The gray bar regroups various icons linked to your message.

* **Summary**: shows/hides the main information regarding the message.
* **Edit properties**: lets you edit the message's advanced parameters.
* **Reports**: gives you access to the reports relating to the message.

**Related topics**

* [Configuring channels](../../administration/using/about-channel-configuration.md)
* [Accessing reports](../../reporting/using/about-dynamic-reports.md)

## Action bar {#action-bar}

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

  For more on confirming sending, see [Sending messages](../../sending/using/confirming-the-send.md).

## Blocks {#blocks}

The main screen is made up of different blocks. Click inside a block to access the corresponding parameter screen:

![](assets/delivery_dashboard_3.png)

* **Deployment**: allows you to track the progress of the message preparation or send. Click the button found in the lower right section of this block to access the send and analysis logs. This block only appears once the send has been prepared. For more on this. See [Confirming send](../../sending/using/confirming-the-send.md).
* **Audience**: allows you to establish the message's main target as well as the test profiles. See [Creating audiences](../../audiences/using/creating-audiences.md).
* **Schedule**: allows you to specify the date on which your message will be sent. See [Scheduling](../../sending/using/about-scheduling-messages.md).
* **Content**: allows you to define the message's content and preview it. See [Defining content](../../designing/using/designing-content-in-adobe-campaign.md).

