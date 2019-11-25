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

# GET / POST / PATCH / DELETE verbs {#verbs}

Available verbs to perform operations on the resources are:

* `GET`: retrieves one element or a collection of elements
* `POST`: creates a resource with parameters.
* `PATCH`: updates a resource with parameters.
* `DELETE`: deletes a resource.

<!-- ajouter codes retour -->


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
                "firstName": "Olivia",
                "lastName": "Varney",
                "birthDate": "1977-09-°4",
                "email": "o.varney@mail.com",
            },
            {
                "PKey": "<PKEY>",
                "firstName": "John",
                "lastName": "Doe",
                "birthDate": "1985-08-17",
                "email": "johndoe@mail.com",
            }
        ],
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

    It returns the profile with the default fields.

    ```

    {
        "PKey": "<PKEY>",
        "firstName": "John",
        "lastName": "Doe",
        "birthDate": "1985-08-17",
        "email": "johndoe@mail.com",
    }

    ```

* Sample PATCH request to update a profile.

    ```

    -X PATCH https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/<PKEY> \
    -H 'Content-Type: application/json' \
    -H 'Authorization: Bearer <ACCESS_TOKEN>' \
    -H 'Cache-Control: no-cache' \
    -H 'X-Api-Key: <API_KEY>' \
    -d '{"firstName":"Mark"',"lastName":"Smith"}'

    ```

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
