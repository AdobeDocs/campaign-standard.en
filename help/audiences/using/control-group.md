---
title: "Workflow use-case: Control group"
description: "Workflow use-case: Control group"
page-status-flag: never-activated
uuid: 396a3de1-6ffa-4385-ac9f-15fdeae5a366
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: execution-activities
discoiquuid: 377821e6-69f8-41cc-a1ad-8a2f5ed4d409
context-tags: workflow,use-case,query,segmentation,delivery 
internal: n
snippet: y
---

# Defining a control group {#defining-control-group}

To measure the impact of a delivery, you may want to exclude some profiles from your target so that they will not receive a given message. This control group can be used to make a comparison with the behavior of the target population which received the message.

To do this in Adobe Campaign Standard, you can create a control group when defining your main target.

## Creating a control group {#creating-a-control-group}

1. From the delivery dashboard, click the **[!UICONTROL Audience]** block.
1. Select the [!UICONTROL Control group] tab.

    ![](assets/xxx.png)

1. From the **[!UICONTROL Target extraction]** section, select one of the following options:

    * **[!UICONTROL No extraction]**: the target that you define as the control group will simply be excluded.
    * **[!UICONTROL Random sampling]**: you can define a percentage or a maximum number of the targeted population. For example, if you enter 10%, the control group will be made up of 10% from the targeted population, selected randomly.
    * **[!UICONTROL Keep only the first records after sorting]**: select a criterion, for example "email", to sort on the email: 10% of the targeted population will be excluded based on the email taken in descending alphabetical order.

1. Launch the delivery preparation. See [Preparing the send](../../sending/using/preparing-the-send.md).
1. Check the **[!UICONTROL Sending logs]**. You can see the excluded profiles with the [!UICONTROL Ignored] status and **[!UICONTROL Control group]** as the nature of failure.

The control group will then be excluded from the delivery when you confirm sending.

You can extract logs to compare how the control group that did not receive the communication reacted compared to the effective target.

>[!NOTE]
>
>As Dynamic Reporting are based on Delivery dimension, we cannot analyze what is excluded. We won’t change this behavior and this is the reason why Dynamic Reporting cannot help us here.
Also, we won’t build dedicated report for this.

## Reusing the same control group {#reusing-same-control-group}

The example above enables to create a global control group, as this is stored as a profile attribute independently from deliveries.

Consequently, next time you want to use the same control group, you can segment on the new “Control group” field rather than doing a random segmentation.

To do this:
