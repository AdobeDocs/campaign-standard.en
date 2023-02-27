---
title: Configuring tag rules to support Adobe Campaign Standard use cases
description: Learn how to configure tag rules to support Adobe Campaign Standard use cases
audience: channels
content-type: reference
topic-tags: push-notifications
context-tags: mobileApp,overview
feature: Instance Settings
role: Admin
level: Experienced
exl-id: b5f4f612-ea23-4007-b427-069777ecdd58
---
# Configuring tag rules to support Adobe Campaign Standard use cases {#configuring-rules-launch}

In the Data Collection UI, create data elements and rules to send PII and other data from mobile applications to [!DNL Adobe Campaign Standard].

To ensure that all configuration changes in the Data Collection UI take effect, you must publish these changes. For more information, see [Publishing](https://developer.adobe.com/client-sdks/documentation/getting-started/create-a-mobile-property/#publish-the-configuration).

To create rules in the Data Collection UI, follow these steps:

1. [Creating data elements](../../administration/using/configuring-rules-launch.md#create-data-elements)
2. [Creating rules](../../administration/using/configuring-rules-launch.md#create-data-elements) for use cases you want to support:
    * [PII postback](../../administration/using/configuring-rules-launch.md#pii-postback)
    * [In-App tracking postback](../../administration/using/configuring-rules-launch.md#inapp-tracking-postback)
    * [Push notifications tracking postback](../../administration/using/configuring-rules-launch.md#push-tracking-postback)
    * [Location postback](../../administration/using/configuring-rules-launch.md#location-postback)

## Creating data elements {#create-data-elements}

Here are the data elements we recommend that you create in the Data Collection UI.
You can create additional data elements as per your needs.

* **[!UICONTROL Experience Cloud ID]**
* **[!UICONTROL Pkey]**
* **[!UICONTROL Campaign server]**

To create these data elements:

1. In the Data Collection UI, from your mobile application dashboard, click the **[!UICONTROL Data Elements]** tab.

1. To create the **[!UICONTROL Experience Cloud ID]** data element, click **[!UICONTROL Create New Data Element]**.

1. In the **[!UICONTROL Name]** field, for example, type in **mcid**.

1. From the **[!UICONTROL Extension]** drop-down, select **[!UICONTROL Mobile Core]**. Then **[!UICONTROL Experience Cloud ID]** in the **[!UICONTROL Data element]** type drop-down.

    ![](assets/do-not-localize/rules_1.png)

1. To create the Pkey data element, click **[!UICONTROL Add data element]**.

1. In the **[!UICONTROL Name]** field, for example, type in **pkey**.

1. From the **[!UICONTROL Extension]** drop-down, select **[!UICONTROL Adobe Campaign Standard]**. Then **[!UICONTROL pkey]** in the **[!UICONTROL Data element]** type drop-down.

1. To create the Campaign server data element, click **[!UICONTROL Add data element]**.

1. In the **[!UICONTROL Name]** field, type a name, for example, **camp-server**.

1. From the **[!UICONTROL Extension]** drop-down, select **[!UICONTROL Adobe Campaign Standard]**. Then, **[!UICONTROL Campaign Server]** in the **[!UICONTROL Data element]** type drop-down.

## Creating rules {#creating-rules}

You must create rules for the following:

* [PII postback](../../administration/using/configuring-rules-launch.md#pii-postback)
* [In-App tracking postback](../../administration/using/configuring-rules-launch.md#inapp-tracking-postback)
* [Push notifications tracking postback](../../administration/using/configuring-rules-launch.md#push-tracking-postback)
* [Location postback](../../administration/using/configuring-rules-launch.md#location-postback)

### PII postback {#pii-postback}

>[!NOTE]
>
>To send PII information from a mobile app to Adobe Campaign, you must implement an SDK API. For more information, go to [CollectPII](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#collectpii).

To send PII data to [!DNL Adobe Campaign Standard], create a rule in the Data Collection UI:

1. In the Data Collection UI, from your mobile application dashboard, click the **[!UICONTROL Rules]** tab then **[!UICONTROL Create New Rule]**.

1. Type a name, for example, **Mobile Core - Collect PII**.

1. In the **[!UICONTROL Events]** section, click **[!UICONTROL Add]**.

1. From the **[!UICONTROL Extension]** drop-down, select **[!UICONTROL Mobile Core]**. Then, **[!UICONTROL Collect PII]** in the **[!UICONTROL Event type]** drop-down.

1. Click **[!UICONTROL Keep changes]**.

1. In the **[!UICONTROL Actions]** section, click **[!UICONTROL Add]**.

1. From the **[!UICONTROL Extension]** drop-down, select **[!UICONTROL Mobile Core]**. Then, **[!UICONTROL Send PII]** in the **[!UICONTROL Action type]** drop-down.

1. In **[!UICONTROL URL]**, enter the following URL:

    ```
    https://{%%camp-server%%}/rest/head/mobileAppV5/{%%pkey%%}/subscriptions/{%%mcid%%}
    ```

1. Select the **[!UICONTROL Add Post Body]** check box.

1. In **[!UICONTROL Post Body]**, type the following:

    ```
    {
    "marketingCloudId":
    "{%%mcid%%}",
    "pushPlatform":
    "{%contextdata.pushPlatform%}",
    "cusEmail":
    "{%contextdata.email%}",
    "cusFirstName":
    "{%contextdata.firstName%}",
    "cusLastName":
    "{%contextdata.lastName%}" }
    ```

    The marketingCloudId enables you to reconcile your app subscribers with the recipients in the database and, as a result, is required. You can specify other key-value pairs as per your business needs. In the example above, Email, First Name, and Last Name are being passed from the app.

    The keys (for example cusEmail, cusFirstName, and cusLastName) should match the field IDs that are defined in your custom resource in the Adobe Campaign Standard instance. The value variables (for example email, firstName, and LastName) should match the keys in the JSON data that is sent from the mobile app while calling the AMS collectPII API from the app code.

    You can also pass Lifecycle data in the Collect PII postback or a different postback depending on your Event triggers. here is an example of the Lifecycle data JSON:

    ```
    {
    "marketingCloudId":"{%%mcid%%}",
    "pushPlatform":"{%contextdata.pushPlatform%}",
    "cusDayslastlaunch": "{%%DaysSinceLastUse%%}", 
    "cusDaysfirstlaunch": "{%%DaysSinceFirstUse%%}", 
    "cusLaunches": "{%%Launches%%}"
    }
    ```

    The data elements that are defined in the Data Collection UI should be enclosed in double percentages, for example `%%mcid%%`, and context variables from app should be enclosed in single percentages, for example %contextdata.email%.

1. In **[!UICONTROL Content Type]**, type **application/json**.

1. In **[!UICONTROL Timeout]**, select 0.

    ![](assets/do-not-localize/rules_2.png)

Your user data is now configured to be sent to Campaign.

### In-App tracking postback {#inapp-tracking-postback}

>[!NOTE]
>
>If you are using Android ACPCore v1.4.0 or later/ iOS ACPCore v2.3.0 or later, configuring tracking postbacks is not required.

To send tracking data to [!DNL Adobe Campaign Standard] for reporting on how your users interact with In-App messages in your mobile application, create the following rule in the Data Collection UI:

1. In the Data Collection UI, from your mobile application dashboard, select the **[!UICONTROL Rules]** tab and click **[!UICONTROL Add Rule]**.

1. Type a name, for example, **Adobe Campaign - In-App click tracking**.

1. In the **[!UICONTROL Events]** section, click **[!UICONTROL Add]**.

1. From the **[!UICONTROL Extension]** drop-down, select **[!UICONTROL Adobe Campaign Standard]**. Then, **[!UICONTROL In-App click tracking]** in the **[!UICONTROL Event type]** drop-down.

1. Click **[!UICONTROL Keep changes]**.

1. In the **[!UICONTROL Actions]** section, click **[!UICONTROL Add]**.

1. From the **[!UICONTROL Extension]** drop-down, select **[!UICONTROL Mobile Core]**. Then, **[!UICONTROL Send postback]** in the **[!UICONTROL Event type]** drop-down.

1. In **[!UICONTROL URL]**, type the following URL:

    ```
    https://{%%camp-server%%}/r/?id={%id%}&mcid={%%mcid%%}
    ```

1. Select the **[!UICONTROL Add post body]** check box.

1. In **[!UICONTROL Post Body]**, type **{}**.

1. In **[!UICONTROL Content Type]**, type **application/json**.

1. In **[!UICONTROL Timeout]**, select 0.

    ![](assets/do-not-localize/rules_3.png)

### Push notifications tracking postback {#push-tracking-postback}

>[!NOTE]
>
>If you are using Android ACPCore v1.4.0 or later/ iOS ACPCore v2.3.0 or later, configuring tracking postbacks is not required.

To send tracking data to [!DNL Adobe Campaign Standard], which helps track your Push notification deliveries and your users’ interaction with your mobile application, you must create a rule in the Data Collection UI.

For more information about push tracking, see [Push Tracking](../../administration/using/push-tracking.md).

To track app actions, use the trackAction API. For more information, see [Track app actions](https://app.gitbook.com/@aep-sdks/s/docs/using-mobile-extensions/mobile-core/mobile-core-api-reference#track-app-actions).

1. In the Data Collection UI, from your mobile application dashboard, click the **[!UICONTROL Rules]** tab and click **[!UICONTROL Add Rule]**.

1. Type a name, for example, **Adobe Campaign - push click tracking**.

1. In the **[!UICONTROL Events]** section, click **[!UICONTROL Add]**.

1. From the **[!UICONTROL Extension]** drop-down, select **[!UICONTROL Mobile Core]**. Then, **[!UICONTROL Track Action]** in the **[!UICONTROL Event type]** drop-down.

1. From the **[!UICONTROL Action]** drop-down, select **[!UICONTROL Action]**, select **[!UICONTROL equals]**, and type **tracking**.

1. Click **[!UICONTROL Keep changes]**. Then, in the **[!UICONTROL Actions]** section, click **[!UICONTROL Add]**.

1. From the **[!UICONTROL Extension]** drop-down, select **[!UICONTROL Mobile Core]**. Then, **[!UICONTROL Send postback]** in the **[!UICONTROL Action type]** drop-down.

1. In **[!UICONTROL URL]**, enter the following URL:

    ```
    https://{%%camp-server%%}/r/?id={%contextdata.broadlogId%},{%contextdata.deliveryId%},{%contextdata.action%}&mcId={%%mcid%%}
    ```

1. Select the **[!UICONTROL Add post body]** check box.

1. Add your post body, for example, { }.

1. In **[!UICONTROL Content Type]**, type **application/json**.

1. In **[!UICONTROL Timeout]**, select 0.

### Location postback {#location-postback}

1. In the Data Collection UI, from your mobile application dashboard, click the **[!UICONTROL Rules]** tab and click **[!UICONTROL Add Rule]**.

1. Type a name, for example, **Location postback**.

1. In the **[!UICONTROL Events]** section, click **[!UICONTROL Add]**.

1. Create an event, for example, Enter POI or Exit POI. From the **[!UICONTROL Extension]** drop-down, select **Places - Beta**. Then, **Enter POI** or **Exit POI** in the **[!UICONTROL Event type]** drop-down.

1. Enter a name, for example, **Places - Beta - Enter POI** or **Exit POI**.

1. In the **[!UICONTROL Actions]** section, click **[!UICONTROL Add]**.

1. From the **[!UICONTROL Extension]** drop-down, select **[!UICONTROL Mobile Core]**. Then, **[!UICONTROL Send postback]** from the **[!UICONTROL Action type]** drop-down.

1. Enter a name, for example, **Mobile Core - Send Location Postback**.

1. In **[!UICONTROL URL]**, enter the following URL:

    ```
    https://{%%camp-server%%}/rest/head/mobileAppV5/{%%pkey%%}/locations/
    ```

1. Select the **[!UICONTROL Add post body]** check box and add your post body, for example:

    ```
    {
    "locationData": {
        "distances": "{%%Distance%%}",
        "poiLabel": "{%%POILabel%%}",
        "latitude": "{%%Latitude%%}",
        "longitude": "{%%Longitude%%}",
        "appId": "{%%AppId%%}",
        "marketingCloudId": "{%%ECID%%}"
    }
    }
    ```

    >[!NOTE]
    >
    >In the example above, the data elements on the right-hand side must be configured in the Data Collection UI by leveraging the steps in [Creating data elements](../../administration/using/configuring-rules-launch.md#create-data-elements). The data elements on the left-hand side are supported in [!DNL Adobe Campaign Standard] and do not need any configuration. If you require additional data, you must carry out custom resource extensions in [!DNL Adobe Campaign Standard].

1. In **[!UICONTROL Content Type]**, type **application/json**.

1. In **[!UICONTROL Timeout]**, select 5.

    ![](assets/do-not-localize/rules_4.png)
