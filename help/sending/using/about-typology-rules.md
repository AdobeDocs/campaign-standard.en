---
title: About typologies and typology rules
description: Discover how typologies and typology rules work in Adobe Campaign.
audience: administration
content-type: reference
topic-tags: working-with-typology-rules
context-tags: typology,overview;typologyRule,main;typologyRule,overview
feature: Typology Rules
role: User
level: Intermediate
exl-id: dff72856-d28c-45c4-a073-12cc25f51f23
TQID: https://experienceleague.adobe.com/fFTJTgKfIhII-D6pefx9hqnX3a022odFZS5AAmNK1Ao
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
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
