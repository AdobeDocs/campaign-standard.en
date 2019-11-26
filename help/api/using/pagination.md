---
title: Pagination
description: Learn how to perform pagination operations.
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

# Pagination

By default, 25 resources are loaded in a list.

The **_lineCount** parameter allows you to limit the number of resources listed in the response.  You can then use the **next** node to display the next results.

>[!NOTE]>
>
>Always use the URL value returned in the **next** node to perform a pagination request.
>
>The **_lineStart** request is calculated and must always be used within the URL returned in the **next** node.

<!-- serverside pagination. quand table très longue (au delà de 100.000), on peut plus faire de next. doit utiliser à la place les trucs type lineStart etc. si false: voudra dirre que ça a atteint la limite-->

<br/>

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
            "firstName": "John",
            "lastName":"Doe",
            "birthDate": "1980-10-24",
            ...
        }
    ],
    ...
}

```
