---
title: Using traps
description: Learn how to use traps in messages.
page-status-flag: never-activated
uuid: eb4d893b-3724-4b15-9312-1ec74784368d
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: preparing-and-testing-messages
discoiquuid: 37320ec5-196c-4260-8156-98932da3e4a5
context-tags: seedMember,overview
internal: n
snippet: y
---

# Using traps {#using-traps}

When using traps, the message is sent to the [test profile](../../audiences/using/managing-test-profiles.md) just as it is sent to the main target, as a means to identify whether your client file is being used fraudulently.

Traps were originally designed for direct mail deliveries. They allow you to:

* Verify that your direct mail provider is really sending the communication.
* Receive the mail at the same time and in the same conditions as your customers.
* Keep an exact copy of the mail that was sent.
* Check that your client list is not misused by your direct mail provider. Indeed, if any other communication is sent to your test profile's address, your client file may have been used without your knowing. This is why the test profile's address should only be used to this purpose.

 For more on adding traps to a direct mail's audience, see [Adding test and trap profiles](../../channels/using/defining-the-direct-mail-audience.md#adding-test-and-trap-profiles).

For the other communication channels, you can add trap test profiles to your main target in order to:

* Check that your message was successfully sent.
* Get and keep an exact copy of your message.
* Track when it was sent and received.

To use a test profile as a trap, it must be included in your message's audience.

>[!NOTE]
>
>As opposed to test profiles used for [proofs](../../sending/sending-proofs.md) or [email rendering](../../sending/using/email-rendering.md), the message is sent at the same time to the main target and to the test profiles used as traps.

When defining a message's audience:

1. From the **[!UICONTROL Test profiles]** tab, select a test profile. Make sure that it has **[!UICONTROL Trap]** as the intended use.

   ![](assets/trap_select.png)

1. Once your message content is ready, click the **[!UICONTROL Prepare]** button. See [Preparing the send](../../sending/using/preparing-the-send.md).
   >[!NOTE]
   >
   >Make sure you selected a main target. Otherwise, your message cannot be sent.

1. Click the **[!UICONTROL Confirm]** button. See [Confirming the send](../../sending/using/confirming-the-send.md).

   ![](assets/trap_confirm.png)

The message is sent to the main target and to the test profile.

>[!NOTE]
>
>When using a test profile as a trap, for any enriched fields in a message, the corresponding additional data is randomly picked from a real targeted profile and assigned to the trap test profile. For more on enrichment, see [this example](../../automating/using/enrichment.md#example--enriching-profile-data-with-data-contained-in-a-file).
