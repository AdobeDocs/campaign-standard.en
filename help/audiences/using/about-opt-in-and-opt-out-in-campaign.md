---
title: About opt-in and opt-out in Campaign
seo-title: About opt-in and opt-out in Campaign
description: About opt-in and opt-out in Campaign
seo-description: Opt-out (or blacklist) results in a profile no longer being targeted by any delivery or by deliveries from a specific channel.
page-status-flag: never-activated
uuid: 501d9485-976b-4de7-b242-6886f2814c6c
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: audiences
content-type: reference
topic-tags: understanding-opt-in-and-opt-out-processes
discoiquuid: 2f26ec22-0809-4541-b2a1-e84ff868ba6e

internal: n
snippet: y
---

# About opt-in and opt-out in Campaign{#about-opt-in-and-opt-out-in-campaign}

Opt-out (or blacklist) results in a profile no longer being targeted by any delivery or by deliveries from a specific channel.

To give profiles the ability to opt in or opt out, you have to create a dedicated landing page. For more on this, refer to [Setting up opt-in and opt-out landing pages](../../audiences/using/managing-opt-in-and-opt-out-in-campaign.md#setting-up-opt-in-and-opt-out-landing-pages).

Profiles can also be opted in or out manually by an operator. For more on this, refer to [Managing opt-in and opt-out from a profile](../../audiences/using/managing-opt-in-and-opt-out-in-campaign.md#managing-opt-in-and-opt-out-from-a-profile).

Opt-out profiles are automatically excluded during the delivery analysis in order to speed up deliveries (the error rate has a significant effect on delivery speed).

>[!NOTE]
>
>Opt-out applies to **Profiles**, as opposed to quarantine which is linked to an **email address** or **phone number**. Opting out a profile will therefore exclude from deliveries all the addresses linked to it. If a user has two profiles in the database, he will still be targeted by deliveries as only one of his profiles is opt-out. To make sure all his adresses are excluded, add them to the quarantines addresses. For more on this, refer to [this page](../../sending/using/understanding-quarantine-management.md#identifying-quarantined-addresses-for-the-entire-platform).

For more on services subscriptions, refer to [this page](../../audiences/using/about-subscriptions.md).
