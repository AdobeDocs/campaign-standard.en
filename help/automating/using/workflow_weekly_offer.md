---
title: "Workflow use-case: Create a weekly delivery"
seo-title: "Workflow use-case: Create a weekly delivery"
description: "Workflow use-case: Create a weekly delivery"
seo-description: "Workflow use-case: Create a weekly delivery"
page-status-flag: never-activated
uuid: 396a3de1-6ffa-4385-ac9f-15fdeae5a366
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: execution-activities 
discoiquuid: 377821e6-69f8-41cc-a1ad-8a2f5ed4d409
context-tags: workflow,use-case,query,delivery,scheduler
internal: n
snippet: y
---

# Worflow use case: Create an email delivery every Tuesday{#creating-email-every-tuesday}

You can send an email every Tuesday to all the customers for Special Offers.

1. In a Marketing Activities, click create and select **Workflow**.
1. Select **New Workflow** as workflow type and click **Next**.
1. Enter properties of the workflow and click **Create**.

## Creating a Scheduler activity{#creating-a-scheduler-activity}

1. In **Activities** > **Execution**, drag and drop a **Scheduler activity** ![](assets/scheduler_icon.png).
1. Double-click the activity.
1. Configure the execution of your delivery. 
	1. In **Execution frequency**, select **Weekly**.
	1. Select a **Time** and a **Repetition frequency** for your deliveries.
	1. In **Days of the week**, select **Tuesday**.
	1. Specify a **Start** and an **Expiration** parameter for your workflow.
	![](assets/scheduler_properties.png)

		>[!NOTE]
		>
		>To start your workflow at a specific **Time Zone**, in the **Execution options** tab, set up the time zone for your scheduler in the Time zone field.
 
	1. Confirm your activity and save your workflow.

## Creating a Query activity{#creating-a-query-activity}

1. In **Activities** > **Targeting**, to select recipients, drag and drop a **query** activity and double-click it.
	1. In **Shortcuts** > **Profile**, drag and drop **Email**.
	1. Select **is not empty** as an operator.
	1. In **Shortcuts** > **General**, add profiles and select **no longer contact by email** with the value **No**.
	1. Click **Confirm**.

## Creating an Email delivery{#creating-an-email-delivery}

1. In **Activities** > **Channels**, drag and drop an **Email delivery**.
	1. Click the activity and select ![](assets/edit_darkgrey-24px.png) to edit.
	1. Select **Recurring email** and click **Next**.
	1. Select an email template and click **Next**.
	1. Enter the email properties and click **Next**.
 1. To create the layout of your email, click on **Use Email Designer**.
	1. Insert elements or select an existing template.
	1. Personalize your email using fields and links.
	For more information, refer to [designing an email](../../designing/using/about-email-content-design.md#designing-an-email-content-from-scratch).
1. Click **Save**.

**Related topics:**

* [Query activity](../..//automating/using/query.md)
* [Scheduler activity](../..//automating/using/scheduler.md)
* [Email delivery](../..//automating/using/email-delivery.md)
* [Email channel](../..//channels/using/creating-an-email.md)
