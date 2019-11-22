---
title: GET / POST / PATCH / DELETE verbs
description: Learn more about the verbs used in Campaign Standard APIs.
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

# GET / POST / PATCH / DELETE verbs {#verbs}`

Available verbs to perform operations on the resources are:

* `GET`: retrieves one element or a collection of elements
* `POST`: creates a resource with parameters.
* `PATCH`: updates a resource with parameters.
* `DELETE`: deletes a resource.

<!-- ajouter codes retour -->

<!-- enlever les nodes iniutiles genre pagniation, count etc)-->

***Sample requests***

* Sample GET request on the profile collection.

    ```

    $curl  
    -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile \
    -H 'Content-Type: application/json' \
    -H 'Authorization: Bearer <ACCESS_TOKEN>' \
    -H 'Cache-Control: no-cache' \
    -H 'X-Api-Key: <API_KEY>'

    ```

    It returns an array of profiles.

    ```

    {
        "content": [
            {
                "PKey": "<PKEY>",
                "age": 34,
                ...
            },
            {
                "PKey": "<PKEY>",
                "age": 30,
                ...
            }
        ],
        "count": {
        "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile//_count?_lineStart=@iKTZ2q3IiSEDqZ5Nw1vdoGnQCqF-8DAUJRaVwR9obqqTxhMy"
        },
        "next": {
        "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/?_lineStart=@iKTZ2q3IiSEDqZ5Nw1vdoGnQCqF-8DAUJRaVwR9obqqTxhMy"
        },
        "serverSidePagination": true
    }

    ```

* Sample GET request on a specific profile.

    ```

    $curl  
    -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/<PKEY> \
    -H 'Content-Type: application/json' \
    -H 'Authorization: Bearer <ACCESS_TOKEN>' \
    -H 'Cache-Control: no-cache' \
    -H 'X-Api-Key: <API_KEY>'

    ```

<!-- toujours ces 4 champs dans les exemples: pkey first name lastname email birthdate -->

    It returns the requested profile.

    ```

    {
        "PKey": "<PKEY>",
        "firstName": "John",
        "lastName": "Doe",
        "birthDate": "1985-08-17",
        "email": "johndoe@mail.com",
        ...
    }

    ```

* Sample POST request to create a profile.

    ```

    -X POST https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile \
    -H 'Content-Type: application/json' \
    -H 'Authorization: Bearer <ACCESS_TOKEN>' \
    -H 'Cache-Control: no-cache' \
    -H 'X-Api-Key: <API_KEY>' \
    -d '{"lastName":"Doe"}'

    ```

    <!-- toujours les mêmes champs que dit plus haut-->

    <!-- dans les exemples, mettre email au lieu de age-->

    It returns the profile. <!-- returns  le profil avec tous les champs par défaut . >

    ```

    {
        ...
        "gender": "unknown",
        "lastModified": "2019-09-25 08:25:12.234Z",
        "lastName": "Doe",
        ...
    }

    ```

* Sample PATCH request to update a profile.

    ```

    -X PATCH https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/<PKEY> \
    -H 'Content-Type: application/json' \
    -H 'Authorization: Bearer <ACCESS_TOKEN>' \
    -H 'Cache-Control: no-cache' \
    -H 'X-Api-Key: <API_KEY>' \
    -d '{"lastName":"Smith"}'

    ```

    <!-- mettre un 2ème champ à updater type prénom-->

    It returns the PKEY and URL to retrieve the updated profile.

    ```

    {
        "PKey": "<PKEY>",
        "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/<PKEY>"
    }

    ```

* Sample DELETE request to delete a profile.

    ```

    -X DELETE https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/<PKEY> \
    -H 'Content-Type: application/json' \
    -H 'Authorization: Bearer <ACCESS_TOKEN>' \
    -H 'Cache-Control: no-cache' \
    -H 'X-Api-Key: <API_KEY>'

    ```

    The request returns a 200 response, confirming that the profile has been deleted.
