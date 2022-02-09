---
title: Interacting with marketing history
description: Learn how to interact with profiles' marketing history
feature: API
role: Data Engineer
level: Experienced
exl-id: 67282d21-b4ed-4af5-b751-848a6d705118
---
# Interacting with marketing history{#interacting-with-marketing-history}

The **history** endpoint lets you interact with a profile's marketing history.
This way, you can, for example, easily retrieve the mirror page for a delivery that was sent to a profile. To do this, follow the steps below:

1. Perform a GET  with the **history** endpoint and the profile's primary key.
1. Perform a GET request on the **events** href returned.
1. It returns the list of events for the profile with links to mirror pages in the **mirrorPage** node.

<br/>

***Sample request***

Retrieve the profile's marketing history with a GET request.

```

-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/history/"<PKEY>" \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'

```

The "events" node returns the URL that gives you access to the events on the profile.

```

{
  "PKey": "<PKEY>",
  "firstName": "John",
  "lastName":"Doe",
  "birthDate": "1980-10-24",
  "events": {
    "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/history/<PKEY>/events/",
    "metadata": "subHisto"
    },
}

```

Perform a GET request on the events href returned.

```

-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/history/<PKEY>/events \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'

```

It returns the list of events for the profile with links to mirror pages in the "mirrorPage" node.

```

    {
      "PKey": "<PKEY>",
      "category": "email",
      "date": "2018-05-17 08:44:49.366Z",
      "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/history/<PKEY>/events/<PKEY>",
      "label": "Send via email",
      "mirrorPage": {
        "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/history/<PKEY>/events/<PKEY>/mirrorPage/"
      },
      "type": "outbound"
    }

```
