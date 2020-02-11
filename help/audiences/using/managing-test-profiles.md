---
title: Managing test profiles
description: Learn how to manage test profiles.
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

# Managing test profiles {#managing-test-profiles}

## About test profiles {#about-test-profiles}

The test profiles allow you to target additional recipients who do not match the defined targeting criteria. They are added to a message's audience to detect any fraudulent use of your recipient database or to ensure the emails arrive in the inboxes.

You can manage your test profiles from the advanced menu **[!UICONTROL Profiles & audiences > Test profiles]**.

A test profile contains fictitious contact information, or contact information controlled by the sender, that can then be used in a message in the following contexts:

* For sending **Proofs**: the Proof is a specific message used to check the message before sending the finalized delivery to recipients. A Proof test profile is in charge of checking the delivery, with regard to its content and format. See [Sending proofs](../../sending/using/sending-proofs.md).
* For **Email rendering**: the Email rendering test profile is used to check the way in which a message is displayed according to the message inbox that receives it. For example, webmail, message service, mobile, etc. See [Email rendering](../../sending/using/email-rendering.md).

  The **Email rendering** use is read-only. Test profiles with this use are only available out-of-the-box in Adobe Campaign.

* As a **Trap**: the message is sent to the test profile just as it is sent to the main target. See [Using traps](../../sending/using/using-traps.md).
* To **Preview** messages: a test profile can be selected when previewing a message to test the personalization elements. See [Previewing messages](/help/sending/using/previewing-messages.md).

![](assets/test_profile.png)

## Creating test profiles {#creating-test-profiles}

1. From the advanced menu, via the Adobe Campaign logo, select **Profiles & audiences > Test profiles** to access the list of test profiles.

   ![](assets/test_profile_creation_1.png)

1. From the **[!UICONTROL Test profiles]** dashboard, click **Create**.

   ![](assets/test_profile_creation_2.png)

1. Enter the data for this profile.

   ![](assets/test_profile_creation_3.png)

1. Select the use you intend for your test profile.

   ![](assets/test_profile_creation_4.png)

1. Enter the contact channels **[!UICONTROL Email, Telephone, Mobile, Mobile app]**, as well as the test profile address if necessary.

   >[!NOTE]
   >
   >You can define a preferred email format: **[!UICONTROL Text]** or **[!UICONTROL HTML]**.

1. Specify an event type and the data for this event if you want to use this test profile for testing the personalization of a transactional message.
1. Click **[!UICONTROL Create]** to save the test profile.

The test profile will then be added to the list of profiles.

**Related topic:**

[Creating a test profile](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/profiles-and-audiences/test-profiles.html) video

## Editing test profiles {#editing-test-profiles}

To edit a test profile and consult the data that is linked to it, or to modify it:

1. Select the test profile you would like to edit by clicking on its image.
1. Consult or modify the fields.

   ![](assets/test_profile_edit.png)

1. Click **[!UICONTROL Save]** if you have entered your changes, or select the name of the test profile then **[!UICONTROL Test profiles]** in the section at the top of the screen to go back to the test profiles dashboard.
