---
title: Testing your triggers
description: Learn troubleshooting tips to help you solve the most common problems you may encounter when using Triggers with Adobe Campaign.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-triggers
feature: Triggers
role: Data Architect
level: Intermediate
exl-id: 66628f2a-6ed3-4b12-b2ed-9b9eec440dc3
---
# Testing your triggers{#testing-your-triggers}

The following troubleshooting tips help you solve the most common problems you may encounter when using Triggers with Adobe Campaign:

**Is the functionality activated?**

To check if the Triggers - Campaign integration is activated, click the Adobe Campaign logo, in the top-left corner, then select **[!UICONTROL Marketing plans]** > **[!UICONTROL Transactional messages]**. You should see the **[!UICONTROL Experience Cloud Triggers]** item.

If you see it, move on to the next step.

If not, contact your Adobe account executive or professional services partner. See [Activating the functionality](../../integrating/using/configuring-triggers-in-experience-cloud.md#activating-the-functionality).

**Try creating a trigger**

Follow the steps described in [Creating a mapped trigger in Campaign](../../integrating/using/using-triggers-in-campaign.md#creating-a-mapped-trigger-in-campaign) to create a trigger.

If the trigger is created, move on to the next step. If not, it means that the trigger end point connection failed. Check if Triggers is provisioned in Experience Cloud (Activation services). If it is not, contact your Adobe account executive or professional services partner. The following information is required:

* Marketing Cloud Company Name
* Organization ID
* Analytics Login Company (can be the same as the Marketing Cloud Company Name)

**Try publishing the trigger**

Follow the steps described in [Creating a mapped trigger in Campaign](../../integrating/using/using-triggers-in-campaign.md#creating-a-mapped-trigger-in-campaign) to publish the trigger.

If the publication succeeded, move on to the next step. If not, contact Adobe to restart your instance and try again.

**Generate the trigger from the website**

Follow the steps described in [Editing the transactional message template](../../integrating/using/using-triggers-in-campaign.md#editing-the-transactional-message-template) to edit and publish the transactional template. Then, test the generation of the trigger from the website.

If the trigger is received by Analytics, move on to the next step. If not, check the following items:

* Trigger is enabled for Analytics
* The website used MCID and Analytics is enabled in DTM
* The correct Analytics report suite is used while creating triggers

**Is the trigger received by Campaign?**

If not, check if the trigger is received from the pipeline.

If not, contact Adobe to check the configuration of the pipeline end points.

If it is, follow these guidelines:

* Check the reconciliation ID type in Campaign datasource.
* CustomerId Datasource is created via Customer Attributes.
* Check the Datasource ID.
* Ask Adobe to restart the Campaign instance after the Datasource configuration. 
* Check trigger parsing issues in the trigger report.

**Is the trigger in pending status?**

If not, move on to the next step. If it is, follow these guidelines:

* Check that the transactional template is published.
* Check that the profile is not on denylist.
* Check the application of typology rules.
* Check the transactional message's logs.

**Is the message valid?**

If the message is not valid, check the following items:

* For trigger enrichment personalization fields marked as invalid, validate the transactional template from the associated eventCusResource collections.
* Validate the message format
