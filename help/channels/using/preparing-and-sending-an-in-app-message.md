---
title: Preparing and sending an In-App message
description: Create In-App message to target your application subscribers with specific content.
audience: channels
content-type: reference
topic-tags: in-app-messaging
context-tags: delivery,triggers,back;deliveryCreation,wizard
feature: In App
role: User
exl-id: ef83d991-302b-491e-9cdb-07f5da7a5971
---
# Preparing and sending an In-App message{#preparing-and-sending-an-in-app-message}

Three types of In-App message are available in Adobe Campaign:

* **[!UICONTROL Target users based on their Campaign profile (inAppProfile)]**: This message type enables you to target Adobe Campaign profiles (CRM profiles) who have subscribed to your mobile application. This message type can be personalized with all available profile attributes in Adobe Campaign but requires a secure handshake between Mobile SDK and Campaign's In-App messaging service to ensure that messages with personal and sensitive information are used by authorized users only.

  To download this message type on users' devices, Mobile SDK has to send linkage fields used to connect a mobile profile to a CRM profile in Adobe Campaign. For more information on SDK APIs required to support In-App, refer to this [page](https://developer.adobe.com/client-sdks/documentation/adobe-campaign-standard/api-reference/).

* **[!UICONTROL Target all users of a Mobile app (inAppBroadcast)]**: This message type enables you to send messages to all users (current or future) of your mobile application even if they don't have an existing profile in Adobe Campaign. Personalization is thus not possible when customizing the messages as the user profile may not even exist in Adobe Campaign.
* **[!UICONTROL Target users based on their Mobile profile (inApp)]**: This message type enables you to target all known or anonymous users of a mobile app that have a mobile profile in Adobe Campaign. This messages type can be personalized using only non-personal and non-sensitive attributes and does not require secure handshake between Mobile SDK and Adobe Campaign's In-App messaging service.

  For more information on how to handle personal and sensitive data, refer to [Handling mobile profile fields with personal and sensitive data](../../channels/using/about-in-app-messaging.md#handling-mobile-profile-fields-with-personal-and-sensitive-data).

![](assets/diagram_inapp.png)

## Preparing your In-App message {#preparing-your-in-app-message}

>[!CAUTION]
>
>In-App personalization relies on a linkage field which is typically a CRM ID and/or Mobile App Login ID. You are solely responsible for securing this linkage field when used in connection with Adobe Campaign. If you fail to keep your linkage field(s) secure, your personalized message may be vulnerable. Adobe will not be liable for damages arising out of unauthorized access or use of any profile data if you fail to follow secure linkage field composition, management, and protection practices.

The steps for creating a standalone In-App message with Adobe Campaign are:

1. From Adobe Campaign home page, click the **[!UICONTROL In-App messaging]** card.

   You can also create an In-App from the **Marketing activities** tab, by clicking the **[!UICONTROL Create]** button.

   Note that an In-App message can also be created from a campaign or from the Adobe Campaign home page or in a workflow.

1. Select **In-App message**.

   ![](assets/inapp_creating.png)

1. Select an appropriate template based on your audience targeting needs.

   ![](assets/inapp_creating_2.png)

   By default, you can select one of the following three out-of-the-box templates:

    * **[!UICONTROL Target users based on their Campaign CRM profile (inAppProfile)]** 
    * **[!UICONTROL Target all users of a Mobile app (inAppBroadcast)]** 
    * **[!UICONTROL Target users based on their Mobile profile (inApp)]**

1. Enter the In-App message properties and select your mobile app in the **[!UICONTROL Associate a Mobile App to a delivery]** field. 

   If you don't see any applications in the drop-down list, make sure that your mobile applications are in a **Configured** state. Applications in a **Ready to be configured** state will not appear in the list. For more information on mobile application configuration, refer to this [page](../../administration/using/configuring-a-mobile-application.md#channel-specific-config).

   ![](assets/inapp_creating_3.png)

1. Select the audience you want to target for you In-App message. Your audience is prefiltered depending on the mobile application associated to this delivery.

   Note that this step is not needed with the **[!UICONTROL Broadcast an In-App message (inAppBroadcast)]** since it targets all users of a mobile application.

   ![](assets/inapp_creating_8.png)

1. In the **[!UICONTROL Triggers]** tab, drag and drop the event that will trigger your message. By choosing a trigger, you choose an action done by users which will cause the In-App message to be displayed.

   Four categories of events are available:

    * **[!UICONTROL Mobile Application events]**: Custom events implemented in your mobile application.

      For more on events creations, refer to this [page](../../administration/using/configuring-a-mobile-application.md).
    
    * **[!UICONTROL Life Cycle events]**: Out-of-the-box life cycle events supported by Adobe Mobile SDK.

      For more on life cycle events, refer to this [page](https://experienceleague.adobe.com/docs/mobile-services/android/metrics.html).
    
    * **[!UICONTROL Analytics Events]**: The following three categories are supported depending on what is instrumented in your mobile app: Adobe Analytics, Context data or View state.

      Please note that these events are only available if you have an Adobe Analytics license.
    
    * **[!UICONTROL Places]**: The following three categories leverage real-time location data to deliver contextually relevant mobile experiences: Places context data, Places custom metadata or Places event type.

      For more information on Adobe Places, refer to the [Places documentation](https://experienceleague.adobe.com/docs/places/using/home.html).

   ![](assets/inapp_creating_4.png)

1. If you use an **[!UICONTROL Analytics Events]**, Adobe Analytics and View state events will be automatically populated based on the report suites configured in the Analytics extension in the Data Collection UI whereas Context data events have to be manually added.

   Please note that these events are only available if you have an Adobe Analytics license.

   ![](assets/inapp_creating_7.png)

1. If you use a **[!UICONTROL Places]** trigger, Places context data, Places custom metadata or Places event type will be automatically populated based on all the Libraries and their Points of Interest created in Adobe Places.

   Please note that this trigger will be applied on the device only for the Points of Interest from the Libraries selected in the Places extension in the Data Collection UI. For more information on the Places extension and how to install it, refer to this [documentation](https://experienceleague.adobe.com/docs/places/using/places-ext-aep-sdks/places-extension/places-extension.html).

1. In the **[!UICONTROL Frequency & duration]** tab, choose the frequency for your trigger, the start and end date, day of the week and time of the day when your In-App message will be active.

   ![](assets/inapp_creating_5.png)

1. Edit the content of your message and define the advanced options. See [Customizing an In-App message](../../channels/using/customizing-an-in-app-message.md).

   ![](assets/inapp_creating_6.png)

1. Click **[!UICONTROL Create]**.

Your In-App message is now ready to be sent to your targeted audience.

**Related topics:**

* [Customizing an In-App message](../../channels/using/customizing-an-in-app-message.md)
* [In-App report](../../reporting/using/in-app-report.md)
* [Sending an In-App message within a workflow](../../automating/using/in-app-delivery.md)

## Previewing the In-App message {#previewing-the-in-app-message}

Before sending your In-App message, you can test with your test profiles to check what your targeted audience will see when they receive your delivery.

1. Click the **[!UICONTROL Preview]** button.

   ![](assets/inapp_sending_2.png)

1. Click the **[!UICONTROL Select a test profile]** button and select one of your test profiles to start previewing your delivery. For more information on test profiles, refer to this [section](../../audiences/using/managing-test-profiles.md).
1. Check your message on different devices such as Android, iPhone phones or even tablets. You can also check if your personalization fields are retrieving the right data.

   ![](assets/inapp_sending_3.png)

1. You can now send your message and measure its impact with delivery reports.

## Sending your In-App message {#sending-your-in-app-message}

Once you have finished preparing your delivery and the approval steps have been carried out, you can send your message.

1. Click **[!UICONTROL Prepare]** to compute the target and generate the messages.

   ![](assets/inapp_sending_4.png)

1. Once the preparation has finished successfully, the **Deployment** window presents the following KPIs: **Target** and **To deliver**.

   You can check the Deployment window by clicking the ![](assets/lp_link_properties.png) button for potential exclusions or errors in your delivery.

   ![](assets/inapp_sending_5.png)

1. Click **[!UICONTROL Confirm]** to start sending your In-App message.

   ![](assets/inapp_sending_6.png)

1. Check the status of your delivery through the message dashboard and logs. For more on this, refer to this [section](../../sending/using/monitoring-a-delivery.md).

   **[!UICONTROL Delivered]** and **[!UICONTROL Sent]** KPIs counts are based on what is successfully sent out from Campaign to Message delivery service. Please note that these KPIs are not an indication of the count of mobile devices that received or downloaded the message successfully from Message delivery service.

   ![](assets/inapp_sending_7.png)

1. Measure the impact of your In-App messages with delivery reports. For more on reporting, refer to [this section](../../reporting/using/in-app-report.md).

1. After sending your In-App messages, you can choose to deactivate your delivery. This can be useful if you want to stop a particular delivery or if you want to run a new delivery with the same trigger for example.

   Click **[!UICONTROL Deactivate]** then **[!UICONTROL Ok]** to start the deactivation request.

   ![](assets/inapp_sending_8.png)

1. Once the request has been sent, your delivery will be deactivated and no other message will be sent.

   Note that your reports for this delivery will still be accessible.

   ![](assets/inapp_sending_9.png)

**Related topics:**

* [In-App report](../../reporting/using/in-app-report.md)
* [Sending an In-App message within a workflow](../../automating/using/in-app-delivery.md)
