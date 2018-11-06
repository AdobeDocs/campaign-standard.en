---
title: Event transactional messages
seo-title: Event transactional messages
description: Event transactional messages
seo-description: Learn how to create and publish an event transactional message.
uuid: b78f047b-ae1c-42d5-bb36-4408e65913fc
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/channels/using/event-transactional-messages
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-30T04 54 05.409-0400
cq-lastreplicated: 2018-07-23T06 03 00.012-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: transactional-messaging
cq-template: /apps/help/templates/article-3
discoiquuid: f28ee10d-070b-4a2c-85ac-f9f03042fc94
firstPublishExternalDate: 2018-07-23T06:02:59.976-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 01 20.940-0400
jcr-createdby: admin
jcr-description: Event transactional messages
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T06:02:59.976-0400
lochandoffdate: 2018-07-30T04 54 05.408-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Event transactional messages
publishexternaldate: 2018-07-23T06 02 59.976-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/channels/using/event-transactional-messages.html
sha1: 61249259613b48669887c7b3f7b61df5e103400a
topicBrowsingSortDate: 2018-07-23T06:02:59.976-0400
index: y
internal: n
snippet: y
---

# Event transactional messages

Event transactional messages

Once you have created and published an event (the cart abandonment as explained in [this section](../../channels/using/about-transactional-messaging.md#transactional-messaging-operating-principle)), the corresponding transactional message is created automatically.

The configuration steps are presented in the [Configuring an event to send an event transactional message](../../administration/using/configuring-transactional-messaging.md#use-case--configuring-an-event-to-send-a-transactional-message) section.

In order for the event to trigger sending a transactional message, you have to personalize the message, then test it and publish it.

>[!NOTE]
>
>To access the transactional messages, you must have administration rights or appear in the **Message Center agents** (mcExec) security group. Event transactional messages do not contain profile information, therefore they are not compatible with fatigue rules (even in the case of an enrichment with profiles). See [Fatigue rules](../../administration/using/fatigue-rules.md#choosing-the-channel).

## Defining a test profile in a transactional message

Define an adapted test profile, which will allow you to preview your message and send a proof to check it.

### Creating a test profile within the transactional message

1. To access the message that you created, click the **Adobe Campaign** logo, in the top left corner, then select **Marketing plans** > **Transactional messages** > **Transactional messages**.

   ![](assets/message-center_4.png)

1. Create a test profile that will be linked to your event.

   ![](assets/message-center_test-profile.png)

1. Specify the information to send in JSON format in the **Event data used for personalization** section. This is the content that will be used when previewing the message and when the test profile receives the proof.

   ![](assets/message-center_event-data.png)

   >[!NOTE]
   >
   >You can also enter the information relating to the profile table. See [Enriching the transactional message content](../../administration/using/configuring-transactional-messaging.md#enriching-the-transactional-message-content).

1. After having been created, the test profile will be pre-specified in the transactional message. Click the **Test profiles** block of the message to check the target of your proof.

   ![](assets/message-center_5.png)

### Creating a test profile outside the transactional message

You can also create a new test profile or use one that already exists in the **Test profiles** menu.

1. Click the **Adobe Campaign** logo, in the top left corner, then select **Profiles & audiences** > **Test profiles**.
1. In the **Event** section of the page of the test profile that you have chosen, select the event that you have just created. In this example, select "Cart abandonment (EVTcartAbandonment)".
1. Specify the information to send in JSON format in the **Event data** text box.

   ![](assets/message-center_3.png)

1. Save your changes.

You can now access the message that you created and select the updated test profile.

**Related topics:**

* [Managing test profiles](../../sending/using/managing-test-profiles-and-sending-proofs.md)
* [Defining audiences](../../audiences/using/creating-audiences.md)

## Personalizing a transactional message

To set up personalization in a transactional message, follow the steps below:

1. Click the **Content** block to modify your message's subject and content. For this example, import an HTML template containing images, the style sheet, and an HTML file. Importing HTML templates is presented in the [Loading an existing content](../../designing/using/selecting-an-existing-content.md) section.

   ![](assets/message-center_6.png)

1. Enter your message content. In this example, we have added three personalization fields: last name, last product consulted, total cart amount. The link to the abandoned cart is a link to an external URL that will redirect the person to their cart. This parameter is not managed in Adobe Campaign.

   To add fields that you defined when you created your event (see [Configuring an event](../../administration/using/configuring-transactional-messaging.md#use-case--configuring-an-event-to-send-a-transactional-message)), insert a personalization field in the message content. You can find the fields by selecting **Transactional event** > **Event context**.

   ![](assets/message-center_7.png)

1. To enrich the content of your message, add fields by selecting them from the table with which you linked your event. In our example, select the **Title (salutation)** field in the **Profile** table.

   ![](assets/message-center_7-enrichment.png)

   The steps for inserting a personalization field are detailed in the [Inserting a personalization field](../../designing/using/inserting-a-personalization-field.md) section.

   ![](assets/message-center_8.png)

1. Preview your message by selecting the profile that you defined for this event.

   The steps for previewing a message are detailed in the [Previewing messages](../../sending/using/preparing-the-send.md) section.

   ![](assets/message-center_9.png)

   You can check that the personalization fields match the information entered in the test profile. For more on this, see [Defining a test profile in a transactional message](../../channels/using/event-transactional-messages.md#defining-a-test-profile-in-a-transactional-message).

## Testing a transactional message

Once you have saved your transactional message, you can now send a proof to test it.

![](assets/message-center_10.png)

The steps for sending a proof are detailed in the [Sending a proof](../../sending/using/managing-test-profiles-and-sending-proofs.md#sending-proofs) section.

## Publishing a transactional message

Once you have checked your transactional message, you can publish it.

![](assets/message-center_12.png)

Now, as soon as the "Cart abandonment" event is triggered, it automatically prompts a message containing the recipient's title and last name, the cart URL, the last product consulted, and the total cart amount to be sent.

To access reports concerning your transactional message, use the **Reports** button. See [Reports](../../reporting/using/about-dynamic-reports.md).

![](assets/message-center_13.png)

## Suspending a transactional message publication

You can suspend publishing your transactional message by using the **Pause** button, for example, to modify the data contained in the message. The events are therefore no longer processed, but instead kept in a queue in the Adobe Campaign database.

The queued events are kept during a period of time that is defined in the REST API (see [REST API documentation](https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html)) or in the trigger event if you are using the Triggers core service (see [Working with Campaign and Experience Cloud Triggers](../../integrating/using/about-adobe-experience-cloud-triggers.md)).

![](assets/message-center_pause.png)

When clicking **Resume**, all of the queued events (provided that they are not expired) are processed. They now contain all of the modifications carried out while the template publication was suspended.

## Unpublishing a transactional message

Clicking **Unpublish** allows you to cancel the transactional message publication, but also the publication of the corresponding event, which deletes from the REST API the resource corresponding to the event that you previously created. Now, even if the event is triggered through your website, the corresponding messages are not sent anymore and they are not stored in the database.

![](assets/message-center_unpublish-template.png)

>[!NOTE]
>
>To publish the message again, you need to go back to the corresponding event configuration, publish it, and then publish the message. For more on this, see [Publishing a transactional message](../../channels/using/event-transactional-messages.md#publishing-a-transactional-message).

If you unpublish a paused transactional message, you may have to wait up to 24 hours before you can publish it again. This is to let the **Database cleanup** workflow clean all the events that were sent to the queue. The steps for pausing a message are detailed in the [Suspending a transactional message publication](../../channels/using/event-transactional-messages.md#suspending-a-transactional-message-publication) section.

The **Database cleanup** workflow, which runs every day at 4am, is accessible through **Administration** > **Application settings** > **Workflows**.

## Deleting a transactional message

![](assets/message-center_delete-template.png)

By selecting a transactional message, you can delete it with the **Delete element** button even if it has already been published. However, deleting a transactional message can only be done under certain conditions:

* **For transaction message**: To delete a transactional message, the messages should be unpublished and not paused.

  If the transactional message is unpublished, the event configuration also needs to be unpublished to successfully delete your transactional message unless another transactional message is linked to the corresponding event. For more information on how to unpublish a transactional message, refer to this [section](../../channels/using/event-transactional-messages.md#unpublishing-a-transactional-message).

  >[!CAUTION]
  >
  >Deleting a transactional message that has already sent notifications will also delete its sending and tracking logs.

* **For transactional message from an out-of-the-box event template (internal transactional messages)**: To delete an internal transactional message, the messages should be unpublished and not paused.

  It also shouldn't be the only transactional message in the event, other messages have to be linked to the corresponding event.

