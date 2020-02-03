---
title: About deliverability in Adobe Campaign Standard
description: Learn about the concepts and best practices related to deliverability as well as the tools offered by Adobe Campaign Standard to optimize sending your deliveries.
page-status-flag: never-activated
uuid: 286fceee-65a9-4cb9-b205-9ce5d024675c
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: sheduling-messages
discoiquuid: 9c7fd670-bba9-4f3c-8cb1-87397a1acd27
context-tags: delivery,schedule,back
internal: n
snippet: y
---

# About deliverability{#about-deliverability}

Deliverability allows to measure the success of your campaigns reaching your recipients' inbox without bouncing, or being marked as spam.

The deliverability rate depends on numerous factors, particularly:

* Correct configuration of your instances
* Your IP address reputation
* Quality of the addresses targeted
* Low complaints and hard bounce rates
* Your message content
* Message authentication (SPF, DKIM, DMARC)
* Sender reputation

## Key points to check {#deliverability-key-points}

To optimize the deliverability of your Adobe Campaign emails, we recommend using the best practices listed below. Deliverability problems are generally linked to measures of protection against spam implemented by internet service providers and mail server administrators.

Email deliverability refers to the set of characteristics that determine a message's ability to reach its destination, via a personal e-mail address, within a short time,and with the expected quality in terms of content and format. These characteristics fall into four main categories: data quality, message and content, sending infrastructure, and reputation. Together, they form the foundation of a successful email deliverability program.

The deliverability rate is the number of sent emails that were successfully delivered to its recipients.
Here is a list of the key points to check to ensure good deliverability.

## Deliverability tools {#deliverability-tools}

First, start by consulting the documentation on the deliverability tools provided with Campaign Standard:
* [Delivery best practices](https://helpx.adobe.com/campaign/kb/delivery-best-practices.html)
* [Personalizing the sender name](../../designing/using/personalization.md#personalizing-the-sender)
* [Testing the subject line of an email](../../sending/using/testing-subject-line-email.md)
* [Optimizing the sending time](../../sending/using/optimizing-the-sending-time.md)
* [Previewing messages](../../sending/using/previewing-messages.md)
* [Email rendering](../../sending/using/email-rendering.md)
* [Monitoring a delivery](../../sending/using/monitoring-a-delivery.md)
* [Receiving alerts when failures happen](../../sending/using/receiving-alerts-when-failures-happen.md)
* [Understanding delivery failures](../../sending/using/understanding-delivery-failures.md)
* [Understanding quarantine management](../../sending/using/understanding-quarantine-management.md)
* [Quarantine vs blacklisting](../../sending/using/understanding-quarantine-management.md#quarantine-vs-blacklisting)
* [Dynamic reports](../../reporting/using/about-dynamic-reports.md)

## Checking network configuration {#network-configuration}

Spammers try to conceal their real identity and as a consequence make their servers difficult to identify. A legitimate network configuration that does not try to hide the identity of the server is essential to sending emails in large volumes.

## Sending to valid addresses {#valid-addresses}

Spammers often use address generators based on lists of frequent names and first names; in addition, they rarely process technical notifications sent back by mail servers. A high rate of invalid addresses is often interpreted as a sign of spam. Double opt-in mechanisms and effective handling of technical bounce messages make it possible to avoid this.

## Reducing complaint rate {#reduce-complaint-rate}

ISPs usually have a prominent means of reporting a received message as spam. This makes it possible to identify unreliable sources. By rapidly honoring opt-out requests, making regular use of a given list, verifying consent through a double opt-in system, and implementing feedback loops, you can reduce complaint rates.

## Sending to honeypot addresses {#honeypot-addresses}

ISPs and other organizations (refer to https://www.projecthoneypot.org/) make use of mailboxes that do not correspond to physical persons but are created simply to trick spammers. These so-called "honey pot" addresses are published on the Web in order to be collected by spambots and thus catch illegitimate senders. The use of a double opt-in mechanism precludes this sort of address being added to a list. When using a third-party list, you must be sure of the methods employed by its maintainer.

## Adapting message content {#adapt-message-content}

To a lesser degree, the content of certain messages can lead certain filters to detect it as spam. The use of certain words, the use of exclamation points in the subject line and within the messages are read as tell-tale signs of spam. Spammers are also known to replace text with images to stop offending text from being analyzed automatically by anti-spam filters. In response to this, a message (in HTML format) with a high proportion of images, or images as attachments, may end up being blocked.

## Sending on a regular basis {#regular-deliveries}

Spammers make programmed deliveries to maintain their reputation over time. They sometimes need to adapt their marketing plan to meet the best practices imposed by the ISPs and so, after a peak in reputation (ramp-up), they configure regular deliveries.
