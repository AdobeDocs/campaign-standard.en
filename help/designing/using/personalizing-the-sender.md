---
title: Personalizing the sender
seo-title: Personalizing the sender
description: Personalizing the sender
seo-description: Learn how to personalize the name or the address of the sender for your messages.
uuid: d00136ff-c0e1-4cf0-9dc4-9e759bf0bd8d
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: personalizing-content
discoiquuid: f68c8300-a081-43bb-a2b9-cd716e1ecb64
index: y
internal: n
snippet: y
---

# Personalizing the sender{#personalizing-the-sender}

Personalizing the sender

## Email sender {#email-sender}

To define the name of the sender which will appear in the header of messages sent, go the **[!UICONTROL Properties]** tab of the Email Designer home page (accessible through the home icon).

![](assets/delivery_content_edition16.png)

* The **[!UICONTROL From: name]** field allows you to enter the sender name. By default, the default **Sender name** block is automatically entered in the field. Adobe Campaign refers to the email channel configuration (from the advanced menu **[!UICONTROL Administration > Channels > Email > Email accounts]** via the Adobe Campaign logo) to designate this sender.

  You can change the sender name by clicking the **Sender name** block. The field then becomes editable and you can enter the name you would like to use.

  This field can be personalized. To do this, you can add personalization fields, content blocks and dynamic content by clicking the icons below the sender name.

* The **[!UICONTROL From: email address]** field cannot be edited from this section. You can change it by editing the properties of the email from its dashboard. For more on this, see [List of email advanced parameters](../../administration/using/configuring-email-channel.md#list-of-email-advanced-parameters).

>[!NOTE]
>
>The header parameters must not be empty. The sender's address is mandatory to allow an email to be sent (RFC standard). Adobe Campaign checks the syntax of email addresses entered.

**Related topics:**

* 
* 
*

## SMS sender {#sms-sender}

You can personalize the name of the SMS sender. For more on this, refer to the [SMS configuration](../../administration/using/configuring-sms-channel.md#configuring-sms-properties) section.
