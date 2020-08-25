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


<img src="assets/do-not-localize/icon_transactional.svg" width="60px">

Transactional messaging enables you to <b>send individual and unique messages</b> to your customers in real-time. It can be welcome messages, order shipping confirmations, password modification, etc.

Adobe Campaign allows you to integrate this functionality with an information system which sends events that are to be transformed into custom transactional messages.

>[!NOTE]
>
>Transactional messages can be sent by email, SMS or push notification, depending on your options. Please check your license agreement.
>
>Adobe Campaign prioritizes processing transactional messages over any other delivery.

Transactional messaging is also available from the Adobe Campaign Standard API. For more on this, refer to the [dedicated documentation](../../api/using/managing-transactional-messages.md).

>[!NOTE]
>
>All transactional messages are now sent with the Adobe Campaign Enhanced MTA for improved deliverability, throughput, and bounce handling. All impacts are the same as for standard marketing messages. For more on this, see this [section](../../administration/using/configuring-email-channel.md).

## Transactional messaging definition {#transactional-messaging-definition}

<table>
<tr>
<td align="center"><img src="assets/do-not-localize/icon_concepts.svg" width="60px"><br><p><b>What is a transactional message?</b></p></td>
<td><p>It is an individual and unique communication, sent by a provider such as a website.</p></td>
<td><p>It is particularly expected, because it contains important information that the recipient wants to check or confirm.</p></td>
</tr>
<tr>
<td align="center"><img src="assets/do-not-localize/icon_channels.svg" width="60px"><br><p><b>When is it due?</b></p></td>
<td><p> Because this message contains important information, the user expects it to be sent in real time.</p></td>
<td><p>Consequently, the delay between the event being triggered and the message arriving has to be very short.</p></td>
</tr>
<tr>
<td align="center"><img src="assets/do-not-localize/icon_important.svg" width="60px"><br><p><b>Why is it important?</b></p></td>
<td><p>Generally, a transactional message has high open rates. It should therefore be carefully designed.</p></td>
<td><p>Indeed, it can have a strong impact on the customers' behavior as it defines the client relation.</p></td>
</tr>
<tr>
<td align="center"><img src="assets/do-not-localize/icon_example.svg" width="60px"><br><b>For example?</b></td>
<td><p>It could be a welcome message after creating an account, a confirmation that an order has shipped, an invoice...</p></td>
<td><p>It can also be a message confirming a password change, or a notification after a customer browsed your website...</p></td>
</tr>
</table>

## Transactional message types

Two types of transactional messages are available in Adobe Campaign:

<!--[Event transactional messages](../../channels/using/event-transactional-messages.md) targeting an **event**. The data contained in the event itself is used to define the delivery target.-->

<table>
<tr>
<td align="center"><img src="assets/do-not-localize/icon_event.svg" width="60px"><br><a href="../../channels/using/event-transactional-messages.md">Event transactional messages</a><br>targeting an <b>event</b>.</td>
<td><p><ul><li>They do not contain profile information.</li><li>They are not compatible with <a href="../../sending/using/fatigue-rules.md">fatigue rules</a> (even in the case of an enrichment with profiles).</li><li>The delivery target is defined by the data contained in the event itself.</li></ul></p></td>
</tr>
<tr>
<td align="center"><img src="assets/do-not-localize/icon_profile.svg" width="60px"><br><a href="../../channels/using/profile-transactional-messages.md">Profile transactional messages</a><br>targeting <b>profiles from the Adobe Campaign marketing database</b>.</td>
<td><p>Profile transactional messages alow you to:<ul><li>Apply marketing typology rules such as <b>Address on block list</b> or <a href="../../sending/using/fatigue-rules.md">fatigue rules</a>.</li><li>Include the unsubscription link within the messages.</li><li>Add the transactional messages to the global delivery reporting.</li><li>Leverage the transactional messages in the customer journey.</li></ul></p></td>
</tr>
</table>

<!--[Profile transactional messages](../../channels/using/profile-transactional-messages.md) targeting **profiles from the Adobe Campaign marketing database**. You can use information from the Adobe Campaign database to send a transactional message based on customer marketing profiles.-->

The message type is defined when configuring the event that will be transformed into a transactional message. See [Transactional messaging configuration](../../administration/using/configuring-transactional-messaging.md).

>[!IMPORTANT]
>
>To access all transactional messages, you must be part of the **[!UICONTROL Administrators (all units)]** security group.

<!--Event transactional messages do not contain profile information, therefore they are not compatible with fatigue rules (even in the case of an enrichment with profiles). However, profile transactional messages are compatible. For more on fatigue rules, see [this section](../../sending/using/fatigue-rules.md#choosing-the-channel).-->

## Transactional messaging operating principle {#transactional-messaging-operating-principle}

Let's take the example of a company that has a website and on this website its customers can buy products.

Adobe Campaign allows you to send a notification email to site users who have added products to their cart: when one of them leaves the site without going through with their purchases, a cart abandonment email is automatically sent to them.

The steps for putting this into place are the following.

### Step 1 - Create and publish the event configuration {#create-event-configuration}

<img src="assets/do-not-localize/icon_config.svg" width="60px">

Configure an event that will be named "Cart abandonment" and publish this event configuration.

The API that will be used by your website developer is deployed and a transactional message is automatically created.

Creating and publishing an event are presented in the [Configuring an event to send an event transactional message](../../administration/using/configuring-transactional-messaging.md#use-case--configuring-an-event-to-send-a-transactional-message) section.

### Step 2 - Edit and publish the transactional message {#create-transactional-message}

<img src="assets/do-not-localize/icon_transactional.svg" width="60px">

Edit and personalize the transactional message, test it, and then publish it.

For more on editing and publishing a transactional message, see [Event transactional messages](../../channels/using/event-transactional-messages.md).

### Step 3 - Integrate the event triggering {#integrate-event-trigger}

<img src="assets/do-not-localize/icon_api.svg" width="60px">

Use the REST Transactional Messages API to integrate the event into your website.

The event will be triggered when a client abandons their cart.

For more on integrating the event into your website, see [Site integration](../../administration/using/configuring-transactional-messaging.md#integrating-the-triggering-of-the-event-in-a-website).

### Step 4 - Message delivery {#message-delivery}

<!--Once all of these steps have been carried out, the message can be delivered:-->

<img src="assets/do-not-localize/icon_notification.svg" width="40px">

As soon as a user leaves the site without ordering the products in their cart, they automatically receive a notification email.

## Key steps {#key-steps}

The main steps when creating and managing personalized transactional messages in Adobe Campaign are summarized in the chart below.

![](assets/message-center-overview.png)

<!--## Transactional messaging publication process {#transactional-messaging-pub-process}

The chart below illustrates the whole transactional messaging publication process.

![](assets/message-center_pub-process.png)

For more on the event configuration steps, see [Transactional messaging configuration](../../administration/using/configuring-transactional-messaging.md).

Read more:

* [About transactional messaging](../../channels/using/about-transactional-messaging.md)
* [Event transactional messages](../../channels/using/event-transactional-messages.md)
* [Profile transactional messages](../../channels/using/profile-transactional-messages.md)
* [Transactional push notifications](../../channels/using/transactional-push-notifications.md)
* [Follow-up messages](../../channels/using/follow-up-messages.md)-->

**Related topics:**

* [Key steps to send a message](../../channels/using/key-steps-to-send-a-message.md)
* [Get started with communication channels](../../channels/using/get-started-communication-channels.md)