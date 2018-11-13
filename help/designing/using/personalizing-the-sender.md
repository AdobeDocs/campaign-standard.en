---
title: Personalizing the sender
seo-title: Personalizing the sender
description: Personalizing the sender
seo-description: Learn how to personalize the name or the address of the sender for your messages.
uuid: cd306696-4d1f-4c87-9b06-676dd14f7ed6
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/designing/using/personalizing-the-sender
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-10T07 25 19.746-0400
cq-lastmodifiedby: mancini
cq-lastreplicated: 2018-09-07T15 01 22.032-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: personalizing-content
cq-template: /apps/help/templates/article-3
discoiquuid: 332c3808-6408-4b38-bca0-5e52ea8c0a5c
firstPublishExternalDate: 2018-09-07T15:01:15.134-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-07-23T07 30 14.080-0400
jcr-createdby: admin
jcr-description: Personalizing the sender
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T15:01:15.134-0400
lochandoffdate: 2018-09-10T07 25 19.745-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
moreHelpPaths: /content/help/en/campaign/standard/designing/morehelp/personalizing-content;/content/help/en/campaign/standard/designing/morehelp/personalizing-content
navTitle: Personalizing the sender
publishexternaldate: 2018-09-07T15 01 15.134-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/designing/using/personalizing-the-sender.html
sha1: 5ff78a8d8f72ef0e1e1196ed76dcf434638809df
topicBrowsingSortDate: 2018-09-07T15:01:15.134-0400
index: y
internal: n
snippet: y
---

# Personalizing the sender{#personalizing-the-sender}

Personalizing the sender

## Email sender {#email-sender}

To define the name of the sender which will appear in the header of messages sent:

* In the [Creative Designer](../../designing/using/about-email-content-design.md#using-the-creative-designer), click the **Email properties** icon next to the email's label.

  ![](assets/delivery_content_edition16.png)

* In the [content editor](../../designing/using/about-email-content-design.md#using-the-email-content-editor), go to the upper part of the screen.

  ![](assets/delivery_content_edition16_default.png)

The **From (name)** field allows you to enter the sender name. By default, the **Default sender name** is automatically entered in the field. Adobe Campaign refers to the email channel configuration (from the advanced menu **Administration > Channels > Email > Email accounts** via the Adobe Campaign logo) to designate this sender.

You can change the sender name by clicking the pencil that appears to its right. The field then becomes editable and you can enter the name you would like to use.

This field can be personalized. (To do this, you must use personalization fields, inserted via the **Sender** button, to the right of the input field.) Inserting and using the personalization fields is detailed in the [Inserting a personalization field](../../designing/using/inserting-a-personalization-field.md) section.

The **From (email address)** field cannot be edited from the **Content** block. You can change it by editing the properties of the email from its dashboard. For more on this, refer to [List of email advanced parameters](../../administration/using/configuring-email-channel.md#list-of-email-advanced-parameters).

>[!NOTE]
>
>The header parameters must not be empty. The sender's address is mandatory to allow an email to be sent (RFC standard). Adobe Campaign checks the syntax of email addresses entered.

## SMS sender {#sms-sender}

You can personalize the name of the SMS sender. For more on this, refer to the [SMS configuration](../../administration/using/configuring-sms-channel.md#configuring-sms-properties) section.
