---
title: Personalizing SMS messages
seo-title: Personalizing SMS messages
description: Personalizing SMS messages
seo-description: Discover the specificity of the transliteration options when personalizing SMS messages.
page-status-flag: never-activated
uuid: 4cae3cd4-c65f-4bbc-a14f-ceb0e6858892
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: sms-messages
discoiquuid: 91f33a9d-0a64-40dd-a20a-4bd87019592c
isreadyforlocalization: true
index: y
internal: n
snippet: y
---

# Personalizing SMS messages{#personalizing-sms-messages}

Personalizing SMS messages

The principles for personalizing SMS messages are the same as those for [emails](../../designing/using/inserting-a-personalization-field.md). You must nevertheless be aware of the transliteration options as these can impact the encoding and therefore the number of SMS messages to send. For more on this, refer to the [Transliteration and SMS length](../../administration/using/configuring-sms-channel.md#sms-encoding--length-and-transliteration) section.

Here we take a sample SMS message containing personalization fields which, depending on whether or not transliteration has been selected, will not generate the same number of sends:

**'Hey **

* For a recipient named 'John Smith', as it contains no special characters, Adobe Campaign will choose GSM encoding which will authorize up to 160 characters per SMS message. The message will therefore be sent in a single part.
* For a recipient named 'Raphaël Forêt', the characters 'ë' and 'ê' cannot be encoded in GSM. Depending on whether transliteration has been enabled or not, Adobe Campaign can select between two behaviors:

    * If transliteration is authorized 'ë' and 'ê' will be replaced by 'e', which means GSM encoding can be used and so up to 160 characters can be used in the SMS. This message will be sent as a single SMS message, but it will be slightly altered.
    * If transliteration is not authorized, Adobe Campaign will choose to send the message in binary format (Unicode): all of the characters will therefore be sent as such. As the SMS messages in Unicode are limited to 70 characters Adobe Campaign will have to send the message in two parts.

>[!NOTE]
>
>The algorithm which automatically chooses the best encoding is executed independently for each message, case by case. This way, only the personalized messages that require Unicode encoding will be sent in Unicode; all the others will use GSM encoding.

