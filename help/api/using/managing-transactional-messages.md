---
title: Managing transactional messages
description: Learn how to manage transactional messages with APIs.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis

feature: API
role: Data Engineer
level: Experienced
exl-id: 00d39438-a232-49f1-ae5e-1e98c73397e3
---
# Managing transactional messages {#managing-transactional-messages}

Once you have created and published a transactional event, you need to integrate the triggering of this event into your website.

>[!NOTE]
>
>Event configuration is detailed in [this section](../../channels/using/configuring-transactional-event.md).

For example, you want a "Cart abandonment" event to be triggered whenever one of your clients leaves your website before purchasing the products in their cart. To do this, as a web developer, you must use the REST Transactional Messages API.

1. Send a request according to the POST method, which triggers the [sending of the transactional event](#sending-a-transactional-event).
1. The response to the POST request contains a Primary Key, which allows you to  send one or multiple requests through a GET request. You are then able to obtain the [event status](#transactional-event-status).

## Sending a transactional event {#sending-a-transactional-event}

The transactional event is sent through a POST request with the following URL structure:

```

POST https://mc.adobe.io/<ORGANIZATION>/campaign/<transactionalAPI>/<eventID>

```

* **&lt;ORGANIZATION&gt;**: your personal ORGANIZATION ID. Refer to [this section](../../api/using/must-read.md).

* **&lt;transactionalAPI&gt;**: the Transactional Messages API endPoints.

  The name of the Transactional Messages API endpoint depends on your instance configuration. It corresponds to the value "mc" followed by your personal organization ID. Let's take the example of the Geometrixx company, with "geometrixx" as its organization ID. In that case, the POST request would be as follows:

  `POST https://mc.adobe.io/geometrixx/campaign/mcgeometrixx/<eventID>`

  Note that the transactional messages API endpoint is also visible during the API preview.

* **&lt;eventID&gt;**: the type of event you want to send. This ID is generated when creating the event configuration (refer to [this section](../../channels/using/configuring-transactional-event.md#creating-an-event)).

### POST request header

The request must contain a "Content-Type: application/json" header.

You must add a charset, for example **utf-8**. Note that this value depends on the REST application you are using.

```

-X POST \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>' \
-H 'Content-Type: application/json;charset=utf-8' \
-H 'Content-Length:79' \

```

### POST request body

The event data are contained inside the JSON POST body. The event structure depends on its definition. The API preview button in the resource definition screen provides a request sample. Refer to [this section](../../channels/using/publishing-transactional-event.md#previewing-and-publishing-the-event).

The following optional parameters can be added to the event content to manage the sending of transactional messages linked to the event:

* **expiration** (optional): after this date, the sending of the transactional event will be cancelled.
* **scheduled** (optional): from this date, the transactional event will be processed and the transactional message will be sent.

>[!NOTE]
>
>The values of the "expiration" and "scheduled" parameters follow the ISO 8601 format. ISO 8601 specifies the use of the uppercase letter "T" to separate the date and time. It can however be removed from the input or output for better readability.

### Response to the POST request

The POST response returns the transactional event status at the time it was created. To retrieve its current status (event data, event status...), use the Primary Key returned by the POST response in a GET request:

`GET https://mc.adobe.io/<ORGANIZATION>/campaign/<transactionalAPI>/<eventID>/`

<br/>

***Sample request***

POST request to send the event.

```

-X POST https://mc.adobe.io/<ORGANIZATION>/campaign/mcAdobe/EVTcartAbandonment \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>' \
-H 'Content-Type: application/json;charset=utf-8' \
-H 'Content-Length:79'

{
  "email":"test@example.com",
  "scheduled":"2017-12-01 08:00:00.768Z",
  "expiration":"2017-12-31 08:00:00.768Z",
  "ctx":
  {
    "cartAmount": "$ 125",
    "lastProduct": "Leather motorbike jacket",
    "firstName": "Jack"
  }
}

```

Response to the POST request.

```

{
  "PKey":"<PKEY>",
  "ctx":
  {
    "cartAmount": "",
    "lastProduct": "",
    "firstName": ""
  }
  "email":"",
  "scheduled":"2017-12-01 08:00:00.768Z",
  "expiration":"2017-12-31 08:00:00.768Z",
  "href": "mcAdobe/EVTcartAbandonment/<PKEY>",
  "serverUrl":" https://myserver.com ",
  "status":"pending",
  "type":""
}

```

### Transactional event status {#transactional-event-status}

In the response, the "status" field allows you to know whether the event has been processed or not:

* **pending**: the event is pending - the event takes on this status when it has just been triggered.
* **processing**: the event is pending delivery - it is being transformed into a message and the message is being sent.
* **paused**: the event process is being paused. It is no longer processed, but kept in a queue in the Adobe Campaign database. For more on this, refer to [this section](../../channels/using/publishing-transactional-message.md#suspending-a-transactional-message-publication).
* **processed**: the event was processed and the message was sent successfully.
* **ignored**: the event was ignored by the delivery, typically when an address is in quarantine.
* **deliveryFailed**: a delivery error occurred while the event was being processed.
* **routingFailed**: the routing phase failed - this may occur for example when the type of event specified cannot be found.
* **tooOld**: the event expired before it was able to be processed - this can happen for various reasons, for example, when a send fails several times (this results in the event no longer being up to date) or when the server can no longer process events after becoming overloaded.
* **targetingFailed**: Campaign Standard failed to enrich a link that is being used for message targeting.
