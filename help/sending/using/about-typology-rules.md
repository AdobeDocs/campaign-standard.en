---
solution: Campaign Standard
product: campaign
title: About typologies and typology rules
description: Discover how typologies and typology rules work in Adobe Campaign.
audience: administration
content-type: reference
topic-tags: working-with-typology-rules
context-tags: typology,overview;typologyRule,main;typologyRule,overview
feature: Typology Rules
role: Business Practitioner
level: Intermediate
exl-id: dff72856-d28c-45c4-a073-12cc25f51f23
---
# About typologies and typology rules{#about-typology-rules}

Campaign Standard allows you to link a message to a **typology**, in order to check wether the message is valid and meets your quality criteria.

Typologies are sets of **typology rules**, that are executed during the message analysis phase. They allow you to make sure your emails always contain certain elements (such as an unsubscription link or a subject line) or filtering rules to exclude groups from your intended target (like unsubscribers, competitors, or non-loyalty customers).

![](assets/typology_messagelink.png)

Ready-to-use typologies and typology rules are available in Campaign Standard. Depending on your needs, you can also create new rules, and add them to existing or new typologies to link to your messages.

The steps to create and apply a typology to messages are:

1. Create typology rules (see [this section](../../sending/using/managing-typology-rules.md#creating-a-typology-rule)).
1. Create a typology and reference the rules you created into it (see [this section](../../sending/using/managing-typologies.md#creating-a-typology)).
1. Configure your delivery to use the typology you created (see [this section](../../sending/using/managing-typologies.md#applying-typologies-to-messages)).
1. During the message preparation, profiles are excluded when criterion is met. You can check logs to monitor exclusions.
