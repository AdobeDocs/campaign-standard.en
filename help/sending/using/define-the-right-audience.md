---
title: Define the right audience
seo-title: Define the right audience
page-status-flag: never-activated
uuid: a540efc7-105d-4c7f-a2ee-ade4d22b3445
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: delivery
content-type: reference
topic-tags: deliveries-best-practices
discoiquuid: 0cbc4e92-482f-4dac-a1fb-b738e7127938
index: y
internal: n
snippet: y
---

# Define the right audience {#define-the-right-audience}

Targeted population is key: build your lists carefully, test your emails on popular email clients and mobile devices, and ensure that your email lists are up-to-date (with no unknown or obsolete addresses). You can also send proofs that help set up a complete validation cycle.

Learn more about target populations [in this section](../../audiences/using/selecting-an-audience-in-a-message.md)

## Target the right audience {#target-the-right-audience}

When you have your content ready, you need to carefully define who will receive your message.

To make your delivery successful, you want to send the most relevant personalized content to the right recipients. Adobe Campaign enables you to build the most accurate target: you can select recipients according to their age, localization, what they bought, if they clicked a link in a previous delivery, etc. With Adobe Campaign, you can also define test profiles, control groups and seed addresses to make sure your target is correct.

## Target mappings {#target-mappings}

By default, delivery templates target **Profiles**. Adobe Campaign offers other target mappings for your deliveries, that you can change based on your needs.

These mappings are presented [in this section](../../automating/using/query.md#targeting-dimensions-and-resources).

You can also create and use a customized target mapping. For more on this, refer to [this section](../../administration/using/target-mappings-in-campaign.md).

## External data {#external-data}

You can deliver to recipients who are stored in an external file rather than saved in the database. To do this, design a workflow will load data into your database from a file and create an associated audience.  Learn more [in this use case](../../automating/using/use-case-calling-workflow.md). See also [Calling a workflow with parameters](../../automating/using/calling-a-workflow-with-external-parameters.md).

## Send to your subscribers {#send-to-subscribers}

To send messages to the subscribers of a newsletter, you can directly target the subscribers to the corresponding information service. Learn more [in this section](../../audiences/using/about-subscriptions.md).

**Tip** - You can create a List audience which targets the subscribers to your newsletter using a workflow. You can then select this audience in a delivery. For more on this, see [Creating list audiences](../../audiences/using/creating-audiences.md#creating-list-audiences).

## Proofs, test profiles and control groups {#proofs-test-control-groups}

To test your delivery, use proofs before sending to the main target.
Make sure you select appropriate proof recipients, because they validate the form and the content of the message. The steps for sending proofs are presented [in this section](../../sending/using/sending-proofs.md).

Learn more about test profiles [in this section](../../audiences/using/managing-test-profiles.md).

You can use [Control groups](../../sending/using/control-group.md) to measure the impact of your campaigns by excluding a portion of their audience. You will then be able to compare the behavior of the target population which did receive the message with the behavior of contacts which were not targeted. Based on the sending logs, you can also target a control group in future campaigns.

## Deduplicate addresses {#deduplicate-addresses}

It is important to avoid having duplicate email addresses, because this can have an impact on your target:

* The same message can be sent more than once when a target is split.

* If a recipient unsubscribes after receiving a message, their duplicate profile will still receive future messages.

Deduplicating addresses protects your sending reputation and ensures good quarantine management.

Learn more [in this use case](../../automating/using/deduplicating-data-imported-file.md).
