---
title: Follow-up messages
seo-title: Follow-up messages
description: Follow-up messages
seo-description: Learn how to create and publish a follow-up message.
uuid: 3e0bfd11-63ec-40e4-aae4-79fbd4a51947
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/channels/using/follow-up-messages
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-30T04 54 08.339-0400
cq-lastreplicated: 2018-07-23T06 03 13.878-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: transactional-messaging
cq-template: /apps/help/templates/article-3
discoiquuid: 8b6b355b-d758-4e94-8216-f9fe2e0aec7c
firstPublishExternalDate: 2018-07-23T06:03:13.845-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 01 28.109-0400
jcr-createdby: admin
jcr-description: Follow-up messages
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T06:03:13.845-0400
lochandoffdate: 2018-07-30T04 54 08.339-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Follow-up messages
publishexternaldate: 2018-07-23T06 03 13.845-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/channels/using/follow-up-messages.html
sha1: 5a5d8a8b9f9c5b18f366fece2983d778b5d57d05
topicBrowsingSortDate: 2018-07-23T06:03:13.845-0400
index: y
internal: n
snippet: y
---

# Follow-up messages

Follow-up messages

You can send a follow-up message to the customers who received a specific transactional message. To do this, you need to set up a workflow targeting the corresponding event.

Let's reuse the example described in the [Transactional messaging operating principle](../../channels/using/about-transactional-messaging.md#transactional-messaging-operating-principle) section: a cart abandonment email is sent to your website users who added products to their cart, but left the site without going through with their purchases.

You want to send a friendly reminder to all of the customers who received the cart abandonment notification but who did not open it after three days.

Each concerned customer will then receive a follow-up message based on the same data that was used in the first email that was sent.

## Accessing the follow-up messages

Once you have created and published an event (the cart abandonment as per the [example](../../channels/using/about-transactional-messaging.md#transactional-messaging-operating-principle) above), the corresponding transactional message and follow-up message are created automatically.

The configuration steps are presented in the [Configuring an event to send a follow-up message](../../administration/using/configuring-transactional-messaging.md#use-case--configuring-an-event-to-send-a-transactional-message) section.

To handle an event in a workflow, a delivery template is required. However, when publishing the event, the [transactional message](../../channels/using/event-transactional-messages.md) that is created cannot be used as a template. Therefore, you need to create a specific follow-up delivery template designed to support this event type and to be used as a template in a workflow.

To access this template:

1. Click the **Adobe Campaign** logo, in the top left corner.
1. Select **Resources** > **Templates** > **Delivery templates**.
1. Check the **Follow-up messages** box in the left pane.

   ![](assets/message-center_follow-up-search.png)

Only the follow-up messages are displayed.

>[!NOTE]
>
>To access the transactional messages, you must have administration rights or appear in the **Message Center agents** (mcExec) security group.

## Sending a follow-up message

Once you created the follow-up delivery template, you can use it in a workflow to send a follow-up message.

1. Access the marketing activity list and create a new workflow.

   See [Creating a workflow](../../automating/using/building-a-workflow.md#creating-a-workflow).

1. Drag and drop a **Scheduler** activity into your workflow and open it. Set the execution frequency to once a day.

   The Scheduler activity is presented in the [Scheduler](../../automating/using/scheduler.md) section.

1. Drag and drop a **Query** activity into your workflow and open it.

   The Query activity is presented in the [Query](../../automating/using/query.md) section.

1. To run the query on a resource other than the profile resource, go to the activity's **Properties** tab and click the **Resource** drop-down list.

   ![](assets/message-center_follow-up-query-properties.png)

   >[!NOTE]
   >
   >By default, the activity is pre-configured to search for profiles.

1. Select the event that you want to target so that you only access data from this event.

   ![](assets/message-center_follow-up-query-resource.png)

1. Go to the activity's **Target** tab and drag and drop the **Delivery logs (logs)** element from the **Email** section into the workspace.

   ![](assets/message-center_follow-up-delivery-logs.png)

   Select **Exists** to target all of the customers who received the email.

   ![](assets/message-center_follow-up-delivery-logs-exists.png)

1. Move the **Tracking logs (tracking)** element from the palette to the workspace and select **Does not exist** to target all of the customers who did not open the email.

   ![](assets/message-center_follow-up-delivery-and-tracking-logs.png)

1. Drag and drop the event that you are targeting (**Cart abandonment** in this example) from the **Email** section into the workspace. Then define a rule to target all messages sent three days ago.

   ![](assets/message-center_follow-up-created.png)

   This means that all recipients who received the transactional message three days before the execution of the workflow and still have not opened it are targeted.

   Click **Confirm** to save the query.

1. Drag and drop an **Email delivery** activity into your workflow.

   The Email delivery activity is presented in the [Email delivery](../../automating/using/email-delivery.md) section.

   ![](assets/message-center_follow-up-workflow.png)

   You can also use an [SMS delivery](../../automating/using/sms-delivery.md) or a [Mobile app delivery](../../automating/using/mobile-app-delivery.md) activity. In this case, make sure you select the **Mobile (SMS)** or **Mobile application** channel when creating your event configuration. See [Creating an event](../../administration/using/configuring-transactional-messaging.md#creating-an-event).

1. Open the **Email delivery** activity. In the creation wizard, check the **Follow-up messages** box and select the follow-up delivery template that was created after publishing the event.

   ![](assets/message-center_follow-up-template.png)

1. In the follow-up message content, you can leverage the content of your event by adding personalization fields.

   ![](assets/message-center_follow-up-content.png)

1. Find the fields that you defined when creating your event by selecting **Transactional event** > **Event context**. See [Personalizing a transactional message](../../channels/using/event-transactional-messages.md#personalizing-a-transactional-message).

   ![](assets/message-center_follow-up-personalization.png)

   This means that you can leverage the same content, including enriched data, that was used the first time the event was sent, to create a personalized friendly reminder.

1. Save the activity and start the workflow.

Once the workflow is started, every customer that received your cart abandonment notification three days ago but did not open it will receive a follow-up message based on the same data.

>[!NOTE]
>
>If you selected the **Profile** targeting dimension when creating the event configuration, the follow-up message will also leverage the Adobe Campaign marketing database. See [Profile transactional messages](../../channels/using/profile-transactional-messages.md).

