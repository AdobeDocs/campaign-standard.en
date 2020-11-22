---
solution: Campaign Standard
product: campaign
title: Improving your reputation with Adobe Campaign Standard
description: Learn how to improve your reputation with Adobe Campaign Standard by managing duplicate email addresses and quarantines.
audience: sending
content-type: reference
topic-tags: sheduling-messages
context-tags: delivery,schedule,back
---

# Improving your reputation{#improving-reputation}

To avoid exhausting your recipients, delete duplicate email addresses from your target. This step protects your sending reputation and ensures good quarantine management. Adobe Campaign offers the necessary tools to implement these recommendations and avoid the risk of being added to the denylist by the ISPs.

Below you will find details on duplicate and quarantine management.

## Duplicates {#duplicates}

Having duplicate email addresses can have multiple consequences:
* The same message being sent more than once. Even if Campaign performs a deduplication procedure by default before sending, there is nothing to stop the same message being sent by different actions having the same content when a target is split.
* Unsubscription requests not honored. If a recipient unsubscribes after receiving a message, their duplicate profile will still be eligible for future messages.

Besides this side-stepping of opt-in procedures, this situation will likely lead users to consider the messages as spam and to trigger a denylist procedure at the ISP.

You must be especially cautious when performing operations on the database. To avoid duplicates as much as possible, the following actions must be carried out:
* **Imports must be meticulously configured.** This is particularly important when choosing the reconciliation key.
* **Pay attention when modifying email addresses.** Changed email addresses can also be a source of duplicates. In particular, two addresses with different domains may be routed to the same mailbox, for example in the case of a company that has changed name and has maintained the former domain for a certain period of time: joe.doe@amce-co.com and joe.doe@acme-rebranded.com.
* **Pay attention during automatic imports.** Whether of lists or from other databases, they are elements to be taken into account when managing profiles. What happens when you delete or move a profile in another partition? It might be recreated in the initial partition by an automatic import, for example, when a purchase order is placed.
* **Profiles should be sorted into different folders.**

There are, all the same, cases in which duplicates between the different partitions are normal. For example, when sending for third-parties or different company entities, it is logical for the same person to be a recipient for different reasons. It is, however, rarely normal to find duplicates within the same partition.

## Quarantines {#quarantines}

Adobe Campaign manages a list of quarantined addresses. The recipients whose addresses are quarantined are excluded by default during the delivery analysis: they are not targeted.

Quarantine management is detailed in [this section](../../sending/using/understanding-quarantine-management.md).

An email address can be quarantined for example when the inbox is full or if the address does not exist. In all cases, quarantining corresponds to the specific rules presented in [this section](../../sending/using/understanding-quarantine-management.md#conditions-for-sending-an-address-to-quarantine).
