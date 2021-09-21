---
title: Updating a profile's Organizational unit
description: Learn how to update a profile's Organizational unit with APIs.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis

feature: API
role: Data Engineer
level: Experienced
exl-id: 6ce49aeb-a113-43ee-bfe3-f26a4a9e2a56
---
# Updating a profile's Organizational unit {#managing-organizational-units}

1. Perform a GET request on the **orgUnitBase** resource to retrieve the Organizational unit PKey
1. Perform a PATCH request on the profile PKey, with the desired Organizational unit PKey in the payload.

<br/>

***Sample request***

Retrieve the list of Organizational units.

```

-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/orgUnitBase/ \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'

```

It returns all Organizational units. Retrieve the PKey of the unit to which you want to assign the profile.

```

{
  "PKey": "<PKEY>",
  "created": "2019-04-02 22:36:13.252Z",
  "desc": "",
  "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/orgUnitBase/<PKEY>",
  "label": "Brand 4",
  "lastModified": "2019-04-03 07:34:56.579Z",
  "name": "brand4",
  "parentTitle": "All (all)",
  "title": "Brand 4 (brand1)"
},

```

Perform a PATCH request on the profile, with the PKey of the desired Organizational unit in the payload.

```

-X PATCH https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/profile/<PKEY> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
-i
-d {
-d "orgUnit":{
-d    "PKey":"<PKEY>"
-d  }
-d }

```

<!-- + réponse -->
