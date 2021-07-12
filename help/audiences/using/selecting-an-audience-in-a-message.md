---
solution: Campaign Standard
product: campaign
title: Selecting an audience in a message
description: "Step-be-step procedure to choose audiences of an email: main target population and test profiles."
audience: audiences
content-type: reference
topic-tags: managing-audiences
context-tags: deliveryCreation,wizard;delivery,audience,back
feature: Audiences
role: User
level: Intermediate
exl-id: 239959ad-6386-42bf-a86a-5694cdaecd83
---
# Selecting an audience in a message{#selecting-an-audience-in-a-message}

Adobe Campaign lets you configure several profile types within a message's audience.

Audiences can be defined when creating the message via the creation wizard or from the message dashboard if the message has already been created.

>[!NOTE]
>
>If the audience has been built within a workflow and enriched with additional data, you will not be able to use these data to personalize a standalone delivery. They can only be used from a delivery executed in a workflow.

1. From the dashboard, go to the audience block to start.

   ![](assets/delivery_audience_definition_1.png)

   The screen to define the audiences then opens. It has two tabs that allow you to separately define each type of audience that will receive the message:

    * Target
    * Test profiles

   ![](assets/delivery_audience_definition_2.png)

1. Define the main **[!UICONTROL Target]** of the email. This is the regular target audience of the email.

   The target is defined in the **[!UICONTROL Target]** tab and is made up of identified profiles from your database. You can establish your main target using the [query editor](../../automating/using/editing-queries.md#creating-queries) functionalities.

   In this tab, the **[!UICONTROL Shortcuts]** palette only contains predefined filters and the audiences that have been defined in the identified profiles. The **[!UICONTROL Explorer]** tab allows you to access additional configurations.

   You can therefore re-use and combine existing audiences, apply additional filters to them, etc.

   >[!NOTE]
   >
   >When targeting an audience, note that the audience's definition is not referenced but **copied** into the query. If you make any change to the audience after it has been targeted in a query, make sure you configure the query again to take the new definition into account.

1. Define the **[!UICONTROL Test profiles]** you want to use for the email. The test profiles will receive the proofs that you can send before to test the email before sending it to the main target.

   For more information on configuring test profiles, refer to the [Test profiles](../../audiences/using/managing-test-profiles.md) section.

1. If needed, you can define a control group using the corresponding tab. This will enable you to withdraw some profiles from your target so that they will not receive the message. For more on this, see [Adding a control group](../../sending/using/control-group.md).

1. You can also use substitution addresses to get an exact representation of the message that the profile will receive.  For more on this, see [Testing email messages using targeted profiles](../../sending/using/testing-messages-using-target.md).

The audiences block is then updated and shows that a target and test profiles have been selected for the email in question.

![](assets/delivery_audience_definition_3.png)
