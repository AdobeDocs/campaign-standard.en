---
title: "Workflow use-case: Creating deliveries with a complement"
seo-title: "Workflow use-case: Creating deliveries with a complement"
description: "Workflow use-case: Creating deliveries with a complement"
seo-description: "Workflow use-case: Creating deliveries with a complement"
page-status-flag: never-activated
uuid: 396a3de1-6ffa-4385-ac9f-15fdeae5a366
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: execution-activities
discoiquuid: 377821e6-69f8-41cc-a1ad-8a2f5ed4d409
context-tags: workflow,use-case,segmentation
internal: n
snippet: y
---

# Workflow use-case: Creating deliveries with a complement {#deliveries-with-complement}

You can send an email to customers: one for clients created less than a year ago, one for clients created more than a year ago.

1. In a Marketing Activities, click create and select **Workflow**.
1. Select **New Workflow** as workflow type and click **Next**.
1. Enter properties of the workflow and click **Create**.

## Create a Query activity {#create-a-query-activity}

1. In **Activities** > **Targeting**, drag and drop a **Query activity** ![](assets/query.png).
1. Double-click the activity.
1. In **Shortcuts**, drag and drop **Profiles** and select **email** with the operator **is not empty**.
1. In **Shortcuts**, drag and drop **Profiles** and select **no longer contact by email** with the value **no**.
1. Click **Confirm**.

## Create a Segmentation activity {#create-a-segmentation-activity}

1. In **Activities** > **Targeting**, drag and drop a **Segmentation** activity and double-click it.
1. Hover over the segment then click on ![](assets/edit_darkgrey-24px.png) to target customers added this year in the database. 
1. Drag and drop **Profiles** and select **Created** with the filter type **Relative**.
1. Change the **Level of precision** to **Year** and select **This year**.
Note: To observe the structure of the rule, click on **Advanced Mode**.
1. Click **Confirm** twice.
1. In **Advanced Options**, check **Generate complement** to create a segment targeting the remaining recipients.
1. Click **Confirm**.
1. Click **Save**.

## Creating an Email delivery {#create-an-email-delivery}

1. In **Activities** > **Channels**, drag and drop an email delivery after each segment.
	1. Click the activity and select ![](assets/edit_darkgrey-24px.png) to edit.
	1. Select **Single send email** and click **Next**.
	1. Select an email template and click **Next**.
	1. Enter the email properties and click **Next**.
  1. To create the layout of your email, click on **Email Designer**.
	1. Insert elements or select an existing template.
	1. Personalize your email with offers specific to each delivery.
	For more information, refer to [designing an email](../../designing/using/about-email-content-design.md#designing-an-email-content-from-scratch).
1. Click **Preview** to check your layout.
1. Click **Save**.

**Related topics:**

* [Query](../../automating/using/query.md)
* [Segmentation activity](../../automating/using/segmentation.md)
* [Email delivery](../../automating/using/email-delivery.md)
