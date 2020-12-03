---
solution: Campaign Standard
product: campaign
title: Configuring transactional messaging
description: Learn how to configure transactional messaging.
audience: administration
content-type: reference
topic-tags: configuring-channels
context-tags: 
---

# Configuring a transactional event {#configuring-transactional-event}

To send a transactional message with Adobe Campaign, you first need to describe the structure of the event data by creating and configuring an event.

>[!IMPORTANT]
>
>Only [administrators](../../administration/using/users-management.md#functional-administrators) being part of the **[!UICONTROL All]** [organizational unit](../../administration/using/organizational-units.md) have the appropriate rights to create and edit event configurations.

The configuration varies depending on the [type of transactional message](../../channels/using/getting-started-with-transactional-msg.md#transactional-message-types) you want to send, and on the channel that will be used. For more on this, see [Specific configurations](#transactional-event-specific-configurations).

Once configuration is done, the event must be published. See [Publishing a transactional event](../../channels/using/publishing-transactional-event.md).

## Creating an event {#creating-an-event}

To get started, create the event corresponding to your needs.

1. Click the **[!UICONTROL Adobe Campaign]** logo, in the top left corner, then select **[!UICONTROL Marketing plans]** > **[!UICONTROL Transactional messages]** > **[!UICONTROL Event configuration]**.
1. Click the **[!UICONTROL Create]** button.
1. Enter a **[!UICONTROL Label]** and an **[!UICONTROL ID]** for the event. The **[!UICONTROL ID]** field is mandatory and should begin with the prefix "EVT". If you do not use this prefix, it is automatically added once you click **[!UICONTROL Create]**. 

   ![](assets/message-center_1.png)

   >[!IMPORTANT]
   >
   >The ID must not exceed 64 characters, including the EVT prefix.

1. Select the channel that will be used to send your transactional messages **[!UICONTROL Email]**, **[!UICONTROL Mobile (SMS)]** or **[!UICONTROL Mobile application]** (push notification). Only one channel can be used for each event and it cannot be changed afterwards.

1. Select the targeting dimension corresponding to the desired event configuration and click **[!UICONTROL Create]**.

   Event-based transactional messages target data contained in the event itself, whereas profile-based transactional messages target data contained in the Adobe Campaign database. For more on this, refer to [Specific configurations](#transactional-event-specific-configurations).

>[!NOTE]
>
>The number of real-time events can have an impact on your platform. To ensure optimal performance, make sure you delete unused real-time events. See [Deleting an event](../../channels/using/publishing-transactional-event.md#deleting-an-event).

## Defining the event attributes {#defining-the-event-attributes}

In the **[!UICONTROL Fields]** section, define the attributes that will be integrated into the event content and will then be able to be used to personalize the transactional message.

The steps for adding and modifying fields are the same as for [custom resources](../../developing/using/configuring-the-resource-s-data-structure.md#adding-fields-to-a-resource).

![](assets/message-center_2.png)

>[!NOTE]
>
>If you want to create a multilingual transactional message, define an additional event attribute with the **[!UICONTROL AC_language]** ID. This only applies to event transactional messages. After the event is published, the steps for editing the content of a multilingual transactional message are the same as for a multilingual standard email. See [Creating a multilingual email](../../channels/using/creating-a-multilingual-email.md).

## Defining data collections {#defining-data-collections}

You can add to the event content a collection of elements, each element itself including several attributes.

This collection can be used in a transactional email to add [product listings](../../channels/using/editing-transactional-message.md#using-product-listings-in-a-transactional-message) to the content of the message, for example a list of products - with the price, reference number, quantity, etc. for each product of the list.

1. In the **[!UICONTROL Collections]** section, click the **[!UICONTROL Create element]** button.

   ![](assets/message-center_collection_create.png)

1. Add a label and an ID for your collection.
1. Add all the fields you want to display in the transactional message for each product of the list.

   In this example, we added the following fields:

   ![](assets/message-center_collection_fields.png)

1. The **[!UICONTROL Enrichment]** tab allows you to enrich each item of the collection. This will enable you to personalize the elements of the corresponding product listing with information from the Adobe Campaign database or from other resources that you created.

>[!NOTE]
>
>The steps for enriching the elements of a collection are the same as described in the [Enriching the event](#enriching-the-transactional-message-content) section. Note that enriching the event will not allow you to enrich a collection: you need to add an enrichment to the collection itself in the **[!UICONTROL Collections]** section.

Once the event and the message are published, you will be able to use this collection in your transactional message.

Here is the API preview for this example:

![](assets/message-center_collection_api-preview.png)

**Related topics:**

* [Previewing and publishing the event](../../channels/using/publishing-transactional-event.md#previewing-and-publishing-the-event)
* [Using product listings in a transactional message](../../channels/using/editing-transactional-message.md#using-product-listings-in-a-transactional-message)
* [Publishing a transactional message](../../channels/using/publishing-transactional-message.md#publishing-a-transactional-message)

## Enriching the event {#enriching-the-transactional-message-content}

You can enrich the transactional message content with information from the Adobe Campaign database in order to personalize your messages. From the last name or CRM ID of each of your recipients, for example, you can recover data such as their address or date of birth or any other custom field added in the Profile table, in order to personalize the information that is sent to them.

It is possible to enrich the transactional message content with information from extended **[!UICONTROL Profile and services Ext API]**. For more information, see [Extending the API: Publishing the extension](../../developing/using/step-2--publish-the-extension.md)

This information can also be stored in new resources. In that case, the resource must be linked to the **[!UICONTROL Profile]** or **[!UICONTROL Service]** resources either directly, or via another table. For example, in the configuration below, it is possible to enrich the transactional message content with information from the **[!UICONTROL Product]** resource like the product category or ID, if the **[!UICONTROL Product]** resource is linked to the **[!UICONTROL Profile]** resource.

![](assets/message-center_usecaseschema.png)

For more on creating and publishing resources, see [this section](../../developing/using/key-steps-to-add-a-resource.md).

1. In the **[!UICONTROL Enrichment]** section, click the **[!UICONTROL Create element]** button.

   ![](assets/message-center_addenrichment.png)

1. Select the resource with which you want to link your message. In this case, choose the **[!UICONTROL Profile]** resource.

   ![](assets/message-center_new-enrichment.png)

1. Use the **[!UICONTROL Create element]** button to link a field from the selected resource to one of the fields you previously added to the event (see [Defining the event attributes](#defining-the-event-attributes)).

   ![](assets/message-center_enrichment-join.png)

1. In this example, we reconcile the **[!UICONTROL Last name]** and the **[!UICONTROL First name]** fields with the corresponding fields in the **[!UICONTROL Profile]** resource.

   ![](assets/message-center_enrichment-join-fields.png)

    You can also enrich the transactional message content using the **[!UICONTROL Service]** resource. For more on services, see [this section](../../audiences/using/creating-a-service.md).

1. If you are creating or editing a [profile-based event](#profile-based-transactional-messages), in the **[!UICONTROL Targeting enrichment]** section, select the enrichment that will be used as the message target during the delivery execution.

   ![](assets/message-center_marketing_targeting_enrichment.png)

   >[!NOTE]
   >
   >Selecting a targeting enrichment based on the **[!UICONTROL Profile]** resource is mandatory for profile-based events.

Once the event and the message are published, this link will allow you to enrich the content of the transactional message.

**Related topics:**

* [Previewing and publishing the event](../../channels/using/publishing-transactional-event.md#previewing-and-publishing-the-event)
* [Personalizing a transactional message](../../channels/using/editing-transactional-message.md#personalizing-a-transactional-message)
* [Publishing a transactional message](../../channels/using/publishing-transactional-message.md#publishing-a-transactional-message)

## Searching transactional events {#searching-transactional-events}

To access and search the transactional events already created, follow the steps below.

1. Click the **[!UICONTROL Adobe Campaign]** logo, in the top left corner, then select **[!UICONTROL Marketing plans]** > **[!UICONTROL Transactional messages]** > **[!UICONTROL Event configuration]**.
1. Click the **[!UICONTROL Show search]** button.

   ![](assets/message-center_search-events.png)

1. You can filter on the **[!UICONTROL Publication status]**. This allows you to display only the published events for example.
1. You can also filter the events using the **[!UICONTROL Last event received]**. For example, if you enter 10, only the event configurations with the last event received 10 days ago or more will be displayed. This enables you to display which events have been inactive for a given period.

   ![](assets/message-center_last-event-received.png)

   >[!NOTE]
   >
   >The default value is 0. All events are then displayed.

## Specific configurations {#transactional-event-specific-configurations}

Transactional event configuration may vary depending on the [type of transactional message](../../channels/using/getting-started-with-transactional-msg.md#transactional-message-types) you want to send (event or profile), and on the channel that will be used.

The following sections detail what specific configuration should be set according to the desired transactional message. For more on the general steps to configure an event, refer to [Creating an event](#creating-an-event).

### Event-based transactional messages {#event-based-transactional-messages}

You can send event transactional messages targeting an event. This type of transactional messages does not contain profile information: the delivery target is defined by the data contained in the event itself.

To send an event-based transactional message, you first need to create and configure an event targeting the **data contained in the event itself**.

1. When creating the event configuration, select the **[!UICONTROL Real-time event]** targeting dimension (see [Creating an event](#creating-an-event)).
1. Add fields to the event, in order to be able to personalize the transactional message (see [Defining the event attributes](#defining-the-event-attributes)).
1. Enrich the transactional message content if you want to use additional information from the Adobe Campaign database (see [Enriching the transactional message content](#enriching-the-transactional-message-content)).

   >[!NOTE]
   >
   >Event-based transactional messaging is supposed to use only the data that are in the sent event to define the recipient and the message content personalization. However, you can enrich the content of your transactional message using information from the Adobe Campaign database.

1. Preview and publish the event (see [Previewing and publishing the event](../../channels/using/publishing-transactional-event.md#previewing-and-publishing-the-event)).

   When previewing the event, the REST API contains an attribute specifying the email address or mobile phone according to the selected channel.

   Once the event has been published, a transactional message linked to the new event is automatically created. In order for the event to trigger sending a transactional message, you must [modify](../../channels/using/editing-transactional-message.md) and [publish](../../channels/using/publishing-transactional-message.md) the message that was just created.

1. Integrate the event into your website (see [Integrate event triggering](../../channels/using/getting-started-with-transactional-msg.md#integrate-event-trigger)).

### Profile-based transactional messages {#profile-based-transactional-messages}

You can send transactional messages based on customer profiles, which allows you to apply marketing typology rules, include the unsubscribe link, add the message to the global delivery reporting and leverage it in the customer journey.

To send a profile-based transactional message, you first need to create and configure an event targeting **data from the Adobe Campaign database**.

1. When creating the event configuration, select the **[!UICONTROL Profile event]** targeting dimension (see [Creating an event](#creating-an-event)).
1. Add fields to the event, in order to be able to personalize the transactional message (see [Defining the event attributes](#defining-the-event-attributes)). You must add at least one field to create an enrichment. You do not need to create other fields such as **First name** and **Last name** as you will be able to use personalization fields from the Adobe Campaign database. 
1. Create an enrichment in order to link the event to the **[!UICONTROL Profile]** resource (see [Enriching the transactional message content](#enriching-the-transactional-message-content)). Creating an enrichment is mandatory when using a **[!UICONTROL Profile]** targeting dimension.
1. Preview and publish the event (see [Previewing and publishing the event](../../channels/using/publishing-transactional-event.md#previewing-and-publishing-the-event)).

   When previewing the event, the REST API does not contain an attribute specifying the email address or the mobile phone as it will be retrieved from the **[!UICONTROL Profile]** resource.

   Once the event has been published, a transactional message linked to the new event is automatically created. In order for the event to trigger sending a transactional message, you must [modify](../../channels/using/editing-transactional-message.md) and [publish](../../channels/using/publishing-transactional-message.md) the message that was just created..

1. Integrate the event into your website (see [Integrate event triggering](../../channels/using/getting-started-with-transactional-msg.md#integrate-event-trigger)).

### Transactional push notifications {#transactional-push-notifications}

You can send two types of transactional push notifications:
* An anonymous transactional push notification to all users who have opted in to receive notifications from your mobile application. See [Configuring event-based transactional push notifications](../../channels/using/transactional-push-notifications.md#event-based-transactional-push-notifications).
* A transactional push notification to the Adobe Campaign profiles who have subscribed to your mobile application. See [Configuring profile-based transactional push notifications](../../channels/using/transactional-push-notifications.md#profile-based-transactional-push-notifications).

>[!IMPORTANT]
>
>To be able to send transactional push notifications, you need to configure Adobe Campaign accordingly. See [Configuring a mobile application](../../administration/using/configuring-a-mobile-application.md).

### Follow-up messages {#follow-up-messages}

You can send a follow-up message to the customers who received a specific transactional message.

The steps to configure an event allowing to send a follow-up message are detailed in [this section](../../channels/using/follow-up-messages.md#configuring-an-event-to-send-a-follow-up-message).
