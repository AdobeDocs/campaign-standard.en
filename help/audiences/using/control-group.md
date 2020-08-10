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

## Overview {#overview}

There are two ways you can define a control group:
* Extracting part of your target based on a sorting that you define. To do this, use the **[!UICONTROL Target extraction]** option.
* Excluding some profiles based on criteria that you define. To do this, use the **[!UICONTROL Target exclusion]** option.

You can use a combination of the two. All profiles that are extracted and excluded will be removed from the main target and will not receive the delivery.

## Creating a control group {#creating-a-control-group}

1. Create a delivery. For more on this, see [Creating a marketing activity](../../start/using/marketing-activities.md#creating-a-marketing-activity) section.
1. Define the target of your message. For more on this, see [About profiles](../../audiences/using/about-profiles.md).

    ![](assets/control-group-audience.png)

    When editing a delivery, from the delivery dashboard, click the **[!UICONTROL Audience]** block.

1. Select the **[!UICONTROL Control group]** tab.

    ![](assets/control-group-tab.png)

1. From the **[!UICONTROL Target extraction]** section, select one of the following options:

    * **[!UICONTROL No extraction]**: select this option if you do not want to use the **[!UICONTROL Target extraction]** option. You must define a control group in the **[!UICONTROL Target exclusion]** section. (The target that you define as the control group will simply be excluded.)

    ![](assets/control-group-no-extraction.png)

    * **[!UICONTROL Random sampling]**: you can define a percentage or a maximum number of the targeted population. For example, if you enter 10%, the control group will be made up of 10% from the targeted population, selected randomly.

    ![](assets/control-group-random-sampling.png)

    * **[!UICONTROL Keep only the first records after sorting]**: select a criterion, for example "email", to sort on the email: 10% of the targeted population will be excluded based on the email taken in descending alphabetical order.
    Another example: if you sort on the age and set 20 as the maximum size, leaving the Descending sort option checked, the 20 older profiles from your target will be excluded. If you uncheck the Descending sort option, the 20 younger profiles will be excluded.

    ![](assets/control-group-keep-first-records.png)

1. From the **[!UICONTROL Target exclusion]** section, define the profiles that will be excluded from your target based on the criteria of your choice using the query editor. For more on using the query editor, see the [Editing queries](automating/using/editing-queries.md) section. For example, Email starts with "ba" or "Age is greater than 20".

1. Launch the delivery preparation. See [Preparing the send](../../sending/using/preparing-the-send.md).
1. Confirm sending (see [Preparing the send](../../sending/using/preparing-the-send.md)).
The control group will be excluded from the delivery.

## Reporting {#reporting}

1. Check the **[!UICONTROL Sending logs]**. You can see the excluded profiles with the **[!UICONTROL Ignored]** status and **[!UICONTROL Control group]** as the reason of failure.

    ![](assets/control-group-sending-logs.png)

1. You can also check the **[!UICONTROL Exclusion causes]** tab to see the number of profiles excluded from the delivery.

    ![](assets/control-group-exclusion-causes.png)

1. You can extract logs to compare how the control group that did not receive the communication reacted compared to the effective target.

>[!NOTE]
>
>As dynamic reporting is based on the delivery dimension, no report is available to analyze the control group that is excluded.

<!--As Dynamic Reporting are based on Delivery dimension, we cannot analyze what is excluded. We won’t change this behavior and this is the reason why Dynamic Reporting cannot help us here.
Also, we won’t build dedicated report for this.-->

## Reusing the same control group {#reusing-same-control-group}

The example above enables to create a global control group, as this is stored as a profile attribute independently from deliveries.

Consequently, next time you want to use the same control group, you can segment on the new “Control group” field rather than doing a random segmentation.

Can you do this?
