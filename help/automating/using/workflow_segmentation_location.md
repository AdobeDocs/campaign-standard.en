---
title: "Workflow use-case: Segmentation on location"
seo-title: "Workflow use-case: Segmentation on location"
description: "Workflow use-case: Segmentation on location"
seo-description: "Workflow use-case: Segmentation on location"
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

# Workflow use-case: Segmentation on location {#segmentation-on-location}

You can send a targeting email to customers with offers on their local shops.

1. In a **Marketing Activities**, click create and select **Workflow**.
1. Select **New Workflow** as workflow type and click **Next**.
1. Enter properties of the workflow and click **Create**.

## Selecting recipients contactable via email{#selecting-recipients-contactable-via-email}

1. In **Activities** > **Targeting**, drag and drop a **Query activity** ![](assets/query.png).
1. Double-click the activity.
1. In **Shortcuts**, drag and drop **Profiles** and select the field **email** with the operator **is not empty**.
1. In **Shortcuts**, drag and drop **Profiles** and select the field**no longer contact by email** with the value **no**.
1. Click **Confirm** twice.

## Creating a Segmentation activity{#creating-a-segmentation-activity}

1. Drag and drop a **Segmentation** activity and double-click it.
1. Click on segment then open transition to target people in the first city. Here Boston.
1. Drag and drop **Location** and select **City** with the operator **equals to** and the value **Boston**.
Note: To reach all the people that entered boston, unregarding of the case uncheck the case sensitive option.
1. Click **Confirm**.
1. In **List of outbound segments**, click **Add an element** and click on ![](assets/edit_darkgrey-24px.png)  to create a segment targeting people in the second city. Here Chicago.
1. Drag and drop **Location** and select **City** with the operator **equals to** and enter **Chicago** in value.

	>[!NOTE]
	>
	>To reach all the people that entered chicago, unregarding of the case uncheck the case sensitive option.

1. Click **Confirm**.

## Creating an email delivery{#creating-an-email-delivery}

1. In **Activities** > **Channels**, drag and drop an **Email Delivery** after each segment.
	1. Click the activity and select ![](assets/edit_darkgrey-24px.png) to edit.
	1. Select **Simple email** and click **Next**.
	1. Select an email template and click **Next**.
	1. Enter the email properties and click **Next**.
  1. To create the layout of your email, click on **Email Designer**.
	1. Insert elements or select an existing template.
	1. Personalize your email with offers specific to each location.
	For more information, refer to [designing an email](../../designing/using/about-email-content-design.md#designing-an-email-content-from-scratch).
1. Click **Preview** to check your layout.
1. Click **Save**.

**Related topics:**

* [Query activity](../../automating/using/query.md)
* [Segmentation activity](../../automating/using/segmentation.md)
* [Email delivery](../../automating/using/email-delivery.md)
