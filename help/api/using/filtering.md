---
title: Filtering
description: Learn how to perform filtering operations.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis

feature: API
role: Data Engineer
level: Experienced
exl-id: cdb050b7-d327-42f7-b534-d32d988c8ffb
---
# Filtering {#filtering}

## Retrieving filters metadata
  
Filters are available for each resource. To identify the filters associated to a resource, you need to perform a GET request on the resource metadata. This request returns the URL where all of the filters are defined for a given resource. For more on metadata, refer to [this section](../../api/using/metadata-mechanism.md).
  
To identify the metadata of a filter and determine how to use it, you have to perform a GET request on the previously returned URL.

<br/>

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
}

```

## Filters metadata structure

The same metadata structure is available for each filter:
  
* The **@formType** and **@webPage** fields are technical fields.
* The **data** field gives a sample on how to use the filter.
* The **metadata** node describes the filter parameters.
* The **condition** node describes what the filter is intended to do. The filter parameters described in the metadata node are used to create filter conditions. For each filter condition, if **enabledIf** is true, the **expr** will be applied.

<br/>

Filter metadata structure sample:

```

"byText": {
        "PKey": "...",
        "category": "99_none",
        "condition": ...,
        "data": "/profileAndServices/profile/byText?text=$value",
        "formType": "none",
        "fragmentName": "",
        "label": "By name or email",
    }

```

## Using filters

Filtering is performed with the following request:
  
`GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/<resourceName>/by<filterName>?<filterParam>=<filterValue>`
  
It is possible to combine multiple filters in a single request:
  
`GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/<resourceName>/<filter1name>/<filter2name>?<filter1param>=<filter1value>&<filter2param>=<filter2value>`

<br/>

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
                "created": "2019-09-25 23:20:35.000Z",
                "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/@I_FIiDush4OQPc0mbOVR9USoh36Tt5CsD35lATvQjdWlXrYc0lFkvle2XIwZUbD8GqTVvSp8AfWFUvjkGMe1fPe5nok",
                "label": "Marketing Newsletter",
                "lastModified": "2019-09-25 23:20:35.000Z",
                "limitedDuration": false,
                "messageType": "email",
                "mode": "newsletter",
                ...
            },
            ...
        ],
        ...
    }

    ```

* Sample GET request to retrieve the "profile" resources containing "Doe" in
the email or last name fields (the byText filter searches into both the email and last name fields).

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
                "PKey": "<PKEY>",
                "firstName": "John",
                "lastName":"Doe",
                "birthDate": "1980-10-24",
                ...
            }
            ...
        ],
        ...
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
                "created": "2019-09-26 09:36:01.014Z",
                "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/<PKEY>",
                "label": "sport",
                "lastModified": "2019-09-26 09:36:01.014Z",
                "limitedDuration": false,
                "messageType": "email",
                "mode": "newsletter",
                "name": "SVC13",
                ...
            }
        ],
        ...
    }

    ```

## Custom filters
  
If you want to use a custom filter, you have to create and customize it in the Adobe Campaign Standard interface. The custom filter will then have the same behavior as out of the box filters:

`GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/<resourceName>/by<customFilterName>?<customFilterparam>=<customFilterValue>`
  
For more on this, refer to the Campaign Standard documentation:
  
* [Configuring filter definition](https://helpx.adobe.com/campaign/standard/developing/using/configuring-filter-definition.html).
* [Use case: Calling a resource using a composite identification key](https://experienceleague.adobe.com/docs/campaign-standard/using/developing/adding-or-extending-a-resource/uc-calling-resource-id-key.html).

<br/>

***Sample request***

Sample GET request to retrieve the "profile" resources with transaction amounts of 100$ or more. Note that the "byAmount" filter has first been defined in the Adobe Campaign Standard interface and linked to the "Transaction" custom table.

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
