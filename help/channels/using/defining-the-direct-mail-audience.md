---
title: Defining the direct mail audience
seo-title: Defining the direct mail audience
description: Defining the direct mail audience
seo-description: Learn how to define the target for your direct mail delivery.
uuid: 9eb23383-2561-4360-a0dc-041e6343d5d3
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: direct-mail
discoiquuid: 63f1559d-2e65-4205-b91e-956126b34247
isreadyforlocalization: false
index: y
internal: n
snippet: y
---

# Defining the direct mail audience{#defining-the-direct-mail-audience}

Defining the direct mail audience

You can either define the audience in the creation wizard or by clicking on the **Audience** section of the delivery dashboard.

![](assets/direct_mail_15.png)

## Defining the main target {#defining-the-main-target}

For direct mail, the targeted profiles are the ones that will be included in the extraction file that you will send to your direct mail provider.

For each targeted profile a new line is added in the extraction file. The amount of profile information that will be included for each recipient is defined in the [Defining the extraction](../../channels/using/defining-the-direct-mail-content.md#defining-the-extraction) screen.

>[!CAUTION]
>
>Make sure that your profiles include a postal address as this information is essential to the direct mail provider. Also make sure you have checked the **[!UICONTROL Address specified]** box in your profiles' information. See [Recommendations](../../channels/using/about-direct-mail.md#recommendations).

## Adding test and trap profiles {#adding-test-and-trap-profiles}

Add test profiles so that you can test your file with a small number of profiles. It allows you to quickly create a file sample to test and validate the structure before preparing the actual file. Refer to [Managing test profiles and sending proofs](../../sending/using/managing-test-profiles-and-sending-proofs.md).

The use of traps is essential to direct mail deliveries. For instance, they allow you to verify that your direct mail provider is really sending the communication and that they are not sending your client list to another provider.

For direct mail deliveries, traps are added during extraction and mixed in the output document. By default, they are inserted in the sorting order of the output file, but you can choose to insert them at the end or the beginning of the file ( **[!UICONTROL Trap insertion mode]** tab).
