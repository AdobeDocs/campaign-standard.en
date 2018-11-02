---
title: Configuration
seo-title: Configuration
description: Configuration
seo-description: Learn how to configure the Adobe Marketing Cloud Triggers integration to start sending personalized deliveries to your customers based on their previous behaviors. 
page-status-flag: never-activated
uuid: 2ba6236e-9b7c-4114-91ad-8f621a81aa16
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/integrating/using/configuration
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-01-10T15 24 19.304-0500
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: marketing-cloud-triggers
cq-template: /apps/help/templates/article-3
discoiquuid: 2e14e525-bc42-4f19-bea6-de6a6e87a882
firstPublishExternalDate: 2018-01-10T15:24:19.298-0500
herogradient: light
jcr-created: 2018-01-11T19 02 17.342-0500
jcr-createdby: admin
jcr-description: Configuration
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-01-10T15:24:19.298-0500
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Configuration
publishexternaldate: 2018-01-10T15 24 19.298-0500
publishExternalURL: https://helpx.adobe.com/campaign/standard/integrating/using/configuration.html
sha1: 702229967238945c251f32d2bdec73571fe26cbe
topicBrowsingSortDate: 2018-01-10T15:24:19.298-0500
index: y
internal: n
snippet: y
---

# Configuration

Configuration

## Activating the functionality

The functionality must be activated in Adobe Campaign by Adobe. Please contact your Adobe account executive or professional services partner.

## Defining aliases

Aliases enable a contact in Analytics to be reconciled with a profile in Campaign. These aliases have to be defined in the Marketing Cloud ID service and a matching AMC Data source has to be defined in Campaign.

To define the Adobe Marketing Cloud data sources, select the **Administration** > **Application settings** > **AMC Data sources** advanced menu.

## AMC Prerequisites

You should make sure to define the behaviors that you want to monitor beforehand in Adobe Marketing Cloud (**Triggers** core service). For more on this, refer to the [Adobe Marketing Cloud documentation](https://marketing.adobe.com/resources/help/en_US/mcloud/t_create-trigger.html). Note that when you define the trigger, you need to enable the aliases.

For each behavior (cart abandonment, adding/deleting products, session expired, etc.), a new trigger must be added in Adobe Marketing Cloud.

## Defining the trigger event

You now have to create a trigger event in Adobe Campaign based on an existing Adobe Marketing Cloud trigger.

The steps for putting this into place are:

1. Click the **Adobe Campaign** logo, in the top left corner, then select **Marketing plans** > **Transactional messages** > **Marketing Cloud Triggers**.

   ![](assets/remarketing_1.png)

1. Click the **Create** button. The creation wizard that opens displays the list of all of the triggers defined in Adobe Marketing Cloud. The **Fired by Analytics** column displays the number of events sent by the Adobe Marketing Cloud trigger to Campaign.

   ![](assets/remarketing_2.png)

1. Select the Adobe Marketing Cloud trigger that you want to use and click **Next**.
1. Configure the general properties of the trigger. At this step of the wizard, also specify the channel and the targeting dimension to use for the trigger. Then confirm the trigger creation.
1. Click the button to the right of the **Event content and enrichment** field to view the content of the payload. This screen also allows you to enrich the event data with profile data stored in the Adobe Campaign database. The enrichment is performed in the same way as for a standard transactional message. 

   ![](assets/remarketing_3.png)

1. In the **Transactional message validity duration** field, define the duration for which the message will stay valid after the event is sent by Analytics. If a duration of 2 days is defined, the message will no longer be sent after that duration has passed. If you put several messages on hold, this ensures that those messages will not be sent if you resume them after a certain period of time.

   ![](assets/remarketing_4.png)

1. If a propensity scoring is defined in Analytics (see the [Marketing Cloud documentation](https://marketing.adobe.com/resources/help/en_US/mcloud/propensity-scoring.html)), you can choose not to send the message if the customer has a high probability of coming back to the website in the near future. The content of the score and the threshold is available in the content of the payload so that you can use those values to personalize the message. To use this option, check the box at the bottom of the screen. The clients with a strong probability of coming back to the site in the near future will not receive a message.
1. Click the **Publish** button to start publishing the trigger event.

The **Show Trigger in Marketing Cloud** button allows you to view the trigger definition in Adobe Marketing Cloud.

Once the event has been published, a transactional template linked to the new event is then automatically created. You then have to modify and publish the template that was just created. For more on this, refer to the [Editing the template](../../start/using/about-templates.md) section.

## Editing the template

Once you have created and published the trigger event, the corresponding transactional template is created automatically. For more on this, refer to the [Defining the trigger event](../../integrating/using/configuration.md#defining-the-trigger-event) section.

In order for the event to trigger sending a transactional message, you have to personalize the template, then test it and publish it. These steps are the same as for a standard transactional message. For more on this, refer to the [Transactional template](../../channels/using/event-transactional-messages.md#personalizing-a-transactional-message) section.

>[!NOTE]
>
>If you unpublish the template, it will automatically unpublish the trigger event.

When editing content, you can add a personalization field based on the information sent by the Analytics trigger. If you enrich the event data with Adobe Campaign profile data, you can personalize the message based on this information. To personalize your message, select **Transactional event** > **Event context** and select a field.

![](assets/remarketing_8.png)

## Accessing the reports

To view the dedicated trigger report in Adobe Campaign, open the trigger event that you previously created, and click **Show trigger report**. 

![](assets/remarketing_9.png)

The report shows the number of processed events compared to the number of events sent by Analytics. It also displays a list of all the recent triggers. 

![](assets/remarketing_10.png)

