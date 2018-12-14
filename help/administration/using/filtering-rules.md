---
title: Filtering rules
seo-title: Filtering rules
description: Filtering rules
seo-description: Use filtering rules to refine the audience of your messages.
page-status-flag: never-activated
uuid: 638f6fdf-098c-4c50-ba80-e6a153422ecd
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: working-with-typology-rules
discoiquuid: 5a4f67d5-4499-43b7-80de-c71c4bf120ce
isreadyforlocalization: true
index: y
internal: n
snippet: y
---

# Filtering rules{#filtering-rules}

Filtering rules

Filtering rules allow you to exclude one part of the message target according to criteria defined in a query, such as quarantined profiles or profiles that have already been sent a certain number of emails.

For example, you can filter the newsletter subscribers so that the subscribers that are younger than 18 years old never receive communications.

## Creating a filtering rule {#creating-a-filtering-rule}

1. Create a **Filtering** typology rule, one that can be applied on all communication channels.

   ![](assets/typology_create-rule.png)

1. In the **Filtering criteria** tab, select the subscriptions in the **Subscription** category.

   ![](assets/typology_create-rule-subscription.png)

1. In the **Explorer** tab of the query editor, drag and drop the **Subscriber** node into the main part of the screen.

   ![](assets/typology_create-rule-subscriber.png)

1. Select the **Age** field and define the filtering conditions so that the age of the subscribers is 18 or above.

   ![](assets/typology_create-rule-age.png)

1. In the **Typologies** tab, link this rule to a typology.

   ![](assets/typology_create-rule-typology.png)

1. Make sure that the typology in question is selected in the delivery template that you want to use.

   ![](assets/typology_template.png)

   >[!NOTE]
   >
   >To access the delivery templates, select **Resources** > **Templates** in the navigation menu, which can be accessed via the Adobe Campaign logo.

Whenever this rule is used in a message, the subscribers who are considered minors will be automatically excluded.

## Restricting the applicability of a filtering rule {#restricting-the-applicability-of-a-filtering-rule}

You can restrict the applicability of a filtering rule according to the message to send.

1. In the typology rule's **Application criteria** tab, uncheck the **Apply the rule on all deliveries** option, which is enabled by default.

   ![](assets/typology_limit.png)

1. Use the query editor to define a filter. For example, you can apply the rule only on messages whose label starts with a given word or whose ID contains certain letters.

   ![](assets/typology_limit-rule.png)

In this case, the rule is only applied to the messages that correspond to the defined criteria.

## Default deliverability exclusion rules {#default-deliverability-exclusion-rules}

Two filtering rules are available by default: **Exclusion of addresses** (**addressExclusions**) and **Exclusion of domains** (**domainExclusions**). During the email analysis, these rules compare the recipient email addresses with the forbidden addresses or domain names contained in an encrypted global suppression list managed in the deliverability instance. If there is a match, the message is not sent to that recipient.

This is to avoid being blacklisted due to malicious activity, especially the use of a Spamtrap. For example, if a Spamtrap is used to subscribe via one of your web forms, a confirmation email is automatically sent to that Spamtrap, and this results in your address being automatically blacklisted.

>[!NOTE]
>
>The addresses and domain names contained in the global suppression list are hidden. Only the number of excluded recipients is indicated in the delivery analysis logs.

