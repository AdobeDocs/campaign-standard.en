---
title: Updating a profile's Geographical unit
description: Learn how to manage geographical units with APIs.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis

feature: API
role: Data Engineer
level: Experienced
exl-id: 9dc07d86-00b2-4885-b6ac-0a6f9bc45236
---
# Updating a profile's Geographical unit {#updating-a-geographical-unit}

1. Perform a GET request on the **geoUnitBase** resource to retrieve the Geographical unit PKey.
1. Perform a PATCH request on the profile PKey, with the desired Geographical unit PKey in the payload.

<br/>

***Sample request***

Retrieve the list of Geographical units.

```

-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/geoUnitBase/ \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'

```

It returns all Geographical units. Retrieve the PKey of the unit to which you want to assign the profile.

```

{
 "PKey": "<PKEY>",
 "created": "2019-04-06 22:36:19.089Z",
 "desc": "",
 "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/geoUnitBase/<PKEY>",
 "label": "Europe",
 "lastModified": "2019-04-06 22:36:19.086Z",
 "name": "eu",
 "parentTitle": "All (all)",
 "title": "Europe (eu)"
},

```

Perform a PATCH request on the profile, with the PKey of the desired Geographical unit in the payload.

```

-X PATCH https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/profile/<PKEY> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
-i
-d {
-d "geoUnit":{
-d    "PKey":"<PKEY>"
-d  }
-d }

```

<!-- + réponse -->
