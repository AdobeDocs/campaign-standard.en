---
title: Profile transactional messages
seo-title: Profile transactional messages
description: Profile transactional messages
seo-description: Learn how to create and publish a profile transactional message.
uuid: 1da19aff-eb0e-4f5e-8443-5c962e33110e
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/channels/using/profile-transactional-messages
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-30T04 54 06.913-0400
cq-lastreplicated: 2018-07-23T06 03 06.212-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: transactional-messaging
cq-template: /apps/help/templates/article-3
discoiquuid: 0a20a064-b590-4cb9-a4cb-728d5f2f3cd9
firstPublishExternalDate: 2018-07-23T06:03:06.101-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 01 17.623-0400
jcr-createdby: admin
jcr-description: Profile transactional messages
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T06:03:06.101-0400
lochandoffdate: 2018-07-30T04 54 06.912-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Profile transactional messages
publishexternaldate: 2018-07-23T06 03 06.101-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/channels/using/profile-transactional-messages.html
sha1: 85241389a92428141fb3f5e2a59e73e98cdedc25
topicBrowsingSortDate: 2018-07-23T06:03:06.101-0400
index: y
internal: n
snippet: y
---

# Profile transactional messages

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

## Sending a profile transactional message

1. Go the transactional message that was created to edit it. See [Event transactional messages](../../channels/using/event-transactional-messages.md).
1. In the transactional message, click the **Content** section. In addition to the transactional template, you can also choose the default email template, which targets **Profile**.

   ![](assets/message-center_marketing_templates.png)

1. Select the default email template.

   Similar to all marketing emails, it includes an unsubscription link.

   ![](assets/message-center_marketing_perso_unsubscription.png)

   Also, as opposed to configurations based on real-time events, you have direct access to all profile information to personalize your message. See [Inserting a personalization field](../../designing/using/inserting-a-personalization-field.md).

1. Save your changes and publish the message. See [Publishing a transactional message](../../channels/using/event-transactional-messages.md#publishing-a-transactional-message).

## Monitoring a profile transactional message delivery

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

