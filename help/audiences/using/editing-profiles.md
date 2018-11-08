---
title: Editing profiles
seo-title: Editing profiles
description: Editing profiles
seo-description: Learn how to edit existing profiles and access contact information, prefered channels, tracking logs, subscriptions, etc.
uuid: f11bf8b5-f362-4205-8719-b1129327b4ec
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/audiences/using/editing-profiles
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-10T07 22 30.973-0400
cq-lastreplicated: 2018-09-07T14 43 32.010-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: audiences
content-type: reference
topic-tags: managing-profiles
cq-template: /apps/help/templates/article-3
discoiquuid: 4c4aa25c-af33-4cb1-9c32-f08bf1801037
firstPublishExternalDate: 2018-09-07T14:43:29.446-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 01 08.089-0400
jcr-createdby: admin
jcr-description: Editing profiles
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T14:43:29.446-0400
lochandoffdate: 2018-09-10T07 22 30.971-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Editing profiles
publishexternaldate: 2018-09-07T14 43 29.446-0400
publishExternalURL: "https://helpx.adobe.com/campaign/standard/audiences/using/editing-profiles.html"
sha1: 84a9433a6685edef2118949571ac3777551a154c
topicBrowsingSortDate: 2018-09-07T14:43:29.446-0400
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
* Access authorization, which indicates the recipient's geographical and organisational units (to [manage permissions](../../administration/using/about-access-management.md)). See also [Partitioning profiles](../../administration/using/organizational-and-geographical-units.md#partitioning-profiles).

![](assets/profile_creation4.png)

## Sending and tracking logs {#sending-and-tracking-logs}

The **Sending logs** and **Tracking logs** tabs group the list of deliveries that were sent to the profile, and all related tracking data.

For more on sending and tracking logs, refer to the [delivery logs](../../sending/using/monitoring-a-delivery.md#delivery-logs) and the [tracking messages](../../sending/using/tracking-messages.md) sections.

## Subscriptions {#subscriptions}

The contact's subscriptions are listed in the corresponding tab. For more on subscribing to a service, refer to [this section](../../audiences/using/about-subscriptions.md).

The **Mobile App Subscriptions** tab refer to the push notifications. For more information, refer to the [Push notification](../../channels/using/about-push-notifications.md) channel.
