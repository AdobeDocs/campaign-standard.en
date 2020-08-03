---
title: Configuring Adobe Experience Platform Launch rules to support Adobe Campaign Standard use cases
description: Configuring Adobe Experience Platform Launch rules to support Adobe Campaign Standard use cases
page-status-flag: never-activated
uuid: 961aaeb5-6948-4fd2-b8d7-de4510c10566
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: push-notifications
discoiquuid: 23b4212e-e878-4922-be20-50fb7fa88ae8
context-tags: mobileApp,overview
internal: n
snippet: y
---

# Configuring Launch rules to support Adobe Campaign Standard use cases {#configuring-rules-launch}

In Adobe Experience Platform Launch, you need to create data elements and rules to send PII and other data from mobile applications to Adobe Campaign Standard.

To ensure that all configuration changes in Adobe Experience Platform Launch take effect, you must publish these changes. For more information, see [Publishing](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property#publish-the-configuration).

To create rules in Experience Platform Launch, follow these steps:

1. Create data elements
2. Create rules for use cases you want to support:
    * PII postback
    * In-App tracking postback
    * Push notifications tracking postback
    * Location postback

## Creating data elements {#create-data-elements}

Here are the data elements we recommend that you create in Experience Platform Launch.
You can create additional data elements as per your needs.

* Experience Cloud ID
* Pkey
* Campaign server

To create these data elements:

1. In Experience Platform Launch, from your mobile application dashboard, click the Data Elements tab.

1. To create the Experience Cloud ID data element, click Create New Data Element.

1. Complete the following steps:

    1. In the Name field, for example, type in mcid.
    1. From the Extension drop-down, select Mobile Core.
    1. From the Data element type drop-down, select Experience Cloud ID.
creating a data element
    1. Click Save.

1. To create the Pkey data element, click Add data element.

1. Complete the following steps:

    1. In the Name field, for example, type in pkey.
    1. From the Extension drop-down, select Adobe Campaign Standard.
    1. From the Data element type drop-down, select PKey.
    1. Click Save.

1. Click Save.

1. To create the Campaign server data element, click Add data element.

1. Complete the following steps:
    1. In the Name field, type a name, for example, camp-server.
    1. From the Extension drop-down, select Adobe Campaign Standard.
    1. From the Data element type drop-down, select Campaign Server.
    1. Click Save.

1. Click Save.

## Creating rules {#creating-rules}

You need to create rules for the following:

* [PII postback](../administration/using/configuring-rules-launch#pii-postback)
* [In-App tracking postback](../administration/using/configuring-rules-launch#inapp-tracking-postback)
* [Push notifications tracking postback](../administration/using/configuring-rules-launch#push-tracking-postback)
* [Location postback](../administration/using/configuring-rules-launch#location-postback)

### PII postback {#pii-postback}

Note:

To send PII information from a mobile app to Campaign, you need to implement an SDK API. For more information, go to CollectPII.

To send PII data to Campaign Standard, create a rule in Experience Platform Launch:

In Experience Platform Launch, from your mobile application dashboard, click the Rules tab.

Click Create New Rule.

Type a name, for example, Mobile Core - Collect PII.

In the Events section, click Add.

Complete the following steps:

From the Extension drop-down, select Mobile Core.
From the Event type drop-down, select Collect PII.
Click Keep changes.

In the Actions section, click Add.

Complete the following steps:

From the Extension drop-down, select Mobile Core.
From the Action type drop-down, select Send PII.
In URL, enter the following URL:

https://{%%camp-server%%}/rest/head/mobileAppV5/{%%pkey%%}/subscriptions/{%%mcid%%}

Select the Add Post Body check box.

In Post Body, type the following:

{
"marketingCloudId":
"{%%mcid%%}",
"cusEmail":
"{%contextdata.email%}",
"cusFirstName":
"{%contextdata.firstName%}",
"cusLastName":
"{%contextdata.lastName%}" }
Note:

The marketingCloudId enables you to reconcile your app subscribers with the recipients in the database and, as a result, is required. You can specify other key-value pairs as per your business needs. In the example above, Email, First Name, and Last Name are being passed from the app.

The keys (for example cusEmail, cusFirstName, and cusLastName) should match the field IDs that are defined in your custom resource in the Adobe Campaign Standard instance. The value variables (for example email, firstName, and LastName) should match the keys in the JSON data that is sent from the mobile app while calling the AMS collectPII API from the app code.
You can also pass Lifecycle data in the Collect PII postback or a different postback depending on your Event triggers. here is an example of the Lifecycle data JSON: 

{
"marketingCloudId":"{%%mcid%%}",

"cusDayslastlaunch": "{%%DaysSinceLastUse%%}", 

"cusDaysfirstlaunch": "{%%DaysSinceFirstUse%%}", 

"cusLaunches": "{%%Launches%%}"

}

The data elements that are defined in Experience Platform Launch should be enclosed in double percentages, for example %%mcid%%, and context variables from app should be enclosed in single percentages, for example %contextdata.email%.
In Content Type, type application/json. 

In Timeout, select 0.

Collect PII
Click Keep changes and then Save.

Your user data is now configured to be sent to Campaign.

### In-App tracking postback {#inapp-tracking-postback}

To send tracking data to Campaign Standard for reporting on how your users interact with In-App messages in your mobile application, create the following rule in Experience Platform Launch:

In Experience Platform Launch, from your mobile application dashboard, select the Rules tab.

Click Add Rule.

Type a name, for example, Adobe Campaign - In-App click tracking.

In the Events section, click Add.

Complete the following steps:

From the Extension drop-down, select Adobe Campaign Standard.
From the Event type drop-down, select In-App click tracking.
Click Keep changes.

In the Actions section, click Add.

Complete the following steps:

From the Extension drop-down, select Mobile Core.
From the Event type drop-down, select Send postback.
In URL, type the following URL:

https://{%%camp-server%%}/r/?id={%id%}&mcid={%%mcid%%}

Select the Add post body check box.

In Post Body, type {}.

In Content Type, type application/json. 

In Timeout, select 0.

creating a rule for an in-app postback
Click Keep changes and then Save.

### Push notifications tracking postback {#push-tracking-postback}

To send tracking data to Campaign Standard, which helps track your Push notification deliveries and your users’ interaction with your mobile application, you need to create a rule in Experience Platform Launch.

Note:

For more information about push tracking, see Push Tracking.

Note:

To track app actions, use the trackAction API. For more information, see Track app actions. 

In Experience Platform Launch, from your mobile application dashboard, click the Rules tab.

Click Add Rule.

Type a name, for example, Adobe Campaign - push click tracking.

In the Events section, click Add.

Complete the following steps:

From the Extension drop-down, select Mobile Core.
From the Event type drop-down, select Track Action.
From the Action drop-down, select Action, select equals, and type tracking.

Click Keep changes.

In the Actions section, click Add.

Complete the following steps:

From the Extension drop-down, select Mobile Core.
From the Action type drop-down, select Send postback.
In URL, enter the following URL:

https://{%%camp-server%%}/r/?id={%contextdata.broadlogId%},{%contextdata.deliveryId%},{%contextdata.action%}&mcId={%%mcid%%}

Select the Add post body check box. 

Add your post body, for example, { }.

In Content Type, type application/json. 

In Timeout, select 0.

Click Keep changes and then Save.

### Location postback {#location-postback}

In Experience Platform Launch, from your mobile application dashboard, click the Rules tab.

Click Add Rule.

Type a name, for example, Location postback.

In the Events section, click Add.

Create an event (for example, Enter POI or Exit POI):

From the Extension drop-down, select Places - Beta.
From the Event type drop-down, select Enter POI or Exit POI.
Enter a name, for example, Places - Beta - Enter POI or Exit POI.
In the Actions section, click Add.

Complete the following steps:

From the Extension drop-down, select Mobile Core.
From the Action type drop-down, select Send postback.
Enter a name, for example, Mobile Core - Send Location Postback.
In URL, enter the following URL:

https://{%%camp-server%%}/rest/head/mobileAppV5/{%%pkey%%}/locations/

Select the Add post body check box. 

Add your post body, for example:

1
2
3
4
5
6
7
8
9
10
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
Note:

In the example above, the data elements on the right-hand side need to be configured in Experience Platform Launch by leveraging the steps in Step 1 Create data elements. The data elements on the left-hand side are supported in Campaign Standard and do not need any configuration. If you require additional data, you need to carry out custom resource extensions in Campaign Standard.

In Content Type, type application/json. 

In Timeout, select 5.

Click Keep changes and then Save.

location postback