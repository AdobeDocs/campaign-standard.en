---
title: Testing deliveries using real profiles and substitution addresses
description: Learn how to manage test profiles and proofs.
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

# Testing and previewing deliveries as a recipient {#testing-deliveries-profiles}

>[!IMPORTANT]
>
>This feature will be available with Campaign Standard 20.2 release.

## Overview {#overview}

Additionally to test profiles, you can test and preview a delivery by placing yourself in the position of one of the targeted recipients.

This allows you to get a real representation of the delivery your recipients will receive, including all custom fields, and personalized/dynamic information.

To do this, Campaign Standard allows you to select one or several profiles among the targeted recipients, and to specify for each of them a subsitution address to which a test delivery (proof) will be sent. Moreover, you can preview the delivery directly from the Email Designer using this same recipient(s). This can be performed either from standalone deliveries or workflows.

>[!NOTE]
>
>For now, this feature is only available with **single** deliveries and for the **email** channel.

The key steps are as follows:

1. Prepare the delivery.
1. Select among the targeted recipients the one(s) that you want to use for testing and previewing.
1. Define for each recipient the substitution address that will receive the test delivery.
1. Preview the delivery in the Email Designer using the selected recipients.
1. Send a proof of the delivery using the recipients' data to the substitution addresses defined earlier.

## Selecting the profiles and defining substitution addresses

To use recipients for testing and previewing, you must first select them and define the substitution address(ses) that will receive the test deliveries.

>[!NOTE]
>
>You can select up to 100 recipients for testing and previewing.

To do this, follow these steps:

1. In the delivery dashboard, make sure that the delivery preparation has been successfull, then click the **[!UICONTROL Audience]** block.

       ![](assets/substitution_preparation.png)

1. In the **[!UICONTROL Profile substitutions]** tab, click the **[!UICONTROL Create element]** button to select the recipients to use for testing.

   ![](assets/substitution_tab.png)

1. Click the profile selection button to display the list of recipients targeted by the delivery.

       ![](assets/substitution_recipient_selection.png)

1. Select the recipient to add, then enter in the **[!UICONTROL Address]** field the substitution address that you want to use for this profile. All test deliveries will be sent to this address, rather than the one specified in the database for the profile.

    If you want to add a specific prefix to all the test deliveries sent for this recipient, use the **[!UICONTROL Prefix]** field. The prefix will be added to the subject line of the proof.

       ![](assets/substitution_address.png)

    >[!NOTE]
    >
    >The eye button allows you to access the profile's details. Make sure you saved your changes before clicking.

1. The profile is added to the list, with its associated substitution address and prefix.

    Repeat the above steps for all the recipients that you want to use for testing and/or previewing, then click **[!UICONTROL Confirm]**.

      ![](assets/substitution_recipients_confirm.png)

1. Once all profiles and substitution addresses are defined, you can send a proof to test the delivery.

    To do this, click the **[!UICONTROL Test]** button, then select the type of test to perform. For more on how to send proofs, refer to [this section](../../sending/using/sending-proofs.md).

        ![](assets/substitution_send_test.png)

### Selecting profiles and substitution addresses from an audience

1. To import from an audience,  click Import from an audience: only profiles from the audience corresponding to the target will be selected)

1. Que signifie fill subsitutiojn address section? Permet de selectionner la colonne qui contient le mail pour le test ? 

### Importing profiles and substitution addresses from a file

need to build a specific workflow, detail steps

## Previewing the delivery on the selected profiles

substitution addresses must have been configured in the email
	
1. Une fois préparé, double cliquer sur email pour l'ouvrir dans email designer

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