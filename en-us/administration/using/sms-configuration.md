---
title: SMS configuration
seo-title: SMS configuration
description: SMS configuration
seo-description: Find out the SMS configuration steps. 
page-status-flag: never-activated
uuid: e764594e-2c3d-4c02-884d-b87d06700424
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
discoiquuid: 696b0276-818c-4f6e-ab5a-3dd70019311e
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
sha1: 37d0224c5a44c57d1a3352ce9eb43e660a414697
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

**Basic characters**

|  @  |  ![](assets/delta.png)

| SP  | 0  | ¡  | P  | ¿  | P  |
|---|---|---|---|---|---|---|---|
|  £  | _  | !  | 1  | A  | Q  | a  | q  |
|  $  |  ![](assets/phi.png)

| "  | 2  | B  | R  | b  | r  |
|  ¥  |  ![](assets/gamma.png)

| #  | 3  | C  | S  | c  | s  |
|  è  |  ![](assets/delta.png)

| ¤  | 4  | D  | T  | d  | t  |
|  é  |  ![](assets/omega.png)

| %  | 5  | E  | U  | e  | u  |
|  ù  |  ![](assets/pi.png)

| &  | 6  | F  | V  | f  | v  |
|  ì  |  ![](assets/psi.png)

| '  | 7  | G  | W  | g  | w  |
|  ò  |  ![](assets/sigma.png)

| (  | 8  | H  | X  | h  | x  |
|  Ç  |  ![](assets/theta.png)

| )  | 9  | I  | Y  | i  | y  |
|  LF  |  ![](assets/xi.png)

| &#42;  | :  | J  | Z  | j  | z  |
|  Ø  | ESC  | +  | ;  | K  | Ä  | k  | ä  |
|  ø  | Æ  | ,  | <  | L  | Ö  | l  | ö  |
|  CR  | æ  | -  | =  | M  | Ñ  | m  | ñ  |
|  Å  | ß  | .  | >  | N  | Ü  | n  | ü  |
|  å  | É  | /  | ?  | O  | §  | o  | à  |

SP: Space

ESC: Escape

LF: Line Feed

CR: Carriage Return

**Advanced characters (counted twice)**

^ { } [ ~ ] | €

### SMS-C specifics

When sending an SMS message, Adobe Campaign can use one or several text encodings. Each encoding has its own specific character set and determines the number of characters that fit into an SMS message.

The **DATA_CODING** field allows Adobe Campaign to communicate to the SMS-C which encoding is used.

>[!NOTE]
>
>The mapping between the **data_coding** value and the encoding actually used is standardized. Nevertheless, certain SMS-C have their own specific mapping: in this case, your **Adobe Campaign** administrator needs to declare this mapping. Check with your provider to find out more.

The **Define a specific mapping of encodings** functionality allows you to declare **data_codings** and to force the encoding if necessary: to do this, specify a single encoding in the table.

**Configuration**

* When the **Define a specific mapping of encodings** functionality is not checked, the connector takes on a generic behavior:

  * It will try to use GSM encoding to which it assigns the value **data_coding = 0**.
  * If GSM encoding fails, it will use **UCS2** encoding to which it assigns the value **data_coding = 8**.

  ![](assets/sms_data_coding.png)

* When the **Define a specific mapping of encodings** functionality is checked, you can define the encodings that you would like to use as well as the linked **data_coding** field values. Adobe Campaign will try to use the first encoding in the list, then the following, if the first encoding proves impossible.

  The order of declaration is important: it is recommended that you put the list in ascending order **of cost** in order to favor the encodings allowing you to fit as many characters as possible in each SMS message.

  Only declare the encodings that you would like to use. If some of the encodings provided by the SMS-C should not correspond to your purpose of use, do not declare them in the list.

  ![](assets/sms_data_coding1.png)

### SMS automatic replies

When a subscriber replies to an SMS message which was sent to them via Adobe Campaign and their message contains a keyword such as "STOP", you can configure messages which are automatically sent back to them in the **Automatic reply sent to the MO** section.

>[!NOTE]
>
>The keywords are not case-sensitive.

For each keyword, specify a short code, which is a number that is usually used to send deliveries and will serve as a sender name, then enter the message that will be sent to the subscriber.

You can also link an action to your automatic reply: **Blacklist** or **Unblacklist**. For example, if a recipient sends the keyword "STOP", they will automatically receive an unsubscription confirmation and are blacklisted.

![](assets/sms_mo.png)

If you link the **Unblacklist** action to an automatic reply, the recipients sending the corresponding keyword are automatically whitelisted.

The blacklisted and whitelisted recipients are listed in the **Addresses** table available through the **Administration** > **Channels** > **Quarantines** menu.

To send the same reply no matter what the short code, leave the **Short code** column empty.

To send the same reply no matter what the keyword, leave the **Keyword** column empty.

To carry out an action without sending a reply, leave the **Answer** column empty. For example, this allows you to unblacklist a user who replies with a message other than "STOP".

You can define an action to perform when a reply matches these three fields.

## List of SMS properties

This section details the list of parameters unique to SMS in the properties screen of an SMS delivery or an SMS template.

The specific parameters for sending SMS messages are regrouped in the **Send** and in the **Advanced parameters** sections.

![](assets/sms_options.png)

* The **From** option allows you to personalize the name of the SMS message sender using a string of characters. This is the name that will appear as the sender name of the SMS message on the recipient's mobile telephone.

  If this field is empty, then it will be the source number provided in the external account that will be used. If no source number is provided, it will be the short code that will be used. The external account specific to SMS delivery is presented in the [External SMS account](../../administration/using/sms-configuration.md) section.

  ![](assets/sms_SMPP.png)

  >[!CAUTION]
  >
  >Please check the legislation in your country regarding modifying the sender address. You should also check with your SMS service provider to see whether they offer this functionality.

* The **Maximum number of SMSes per message** option allows you to define the number of SMS messages to use to send a message. If this number is exceeded, the message will not be sent.

  >[!CAUTION]
  >
  >If you have inserted personalization fields or conditional text into the content of your SMS message, the length of the message and, as a result, the number of SMS messages to send, may vary from one recipient to another. For more on this, refer to the [Personalizing SMS messages](../../designing/using/personalizing-sms-messages.md) section.

* The **Transmission mode** field allows you to determine the delivery method for SMS messages:

  * **Saved on SIM card**: the message is stored on the recipient's telephone SIM card.
  * **Saved on mobile**: the message is stored on the telephone's internal memory.
  * **Flash**: the message is displayed on the recipient's mobile telephone as a notification, then it disappears without being saved.
