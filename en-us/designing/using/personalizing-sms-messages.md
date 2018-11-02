---
title: Personalizing SMS messages
seo-title: Personalizing SMS messages
description: Personalizing SMS messages
seo-description: Discover the specificity of the transliteration options when personalizing SMS messages.
uuid: 97d67c8d-e4f7-4a1d-86af-d8a645593f25
content-encoding: UTF-8
aemsrcnodepath: /content/help/en/campaign/standard/designing/using/personalizing-sms-messages
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-06-25T08 45 08.405-0400
cq-lastreplicated: 2018-06-14T08 43 42.419-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: editing-message-and-landing-page-content
cq-template: /apps/help/templates/article-3
discoiquuid: 44ef9758-3594-45b9-88e8-df52d9d1718a
firstPublishExternalDate: 2018-06-14T08:43:42.401-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 09.547-0400
jcr-createdby: admin
jcr-description: Personalizing SMS messages
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-06-14T08:43:42.401-0400
lochandoffdate: 2018-06-25T08 45 08.405-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Personalizing SMS messages
publishexternaldate: 2018-06-14T08 43 42.401-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/designing/using/personalizing-sms-messages.html
sha1: bba93264596beaa3d533e17270fc426d648bc67e
topicBrowsingSortDate: 2018-06-14T08:43:42.401-0400
index: y
internal: n
snippet: y
---

# Personalizing SMS messages

Personalizing SMS messages

The principles for personalizing SMS messages are the same as those for emails. You must nevertheless be aware of the transliteration options as these can impact the encoding and therefore the number of SMS messages to send. For more on this, refer to the [Transliteration and SMS length](../../administration/using/configuring-sms-channel.md#sms-encoding--length-and-transliteration) section.

Here we take a sample SMS message containing personalization fields which, depending on whether or not transliteration has been selected, will not generate the same number of sends:

**"Hey &lt;FirstName&gt; &lt;LastName&gt;, new products now available. Come and check them out in store!"**

* For a recipient named "John Smith", as it contains no special characters, Adobe Campaign will choose GSM encoding which will authorize up to 160 characters per SMS message. The message will therefore be sent in a single part.
* For a recipient named "Raphaël Forêt", the characters "ë" and "ê" cannot be encoded in GSM. Depending on whether transliteration has been enabled or not, Adobe Campaign can select between two behaviors:

    * If transliteration is authorized "ë" and "ê" will be replaced by "e", which means GSM encoding can be used and so up to 160 characters can be used in the SMS. This message will be sent as a single SMS message, but it will be slightly altered.
    * If transliteration is not authorized, Adobe Campaign will choose to send the message in binary format (Unicode): all of the characters will therefore be sent as such. As the SMS messages in Unicode are limited to 70 characters Adobe Campaign will have to send the message in two parts.

>[!NOTE]
>
>The algorithm which automatically chooses the best encoding is executed independently for each message, case by case. This way, only the personalized messages that require Unicode encoding will be sent in Unicode; all the others will use GSM encoding.

