---
title: Managing typologies
description: Discover how to use typologies.
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

# Managing typologies {#managing-typologies}

## About typologies {#about-typologies}

Typologies are sets of rules that allow you to check the validity of your message before sending it. For example: The message content is not empty, an unsubscription is present, exclusion of duplicates, etc.).

Typologies are accesible via the **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Typologies]** menu. By default, a default typology is available in the application. Based on your needs, you can create your own typologies or modify existing ones.

![](assets/typologies-list.png)

For each typology, the **[!UICONTROL Typology rules]** section lists the set of rules that are executed when using the typology with a message.

   >[!NOTE]
   >
   >To get more details on one of the typology rules, double-click it. The rule will display in read-only mode.

![](assets/typology_typo-rule-list.png)

## Creating a typology {#creating-a-typology}

To create a new typology, follow these steps:

1. Access the **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Typologies]** menu.

1. The list of typologies displays. Click the **[!UICONTROL Create]** button.

   ![](assets/typologies-list.png)

1. Define the typology's **[!UICONTROL Label]**, then click the **[!UICONTROL Add an element]** button to select the typology rules that you want to include. For more on typology rules, refer to [this section](../../sending/using/managing-typology-rules.md).

   ![](assets/typology_addrules.png)

   >[!NOTE]
   >
   >The **[!UICONTROL IP affinity]** field allows you to manage the affinities according to your configuration. These are defined in the instance's configuration file. If you want to use the affinities, contact your administrator.

1. Click **[!UICONTROL Create]** to confirm your selection. Your typology is now ready to be used in messages.

## Applying typologies to messages {#applying-typologies-to-messages}

When associating a typology with a message or message template, the typology rules included in the typology will be executed to check the message validity.

>[!NOTE]
>
>Each message can only be assigned a single typology.

1. To link a typology to a message, access the message properties, then select the **[!UICONTROL Advanced parameters]** section.

   ![](assets/typology_message.png)

1. By default, the out-of-the-box typology is linked to all messages. Select the typology of your choice from the list, then confirm.

The selected typology is now associated with the message. All its associated typology rules will be executed to check the message validity.
