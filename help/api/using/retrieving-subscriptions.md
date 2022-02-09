---
title: Retrieving subscriptions
description: Learn how to retrieve subscriptions with APIs
feature: API
role: Data Engineer
level: Experienced
exl-id: 6d935074-3196-45c5-97cd-ccb7c80bbba8
---
# Retrieving subscriptions with APIs {#retrieving-subscriptions-api}

## Retrieving the profiles that subscribed to a service

This is a two-steps procedure.

1. Retrieve the subscriptions URL for the desired service.
1. Perform a GET request on the subscriptions URL. It returns the list of subscriptions for the service, with each associated profile.

>[!CAUTION]
>
>The REST API returns the "href" property, which contains the URL to use. <b>Always use the URL contained in the response to make the subsequent API request</b>.

<br/>

***Sample request***

Perform a GET request to retrieve the service.

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
    "name": "SVC1",
    "subscriptions": {
                "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/<PKEY>/subscriptions/"
    },
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

The list of subscriptions for the service displays, with each associated profile.

```

  {
    ...
    "service": ...,
    "serviceName": "SVC3",
    "subscriber": {
        "PKey": "<PKEY>",
        "email": "",
        "firstName": "John",
        "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/<PKEY>",
        "lastName": "Doe",
    },
  }

```

## Retrieving the services to which a profile subscribed

This is a two-steps procedure.

1. Retrieve the subscriptions URL for a given profile.
1. Perform a GET request on the URL. It returns the list of subscriptions for the profile, with each associated service.

<br/>

***Sample request***

Perform a GET request to retrieve the profile.

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
    ...
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

It returns the list of services to which the profile subscribed.

```

  {
    ...
    "PKey": "<PKEY>",
    "created": "2017-03-03 10:54:00.363Z",
    "service": {
      "PKey": "<PKEY>",
      "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/<PKEY>",
      "label": "Sport Newsletter",
      "name": "SVC1",
      "title": "Sport Newsletter (SVC1)"
    },
    ...
  }

```
