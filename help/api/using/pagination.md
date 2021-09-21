---
title: Pagination
description: Learn how to perform pagination operations.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis

feature: API
role: Data Engineer
level: Experienced
exl-id: d6ebce3c-1e84-4b3b-a68d-90df4680af64
---
# Pagination

By default, 25 resources are loaded in a list.

The **_lineCount** parameter allows you to limit the number of resources listed in the response.  You can then use the **next** node to display the next results.

>[!NOTE]
>
>Always use the URL value returned in the **next** node to perform a pagination request.
>
>The **_lineStart** request is calculated and must always be used within the URL returned in the **next** node.

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

Response to the request, with the **next** node to perform pagination.

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
    "next": {
        "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/email?_lineCount=10&_
        lineStart=@Qy2MRJCS67PFf8soTf4BzF7BXsq1Gbkp_e5lLj1TbE7HJKqc"
    }
    ...
}

```

By default, the **next** node is not available when interacting with tables with large amount of data. To be able to perform pagination, you must add the **_forcePagination=true** parameter to your call URL.

```

-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile?_forcePagination=true \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'

```

>[!NOTE]
>
>The number of records above which a table is considered as large is defined in Campaign Standard **XtkBigTableThreshold** option. The default value is 100,000 records.
