---
title: Metadata mechanism
description: Learn more about metadata mechanism.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis

feature: API
role: Data Engineer
level: Experienced
exl-id: 58ec0999-b28a-4198-8d57-729b074c6a6d
---
# Metadata mechanism {#metadata-mechanism}

You can retrieve the resources metadata using **resourceType** in a GET request:

`GET /profileAndServices/resourceType/<resourceName>`

The response returns the main metadata from the resource (all other fields are descriptive or internal):

* The **Content** node returns the resource's fields. For each field in the **content** node, we can find the following fields:

    * "apiName": name of the attribute used in the APIs.
    * "type": this is the high-level type definition (string, number, link, collection, enumeration...).
    * "dataPolicy": the value of the field must follow the given policy rules. For example, if dataPolicy rule is set to "email", the value must be a valid email. During a PATCH or a POST, the dataPolicy can check the value or modify the value to transform (smartCase for example).
    * "category": gives the category of the field in the query editor.
    * "resType": this the technical type.

        If "type" is completed with the value "link" or "collection", the resTarget value is the name of the resource targeted by the link.
        If "type" is completed with the value "enumeration", a "values" field is added and each enumeration value are detailed in the **values** node.

* The **Filters** node returns the URL to retrieve the associated filters. For more on filters, refer to [this section](../../api/using/filtering.md) section.

<!-- créer une section au même niveau sur les liens -->
<!-- dans l'exemple: birthdate, email +  mettre 2 liens : un de type 1-1 , 1-N
si on prend l'exemple de l'org unit, on aura un bon exemple lien -->
<!-- plus reparler du node Data -->

<br/>

***Sample request***

Perform a GET request on the resource.

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
