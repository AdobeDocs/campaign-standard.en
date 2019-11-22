---
title: Managing geographical units
description: Learn how to manage geographical units with APIs.
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

# Managing geographical units {#managing-geographical-units}

The **geoUnitBase** endpoint lets you interact with Geographical units, enabling you, for example, to update their attributes or update a profile's Geographcal unit.

>[!CAUTION]
>
>The Geographical unit feature has been deprecated with the Campaign Standard 18.7 release.
As a result, new Campaign Standard instances, as well as existing instances with no geographical units created, cannot have this capability implemented starting the 18.7 release.
For more on this, refer to the <a href="https://helpx.adobe.com/campaign/kb/acs-deprecated-and-removed-features.html">Deprecated features</a> page.

The **Geographcal unit** field is added to a profile when extending the profile resource. As a result, remember to always use the **profileAndServicesExt** endpoint to interact with Geographical units. For more on the profile's resource extension, refer to the [Campaign documentation](https://helpx.adobe.com/campaign/standard/administration/using/organizational-units.html#partitioning-profiles).

## Retrieving a profile's Geographical unit

1. Perform a GET request on the profile PKey to retrieve the **geoUnit** URL.
1. Perform a GET request on the URL to retrieve more details about the Geographical unit.

***Sample request***

Retrieve the profile record.

```

-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/profile/<PKEY> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'

```

It returns the geoUnit URL for the profile.

```

{
  ...
  "geoUnit": {
    "PKey": "@zYV4vIjP1wpBebml6s71hjGiDhs4_gHgbC_UhuJFk8h7XTZxZ5QnZrPnQPEfB__TxwR2ge6sz61D8RR4zvD75CLDZtc<PKEY>",
    "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/orgUnitBase/<PKEY>",
    "title": "All (all)"
    },
  ...
}

```

Perform a GET request on the URL to retrieve more information.

```

-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/geoUnitBase/<PKEY> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'

```

It returns the details below.

```

{
  "PKey": "<PKEY>",
  "created": "2019-04-02 22:36:13.252Z",
  "desc": "Default geographical entity (accessible to everyone)",
  "label": "All",
  "lastModified": "2019-04-03 08:17:19.100Z",
  "name": "all",
  "parentTitle": "",
  "title": "All (all)"
}

```

## Updating a profile's Geographical unit

1. Perform a GET request on the **geoUnitBase** resource to retrieve the Geographical unit PKey.
1. Perform a PATCH request on the profile PKey, with the desired Geographical unit PKey in the payload.

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

## Updating a Geographical unit attributes

1. Perform a GET request on the **geoUnitBase** resource to retrieve the Geographical unit PKey.
1. Perform a PATCH request on the Geographical unit, with the attributes to update in the payload.

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
