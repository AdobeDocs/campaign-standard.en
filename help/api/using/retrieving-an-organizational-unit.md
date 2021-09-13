---
title: Retrieving a profile's Organizational unit
description: Learn how to a profile's Organizational unit with APIs.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis

feature: API
role: Data Engineer
level: Experienced
exl-id: 37048884-bd03-46ea-8e2e-a73ad568153b
---
# Retrieving a profile's Organizational unit {#retrieving-organizational-units}

1. Perform a GET request on the profile PKey to retrieve the **orgUnit** URL.
1. Perform a GET request on the URL to retrieve more details about the Organizational unit.

<br/>

***Sample request***

Retrieve the profile record.

```

-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/profile/<PKEY> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'

```

It returns the orgUnit URL for the profile.

```

{
  ...
  "orgUnit": {
    "PKey": "<PKEY>",
    "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/orgUnitBase/<PKEY>",
    "title": "All (all)"
    },
  ...
}

```

Perform a GET request on the URL to retrieve more information.

```

-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/orgUnitBase/<PKEY> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'

```

It returns details about the organizational unit.

```

{
  "PKey": "<PKEY>",
  "created": "2019-04-02 22:36:13.252Z",
  "desc": "",
  "label": "Brand 4",
  "lastModified": "2019-04-03 08:17:19.100Z",
  "name": "brand4",
  "parentTitle": "All (all)",
  "title": "Brand 4 (brand4)"
}

```
