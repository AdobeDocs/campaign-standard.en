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

A typology is a set of rules, executed during the message analysis phase, which allow the target, the content, and the configuration of the following elements to be validated: the subject, URL, images, unsubscription link, proof size, etc.

In Adobe Campaign, each message contains a link to a typology. This link is defined in the advanced parameters of the delivery template's properties (for more on this, refer to the [Preparation](../../administration/using/configuring-email-channel.md#preparation) section).

>[!NOTE]
>
>Each message can only be assigned a single typology.

For each typology, the **[!UICONTROL Typology rules]** section lists the set of rules for this typology.

![](assets/typology_typo-rule-list.png)





Typology rules are business rules that are applied during the message preparation. They are used to check whether a message is valid and meets your quality criteria. They also check if each member of the target audience is eligible to receive the message.