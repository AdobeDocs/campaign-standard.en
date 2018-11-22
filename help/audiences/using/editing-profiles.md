---
title: Editing profiles
seo-title: Editing profiles
description: Editing profiles
seo-description: Learn how to edit existing profiles and access contact information, prefered channels, tracking logs, subscriptions, etc.
page-status-flag: never-activated
uuid: 849f0567-e058-424d-909c-26d7f77e39db
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/audiences/using/editing-profiles
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: audiences
content-type: reference
topic-tags: managing-profiles
discoiquuid: fa1c9185-8f71-42b8-9af9-fb1bddd48a37
isreadyforlocalization: false
navTitle: Editing profiles
publishexternaldate: 2018-11-20
sha1: 28398e5d50f39797fa94d476a5eb7c6e44298dda
index: y
internal: n
snippet: y
---

# Editing profiles{#editing-profiles}

Editing profiles

## Accessing profile properties {#accessing-profile-properties}

To edit an existing profile and consult the data associated to it, or modify it, the steps are as follows:

1. From the Adobe Campaign home page, click the **Customer profiles** card or the **Profiles** tab.
1. Select a contact.
1. Click the **Edit profile properties** icon to access the profile's detailed information.

   ![](assets/profile_creation2.png)

   The profile's properties window offers several tabs that give access to all profile information.

   Other tabs may also appear depending on the custom resources that have been created or extended in Adobe Campaign. For more information about custom resources, see [About custom resources](../../developing/using/data-model-concepts.md).

   >[!NOTE]
   >
   >You can only modify the information in the **General** tab - except for the **Traceability** section.

Related topic:

[Integrated customer profile](../../audiences/using/integrated-customer-profile.md)

[Sending at the recipient's time zone](../../sending/using/sending-messages-at-the-recipient-s-time-zone.md)

## General profile data {#general-profile-data}

The **General** tab groups the following information about the profile:

* Contact information, which contains the recipient's first name, last name, date of birth, photo, preferred language (for [multilingual emails](../../channels/using/creating-a-multilingual-email.md)), etc.
* Channels on which the profile can be contacted, which contains the recipient's email address, mobile phone number, opt-out information. 
* Postal address (for [direct mail](../../channels/using/about-direct-mail.md)), and the contact's time zone (to [schedule messages in its time zone](../../sending/using/sending-messages-at-the-recipient-s-time-zone.md)).
* Access authorization, which indicates the recipient's organisational unit (to [manage permissions](../../administration/using/about-access-management.md)). See also [Partitioning profiles](../../administration/using/organizational-units.md#partitioning-profiles).

![](assets/profile_creation4.png)

## Sending and tracking logs {#sending-and-tracking-logs}

The **Sending logs** and **Tracking logs** tabs group the list of deliveries that were sent to the profile, and all related tracking data.

For more on sending and tracking logs, refer to the [delivery logs](../../sending/using/monitoring-a-delivery.md#delivery-logs) and the [tracking messages](../../sending/using/tracking-messages.md) sections.

## Subscriptions {#subscriptions}

The contact's subscriptions are listed in the corresponding tab. For more on subscribing to a service, refer to [this section](../../audiences/using/about-subscriptions.md).

The **Mobile App Subscriptions** tab refer to the push notifications. For more information, refer to the [Push notification](../../channels/using/about-push-notifications.md) channel.
