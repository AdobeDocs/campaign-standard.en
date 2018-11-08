---
title: Creating an In-App message
seo-title: Creating an In-App message
description: Creating an In-App message
seo-description: Create In-app message to target your application subscribers with specific content.
uuid: b4ea3d35-e241-4823-8292-5f55ad9e408e
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/channels/using/creating-an-in-app-message
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-08T08 23 11.887-0400
cq-lastreplicated: 2018-09-07T15 12 00.312-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: in-app-messaging
cq-template: /apps/help/templates/article-3
discoiquuid: 8d5f331e-175a-4d2b-82ae-1ed20d3f2646
firstPublishExternalDate: 2018-09-07T15:12:00.267-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-11-06T09 43 16.728-0500
jcr-createdby: admin
jcr-description: Creating an In-App message
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T15:12:00.267-0400
lochandoffdate: 2018-09-08T08 23 11.887-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Creating an In-App message
publishexternaldate: 2018-09-07T15 12 00.267-0400
publishExternalURL: "https://helpx.adobe.com/campaign/standard/channels/using/creating-an-in-app-message.html"
sha1: a0993f607ff42864929b748f50bb20ef8c679c6e
topicBrowsingSortDate: 2018-09-07T15:12:00.267-0400
index: y
internal: n
snippet: y
---

# Creating an In-App message{#creating-an-in-app-message}

Creating an In-App message

The steps for creating an In-App message with Adobe Campaign are:

1. From the **Marketing activities** window, create a new marketing activity.

   Note that an In-App message can also be created from a campaign or from the Adobe Campaign home page or in a workflow.

1. Select **In-App message**.

   ![](assets/inapp_creating.png)

1. Select a template.

   ![](assets/inapp_creating_2.png)

   By default, you can select one of the following three out-of-the-box templates:

    * **Send In-App message to Campaign profiles (inAppProfile)**
    * **Broadcast an In-App message (inAppBroadcast)**
    * **Send In-App message to app subscribers (inApp)**

   For more information on templates, refer to [About In-App messaging](../../channels/using/about-in-app-messaging.md).

1. Enter the In-App message properties and select your mobile app in the **Associate a Mobile App to a delivery** field.

   ![](assets/inapp_creating_3.png)

1. Select the audience you want to target for you In-App message. Your audience is prefiltered depending on the mobile application associated to this delivery.

   Note that this step is not needed with the **Broadcast an In-App message (inAppBroadcast)** since it targets all users of a mobile application.

1. In the **Triggers** tab, drag and drop the event that will trigger your message. Three categories of events are available: 

   ![](assets/inapp_creating_4.png)

1. In the **Frequency & duration** tab, choose the frequency for your trigger, the start and end date, day of the week and time of the day your In-App message will be active.

   ![](assets/inapp_creating_5.png)

1. Edit the content of your message and define the advanced options. See [Customizing an In-App message](https://helpx.adobe.com/campaign/standard/channels/using/customizing-a-push-notification.html).

   ![](assets/inapp_creating_6.png)

1. Click **Create**.

Your In-App message is now ready to be sent to your targeted audience.
