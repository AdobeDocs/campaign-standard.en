---
title: Use case: Create a weekly delivery 
seo-title: Use case: Create a weekly delivery 
description: Use case: Create a weekly delivery 
seo-description: Use case: Create a weekly delivery 
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

# Create a mail delivery every Tuesday

You can send an email every Tuesday to all the customers for Special Offers.

1. In a Marketing Activities, click create and select **Workflow**.
1. Select **New Workflow** as workflow type and click **Next**.
1. Enter properties of the workflow and click **Create**. 

## Creating a Scheduler activity

1. In **Activities** > **Execution**, drag and drop a **Scheduler activity**. **ICON**
1. Double-click the activity.
1. Configure the execution of your delivery. **SCREENSHOT**
	1. In **Execution frequency**, select **Weekly**.
	1. Select a **Time** and a **Repetition frequency** for your deliveries.
	1. In **Days of the week**, select **Tuesday**.
	1. Specify a **Start** and an **Expiration** parameter for your workflow.
Note: To start your workflow at a specific **Time Zone**, in the **Execution options** tab, set up the time zone for your scheduler in the Time zone field. 
	1. Confirm your activity and save your workflow.

## Creating a Query activity

1. In **Activities** > **Targeting**, to select recipients, drag and drop a **query** activity and double-click it.
	1. In **Shortcuts** > **Profile**, drag and drop **Email**.
	1. Select **is not empty** as an operator.
	1. In **Shortcuts** > **General**, add profiles and select **no longer contact by email** with the value **No**.
	1. Click **Confirm**.

## Creating an email delivery

1. In **Activities** > **Channels**, drag and drop an **Email delivery**.
	1. Click the activity and select /*"Pencil"*/ to edit.
	1. Select **Recurring email** and click **Next**.
	1. Select an email template and click **Next**.
	1. Enter the email properties and click **Next**.
 1. To create the layout of your email, click on **Use Email Designer**.
	1. Insert elements or select an existing template.
	1. Personalize your email using fields and links.
	For more information, refer to [designing an email](https://helpx.adobe.com/campaign/standard/designing/using/about-email-content-design.html#designing-an-email-content-from-scratch).
1. Click **Save**.

Related topics: 

Query https://helpx.adobe.com/campaign/standard/automating/using/query.html
Segmentation activity https://helpx.adobe.com/campaign/standard/automating/using/segmentation.html
Email delivery https://helpx.adobe.com/campaign/standard/automating/using/email-delivery.html
