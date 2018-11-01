---
title: Personalizing sender
seo-title: Personalizing sender
description: Personalizing sender
seo-description: Learn how to personalize the name or the address of the sender for your messages.
uuid: 2245065d-b7db-4984-b976-e9ff5a61ff93
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/designing/using/personalizing-sender
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-06-25T08 45 04.727-0400
cq-lastreplicated: 2018-06-14T08 43 41.183-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: editing-message-and-landing-page-content
cq-template: /apps/help/templates/article-3
discoiquuid: 1b9627d1-ddbf-4011-bd72-63a9dd8f6f56
firstPublishExternalDate: 2018-06-14T08:43:41.162-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 01 40.292-0400
jcr-createdby: admin
jcr-description: Personalizing sender
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-06-14T08:43:41.162-0400
lochandoffdate: 2018-06-25T08 45 04.726-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Personalizing sender
publishexternaldate: 2018-06-14T08 43 41.162-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/designing/using/personalizing-sender.html
sha1: 2de384e072ddf6e21143b5193163f04013086300
topicBrowsingSortDate: 2018-06-14T08:43:41.162-0400
index: y
internal: n
snippet: y
---

# Personalizing sender

Personalizing sender

## <p>Email sender</p>

To define the name of the sender which will appear in the header of messages sent, click the **Content** block.

![](assets/delivery_content_edition16.png)

The **From (name)** field allows you to enter the sender name. By default, the **Default sender name** is automatically entered in the field. Adobe Campaign refers to the email channel configuration (from the advanced menu **Administration &gt; Channels &gt; Email &gt; Email accounts** via the Adobe Campaign logo) to designate this sender.

You can change the sender name by selecting the field then clicking the X icon that appears to its right. The field then becomes editable and you can enter the name you would like to use.

![](assets/delivery_content_edition17.png)

This field can be personalized. To do this, you must use personalization fields, inserted via the **Sender** button, to the right of the input field. Inserting and using the personalization fields is detailed in the [Adding a personalization field](../../designing/using/adding-a-personalization-field.md) section.

The **From (email address)** field cannot be edited from the **Content** block. You can change it by editing the properties of the email from its dashboard. For more on this, refer to [List of email advanced parameters](../../administration/using/configuring-email-channel.md#list-of-email-advanced-parameters).

>[!NOTE]
>
>The header parameters must not be empty. The sender's address is mandatory to allow an email to be sent (RFC standard). Adobe Campaign checks the syntax of email addresses entered.

## <p>SMS sender</p>

You can personalize the name of the SMS sender. For more on this, refer to the [SMS configuration](../../administration/using/configuring-sms-channel.md) section.
