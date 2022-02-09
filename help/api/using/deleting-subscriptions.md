---
title: Deleting subscriptions
description: Learn how to delete subscriptions with APIs
feature: API
role: Data Engineer
level: Experienced
exl-id: 76e2d102-c877-41a6-af87-2f407201a572
---
# Deleting subscriptions with APIs {#mdeleting-subscriptions-api}

<!--NOTE TO WRITER: There are two duplicate headings that seem to have the same content. Delete one? Rename if different?-->

## Deleting a service subscription for a specific profile {#deleting-service-subscription}

This is a three-steps procedure.

1. Retrieve the subscriptions URL for the desired profile.
1. Perform a GET request on the subscriptions URL.
1. Perform a DELETE request on the desired service URL.

If the delete request is successful, the response status is 204 No Content.

<br/>

***Sample request***

The sample payloads below show how to unsubscribe a profile from a service. First perform a GET request to retrieve the profile.

```

-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/<PKEY> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'

```

It returns the subscriptions URL for the profile.

```

  {
    ...
    "postalAddress":...,
    "preferredLanguage": "none",
    "subscriptions": {
      "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/<PKEY>/subscriptions/"
    },
  }

```

Perform a GET request on the subscriptions URL.

```

-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/<PKEY>/subscriptions \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'

```

It returns the list of subscriptions for the selected profile, with a URL for each subscribed service.

```

...
"service": {
  "PKey": "<PKEY>",
  "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/<PKEY>",
  "label": "Sport Newsletter",
  "name": "SVC1",
  "title": "Sport Newsletter (SVC1)"
},
...

```

Perform a DELETE request on the desired service URL.

```

-X DELETE https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/<PKEY> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'

```

<!-- + réponse -->

## Deleting a service subscription for a specific profile

This is a three-steps procedure.

1. Retrieve the desired service and its subscription URL.
1. Perform a GET request on the subscriptions URL to retrieve all profiles subscriptions.
1. Perform a DELETE request on the desired profile subscription URL.

If the delete request is successful, the response status is 204 No Content.

<br/>

***Sample request***

Retrieve the service record.

```

-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/<PKEY> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'

```

It returns the subscriptions URL for the service.

```

{
  ...
  "messageType": "email",
  "mode": "newsletter",
  "name": "SVC3",
  "subScenarioEventType": "subscriptionEvent",
  "subscriptions": {
    "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/<PKEY>/subscriptions/"
  },
  "targetResource": "profile",
  ...
},

```

Perform a GET request on the subscriptions URL.

```

-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/<PKEY>/subscriptions \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'

```

It returns the list of subscriptions for the selected service, with a URL (href) for each profile subscription.

```

{
  "PKey": "<PKEY>",
  "created": "2019-03-26 08:58:04.764Z",
  "email": "",
  "expirationDate": "",
  "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/<PKEY>/subscriptions/<PKEY>",
  "metadata": "subscriptionRcp",
  "service": ...,
  "serviceName": "SVC3",
  "subscriber": ...,
  ...
}

```

Perform a DELETE request on the desired profile subscription URL.

```

-X DELETE https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/<PKEY>/subscriptions/<PKEY> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'

```

<!-- + réponse -->
