---
title: Testing deliveries using targeted profiles
description: Learn how to test deliveries using targeted profiles and substitution addresses.
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

# Testing deliveries using targeted profiles {#testing-deliveries-profiles}

>[!IMPORTANT]
>
>This feature will be available with Campaign Standard 20.2 release.

## Overview {#overview}

Additionally to test profiles, you can test a delivery by placing yourself in the position of one of the targeted profiles. This allows you to get an exact representation of the delivery the profile will receive (custom fields, personalized and dynamic information...).

The main steps are as follows:

1. Configure your delivery then launch the **Preparation** phase.
1. **Select one or several profiles** among the profiles targeted by the delivery.
1. Associate with each profile a **substitution address** to which proofs will be sent.
1. (optional) For each profile, define a **prefix** to add to the proof subject line.
1. **Preview** in the Email Designer how the delivery will display for each selected profile.

>[!NOTE]
>
>For now, this feature is only available with the **email** channel.

## Selecting profiles and substitution addresses {#selecting-profiles}

To use profiles for proofing and previewing, you must first select them and define the substitution addresses that will receive the test deliveries.

To do this, you can either [select specific profiles](#selecting-individual-profiles) among the recipients of your delivery, or [import them from an existing audience](#importing-from-audience).

>[!NOTE]
>
>You can select up to 100 recipients for testing and previewing.

### Selecting individual profiles {#selecting-individual-profiles}

1. In the delivery dashboard, make sure that the delivery preparation is successfull, then click the **[!UICONTROL Audience]** block.

    ![](assets/substitution_preparation.png)

1. In the **[!UICONTROL Profile substitutions]** tab, click the **[!UICONTROL Create element]** button to select the profiles to use for testing.

   ![](assets/substitution_tab.png)

1. Click the profile selection button to display the full of profiles targeted by the delivery.

    ![](assets/substitution_recipient_selection.png)

1. Select the profile to use for testing, then enter in the **[!UICONTROL Address]** field the desired substitution address. All proofs will be sent to this address, rather than to the address defined for this profile in your database.

    If you want to add a specific prefix to the proofs sent for this profile, fill in the **[!UICONTROL Prefix]** field. The prefix will be added to the subject line of the proofs.

    ![](assets/substitution_address.png)

    >[!NOTE]
    >
    >The eye button allows you to access the profile's details. Make sure you saved your changes before using it.

1. The profile is added to the list, with its associated substitution address and prefix.

    Repeat the above steps for all the recipients that you want to use for testing, then click **[!UICONTROL Confirm]**.

      ![](assets/substitution_recipients_confirm.png)

1. Once all profiles and substitution addresses are defined, you can send a proof to test the delivery.

    To do this, click the **[!UICONTROL Test]** button, then select the type of test to perform. For more information on proofs sending, refer to [this section](../../sending/using/sending-proofs.md).

    ![](assets/substitution_send_test.png)

### Importing profiles from an audience {#importing-from-audience}

Campaign Standard allows you to import an audience of profiles that you can use for proofing and previewing.

This allows you, for example, to send to a unique substitution address an entire set of deliveries targeting different profiles.

>[!NOTE]
>
>When importing an audience, only the profiles corresponding to the delivery target will be selected and added to the **[!UICONTROL Profile substitutions]** tab.

1. In the delivery dashboard, make sure that the delivery preparation has been successfull, then click the **[!UICONTROL Audience]** block.

       ![](assets/substitution_preparation.png)

1. In the **[!UICONTROL Profile substitutions]** tab, select **[!UICONTROL Import from an audience]**.

   ![](assets/substitution_audience_import.png)

1. Select the audience to use, then enter the substitution address and the prefix to use for the proofs sent to the audience.

    ![](assets/substitution_audience_define.png)

    If the substitution addresses and/or prefixes to use have already been defined in your audience, select the **[!UICONTROL From Audience]** option, then specify the column to use to retrieve these information.

    ![](assets/substitution_fromaudience.png)

1. Click the **[!UICONTROL Import]** button to confirm. The profiles from the audience are added to the **[!UICONTROL Profile substitution]** tab, as well as the specified substitution address and prefix.

    ![](assets/substitution_audience_added.png)

>[!NOTE]
>
>If you import the same audience once again, with different substitution addresses and/or prefixes, the profiles will be added to the list in addition to those from the previous import.

## Previewing the delivery on the selected profiles

To be able to preview deliveries using targeted profiles, you must make sure that these profiles have been added to the **[!UICONTROL Profile substitution]** list (see [Defining profiles and substitution addresses](#selecting-profiles)).

1. Open the delivery in the Email Designer, then click the **[!UICONTROL Preview] button.

1. Bouton preview / Change profile > on accède à la liste des profils configurés dans substitution addresses

1. On coche les profils voulus puis select

1. on peut switcher d'un profil à l'autre avec les flèches

## Use case
prepare audience with profiles + substitution addresses in a specific field
build a workflow with a query and an email delivery activity
configure the activity and prepare the email
add the audience in the email activity as substitution addresses to use
preview the delivery on several profiles from the audience
prepare and send the test