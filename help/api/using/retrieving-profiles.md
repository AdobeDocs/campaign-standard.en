---
title: Retrieving profiles
description: Learn more how to retrieve profiles with APIs.
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

# Retrieving profiles {#retrieving-profiles}

Retrieving profiles is performed with a **GET** request.

You can then refine your search by using filters, ordering and pagination. For more on this, refer to the [Additional operations](../../api/using/sorting.md) section.

<br/>

***Sample requests***

* Sample GET request to retrieve all profiles.

    ```

    -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile \
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
            },
            ...
    }

    ```

* Sample GET request to retrieve the first 10 email values.

    ```

    -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/email?_lineCount=10 \
    -H 'Content-Type: application/json' \
    -H 'Authorization: Bearer <ACCESS_TOKEN>' \
    -H 'Cache-Control: no-cache' \
    -H 'X-Api-Key: <API_KEY>'

    ```

    Response to the request. The "next" node returns the URL that gives you access to the 10 next email values.

    ```

    {
    "content": [
        "amy.dakota@mail.com",
        "kristen.smith@mail.com",
        "omalley@mail.com",
        "xander.harrys@mail.com",
        "jane.summer@mail.com",
        "gloria.boston@mail.com",
        "edward.snow@mail.com",
        "dorian.simons@mail.com",
        "peter.paolini@mail.com",
        "mingam+test08@adobe.com"
    ],
    "next": {
        "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/email?_lineCount=10&_
        lineStart=@Qy2MRJCS67PFf8soTf4BzF7BXsq1Gbkp_e5lLj1TbE7HJKqc"
    }
    }

    ```
