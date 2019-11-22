---
title: Additional operations
description: Learn more about additional operations that you can perform with the GET verb.
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

# Additional operations {#global-concepts}

When using the GET verb, you can perform additional operations in order to refine your requests.

## Counting

The Adobe Campaign REST API can count the number of records. Counting is often used with **filters**. For more on filters, refer to [this section](#filtering).

>[!CAUTION]
>
> Always use the URL value returned in the count node to perform a count request.

***Sample request***

To count all the services that have a **messageType** value equaling to "sms", perform a GET request with the **byChannel** filter.

```

-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/byChannel?channel=sms \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'

```

It returns the services corresponding to the filter in the **content** node, and the URL to retrieve the number of results in the **count** node.

```

{
    "content": [
        {
            ...
            "messageType": "sms",
            "mode": "newsletter",
            "name": "SVC6",
            ...
        },
        {
            ...
            "messageType": "sms",
            "mode": "newsletter",
            "name": "SVC7",
            ...
        },
        ...
    ],
    "count": {
        "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/byChannel/_count?channel=sms&_lineStart=@iKTZ2q3IiSEDqZ5Nw1vdoGnQCqF-8DAUJRaVwR9obqqTxhMy"
    },
    "serverSidePagination": true
}

```

Perform a GET request on the **count** URL.

```

-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/byChannel/_count?channel=sms&_lineStart=@iKTZ2q3IiSEDqZ5Nw1vdoGnQCqF-8DAUJRaVwR9obqqTxhMy \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'

```

It returns the number of results in the "count" attribute.

```

{
    "count": 26
}

```

## Pagination

<!-- serverside pagination. quand table très longue (au delà de 100.000), on peut plus faire de next. doit utiliser à la place les trucs type lineStart etc. si false: voudra dirre que ça a atteint la limite-->

By default, 25 resources are loaded in a list. The **_lineCount** parameter allows you to limit the number of listed records.

Always use the URL value returned in the **next** node to perform a pagination request. The **_lineStart** request is calculated and must always be used within the URL returned in the **next** node.

***Sample request***

Sample GET request to display 1 record of the profile resource.

```

-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile?_lineCount=1 \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'

```

<!-- dans l'exemple, avoir le node "next"-->

Response to the request.

```

{
    "content": [
        {
            "PKey": "<PKEY>",
            "age": 85,
            "birthDate": "1933-10-24",
            ...
        }
    ],
    "count": {
        "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile//_count?_lineCount=1&_lineStart=@vnxw2tye3sTSnooV6nR7SMh_y1e-MMtR6FOEOVXjiItJq5XA"
    },
    "next": {
        "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/?_lineCount=1&_lineStart=@vnxw2tye3sTSnooV6nR7SMh_y1e-MMtR6FOEOVXjiItJq5XA"
    },
    "serverSidePagination": true
}

```

## Sorting

Sorting is available in **ascending** or **descending** order. The '%20desc' or '%20asc' parameter needs to be added to the URL.

Sorting is also available on every field. A specific flag is available in the resource metadata to know whether or not the field can be ordered. For more on this, refer to [this section](#metadata-mechanism).

***Sample requests***

* Sample GET request to retrieve emails in the database alphabetically ordered.

    ```

    -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/email/email?_order=email \
    -H 'Content-Type: application/json' \
    -H 'Authorization: Bearer <ACCESS_TOKEN>' \
    -H 'Cache-Control: no-cache' \
    -H 'X-Api-Key: <API_KEY>'

    ```

    Response to the request.

    ```

    {
    "content": [
        "adam@email.com",
        "allison.durance@example.com",
        "amy.dakota@mail.com",
        "andrea.johnson@mail.com",
        "audrey.davis@mail.com",
        "barbara.cooper@mail.com",
        "bette.grant@mail.com"
        ...
    ]
    "next": {
        "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/email?_order=email&_lineStart=@sL3AJfHiOJZzn9Ytm0OSduPdEz_kYoaflOEfSS1N2-ttAfLl"
    }
    }

    ```

* Sample GET request to retrieve the email in the database in a descending alpha order.

    ```

    -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/email?_order=email%20desc \
    -H 'Content-Type: application/json' \
    -H 'Authorization: Bearer <ACCESS_TOKEN>' \
    -H 'Cache-Control: no-cache' \
    -H 'X-Api-Key: <API_KEY>'

    ```

    Response to the request.

    ```

    {
    "content": [
        "tombinder@example.com",
        "tombinder@example.com",
        "timross@example.com",
        "john.smith@example.com",
        "jody.lucassen@example.com",
        "jade.connor@email.com",
        "dannymars@example.com",
        ...
    ]
    }

    ```

## Filtering

### Retrieving filters metadata
  
Filters are available for **each resource**.
  
To **identify the filters** associated to the resource, you need to perform a GET request on the resource metadata. For more on metadata, refer to [this section](#metadata-mechanism). This request returns the URL where all of the filters are defined for a given resource.
  
To identify the filter **metadata** and determine how to use it, you have to perform a GET request on the previously returned URL.

***Sample request***

The sample payloads below show how to retrieve the "byText" filter metadata for the "profile" resource. First perform a GET request on the "profile" resource metada.

```

-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/resourceType/profile \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'

```

It returns the URL where the filters are described.

```

{
"filters": {
        "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/resourceType/<PKEY>/filters/"
    }
  }

```

Perform a GET request on the URL. It returns the list of filters for the profile resource, with the metadata associated to each filter.

```

{
"birthday": {
        "PKey": "@FL-CbDFXbnHbXcVpeCGWL46VXJLn1LqxLMPagt2vz8sCxQ52lvB15KiUaxXkxJYQw-tZXYrgUWG6K8QcB4gxVY9RKoba5bRFY3294YFshDmorRr8",
        "category": "0150_profile",
        "condition": ...,
        "data": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/birthday?type=$value&precision=$value&operator=$value&day=$value&month=$value&includeStart=$value&endDay=$value&endMonth=$value&includeEnd=$value&relativeValue=$value&nextUnitsValue=$value&previousUnitsValue=$value",
        "formType": "webPage",
        "fragmentName": "",
        "label": "Birthday",
        "metadata": ...,
        "resName": "birthday",
        "webPage": "...",
        "webPageName": ""},
        "byEmail": ...,

}

```

### Filters metadata structure

The same metadata structure is available for each filter:
  
* The **@formType** and **@webPage** fields are technical fields.
* The **data** field gives a sample on how to use the filter.
* The **metadata** node describes the filter parameters.
* The **condition** node describes what the filter is intended to do. The filter parameters described in the metadata node are used to create filter conditions. For each filter condition, if **enabledIf** is true, the **expr** will be applied.

Filter metadata structure sample.

```

"byText": {
        "PKey": "...",
        "category": "99_none",
        "condition": ...,
        "data": "/profileAndServices/profile/byText?text=$value",
        "formType": "none",
        "fragmentName": "",
        "label": "By name or email",
        "metadata": ...,
        "resName": "byText",
        "webPage": "",
        "webPageName": ""
    }

```

### Using filters

Filtering can be done with the following request:
  
`GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/<resourceName>/by<filterName>?<filterParam>=<filterValue>`
  
It is possible to combine **multiple filters** in a single request:
  
`GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/<resourceName>/<filter1name>/<filter2name>?<filter1param>=<filter1value>&<filter2param>=<filter2value>`

***Sample requests***

* Sample GET request to retrieve the "service" resources with the type "email".

    ```

    -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/byChannel?channel=email \
    -H 'Content-Type: application/json' \
    -H 'Authorization: Bearer <ACCESS_TOKEN>' \
    -H 'Cache-Control: no-cache' \
    -H 'X-Api-Key: <API_KEY>'

    ```

    Response to the request.

    ```

    {
        "content": [
            {
                "PKey": "<PKEY>",
                "builtIn": false,
                "created": "2019-09-25 23:20:35.000Z",
                "desc": "test description",
                "end": "",
                "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/@I_FIiDush4OQPc0mbOVR9USoh36Tt5CsD35lATvQjdWlXrYc0lFkvle2XIwZUbD8GqTVvSp8AfWFUvjkGMe1fPe5nok",
                "isExternal": false,
                "isTemplate": false,
                "label": "QA Marketing Newsletter bjuiwdsod",
                "lastModified": "2019-09-25 23:20:35.000Z",
                "limitedDuration": false,
                "mainDate": "2019-09-25",
                "messageType": "email",
                "mode": "newsletter",
                ...
            },
            {
                "PKey": "<PKEY>",
                "builtIn": false,
                "created": "2019-09-25 23:33:17.488Z",
                "desc": "test description",
                "end": "",
                "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/@wuKK4-SmPSzNZGhQnqSZRYC8affVMqKeqjsr_mmtmW6qG8R5BQqfbrXNaxyBxGVm_Qu6OLHKPLvMHyhyWNLPovWohvU",
                "isExternal": false,
                "isTemplate": false,
                "label": "QA Marketing Newsletter dvsxmzwpg",
                "lastModified": "2019-09-25 23:33:17.488Z",
                "limitedDuration": false,
                "mainDate": "2019-09-25",
                "messageType": "email",
                "mode": "newsletter",
                ...
            },
            ...
        ],
        "count": {
            "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service//byChannel/_count?channel=email&_lineStart=@sL3AJfHiOJZzn9Ytm0OSduPdEz_kYoaflOEfSS1N2-ttAfLl",
            "value": 12
        },
        "serverSidePagination": true
    }

    ```

* Sample GET request to retrieve the "profile" resources containing "Doe" in
the email or last name fields (the byText filter searchs into both the email and last name fields).

    ```

    -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/byText?text=Doe \
    -H 'Content-Type: application/json' \
    -H 'Authorization: Bearer <ACCESS_TOKEN>' \
    -H 'Cache-Control: no-cache' \
    -H 'X-Api-Key: <API_KEY>'

    ```

    Response to the request.

    ```

    {
        "content": [
            {
                ...
                "email": "john.doe@mail.com",
                "emailFormat": "unknown",
                "externalId": "",
                "fax": "",
                "firstName": "John",
                "gender": "unknown",
                "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/<PKEY>",
                "isExternal": false,
                "lastModified": "2019-09-26 09:30:52.940Z",
                "lastName": "Doe",
                ...
            }
            ...
        ],
        "count": ...,
        "serverSidePagination": true
    }

    ```

* Sample GET request to retrieve the services resources with the type "email" and the label "sport".

    ```

    -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/byChannel/byText?channel=email&text=sport \
    -H 'Content-Type: application/json' \
    -H 'Authorization: Bearer <ACCESS_TOKEN>' \
    -H 'Cache-Control: no-cache' \
    -H 'X-Api-Key: <API_KEY>'

    ```

    Response to the request.

    ```

    {
        "content": [
            {
                "PKey": "<PKEY>",
                "builtIn": false,
                "created": "2019-09-26 09:36:01.014Z",
                "desc": "",
                "end": "",
                "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/<PKEY>",
                "isExternal": false,
                "isTemplate": false,
                "label": "sport",
                "lastModified": "2019-09-26 09:36:01.014Z",
                "limitedDuration": false,
                "mainDate": "2019-09-26",
                "messageType": "email",
                "mode": "newsletter",
                "name": "SVC13",
                ...
            }
        ],
        "count": ...,
        "serverSidePagination": true
    }

    ```

### Custom filters
  
If you want to use a custom filter, you have to create and customize it in the Adobe Campaign Standard interface.
  
The custom filter will then have the same behavior as out of the box filters:

`GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/<resourceName>/by<customFilterName>?<customFilterparam>=<customFilterValue>`
  
For more on this, refer to the Campaign Standard documentation:
  
* [Configuring filter definition](https://helpx.adobe.com/campaign/standard/developing/using/configuring-filter-definition.html).
* [Use case: Calling a resource using a composite identification key](https://docs.adobe.com/content/help/en/campaign-standard/using/developing/adding-or-extending-a-resource/uc-calling-resource-id-key.html).

***Sample request***

Sample GET request to retrieve the "profile" resources with transaction amounts of 100$ or more.

Note that the "byAmount" filter has first been defined in the Adobe Campaign Standard interface and linked to the "Transaction" custom table.

```

-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/profile/byAmount?amount_parameter=100 \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'

```

<!--
Response to the request.

```

{
    "content": [
        {
            "PKey": "<PKEY>",
            "builtIn": false,
            "created": "2019-09-26 09:36:01.014Z",
            "desc": "",
            "end": "",
            "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/<PKEY>",
            ...
        }
    ],
    "count": ...,
    "serverSidePagination": true
}

```

-->

<!-- exemple à vérifier de bout en bout-->

<!--+category = query editor
privacy ?
displayFOrmat ?
pour faire un POST sur une enum, il faut lui passer le @name décrit dans le noeud values, chaque @name a une correspondance en format = au format définit par le resType
-->

<!--
 if link ou collection.* resName +
* resTarget tout ca, ca va ensemble : le système de lien, resTarget va donner la ressource targetée par le lien. type
resType = type technique (long..) resType = link alors unbound='false' ou 'true'
If type = enumeration alors champ "values" rajouté et les valeurs sont dans values
pour faire un POST sur une enum, il faut lui passer le @name décrit dans le noeud values, chaque @name a une correspondance en format = au format définit par le resType
ail faut que la valeur poster soit conforme ,elle doit valider la dataPolicy . La dataPolicy peut soit controler la valeur (email invalide), soit transformé (cas du smartCase par exemple)
type dans les metadata = type de haut-niveau (nombre, text)
-->
