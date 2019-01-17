---
title: Preparing and sending an In-App message
seo-title: Preparing and sending an In-App message
description: Preparing and sending an In-App message
seo-description: Create In-app message to target your application subscribers with specific content.
uuid: 3fc01531-338f-443b-b52c-95b3a7af232e
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: in-app-messaging
discoiquuid: 132cff9c-eee9-4b8e-ad19-3458f4d0d457
isreadyforlocalization: false
index: y
internal: n
snippet: y
---

# Preparing and sending an In-App message{#preparing-and-sending-an-in-app-message}

Preparing and sending an In-App message

## Preparing your In-App message {#preparing-your-in-app-message}

The steps for creating a standalone In-App message with Adobe Campaign are:

1. From Adobe Campaign home page, click the **[!UICONTROL In-App messaging]** card.

   You can also create an In-app from the **Marketing activities** tab, by clicking the **[!UICONTROL Create]** button.

   Note that an In-App message can also be created from a campaign or from the Adobe Campaign home page or in a workflow.

1. Select **In-App message**.

   ![](assets/inapp_creating.png)

1. Select an appropriate template based on your audience targeting needs.

   ![](assets/inapp_creating_2.png)

   By default, you can select one of the following three out-of-the-box templates:

    * **[!UICONTROL Target users based on their Campaign CRM profile (inAppProfile)]** 
    * **[!UICONTROL Target all users of a Mobile app (inAppBroadcast)]** 
    * **[!UICONTROL Target users based on their Mobile profile (inApp)]**

   For more information on templates, refer to [About In-App messaging](../../channels/using/about-in-app-messaging.md).

1. Enter the In-App message properties and select your mobile app in the **[!UICONTROL Associate a Mobile App to a delivery]** field.

   ![](assets/inapp_creating_3.png)

1. Select the audience you want to target for you In-App message. Your audience is prefiltered depending on the mobile application associated to this delivery.

   Note that this step is not needed with the **[!UICONTROL Broadcast an In-App message (inAppBroadcast)]** since it targets all users of a mobile application.

   ![](assets/inapp_creating_8.png)

1. In the **[!UICONTROL Triggers]** tab, drag and drop the event that will trigger your message. By choosing a trigger, you choose an action done by users which will cause the In-App message to be displayed.

   Please note that these events are only available if you have an Adobe Analytics license.

   Three categories of events are available:

    * **[!UICONTROL Mobile Application events]** : Custom events implemented in your mobile application.

      For more on events creations, refer to this [page](https://helpx.adobe.com/campaign/kb/configuring-app-sdk.html).
    
    * **[!UICONTROL Life Cycle events]** : Out-of-the-box life cycle events supported by Adobe Mobile SDK.

      For more on life cycle events, refer to this [page](https://marketing.adobe.com/resources/help/en_US/mobile/android/metrics.html).
    
    * **[!UICONTROL Analytics Events]** : The following three categories are supported depending on what is instrumented in your mobile app: Adobe Analytics, Context data or View state.

   ![](assets/inapp_creating_4.png)

1. If you use an **[!UICONTROL Analytics Events]** , Adobe Analytics and View state events will be automatically populated based on the report suites configured in the Analytics extension in Adobe Launch whereas Context data events have to be manually added.

   Please note that these events are only available if you have an Adobe Analytics licence.

   ![](assets/inapp_creating_7.png)

1. In the **[!UICONTROL Frequency & duration]** tab, choose the frequency for your trigger, the start and end date, day of the week and time of the day when your In-App message will be active.

   ![](assets/inapp_creating_5.png)

1. Edit the content of your message and define the advanced options. See [Customizing an In-App message](https://helpx.adobe.com/campaign/standard/channels/using/customizing-a-push-notification.html).

   ![](assets/inapp_creating_6.png)

1. Click **[!UICONTROL Create]** .

Your In-App message is now ready to be sent to your targeted audience.

## Sending your In-App message {#sending-your-in-app-message}

Once you have finished preparing your delivery and the approval steps have been carried out, you can send your message.

1. Click **[!UICONTROL Prepare]** to compute the target and generate the messages.

   ![](assets/inapp_sending_4.png)

1. Once the preparation has finished successfully, the **Deployment** window presents the following KPIs: **Target** and **To deliver**.

   You can check the Deployment window by clicking the  ![](assets/lp_link_properties.png)

   button for potential exclusions or errors in your delivery.

   ![](assets/inapp_sending_5.png)

1. Click **[!UICONTROL Confirm]** to start sending your In-App message.

   ![](assets/inapp_sending_6.png)

1. Check the status of your delivery through the message dashboard and logs. For more on this, refer to this [section](../../sending/using/monitoring-a-delivery.md).

   **[!UICONTROL Delivered]** and **[!UICONTROL Sent]** KPIs counts are based on what is successfully sent out from Campaign to Message delivery service. Please note that these KPIs are not an indication of the count of mobile devices that received or downloaded the message successfully from Message delivery service.

   ![](assets/inapp_sending_7.png)

