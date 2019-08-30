---
title: Personalizing the sender
seo-title: Personalizing the sender
description: Personalizing the sender
seo-description: Learn how to personalize the name or the address of the sender for your messages.
page-status-flag: never-activated
uuid: 7aa08d5d-9e6c-4dac-bff8-6fde85368c2d
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: personalizing-content
discoiquuid: 49532f6b-3cd0-4d03-932e-bcb7d05c74d4

internal: n
snippet: y
---
# Personalizing the sender{#personalizing-the-sender}

<!-->

## Email sender {#email-sender}

To define the name of the sender which will appear in the header of messages sent, go the **[!UICONTROL Properties]** tab of the Email Designer home page (accessible through the home icon).

![](assets/delivery_content_edition16.png)

* The **[!UICONTROL From: name]** field allows you to enter the sender name. By default, the default **Sender name** block is automatically entered in the field. Adobe Campaign refers to the email channel configuration (from the advanced menu **[!UICONTROL Administration > Channels > Email > Email accounts]** via the Adobe Campaign logo) to designate this sender.

  You can change the sender name by clicking the **Sender name** block. The field then becomes editable and you can enter the name you would like to use.

  This field can be personalized. To do this, you can add personalization fields, content blocks and dynamic content by clicking the icons below the sender name.

* The **[!UICONTROL From: email address]** field cannot be edited from this section. You can change it by editing the properties of the email from its dashboard. For more on this, see [List of email advanced parameters](../../administration/using/configuring-email-channel.md#advanced-parameters).

>[!NOTE]
>
>The header parameters must not be empty. The sender's address is mandatory to allow an email to be sent (RFC standard). Adobe Campaign checks the syntax of email addresses entered.

**Related topics:**

* [Inserting a personalization field](../../designing/using/personalization.md#inserting-a-personalization-field)
* [Adding a content block](../../designing/using/personalization.md#adding-a-content-block)
* [Defining dynamic content in an email](../../designing/using/personalization.md#defining-dynamic-content-in-an-email)-->


