---
title: Sending proofs
description: Learn how to send proofs.
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

# Sending proofs {#sending-proofs}

A proof is a specific message that allows you to test a message before sending it to the main target. Recipients of the proof are in charge of approving the message (its content and form).

There are two types of proofs recipients:

* **Test profiles** allow you to target additional recipients who do not match the defined targeting criteria. They can be added to a message's audience to detect any fraudulent use of your recipient database or to ensure the emails arrive in the inboxes. For more on this, see [Managing test profiles](../../audiences/using/managing-test-profiles.md).

   >[!NOTE]
   >
   >In order to send a proof, the test profiles must be included in your message's audience.

* **Substitution profiles** allow you to place yourself in the position of one of the targeted profiles and to get an exact representation of the message that the profile will receive. For more on this, see [Testing email messages using targeted profiles](../../sending/using/testing-messages-using-target.md).

   >[!NOTE]
   >
   >This feature is avaiable for the email channel only.

To send proofs, follow these steps:

1. Make sure the proofs recipients have been configured:
   * **Test profiles** must be included in your message's audience
   * **Substitution profiles** must be added once the message preparation has been successfull (see [this section](../../sending/using/testing-messages-using-target.md))).

1. Click the **[!UICONTROL Send a test]** button.

   ![](assets/bat_select.png)

1. Select the type of proof you would like to use:

    * **[!UICONTROL Email rendering]**: select this option to test the way your message is received according to the inboxes targeted. For more information, refer to [Email rendering](../../sending/using/email-rendering.md).
    * **[!UICONTROL Proof]**: select this option to test the message before sending it to the main target. The proof recipients are in charge of approving the delivery, by checking both its content and its format.
    * **[!UICONTROL Proof + Email rendering]**: this option combines the two previous options.

   ![](assets/bat_select1.png)

1. Confirm your choice.

   The proofs are sent to the recipients that have been configured.

   ![](assets/bat_select2.png)

1. You can view your proofs using the **[!UICONTROL Proofs]** drop-down list.

   ![](assets/bat_view.png)

1. Select a proof to access its summary. For an email, if you have selected the **Email rendering** option as the proof type, the **[!UICONTROL Access email rendering]** icon is displayed on the right of the proof label. See [Email rendering](../../sending/using/email-rendering.md).

   ![](assets/bat_view2.png)

Depending on the comments from the people who receive the proof, you may be asked to modify the delivery's content. Once the modifications have been carried out, you have to restart email preparation then re-send a proof. Each new proof can be accessed using the **[!UICONTROL Show proofs]** button.

You have to send as many proofs as necessary until you have finalized the content of your delivery. Once this is done, you can send the delivery to the main target and close the approval cycle.

**Related topic:**

* [Sending a test, preparing and sending an email](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/getting-started/sending-test-preparing-sending-email.html) video
* [Testing email messages using targeted profiles](../../sending/using/testing-messages-using-target.md).
* [Managing test profiles](../../audiences/using/managing-test-profiles.md).
