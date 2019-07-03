---
title: Using Triggers in Campaign
seo-title: Using Triggers in Campaign
description: Using Triggers in Campaign
seo-description: 
page-status-flag: never-activated
uuid: d844d013-b38a-4e69-9df5-0edc01fa9c6e
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-triggers
discoiquuid: a524c700-bad6-4fcf-857a-c31bfae4d30c

internal: n
snippet: y
---

# Using Triggers in Campaign{#using-triggers-in-campaign}

## Creating a mapped trigger in Campaign {#creating-a-mapped-trigger-in-campaign}

You should make sure to define the behaviors that you want to monitor beforehand in Adobe Experience Cloud ( **[!UICONTROL Triggers]** core service). For more on this, refer to the [Adobe Experience Cloud documentation](https://marketing.adobe.com/resources/help/en_US/mcloud/triggers.html). Note that when you define the trigger, you need to enable the aliases. For each behavior (browsing/form abandonment, adding/deleting products, session expired, etc.), a new trigger must be added in Adobe Experience Cloud.

You now have to create a trigger event in Adobe Campaign based on an existing Adobe Experience Cloud trigger.

You can watch this [video](https://helpx.adobe.com/marketing-cloud/how-to/email-marketing.html#step-two) to help you understand how triggers are set up in Adobe Campaign.

The steps for putting this into place are:

1. Click the **[!UICONTROL Adobe Campaign]** logo, in the top left corner, then select **[!UICONTROL Marketing plans]** > **[!UICONTROL Transactional messages]** > **[!UICONTROL Experience Cloud Triggers]**. 

   ![](assets/remarketing_1.png)

1. Click the **[!UICONTROL Create]** button. The creation wizard that opens displays the list of all of the triggers defined in Adobe Experience Cloud. The **[!UICONTROL Fired by Analytics]** column displays the number of events sent by the Adobe Experience Cloud trigger to Campaign. This is mapping of triggers created in the Experience Cloud interface.

   ![](assets/remarketing_2.png)

1. Select the Adobe Experience Cloud trigger that you want to use and click **[!UICONTROL Next]**.
1. Configure the general properties of the trigger. At this step of the wizard, also specify the channel and the targeting dimension to use for the trigger (see [targeting dimensions and resources](../../automating/using/query.md#targeting-dimensions-and-resources)). Then confirm the trigger creation.
1. Click the button to the right of the **[!UICONTROL Event content and enrichment]** field to view the content of the payload. This screen also allows you to enrich the event data with profile data stored in the Adobe Campaign database. The enrichment is performed in the same way as for a standard transactional message. 

   ![](assets/remarketing_3.png)

1. In the **[!UICONTROL Transactional message validity duration]** field, define the duration for which the message will stay valid after the event is sent by Analytics. If a duration of 2 days is defined, the message will no longer be sent after that duration has passed. If you put several messages on hold, this ensures that those messages will not be sent if you resume them after a certain period of time.

   ![](assets/remarketing_4.png)

1. If a propensity scoring is defined in Analytics (see the [Experience Cloud documentation](https://marketing.adobe.com/resources/help/en_US/insight/client/c_visitor_propensity.html)), you can choose not to send the message if the customer has a high probability of coming back to the website in the near future. The content of the score and the threshold is available in the content of the payload so that you can use those values to personalize the message. To use this option, check the box at the bottom of the screen. The clients with a strong probability of coming back to the site in the near future will not receive a message.
1. Click the **[!UICONTROL Publish]** button to start publishing the trigger event.
1. If you need to make a change in your trigger schema even after publishing your trigger event, click the **[!UICONTROL Update schema]** button to retrieve the latest changes.

   Please note that this action will unpublish your trigger and transactional message, you will be required to republish them afterwards.

   ![](assets/remarketing_11.png)

The **[!UICONTROL Show Trigger in Experience Cloud]** button allows you to view the trigger definition in Adobe Experience Cloud.

Once the event has been published, a transactional template linked to the new event is then automatically created. You then have to modify and publish the template that was just created. For more on this, refer to the [Editing the template](../../start/using/about-templates.md) section.

## Editing the transactional message template {#editing-the-transactional-message-template}

Once you have created and published the trigger event, the corresponding transactional template is created automatically. For more on this, refer to the [Creating a mapped trigger in Campaign](../../integrating/using/using-triggers-in-campaign.md#creating-a-mapped-trigger-in-campaign) section.

In order for the event to trigger sending a transactional message, you have to personalize the template, then test it and publish it. These steps are the same as for a standard transactional message. For more on this, refer to the [Transactional template](../../channels/using/event-transactional-messages.md#personalizing-a-transactional-message) section.

>[!NOTE]
>
>If you unpublish the template, it will automatically unpublish the trigger event.

When editing content, you can add a personalization field based on the information sent by the Analytics trigger. If you enrich the event data with Adobe Campaign profile data, you can personalize the message based on this information. To personalize your message, select **[!UICONTROL Transactional event]** > **[!UICONTROL Event context]** and select a field.

![](assets/remarketing_8.png)

## Accessing the reports {#accessing-the-reports}

To view the dedicated trigger report in Adobe Campaign, open the trigger event that you previously created, and click **[!UICONTROL Show trigger report]**. 

![](assets/remarketing_9.png)

The report shows the number of processed events compared to the number of events sent by Analytics. It also displays a list of all the recent triggers. 

![](assets/trigger_uc_browse_14.png)

