---
title: Whitelists in Adobe Campaign Standard
description: Learn how to optimize whitelists with Adobe Campaign Standard.
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

# Whitelists{#whitelists}

The main Internet service providers (ISPs) and Web mail providers manage whitelists from recognized email message senders. Adobe Campaign helps you with the process of getting certified on the best whitelists.

An email whitelist is a list of email addresses or domain names from which an email blocking program will allow messages to be received.

There are two types of whitelists:
* Non-commercial whitelists
* Commercial whitelists

## Non-commercial whitelists {#non-commercial-whitelists}

To be accepted by these whitelists, the sender must pass a series of tests based on a technical verification (its email server must not be an open relay but should have a static IP) of the infrastructure or its activity (delivery frequency, volume, number of complaints).

If the sender does not follow one of these rules, it may be deleted from the whitelist. In its **Adobe Campaign Email Deliverability** package, Adobe Campaign offers an accompanying expert consulting service for the certification process for non-commercial whitelists.

## Commercial whitelists {#commercial-whitelists}

Commercial whitelists are based on a system that allows the sender to bypass antispam filters altogether or be assigned incremental points as they enter the system. These paying whitelists (CPT or on an annual basis) are offered by systems such as Return Path Sender Score.

ISPs are free to use these services and the number of ISPs can vary depending on the whitelist. A sender can therefore be more confident when sending his messages by having a delivery guarantee. Certain whitelists also offer to open images and activate links.

Appearing in a whitelist is an undeniable asset for any email campaign. In its **Adobe Campaign Email Deliverability** package, Adobe Campaign offers a commercial whitelist certification service such as CSA and Return Path Sender Score.