---
title: "Workflow use-case: Control group"
seo-title: "Workflow use-case: Control group"
description: "Workflow use-case: Control group"
seo-description: "Workflow use-case: Control group"
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

# Workflow use-case: Building a control group {#building-control-group}

You can send exclude some profiles from a delivery for comparison purpose maintaining a separate table for control groups. For example, you want to compare how the recipients of a campaign will react compared to a small group who was excluded from the delivery and did not receive that campaign.

## Creating a separate table{#selecting-recipients-contactable-via-email}

Create a table with some recipients from profile that you define as the control group.

![](assets/.png)

## Creating a workflow 

1. In **[!UICONTROL Marketing Activities]**, click **[!UICONTROL Create]** and select **[!UICONTROL Workflow]**.
1. Select **[!UICONTROL New Workflow]** as workflow type and click **[!UICONTROL Next]**.
1. Enter the properties of the workflow and click **[!UICONTROL Create]**.

## Creating a query activity

## Creating a Segmentation activity{#creating-a-segmentation-activity}

1. Drag and drop a **[!UICONTROL Segmentation]** activity and double-click it.
1. Define a segment code which is the control group.
1. Click **[!UICONTROL Confirm]**.
1. In **[!UICONTROL List of outbound segments]**, click **[!UICONTROL Add an element]** and click on ![](assets/edit_darkgrey-24px.png)  to create a segment targeting people in the second city. Here Chicago.
1. 
1. Click **[!UICONTROL Confirm]**.

## Creating an Email activity

## Creating an email delivery{#creating-an-email-delivery}

1. In **[!UICONTROL Activities]** > **[!UICONTROL Channels]**, drag and drop an **[!UICONTROL Email Delivery]** after each segment.
1. Click the activity and select ![](assets/edit_darkgrey-24px.png) to edit.
1. Select **[!UICONTROL Simple email]** and click **[!UICONTROL Next]**.
1. Select an email template and click **[!UICONTROL Next]**.
1. Enter the email properties and click **[!UICONTROL Next]**.
1. To create the layout of your email, click on **[!UICONTROL Email Designer]**.
1. Message is sent and tracked in sending logs for other profiles.
1. For control group segment, population is excluded and exported

**Related topics:**

* [Query activity](../../automating/using/query.md)
* [Segmentation activity](../../automating/using/segmentation.md)
* [Email delivery](../../automating/using/email-delivery.md)
