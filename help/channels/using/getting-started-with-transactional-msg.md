---
title: Main steps to set up a transactional message
description: Discover what transactional messaging is and learn the main steps to set up a transactional message in Adobe Campaign Standard.
page-status-flag: never-activated
uuid: b316bf47-7d98-46fa-ab4f-67ff50de8095
contentOwner: lemaitre
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: landing-pages
discoiquuid: ca8d1698-6e8a-4f5a-b017-74a152e14286
context-tags: landingPage,wizard;landingPage,overview;landingPage,main
internal: n
snippet: y
---

# Getting started with transactional messaging {#getting-started-with-transactional-messaging}

## Overview

<table>
<tr>
<td><img src="assets/do-not-localize/icon_transactional.svg" width="60px"></td>
<td><p>Transactional messaging enables you to <b>send individual and unique messages</b> to your customers in real-time.<br>It can be welcome messages, order shipping confirmations, password modification, etc.</p></td>
</tr>
</table>

Adobe Campaign allows you to integrate this functionality with an information system which sends events that are to be transformed into custom transactional messages.

>[!NOTE]
>
>Transactional messages can be sent by email, SMS or push notification, depending on your options. Please check your license agreement.
>
>Adobe Campaign prioritizes processing transactional messages over any other delivery.

There are two types of messages: **event transactional messages** targeting events without profile information, and **profile transactional messages** targeting profiles from your database.

Transactional messaging is also available from the Adobe Campaign Standard API. For more on this, refer to the [dedicated documentation](../../api/using/managing-transactional-messages.md).

>[!NOTE]
>
>All transactional messages are now sent with the Adobe Campaign Enhanced MTA for improved deliverability, throughput, and bounce handling. All impacts are the same as for standard marketing messages. For more on this, see this [section](../../administration/using/configuring-email-channel.md).

### Transactional messaging in four questions {#transactional-messaging-operating-principle}

<img src="assets/do-not-localize/icon_concepts.svg" width="60px"><br>What is a transactional message? | <img src="assets/do-not-localize/icon_transactional.svg" width="60px"><br>Why is it particularly<br>expected? | <img src="assets/do-not-localize/icon_landing.svg" width="60px"><br>Why is it important? | <img src="assets/do-not-localize/icon_channels.svg" width="60px"><br>Why should it be carefully designed? |
|--- |--- |--- | --- |
| It is an individual and unique communication sent to a customer in real-time. | It contains information that the recipient wants to check or confirm. | It defines the client relation. The user expects it to be sent in real time. | Transactional messages generally have high open rates. |
| It is sent by a provider such as a website. | It could be a welcome message after creating an account for example, or a confirmation that an order has shipped, a bill, or a message confirming a password change. | Consequently, the delay between the event being triggered and the message arriving therefore has to be very short. | It is therefore important to design it carefully as it can have a strong impact on the customers behavior. |

### Key steps {#key-steps}

The main steps when creating and managing personalized transactional messages in Adobe Campaign are as follows:

![](assets/message-center-overview.png)

In this page, you will find information on each of these steps, as well as references to the dedicated documentations for more details.

## Transactional message types

Two types of transactional messages are available in Adobe Campaign:

* [Event transactional messages](../../channels/using/event-transactional-messages.md) targeting an event. The data contained in the event itself is used to define the delivery target.

    <table>
    <tr>
    <td><img src="assets/do-not-localize/icon_concepts.svg" width="60px"></td>
    <td><p>This type of transactional messages does not contain profile information.<br><b>The delivery target is defined by the data contained in the event itself</b>.</p></td>
    </tr>
    </table>

* [Profile transactional messages](../../channels/using/profile-transactional-messages.md) targeting profiles from the Adobe Campaign marketing database. You can use information from the Adobe Campaign database to send a transactional message based on customer marketing profiles.

    <table>
    <tr>
    <td><img src="assets/do-not-localize/icon_concepts.svg" width="60px"></td>
    <td><p>Profile transactional messages alow you to:<ul><li>Apply marketing typology rules such as <b>Address on block list</b> or <a href="../../sending/using/fatigue-rules.md">fatigue rules</a>.</li><li>Include the unsubscription link within the messages.</li><li>Add the transactional messages to the global delivery reporting.</li><li>Leverage the transactional messages in the customer journey.</li></ul></p></td>
    </tr>
    </table>

>[!NOTE]
>
>To access all transactional messages, you must be part of the **[!UICONTROL Administrators (all units)]** security group.

The message type is defined when configuring the event that will be transformed into a transactional message. See [Transactional messaging configuration](../../administration/using/configuring-transactional-messaging.md).

>[!NOTE]
>
>Event transactional messages do not contain profile information, therefore they are not compatible with fatigue rules (even in the case of an enrichment with profiles). However, profile transactional messages are compatible. For more on fatigue rules, see [this section](../../sending/using/fatigue-rules.md#choosing-the-channel).

## Transactional messaging operating principle {#transactional-messaging-operating-principle}

Let's take the example of a company that has a website and on this website its users can buy products.

Adobe Campaign allows you to send a notification email to site users who have added products to their cart: when one of them leaves the site without going through with their purchases, a cart abandonment email is automatically sent to them.

The steps for putting this into place are:

### Step 1 - Create and publish the event configuration {#create-event-configuration}

Configure an event that will be named "Cart abandonment" and publishing this event configuration, which automatically creates a transactional message. Creating and publishing an event are presented in the [Configuring an event to send an event transactional message](../../administration/using/configuring-transactional-messaging.md#use-case--configuring-an-event-to-send-a-transactional-message) section.

### Step 2 - Edit and publish the transactional message {#create-transactional-message}

The transactional message has to be personalized, tested, then published. See [Event transactional messages](../../channels/using/event-transactional-messages.md).

### Step 3 - Integrate the event triggering {#xxx}

Furthermore, in order for the event to be triggered when a client abandons their cart, this event has to be sent from the company's website using the Adobe Campaign Standard REST API. See [Site integration](../../administration/using/configuring-transactional-messaging.md#integrating-the-triggering-of-the-event-in-a-website).

Once all of these steps have been carried out, as soon as a user leaves the site without ordering the products in their cart, they automatically receive a notification email.

## Transactional messaging publication process {#transactional-messaging-pub-process}

The chart below illustrates the transactional messaging publication process.

![](assets/message-center_pub-process.png)

For more on the event configuration steps, see [Transactional messaging configuration](../../administration/using/configuring-transactional-messaging.md).

Read more:

* [About transactional messaging](../../channels/using/about-transactional-messaging.md)
* [Event transactional messages](../../channels/using/event-transactional-messages.md)
* [Profile transactional messages](../../channels/using/profile-transactional-messages.md)
* [Transactional push notifications](../../channels/using/transactional-push-notifications.md)
* [Follow-up messages](../../channels/using/follow-up-messages.md)

**Related topics:**

* [Key steps to send a message](../../channels/using/key-steps-to-send-a-message.md)
* [Get started with communication channels](../../channels/using/get-started-communication-channels.md)
* [About emails](../../channels/using/about-emails.md)
* [About SMS message](../../channels/using/about-sms-messages.md)
* [About Push notifications](../../channels/using/about-push-notifications.md)
* [About In-App messages](../../channels/using/about-in-app-messaging.md)
* [About Direct mail deliveries](../../channels/using/about-direct-mail.md)
