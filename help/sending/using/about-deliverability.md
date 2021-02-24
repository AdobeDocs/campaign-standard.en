---
solution: Campaign Standard
product: campaign
title: About deliverability in Adobe Campaign Standard
description: Learn about the concepts and best practices related to deliverability as well as the tools offered by Adobe Campaign Standard to optimize sending your deliveries.
audience: sending
content-type: reference
topic-tags: sheduling-messages
context-tags: delivery,schedule,back
---

# What is deliverability{#about-deliverability}

Deliverability allows to measure the success of your campaigns reaching your recipients' inbox without bouncing, or being marked as spam.

More precisely, email deliverability refers to the set of characteristics that determine a message's ability to reach its destination, via a personal e-mail address, within a short time, and with the expected quality in terms of content and format. These characteristics fall into four main categories: data quality, message and content, sending infrastructure, and reputation. Together, they form the foundation of a successful email deliverability program.

For a deeper dive on what deliverability is and to learn more on key deliverability terms, concepts, and approaches, see the [Adobe Deliverability Best Practice Guide](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/introduction.html).

The deliverability rate is the number of messages that hit the recipients’ inboxes compared to the number of messages that were delivered. With Adobe Campaign, the deliverability rate depends on numerous factors, particularly:

* Correct configuration of your instances
* Your IP address reputation
* Quality of the addresses targeted
* Low complaints and hard bounce rates
* Your message content
* Message authentication (SPF, DKIM, DMARC)
* Sender reputation

## How to improve deliverability {#deliverability-key-points}

Deliverability problems are generally linked to measures of protection against spam implemented by internet service providers and mail server administrators.

For general recommendations on how to design successful email marketing campaigns, see [Deliverability strategy and definition](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/deliverability-strategy-and-definition.html).

To optimize the deliverability of your Adobe Campaign emails, we recommend using the best practices listed on this page / in this section.

<!--Here is a list of the key points to check to ensure good deliverability.-->

>[!NOTE]
>
>Because ISPs are obliged to continuously develop new sophisticated filtering techniques to protect their customers from spammers, email deliverability is characterized by ever-changing criteria and rules. Make sure you refer to the [Adobe Deliverability Best Practice Guide](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/introduction.html) which is regularly updated.

## Campaign deliverability tools {#deliverability-tools}

Adobe Campaign provides a number of tools designed to help with deliverability:
<!-->
* [Delivery best practices](../../sending/using/delivery-best-practices.md)
* [Personalizing the sender name](../../designing/using/personalization.md#personalizing-the-sender)
* [Optimizing the sending time](../../sending/using/optimizing-the-sending-time.md)
* [Previewing messages](../../sending/using/previewing-messages.md)
* [Email rendering](../../sending/using/email-rendering.md)
* [Monitoring a delivery](../../sending/using/monitoring-a-delivery.md)
* [Receiving alerts when failures happen](../../sending/using/receiving-alerts-when-failures-happen.md)
* [Understanding delivery failures](../../sending/using/understanding-delivery-failures.md)
* [Understanding quarantine management](../../sending/using/understanding-quarantine-management.md)
* [Quarantine vs denylist](../../sending/using/understanding-quarantine-management.md#quarantine-vs-denylist)
* [Dynamic reports](../../reporting/using/about-dynamic-reports.md)
-->

### Check network configuration {#network-configuration}

Spammers try to conceal their real identity and as a consequence make their servers difficult to identify.

A legitimate network configuration that does not try to hide the identity of the server is essential to sending emails in large volumes.

### Adapt your message content {#adapt-message-content}

<!--TO REMOVE?-->

The content of certain messages may be detected as spam. To make sure that your emails reach your recipients when designing your message content, follow the principles listed in the [Controlling email content](sending/using/control-email-content.md) section.

For additional tips to optimizing deliverability when designing content, see the [Adobe Deliverability Best Practice Guide](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/content-best-practices-for-optimal-delivery.html).

### Carefully build your message

Make sure you follow the best practices mentioned in the sections listed below when configuring, designing and testing your message.

* [Delivery best practices](../../sending/using/delivery-best-practices.md)
* [Optimizing the sending time](../../sending/using/optimizing-the-sending-time.md)
* [Previewing messages](../../sending/using/previewing-messages.md)
* [Email rendering](../../sending/using/email-rendering.md)

### Leverage quarantine management

Adobe Campaign manages a list that gathers spam complaints, hard bounces, and soft bounces that occur consistently.

To protect your deliverability, the recipients whose addresses are on the suppression list are excluded by default from all future deliveries, because sending to these contacts could hurt your sending reputation.

* [Understanding delivery failures](../../sending/using/understanding-delivery-failures.md)
* [Understanding quarantine management](../../sending/using/understanding-quarantine-management.md)
* [Quarantine vs denylist](../../sending/using/understanding-quarantine-management.md#quarantine-vs-denylist)

### Use monitoring and reporting tools

Use the features offered by Adobe Campaign to monitor your deliverability.

The delivery dashboard allows you to check how your deliveries are performing through a set of real-time indicators. Amongst other things, check the number of messages that are successfully executed, sent and delivered. You can also verify the number of messages that have been opened and the number of messages/links that have been clicked.

* [Monitoring a delivery](../../sending/using/monitoring-a-delivery.md)
* [Receiving alerts when failures happen](../../sending/using/receiving-alerts-when-failures-happen.md)
* [Dynamic reports](../../reporting/using/about-dynamic-reports.md)

### Send to valid addresses {#valid-addresses}

Spammers often use address generators based on lists of frequent names and first names; in addition, they rarely process technical notifications sent back by mail servers. A high rate of invalid addresses is often interpreted as a sign of spam.

Double opt-in mechanisms and effective handling of technical bounce messages make it possible to avoid this.

### Reduce complaint rate {#reduce-complaint-rate}

ISPs usually have a prominent means of reporting a received message as spam. This makes it possible to identify unreliable sources. By rapidly honoring opt-out requests, making regular use of a given list, verifying consent through a double opt-in system, and implementing feedback loops, you can reduce complaint rates.

<!--Sending to honeypot addresses {#honeypot-addresses}
ISPs and other organizations (refer to https://www.projecthoneypot.org/) make use of mailboxes that do not correspond to physical persons but are created simply to trick spammers. These so-called "honey pot" addresses are published on the Web in order to be collected by spambots and thus catch illegitimate senders. The use of a double opt-in mechanism precludes this sort of address being added to a list. When using a third-party list, you must be sure of the methods employed by its maintainer.-->

<!--## Sending on a regular basis {#regular-deliveries}

Spammers make programmed deliveries to maintain their reputation over time. They sometimes need to adapt their marketing plan to meet the best practices imposed by the ISPs and so, after a peak in reputation (ramp-up), they configure regular deliveries.-->
