---
title: Profile transactional messages
seo-title: Profile transactional messages
description: Profile transactional messages
seo-description: Learn how to create and publish a profile transactional message.
page-status-flag: never-activated
uuid: 00cbcd0c-ca8c-4e75-bff6-b2020f21293b
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: transactional-messaging
discoiquuid: b916202c-2bb0-4ac8-9f38-5e98d1f8e32d
isreadyforlocalization: true
index: y
internal: n
snippet: y
---

# Profile transactional messages{#profile-transactional-messages}

Profile transactional messages

You can send transactional messages based on customer marketing profiles, which allows you to:

* Apply marketing typology rules such as **Blacklisted address** or fatigue rules (see [Fatigue rules](../../administration/using/fatigue-rules.md)).
* Include the unsubscription link within the messages.
* Add the transactional messages to the global delivery reporting.
* Leverage the transactional messages in the customer journey.

Once you have created and published an event (the cart abandonment as per the [example](../../channels/using/about-transactional-messaging.md#transactional-messaging-operating-principle) above), the corresponding transactional message is created automatically.

The configuration steps are presented in the [Configuring an event to send a profile transactional message](../../administration/using/configuring-transactional-messaging.md#use-case--configuring-an-event-to-send-a-transactional-message) section.

In order for the event to trigger sending a transactional message, you have to personalize the message, then test it and publish it.

>[!NOTE]
>
>To access the transactional messages, you must have administration rights or appear in the **Message Center agents** (mcExec) security group. Fatigue rules are compatible with profile transactional messages. See [Fatigue rules](../../administration/using/fatigue-rules.md).

## Sending a profile transactional message {#sending-a-profile-transactional-message}

1. Go the transactional message that was created to edit it. See [Event transactional messages](../../channels/using/event-transactional-messages.md).
1. In the transactional message, click the **Content** section. In addition to the transactional template, you can also choose the default email template, which targets **Profile**.

   ![](assets/message-center_marketing_templates.png)

1. Select the default email template.

   Similar to all marketing emails, it includes an unsubscription link.

   ![](assets/message-center_marketing_perso_unsubscription.png)

   Also, as opposed to configurations based on real-time events, you have direct access to all profile information to personalize your message. See [Inserting a personalization field](../../designing/using/inserting-a-personalization-field.md).

1. Save your changes and publish the message. See [Publishing a transactional message](../../channels/using/event-transactional-messages.md#publishing-a-transactional-message).

## Monitoring a profile transactional message delivery {#monitoring-a-profile-transactional-message-delivery}

Once the message is published and your site integration is done, you can monitor the delivery.

1. To view the message delivery log, click the icon at the bottom right of the **Deployment** block.

   For more information on accessing the logs, see [Monitoring the delivery](../../sending/using/monitoring-a-delivery.md).

1. Select the **Sending logs** tab. In the **Status** column, **Sent** indicates that a profile has opted in.

   ![](assets/message-center_marketing_sending_logs.png)

1. Select the **Exclusions logs** tab to view recipients who have been excluded from the message target, such as blacklisted addresses.

   ![](assets/message-center_marketing_exclusion_logs.png)

For any profile that has opted out, the **Blacklisted address** typology rule excluded the corresponding recipient.

This rule is part of a specific typology that applies to all transactional messages based on the **Profile** table.

![](assets/message-center_marketing_typology.png)

**Related topics**:

* [Site integration](../../administration/using/configuring-transactional-messaging.md#integrating-the-triggering-of-the-event-in-a-website)
* [Typologies](../../administration/using/about-typology-rules.md)

