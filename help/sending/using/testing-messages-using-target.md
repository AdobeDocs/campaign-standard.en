---
title: Testing email messages using targeted profiles
description: Learn how to test messages using targeted profiles and substitution addresses.
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

# Testing email messages using targeted profiles {#testing-message-profiles}

>[!IMPORTANT]
>
>This feature will be available with Campaign Standard 20.2 release.

## Overview {#overview}

Additionally to [test profiles](../../audiences/using/managing-test-profiles.md), you can test an email message by placing yourself in the position of one of the targeted profiles. This allows you to get an exact representation of the message that the profile will receive (custom fields, personalized and dynamic information...).

Note that this feature is only available for emails, and from the Email Designer only.

The main steps are as follows:

1. Configure your message then launch the **Preparation** phase.
1. **Select one or several profiles** among the profiles targeted by the message.
1. Associate with each profile a **substitution address** to which proofs will be sent.
1. (optional) For each profile, define a **prefix** to add to the proof subject line.
1. **Preview** in the Email Designer how the message will display for each selected profile.
1. Send the proofs.

>[!IMPORTANT]
>
>This feature allows you to send profile information to third-party systems.
>
>As a result, make sure you execute privacy requests (GDPR & CCPA) in both systems independently, FIRST in the third party system AND THEN in Adobe Campaign Standard.
>
>In general, executing a privacy request in one system WILL NOT execute that request in the other system (exceptions noted in Documentation).

## Selecting profiles and substitution addresses {#selecting-profiles}

To use targeted profiles for testing, you must first select them, then define the substitution addresses that will receive the proofs. To do this, you can either [select specific profiles](#selecting-individual-profiles) among the message's recipients, or [import profiles from an existing audience](#importing-from-audience).

>[!NOTE]
>
>You can select a maximum of 100 profiles for testing.

### Selecting individual profiles {#selecting-individual-profiles}

1. In the message dashboard, make sure that the message preparation is successfull, then click the **[!UICONTROL Audience]** block.

    ![](assets/substitution_preparation.png)

1. In the **[!UICONTROL Profile substitutions]** tab, click the **[!UICONTROL Create element]** button to select the profiles to use for testing.

   ![](assets/substitution_tab.png)

1. Click the profile selection button to display the list of profiles targeted by the message.

    ![](assets/substitution_recipient_selection.png)

1. Select the profile to use for testing, then enter in the **[!UICONTROL Address]** field the desired substitution address, then click **[!UICONTROL Confirm]**. Alls proofs targeting the profile will be sent to this email address, rather than to the one defined in the database for this profile.

    If you want to add a specific prefix to the proofs' subject line, fill in the **[!UICONTROL Subject line prefix]** field.

    ![](assets/substitution_address.png)

    The prefix will display as below:

    ![](assets/substitution_prefixsample.png)

1. The profile is added to the list, with its associated substitution address and prefix. Repeat the above steps for all the profiles that you want to use for testing, then click **[!UICONTROL Confirm]**.

      ![](assets/substitution_recipients_confirm.png)

    If you want to send a proof to multiple substitution addresses for a same profile, you must add this profile as many times as required. 

    In the example below, the proof based on the profile John Smith will be sent to two different substitution addresses:

    ![](assets/substitution_multiple_addresses.png)

1. Once all profiles and substitution addresses are defined, you can send a proof to test the message.

    To do this, click the **[!UICONTROL Test]** button, then select the type of test to perform. For more information on proofs sending, refer to [this section](../../sending/using/sending-proofs.md).

    ![](assets/substitution_send_test.png)

>[!IMPORTANT]
>
>If you make any change to your message, make sure you launch the message preparation again. Otherwise, the changes will not be reflected in the proof.


### Importing profiles from an audience {#importing-from-audience}

Campaign Standard allows you to import an audience of profiles that you can use for testing. This allows you, for example, to send to a unique email address an entire set of messages targeting different profiles.

Moreover, if your audience is already configured with the address and prefix columns, you will be able to import these information in the **[!UICONTROL Profile substitutions]** tab.

>[!NOTE]
>
>When importing an audience, only the profiles corresponding to the message target are selected and added to the **[!UICONTROL Profile substitutions]** tab.

1. In the message dashboard, make sure that the message preparation has been successfull, then click the **[!UICONTROL Audience]** block.

    ![](assets/substitution_preparation.png)

1. In the **[!UICONTROL Profile substitutions]** tab, select **[!UICONTROL Import from an audience]**.

   ![](assets/substitution_audience_import.png)

1. Select the audience to use, then enter the substitution address and the prefix to use for the proofs sent to the audience.

    ![](assets/substitution_audience_define.png)

    If the substitution addresses and/or prefixes to use have already been defined in your audience, select the **[!UICONTROL From Audience]** option, then specify the column to use to retrieve these information.

    ![](assets/substitution_fromaudience.png)

1. Click the **[!UICONTROL Import]** button. The profiles from the audience are added to the **[!UICONTROL Profile substitution]** tab, as well as the associated substitution addresses and prefixes.

    ![](assets/substitution_audience_added.png)

>[!NOTE]
>
>If you import the same audience once again, with different substitution addresses and/or prefixes, the profiles will be added to the list in addition to those from the previous import.

## Previewing the message with targeted profiles

To be able to preview messages using targeted profiles, make sure you have added these profiles to the **[!UICONTROL Profile substitution]** list (see [Defining profiles and substitution addresses](#selecting-profiles)), then follow these steps:

1. In the message dashboard, click the content snapshot to open the message in the Email Designer.

    ![](assets/substitution_preview_access.png)

1. Select the **[!UICONTROL Preview]** tab, then click **[!UICONTROL Change profile]**. 

    ![](assets/substitution_preview_changeprofile.png)

1. Click the **[!UICONTROL Profile Substitution]** tab to display the profiles that have been selected for testing.

    Select the profiles that you want to use for preview, then click **[!UICONTROL Select]**.

    ![](assets/substitution_preview_selection.png)

1. A preview of the message displays. Use the arrows to navigate between the profiles selected in the previous step.

    ![](assets/substitution_preview.png)

## Use case {#use-case}

In this use case, we will build a workflow to target a set of specific profiles, then send them a personnalized email newsletter. Before sending the messages, we will send proofs and preview the messages using internal email addresses that have been defined in a dedicated audience.

The main steps for this use case are as follows:

1. Create and configure the audience to use for testing.
1. Build the worklow with the query and email activities.
1. Add the audience to the address subsitutions to use for testing.
1. Preview the delivery using targeted profiles.
1. Send proofs to the audience.

### Step 1: Create and configure the audience to use for testing

xx

### Step 2: Build the worklow with the query and email activities

xx

### Step 3: Add the audience to the address subsitutions to use for proof and preview

xx

### Step 4: Preview the delivery using targeted profiles

xx

### Step 5: Send proofs to the audience

xx
