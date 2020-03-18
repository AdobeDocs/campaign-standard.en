---
title: About typology rules
description: Discover how typology rules work in Adobe Campaign.
page-status-flag: never-activated
uuid: a98ebc36-172d-4f46-b6ee-b2636a1007c9
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: working-with-typology-rules
discoiquuid: 2590d94c-51ef-4c0f-b1ec-c2837e94da40
context-tags: typology,overview;typologyRule,main;typologyRule,overview
internal: n
snippet: y
---

# About typologies and typology rules{#about-typology-rules}

Campaign Standard allows you to link a message to a **typology**, in order to check wether the message is valid and meets your quality criteria.

Typologies are sets of **typology rules**, that are executed during the message analysis phase. They allow you to make sure your emails always contain certain elements (such as an unsubscription link or a subject line) or filtering rules to exclude groups from your intended target (like unsubscribers, competitors, or non-loyalty customers).

![](assets/typology_messagelink.png)

Ready-to-use typologies and typology rules are available in Campaign Standard. Depending on your needs, you can also create new rules, and add them to existing or new typologies to link to your messages.

The steps to create and apply a typology to messages are:

1. Create typology rules.
1. Create a typology and reference the rules you created into it.
1. Configure your delivery to use the typology you created.
1. During the message preparation, profiles are excluded when criterion is met. You can check logs to monitor exclusions.

**Related topics:**

* [Managing typologies](../../sending/using/managing-typologies.md)
* [Managing typology rules](../../sending/using/managing-typology-rules.md)
