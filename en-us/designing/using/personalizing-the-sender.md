---
title: Personalizing the sender
seo-title: Personalizing the sender
description: Personalizing the sender
seo-description: Learn how to personalize the name or the address of the sender for your messages.
uuid: 5e3c2a9f-e176-4b0f-bb2c-9a9b00ee9add
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/designing/using/personalizing-the-sender
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-26T02 53 53.760-0400
cq-lastreplicated: 2018-07-23T08 13 51.475-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: personalizing-content
cq-template: /apps/help/templates/article-3
discoiquuid: d15892f1-3c8e-4937-bbd7-b72552995dc0
firstPublishExternalDate: 2018-07-23T05:58:40.385-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-07-23T07 30 14.080-0400
jcr-createdby: admin
jcr-description: Personalizing the sender
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T08:13:51.434-0400
lochandoffdate: 2018-07-26T02 53 53.760-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Personalizing the sender
publishexternaldate: 2018-07-23T08 13 51.434-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/designing/using/personalizing-the-sender.html
sha1: f9259b3da3f0465b086e6db283f6ea443d9b9298
topicBrowsingSortDate: 2018-07-23T08:13:51.434-0400
index: y
internal: n
snippet: y
---

# Personalizing the sender

Personalizing the sender

## <p>Email sender</p>

To define the name of the sender which will appear in the header of messages sent, click the **Content** block.

![](assets/delivery_content_edition16.png)

The **From (name)** field allows you to enter the sender name. By default, the **Default sender name** is automatically entered in the field. Adobe Campaign refers to the email channel configuration (from the advanced menu **Administration > Channels > Email > Email accounts** via the Adobe Campaign logo) to designate this sender.

You can change the sender name by clicking the pencil that appears to its right. The field then becomes editable and you can enter the name you would like to use.

This field can be personalized. (To do this, you must use personalization fields, inserted via the **Sender** button, to the right of the input field.) Inserting and using the personalization fields is detailed in the [Inserting a personalization field](../../designing/using/inserting-a-personalization-field.md) section.

The **From (email address)** field cannot be edited from the **Content** block. You can change it by editing the properties of the email from its dashboard. For more on this, refer to [List of email advanced parameters](../../administration/using/configuring-email-channel.md#list-of-email-advanced-parameters).

>[!NOTE]
>
>The header parameters must not be empty. The sender's address is mandatory to allow an email to be sent (RFC standard). Adobe Campaign checks the syntax of email addresses entered.

## <p>SMS sender</p>

You can personalize the name of the SMS sender. For more on this, refer to the [SMS configuration](../../administration/using/configuring-sms-channel.md#configuring-sms-properties) section.
