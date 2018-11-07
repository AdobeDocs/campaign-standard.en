---
title: SMS configuration
seo-title: SMS configuration
description: SMS configuration
seo-description: Find out the SMS configuration steps. 
page-status-flag: never-activated
uuid: 3a2d404b-5f7b-4bbb-b5be-050a5de11ef0
content-encoding: UTF-8
aemsrcnodepath: /content/help/en/campaign/standard/administration/using/sms-configuration
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2017-11-28T11 02 52.405-0500
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: configuring-channels
cq-template: /apps/help/templates/article-3
discoiquuid: f84d6651-9936-4c04-a6e9-0311cd36b4c9
firstPublishExternalDate: 2017-11-16T11:11:49.713-0500
herogradient: light
isreadyforlocalization: false
jcr-created: 2017-11-29T19 03 08.328-0500
jcr-createdby: admin
jcr-description: SMS configuration
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2017-11-16T11:11:49.713-0500
lochandoffdate: 2017-11-28T11 02 52.402-0500
lr-lastreplicatedby: wmyersta@adobe.com
navTitle: SMS configuration
publishexternaldate: 2017-11-16T11 11 49.713-0500
publishExternalURL: https://helpx.adobe.com/campaign/standard/administration/using/sms-configuration.html
sha1: 784d38f911f7dd02a49ddf1c526e0d77ff1ff050
topicBrowsingSortDate: 2017-11-16T11:11:49.713-0500
index: y
internal: n
snippet: y
---

# SMS configuration

SMS configuration

To send SMS messages, one or several external accounts must be configured by an administrator under the **Administration** > **Channels** > **SMS** > **SMS accounts** menu.

The steps for creating and modifying an external account are detailed in the [External accounts](../../administration/using/external-accounts.md) section. You will find below the parameters specific to external accounts for sending SMS messages.

## Defining an SMS Routing

The external account **SMS routing via SMPP** is provided by default, but it can be useful to add other accounts.

1. Create a new external account from **Administration > Application settings > External accounts**.
1. Define the account type as **Routing**, the channel as **Mobile (SMS)** and the delivery mode as **Bulk delivery**.

   Once these routing parameters have been defined, the SMS connector (**Generic SMPP**) is selected automatically. This connector allows Adobe Campaign to send SMS messages directly to the targeted profiles by connecting to a short message service center (SMS-C) via the SMPP protocol.

   ![](assets/sms_routing.png)

1. Define the connection settings.

   To enter the connection settings specific to sending SMS messages, please contact your SMS service provider who will explain to you how to complete the different external account fields.

   ![](assets/sms_connection.png)

1. Contact Adobe who will give you the value to enter into the **SMS-C implementation name** field, depending on the provider chosen.
1. Define the SMPP channel settings. You can learn more in the [About SMS Routing](../../administration/using/sms-configuration.md#about-sms-routing) section.

   Enable the **Remove the '+' prefix from the phone number** option if you want to respect the SMPP protocol and not transfer the '+' prefix to the server of the SMS provider (SMS-C).

   However, given that certain providers require the use of the '+' prefix, it is advised that you check with your provider and they will suggest that you disable this option if necessary.

1. Define the **Throughput and timeouts** parameters.

   You can specify the maximum throughput of outbound messages ("MT", Mobile Terminated) in MT per second. If you enter "0" in the corresponding field, the throughput will be unlimited.

   The values of all of the fields corresponding to durations need to be completed in seconds.

1. Define the SMS-C specific parameters in case you need to define a specific encoding mapping. For more information, refer to the [SMS-C specifics](../../administration/using/sms-configuration.md#sms-c-specifics)
1. If needed, define automatic replies to trigger actions based on the content of a reply.
1. Save the configuration of the SMS routing external account.

You can now use your new routing to send SMS messages with Adobe Campaign.

## About SMS Routing

### SMS encoding, length and transliteration

By default, the number of characters in an SMS meets the GSM (Global System for Mobile Communications) standards.

SMS messages using GSM encoding are limited to 160 characters, or 153 characters per SMS for messages sent in multiple parts.

>[!NOTE]
>
>Certain characters count as two (braces, square brackets, the euro symbol, etc.). The list of available GSM characters is presented in the [Table of characters - GSM Standard](../../administration/using/sms-configuration.md#table-of-characters---gsm-standard) section.

If you like, you can authorize character transliteration by checking the corresponding box.

![](assets/sms_transliteration.png)

Transliteration consists of replacing one character of an SMS by another when that character is not taken into account by the GSM standard.

* If transliteration is **authorized**, each character that is not taken into account is replaced by a GSM character when the message is sent. For example, the letter "ë" is replaced by "e". The message is therefore slightly altered, but the character limit will remain the same.
* When transliteration is **not authorized**, each message that contains characters that are not taken into account is sent in binary format (Unicode): all of the characters are therefore sent as they are. However, the SMS messages using Unicode are limited to 70 characters (or 67 characters per SMS for messages sent in multiple parts). If the maximum number of characters is exceeded, several messages will then be sent, which may create additional costs.

>[!CAUTION]
>
>Inserting personalization fields into the content of your SMS message may introduce characters that are not taken into account by the GSM encoding. A content example is offered in the [Personalizing SMS messages](../../designing/using/personalizing-sms-messages.md) section.

By default, character transliteration is disabled. If you would like all of the characters in your SMS messages to be kept as they are, to not alter proper names for example, we recommend that you do not enable this option.

However, if your SMS messages contain a lot of characters that generate Unicode messages, you can choose to enable this option to limit the costs of sending your messages.

### Table of characters - GSM Standard

This section presents the characters taken into account by the GSM standard. All of the characters inserted into the message body, other than those mentioned below, convert the entire message into binary format (Unicode) and therefore limit it to 70 characters. For more on this, refer to the [SMS encoding, length and transliteration](../../administration/using/sms-configuration.md#sms-encoding--length-and-transliteration) section.

