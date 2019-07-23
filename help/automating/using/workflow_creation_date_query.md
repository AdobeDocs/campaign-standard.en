---
title: Use case: Create deliveries on creation date 
seo-title: Use case: Create deliveries on creation date 
description: Use case: Create deliveries on creation date 
seo-description: Use case: Create deliveries on creation date 
page-status-flag: never-activated
uuid: 396a3de1-6ffa-4385-ac9f-15fdeae5a366
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: execution-activities 
discoiquuid: 377821e6-69f8-41cc-a1ad-8a2f5ed4d409
context-tags: workflow,use-case,query
internal: n
snippet: y
---

# Creation date query 

You can send an offer via email on the anniversary of the customer's profile creation.

1. In a Marketing Activities, click create and select **Workflow**.
1. Select **New Workflow** as workflow type and click **Next**.
1. Enter properties of the workflow and click **Create**. 

## Creating a Scheduler activity

1. In **Activities** > **Execution**, drag and drop a **Scheduler activity**. **ICON**
1. Double-click the activity.
1. Configure the execution of your delivery. **SCREENSHOT**
	1. In **Execution frequency**, select **Daily**.
	1. Select a **Time** and the **Repetition frequency** of execution for your workflow.
	1. Select a **Start** date and **Expiration** for your workflow.
NOTE: To start your workflow at a specific time zone, in the **Execution options** tab, set up the time zone for your scheduler in the **Time zone** field. **SCREENSHOT**
	1. Confirm your activity and save your workflow.

## Creating a query activity

1. To select recipients, drag and drop a query activity and double-click it.
1. Add profiles and select no longer contact by email with the value no. 	

### Retriving profiles created on the same day as the day of execution


1. In Profile, drag and drop the Created field. At the top-right of the window, click on **Advanced Mode**. **SCREENSHOT**
1. In the **list of functions**, double-click Day from the **Date** node.
1. Then, insert the field **Created** as argument.
1. Select **equals to** (=) as the operator.
1. For Value, select **Day** from the **Date** node in the **List of functions**.
1. Insert the **GetDate()** function as argument.  
	You retrieved the profiles which creation day is equal to current day.
	You should end up with this:
	```Day(@created) = Day(GetDate())```
	**SCREENSHOT**
1. Click **Confirm**.

### Retriving profiles created on the same month as the month of execution

1. On the Query editor, select the first query and duplicate it. **SCREENSHOT**
1. Open the duplicate.
1. Replace Day by Month in the query.
	You should end up with this:  
	```Month(@created) = Month(GetDate())```
1. Click **Confirm**.

**SCREENSHOT**

## Creating an email delivery

1. Drag and drop an email delivery.
	1. Click the activity and select /*"Pencil"*/ to edit.
	1. Select **Recurring email** and click **Next**.
	1. Select an email template and click **Next**.
	1. Enter the email properties and click **Next**.
  1. To create the layout of your email, click on **Email Designer**.
	1. Insert elements or select an existing template.
	1. Personalize your email using fields and links.
	For more information, refer to [designing and email](https://helpx.adobe.com/campaign/standard/designing/using/about-email-content-design.html#designing-an-email-content-from-scratch).
1. Click **Preview** to check your layout.
1. Click **Save**.

Related topics:

Query https://helpx.adobe.com/campaign/standard/automating/using/query.html
Scheduler https://helpx.adobe.com/campaign/standard/automating/using/scheduler.html
Email delivery https://helpx.adobe.com/campaign/standard/automating/using/email-delivery.html
Email channel https://helpx.adobe.com/campaign/standard/channels/using/creating-an-email.html
