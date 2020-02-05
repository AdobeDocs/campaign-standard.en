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

# Testing deliveries using real profiles and substitution addresses {#testing-deliveries-profiles}

## Overview {#overview}

principle:
*  do a preview in email designer selecting a "production" profile, not a test profile.
* send a test email using data of a specifically selected production profile, to the address of our choice.

Benefits: allows to test on real profile, to have a more relevant testing with real data // test profiles don't allow this or more complicated (extension of test profiles with good fields etc.)

Limitations
* email only
* depuis delivery standalone ou workflow
* 100 profils maximum

## Prerequisites {#Prerequisites}

* delivery must be created and prepared successfully. (because once prepared, campaign will know the profiles to load according to the target)
* delivery must be a single delivery, not a reccuring

## Selecting the profiles and their substitution addresses

1. In the delivery dashboard, make sure that the delivery preparation has been successfull, then open the **[!UICONTROL Audience]** block.
1. In the **[!UICONTROL Profile substitutions]** tab, click the **[!UICONTROL Create element]** button to select the profiles to use for testing.
1. All the profiles corresponding to the delivery target display in the list. Select the desired profile, then click **[!UICONTROL Confirm]**.

    >[!NOTE]
    >
    >Advanced filters are available  in the left hand-side pane to help you refine your search.

1. Enter the substitution address that you want to use for the profile, then click **[!UICONTROL Confirm]**.

    The proof delivery will be sent to this address, rather than the one specified in the database for this sam profile.

    >[!NOTE]
    >
    >The eye button allows you to access the profile's details. Make sure you saved your changes before clicking.

1. The profile is added to the list, with its associated substitution address. Repeat the above steps for all the profiles that you want to use for your proof, then click **[!UICONTROL Confirm]**.
1. Click à nouveau sur prepare pour faire apparaître bouton test
1. Fenêtre habituelle pour les proofs:
    Envoie à la fois au test profiles + subsitution addresses renseignés

### Selecting profiles and substitution addresses from an audience

	10. To import from an audience,  click Import from an audience: only profiles from the audience corresponding to the target will be selected)
    1. Que signifie fill subsitutiojn address section? Permet de selectionner la colonne qui contient le mail pour le test ? 

### Importing profiles and substitution addresses from a file

need to build a specific workflow, detail steps

## Previewing the delivery on the selected profiles

substitution addresses must have been configured in the email
	
	1. Une fois préparé, double cliquer sur email pour l'ouvrir dans email designer
	3. Bouton preview / Change profile > on accède à la liste des profils configurés dans substitution addresses
	5. On coche les profils voulus puis select
	6. on peut switcher d'un profil à l'autre avec les flèches
	

## Use case
prepare audience with profiles + substitution addresses in a specific field
build a workflow with a query and an email delivery activity
configure the activity and prepare the email
add the audience in the email activity as substitution addresses to use
preview the delivery on several profiles from the audience
prepare and send the test