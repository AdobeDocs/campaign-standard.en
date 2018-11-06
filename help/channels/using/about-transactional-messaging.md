---
title: About transactional messaging
seo-title: About transactional messaging
description: About transactional messaging
seo-description: Discover the different types of transactional messages you can send and how they are used in Adobe Campaign.
uuid: 530f6f21-0d51-4b24-9b27-7fd0e691f422
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/channels/using/about-transactional-messaging
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-08T08 23 17.862-0400
cq-lastreplicated: 2018-09-07T15 12 28.703-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: transactional-messaging
cq-template: /apps/help/templates/article-3
discoiquuid: 9d39a8e1-d85b-41aa-8247-5c33e651005b
firstPublishExternalDate: 2018-09-07T15:12:28.665-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 00.424-0400
jcr-createdby: admin
jcr-description: About transactional messaging
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T15:12:28.665-0400
lochandoffdate: 2018-09-08T08 23 17.862-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: About transactional messaging
publishexternaldate: 2018-09-07T15 12 28.665-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/channels/using/about-transactional-messaging.html
sha1: 1f9e37df5acfc1097e54c657314a23d09c62040c
topicBrowsingSortDate: 2018-09-07T15:12:28.665-0400
index: y
internal: n
snippet: y
---

# About transactional messaging

About transactional messaging

You can create and manage personalized transactional messages in Adobe Campaign.

A transactional message is an individual and unique communication sent to a user by a provider such as a website.

* This type of message is particularly expected, as it contains information that the recipient wants to check or confirm. It could be a welcome message after creating an account for example, or a confirmation that an order has shipped, a bill, or a message confirming a password change.
* It is an important message that defines the client relation: the user expects it to be sent in real time. The delay between the event being triggered and the message arriving therefore has to be very short.
* Transactional messages generally have high open rates.

Adobe Campaign allows you to integrate this functionality with an information system which sends it events that are to be transformed into custom transactional messages.

>[!NOTE]
>
>Transactional messages can be sent by email, SMS or push notification, depending on your options. Please check your license agreement.

Two types of transactional messages are available in Adobe Campaign:

* **Event transactional messages** targeting an event. The data contained in the event itself is used to define the delivery target.
* **Profile transactional messages** targeting profiles from the Adobe Campaign marketing database. You can use information from the Adobe Campaign database to send a transactional message based on customer marketing profiles.

The message type is defined when configuring the event that will be transformed into a transactional message. See [Transactional messaging configuration](../../administration/using/configuring-transactional-messaging.md).

>[!NOTE]
>
>Adobe Campaign prioritizes processing the transactional messages over any other delivery.

## Transactional messaging operating principle

Let's take the example of a company that has a website and on this website its users can buy products.

Adobe Campaign allows you to send a notification email to site users who have added products to their cart: when one of them leaves the site without going through with their purchases, a cart abandonment email is automatically sent to them.

The steps for putting this into place are:

1. Configure an event that will be named "Cart abandonment" and publishing this event configuration, which automatically creates a transactional message. Creating and publishing an event are presented in the [Configuring an event to send an event transactional message](../../administration/using/configuring-transactional-messaging.md#use-case--configuring-an-event-to-send-a-transactional-message) section.
1. The transactional message has to be personalized, tested, then published. See [Event transactional messages](../../channels/using/event-transactional-messages.md).
1. Furthermore, in order for the event to be triggered when a client abandons their cart, this event has to be sent from the company's website using the Adobe Campaign Standard REST API. See [Site integration](../../administration/using/configuring-transactional-messaging.md#integrating-the-triggering-of-the-event-in-a-website).

Once all of these steps have been carried out, as soon as a user leaves the site without ordering the products in their cart, they automatically receive a notification email.
