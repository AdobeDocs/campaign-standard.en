---
title: Metadata mechanism
description: Learn more about metadata mechanism.
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

# Metadata mechanism {#metadata-mechanism}

You can retrieve the resources metadata using 'resourceType' in a GET request:

`GET /profileAndServices/resourceType/<resourceName>`

The response returns the main metadata from the resource:

* **Content**: returns the resource's fields. For each field in the **content** node, we can find the following fields:

    * **apiName**: name of the attribute used in the APIs.
    * **type**: this is the high-level type definition (string, number, link, collection, enumeration...).
    * **dataPolicy**: the value of the field must follow the given policy rules. For example, if dataPolicy rule is set to "email", the value must be a valid email. During a PATCH or a POST, the dataPolicy can check the value or modify the value to transform (smartCase for example).
    * **category**: gives the category of the field in the query editor.
    * **resType**: this the technical type.

        If **type** is completed with the value "link" or "collection", the resTarget value is the name of the resource targeted by the link.
        If **type** is completed with the value "enumeration", a **values** field is added and each enumeration value are detailed in the **values** node.

**Filters**: returns the URL to retrieve the associated filters. See [Filters](#filtering)

All other fields are descriptive or internal.

<!-- créer une section au même niveau sur les liens -->
<!-- dans l'exemple: birthdate, email +  mettre 2 liens : un de type 1-1 , 1-N
si on prend l'exemple de l'org unit, on aura un bon exemple lien -->

<!-- plus reparler du node Data -->

***Sample request***

```

-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/resourceType/profile \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'

```

It returns the complete description of the profile resource.

```

{
...
"content": {
  "email": {...},
    ...
    },
"data": "/profileAndServices/profile/",
"filters": {
        "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/resourceType/<PKEY>"
    },
"help": "Identified profiles",
"href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/metadata",
"label": "Profiles",
"mandatory": false,
"name": "profile",
"pkgStatus": "never",
"readOnly": false,
"schema": "nms:recipient",
"type": "item"
}

```
