---
title: Performing subscriptions
description: Learn how to perform subscriptions with APIs
feature: API
role: Data Engineer
level: Experienced
exl-id: 64f321a3-436a-4b7c-99d8-0c006203012e
---
# Performing subscriptions with APIs{#performing-subscriptions}

## Method 1: Subscribing a profile to a service

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

Perform a POST request on the subscriptions URL with the desired service Primary Key inside the payload.

```

-X POST https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/<PKEY>/subscriptions \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>' \
-i
-d '{"service":{"PKey":"<PKEY>"}}'

```

It returns the updated profile with the service node completed.

```

{
  ...
  "service": {
    "PKey": "<PKEY>",
    "title": "Sport Newsletter (SVC1)"
  },
  "serviceName": "",
  "subscriber": ...,
  ...
}

```

## Method 2: Adding a profile to a service's subscribers

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

Make a POST request on the subscriptions URL with the desired profile Primary Key inside the payload.

```

-X POST https://mc.adobe.io/<ORGANIZATION>/campaign//profileAndServices/service/<PKEY>/subscriptions/ \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>' \
-i
-d '{"subscriber":{"PKey":"<PKEY>"}}'

```

It returns the updated service with the subscribers node completed.

```

{
  ...
  "service": ...,
  "serviceName": "",
  "subscriber": {
    "PKey": "<PKEY>",
    ...
  },
}

```
