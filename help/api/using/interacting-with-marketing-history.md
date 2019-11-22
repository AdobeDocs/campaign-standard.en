---
title: Interacting with marketing history
description: Learn how to interact with profiles' marketing history.
page-status-flag: never-activated
uuid: c7b9c171-0409-4707-9d45-3fa72aee8008
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
discoiquuid: 304e7779-42d2-430a-9704-8c599a4eb1da

internal: n
snippet: y
---

# Interacting with marketing history {#interacting-with-marketing-history}

The **history** endpoint lets you interact with a profile's marketing history.
This way, you can, for example, easily retrieve the mirror page for a delivery that was sent to a profile. To do this, follow the steps below:

1. Perform a GET  with the **history** endpoint and the profile's primary key.
1. Perform a GET request on the **events** href returned.
1. It returns the list of events for the profile with links to mirror pages in the **mirrorPage** node.

***Sample request***

Retrieve the profile's marketing history with a GET request.

```

-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/History/"<PKEY>" \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'

```

The "events" node returns the URL that gives you access to the events on the profile.

```

{
    "PKey": "<PKEY>",
    "age": 45,
    "birthDate": "1972-08-11",
    "blackList": false,
    "blackListEmail": false,
    "blackListFax": false,
    "blackListMobile": false,
    "blackListPhone": false,
    "blackListPostalMail": false,
    "blackListPushnotification": false,
    "countBroadLogEvents": 1,
    "countSubHistoEvents": 0,
    "countryIsoA2": "FR",
    "created": "2018-05-16 23:08:13.006Z",
    "email": "",
    "events": {
        "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/history/<PKEY>/events/",
        "metadata": "subHisto"
    },
    "fax": "",
    "firstName": "",
    "gender": "female",
    "isExternal": false,
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
      "metadata": "broadLog",
      "mirrorPage": {
        "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/history/<PKEY>/events/<PKEY>/mirrorPage/"
      },
      "type": "outbound"
    }

```
