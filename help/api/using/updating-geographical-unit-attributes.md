---
title: Updating a Geographical unit attributes
description: Learn how to update a Geographical unit attributes with APIs
audience: developing
content-type: reference
topic-tags: campaign-standard-apis

feature: API
role: Data Engineer
level: Experienced
exl-id: 86810821-6f62-46ab-ba0b-2175797fe9dd
---
# Updating a Geographical unit attributes {#managing-geographical-units}

1. Perform a GET request on the **geoUnitBase** resource to retrieve the Geographical unit PKey.
1. Perform a PATCH request on the Geographical unit, with the attributes to update in the payload.

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

It returns all Geographical units. Retrieve the PKey of the desired unit.

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

Perform a PATCH request on the Geographical unit, with the attributes to update in the payload.

```

-X PATCH https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/orgUnitBase/<PKEY> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
-i
-d {
-d "label":"Asia",
-d "name":"asia"
-d }

```

<!-- + réponse -->
