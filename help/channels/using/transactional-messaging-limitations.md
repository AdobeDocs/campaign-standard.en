---
solution: Campaign Standard
product: campaign
title: Transactional messaging limitations
description: Learn about the main recommendations and limitations regarding transactional messages in Adobe Campaign Standard.
audience: channels
content-type: reference
topic-tags: transactional-messaging
context-tags: 

---

# Transactional messaging best practices and limitations {#transactional-messaging-limitations}

<img src="assets/do-not-localize/icon_concepts.svg" width="60px">

This section lists the best practices and limitations you should be aware of before starting creating transactional messages.

<!--For more on transactional messages, including on how to configure and create them, see [Getting started with transactional messaging](../../channels/using/getting-started-with-transactional-msg.md).-->

## Permissions {#permissions}

Only users with the [Administration](../../administration/using/users-management.md#functional-administrators) role can configure transactional events and access transactional messages.

## Event configuration and publication {#design-and-publication}

As you are configuring and publishing transactional events, some of the steps you need to perform cannot be reverted. You need to be aware of the following limitations:

* The available channels for transactional messaging are: **[!UICONTROL Email]**, **[!UICONTROL Mobile (SMS)]** and **[!UICONTROL Push notification]**.
* Only one channel can be used for each event configuration. See [Creating an event](../../channels/using/configuring-transactional-event.md#creating-an-event).
* Once the event is created, you cannot change the channel. Therefore, if a message is not sent successfully, you need to design the mechanism allowing to send it from another channel using a workflow. See [Workflow data and processes](../../automating/using/get-started-workflows.md).
* You cannot change the targeting dimension ( **[!UICONTROL Real-time event]** or **[!UICONTROL Profile]** ) after the event is created. See [Creating an event](../../channels/using/configuring-transactional-event.md#creating-an-event).
* It is not possible to rollback a publication, but you can unpublish an event: this operation makes the event and the associated transactional message inaccessible. See [Unpublishing an event](../../channels/using/publishing-transactional-event.md#unpublishing-an-event).
* The only transactional message that can be associated with an event is the message that is automatically created upon publishing that event. See [Previewing and publishing the event](../../channels/using/publishing-transactional-event.md#previewing-and-publishing-the-event).

## Number of transactional messages {#transactional-message-number}

The number of published transactional messages can have a significant impact on your platform. For optimal performance, the number of published transactional messages should remain under 100. To ensure this, unpublish or delete any unused transactional messages. See [Unpublishing a transactional message](../../channels/using/publishing-transactional-message.md#unpublishing-a-transactional-message) and [Deleting a transactional message](../../channels/using/publishing-transactional-message.md#deleting-a-transactional-message).

To ensure best performance, you can also delete unused events. Indeed, deleting an event will also delete the corresponding transactional message(s), and its sending and tracking logs if any. See [Deleting an event](../../channels/using/publishing-transactional-event.md#deleting-an-event).

## Personalization {#personalization}

The way you can personalize a message content depends on the type of transactional message. Specificities are listed below.

### Event-based transactional messages

* The personalization information is coming from the data contained in the event itself. See [Event-based transactional message configuration](../../channels/using/configuring-transactional-event.md#event-based-transactional-messages).
* You **cannot** use **[!UICONTROL Unsubscription link]** content blocks in an event transactional message.
* Event-based transactional messaging is supposed to use only the data that are in the sent event to define the recipient and the message content personalization. However, you can enrich the content of your transactional message using information from the Adobe Campaign database. See [Enriching an event](../../channels/using/configuring-transactional-event.md#enriching-the-transactional-message-content) and [Personalizing a transactional message](../../channels/using/editing-transactional-message.md#personalizing-a-transactional-message).
* As event transactional messages do not contain profile information, they are not compatible with fatigue rules, even in the case of an enrichment with profiles.

### Profile-based transactional messages

* The personalization information can come from the data contained in the event or from the reconciled profile record. See [Profile-based transactional message configuration](../../channels/using/configuring-transactional-event.md#profile-based-transactional-messages) and [Profile-based transactional message specificities](../../channels/using/editing-transactional-message.md#profile-transactional-message-specificities).
* You **can** use **[!UICONTROL Unsubscription link]** content blocks in a profile transactional message. See [Adding a content block](../../designing/using/personalization.md#adding-a-content-block).
* Fatigue rules are compatible with profile transactional messages. See [Fatigue rules](../../sending/using/fatigue-rules.md).

### Product listings

Note that product listings are available in transactional **email messages** only. See [Using product listings in a transactional message](../../channels/using/editing-transactional-message.md#using-product-listings-in-a-transactional-message).

## Branding {#permissions-and-branding}

When it comes to [branding](../../administration/using/branding.md) management, transactional messaging enables less flexibility than standard messaging. Adobe recommends linking all brands used in transactional messages to the **[!UICONTROL All]** [organizational unit](../../administration/using/organizational-units.md). For more on this, read the detailed explanation below.

When editing a transactional message, you can link it to a brand to automatically apply some parameters such as the brand name or the brand logo. The **[!UICONTROL Default brand]** is selected by default in the transactional message properties.

![](assets/message-center_branding.png)

All objects (including branding) used in a transactional message must be visible from the **[!UICONTROL Message Center]** organizational unit, meaning that these objects must be in the **[!UICONTROL Message Center]** or **[!UICONTROL All]** organizational units.

However, if the brand selected in the message properties is linked to an organizational unit which is different from **[!UICONTROL Message Center]** or **[!UICONTROL All]**, this will cause an error and you will not be able to send the transactional message.

Therefore, if you want to use multi-branding in the context of transactional messaging, you should link all brands either to the **[!UICONTROL Message Center]** organizational unit or to the **[!UICONTROL All]** organizational unit.

## Exporting and importing transactional messages {#exporting-and-importing-transactional-messages}

* To export a transactional message, you need to include the corresponding event configuration when [creating the package export](../../automating/using/managing-packages.md#creating-a-package).
* Once the transactional message is [imported through a package](../../automating/using/managing-packages.md#importing-a-package), it is not displayed in the transactional message list. You need to [publish](../../channels/using/publishing-transactional-event.md) the event configuration in order to make the associated transactional message available.
