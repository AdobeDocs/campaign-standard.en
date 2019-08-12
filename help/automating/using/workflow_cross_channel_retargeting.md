---
title: "Workflow use-case: Retargeting non-openers"
seo-title: "Workflow use-case: Retargeting non-openers"
description: "Workflow use-case: Retargeting non-openers"
seo-description: "Workflow use-case: Retargeting non-openers"
page-status-flag: never-activated
uuid: 396a3de1-6ffa-4385-ac9f-15fdeae5a366
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: execution-activities
discoiquuid: 377821e6-69f8-41cc-a1ad-8a2f5ed4d409
context-tags: workflow,use-case,query,wait,delivery 
internal: n
snippet: y
---

# Workflow use-case: Retargeting workflow sending a new delivery to non-openers{#retargeting-delivery-to-non-openers}

You can send an email to customers and then an sms to those who did not open the mail.

1. In **Marketing Activities**, click **Create** and select **Workflow**.
1. Select **New Workflow** as workflow type and click **Next**.
1. Enter properties of the workflow and click **Create**.

## Creating a query activity{#creating-a-query-activity}

1. In **Activities** > **Targeting**, drag and drop a **Query activity** ![](assets/query.png).
1. Double-click the activity.
1. In **Shortcuts**, drag and drop **Profiles** and select **email** with the operator **is not empty**.
1. In **Shortcuts**, drag and drop **Profiles** and select **no longer contact by email** with the value **no**.
1. Click **Confirm**.

## Creating an email delivery{#creating-an-email-delivery}

1. Drag and drop an email delivery after each segment.
	1. Click the activity and select ![](assets/edit_darkgrey-24px.png) to edit.
	1. Select **Simple email** and click **Next**.
	1. Select **Add an outbound transition without the population** and click **Next**.
	1. Select an email template and click **Next**.
	1. Enter the email properties and click **Next**.
	1. Rename the email with **email offer**.
  1. To create the layout of your email, click on **Email Designer**.
	1. Insert elements or select an existing template.
	1. Personalize your email with offers specific to each location.For more information, refer to [designing an email](../../designing/using/about-email-content-design.md#designing-an-email-content-from-scratch).
1. Click **Preview** to check your layout.
1. Click **Save**.

## Targeting non-openers in a query activity{#targeting-non-openers-in-a-query-activity}

1. In **Activities** > **Execution**, drag and drop a **Wait activity** ![](assets/wait.png).
1. In **Duration**, click on ![](assets/duration-icon.png) and select one day.
1. In **Activities** > **Targeting**, drag and drop a **Query activity** ![](assets/query.png).
1. Double-click the activity.
1. In **Shortcuts**, drag and drop **Tracking Logs** and with the operator **exists**.
1. In **Shortcuts** > **Delivery**, drag and drop **delivery** with the operator **is equal to** and select the delivery as value.
1. In **Shortcuts**> **Delivery**, drag and drop **type** and check **Open** as value.
1. Select the operator between rules as **except**.
1. Click **Confirm**.

## Creating a sms delivery{#creating-a-sms-delivery}

1. Drag and drop an sms delivery after each segment.
	1. Click the activity and select ![](assets/edit_darkgrey-24px.png) to edit.
	1. Select **Simple sms** and click **Next**.
	1. Select an sms template and click **Next**.
	1. Enter the sms properties and click **Next**.
  1. To create the layout of your sms, click on **Email Designer**.
	1. Insert elements or select an existing template.
	1. Personalize your sms with offers specific to each location.
	For more information, refer to [designing an sms](../../channels/using/creating-an-sms-message.md).
1. Click **Preview** to check your layout.
1. Click **Save**.

**Related topics:**

* [Query](../../automating/using/query.md)
* [SMS delivery](../../automating/using/sms-delivery.md)
* [Email delivery](../../automating/using/email-delivery.md)
* [Email channel](../../channels/using/creating-an-email.md)
