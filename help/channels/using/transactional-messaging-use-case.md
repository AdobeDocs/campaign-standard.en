---
title: Configuring transactional messaging
description: Learn how to configure transactional messaging.
page-status-flag: never-activated
uuid: 4caeadbe-f4a7-43ce-986d-e99fa9ca0d0d
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: configuring-channels
discoiquuid: 3f968556-e774-43dc-a0b8-7188d7665fbc

internal: n
snippet: y
---

# Use case: configuring an event to send a transactional message {#use-case--configuring-an-event-to-send-a-transactional-message}

In this example, we want to configure an event in order to send confirmation messages after each purchase on our website with the following prerequisites:

As we want to identify our client via his CRM ID, first make sure that the **[!UICONTROL Profile]** resource has been extended with this new field.

In the same way, a custom resource corresponding to purchases must have been created and published, and must be linked to the **[!UICONTROL Profile]** resource. This way, you will be able to retrieve information from this resource to enrich the message content.

For more on resource creation and publishing, refer to [this page](../../developing/using/key-steps-to-add-a-resource.md).

1. Create a new event using the **[!UICONTROL Email]** channel and the **[!UICONTROL Profile]** targeting dimension (see [Creating an event](#creating-an-event)).
1. Define the attributes that will be available to personalize the transactional message. In our case, add the "CRM ID" and the "Product identifier" fields (see [Defining the event attributes](#defining-the-event-attributes)).

   ![](assets/message-center_usecase1.png)

1. To enrich the message content with information regarding the client's previous purchases, create an enrichment targeting the **[!UICONTROL Purchase]** resource (see [Enriching the transactional message content](#enriching-the-transactional-message-content)).

   ![](assets/message-center_usecase2.png)

1. Create a join condition between the "Product identifier" field that was previously added to the message, and the corresponding field from the **[!UICONTROL Purchase]** resource.

   ![](assets/message-center_usecase3.png)

1. Preview and publish the event (see [Previewing and publishing the event](#previewing-and-publishing-the-event)).
1. Integrate the event in your website (see [Integrating the triggering of the event in a website](#integrating-the-triggering-of-the-event-in-a-website)).

