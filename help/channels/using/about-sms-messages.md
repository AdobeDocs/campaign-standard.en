---
title: About SMS messages
seo-title: About SMS messages
description: About SMS messages
seo-description: Discover the main specificities of the SMS channel in Adobe Campaign.
uuid: ccc6bdf6-c641-40df-aec5-180025a80a7c
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/channels/using/about-sms-messages
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-08T08 23 07.427-0400
cq-lastreplicated: 2018-09-07T15 11 46.781-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: sms-messages
cq-template: /apps/help/templates/article-3
discoiquuid: f682039f-bbab-4e4b-a732-b1f9d62b975e
firstPublishExternalDate: 2018-09-07T15:11:46.712-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 01 19.452-0400
jcr-createdby: admin
jcr-description: About SMS messages
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T15:11:46.712-0400
lochandoffdate: 2018-09-08T08 23 07.427-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: About SMS messages
publishexternaldate: 2018-09-07T15 11 46.712-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/channels/using/about-sms-messages.html
sha1: 4dd7436cbca884bd14c267b4b318d6ae9278a092
topicBrowsingSortDate: 2018-09-07T15:11:46.712-0400
index: y
internal: n
snippet: y
---

# About SMS messages{#about-sms-messages}

About SMS messages

Adobe Campaign allows you to deliver SMS (Short Message Service) messages.

>[!NOTE]
>
>SMS channel is an add-on. Please check your license agreement.

For SMS messages, you can create, modify, and personalize messages in text format only. You can also preview your SMS messages before they are sent.

The length of an SMS message is restricted to 160 characters if it is in GSM encoding and only 70 characters if it is in Unicode. However, certain special characters can influence the length of the message. For more on this, refer to the [SMS encoding](../../administration/using/configuring-sms-channel.md#sms-encoding--length-and-transliteration) section.

SMS messages can be created from the **Marketing activities** menu, from a campaign, or in a workflow, see [Creating an SMS message](../../channels/using/creating-an-sms-message.md).

To deliver SMS messages to a mobile telephone you need:

* A **Routing** external account configured on the **Mobile (SMS)** channel with the **Bulk delivery** mode. For more on this, refer to the [Routing](../../administration/using/configuring-sms-channel.md#defining-an-sms-routing) section.
* A delivery template that is correctly linked to this external account.

**Related topics:**

* [Managing templates](../../start/using/about-templates.md)
* [SMS configuration](../../administration/using/configuring-sms-channel.md#defining-an-sms-routing)

## SMS delivery template {#sms-delivery-template}

Adobe Campaign offers a delivery template for mobile devices. This template must be correctly linked to the external account used for the **Mobile (SMS)** channel. To access and modify it:

1. Select **Resources** > **Templates** > **Delivery templates** from the advanced menu.
1. Hover over the **Send via SMS** template with the mouse and select the **Duplicate element** option.
1. Select the new template.
1. Click the **Edit properties** button.
1. In the **Advanced parameters** section of the template properties, make sure that the template is linked to the external account to be used for delivering SMS.

   ![](assets/sms_template.png)

**Related topics:**

* [Managing templates](../../start/using/about-templates.md)

