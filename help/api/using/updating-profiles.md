---
title: Updating profiles
description: Learn more how to update profiles with APIs
feature: API
role: Data Engineer
level: Experienced
exl-id: fa3796ee-a00c-4d70-bf3d-e8d2099f1116
---
# Updating profiles with APIs{#updating-profiles-api}

Updating profiles is performed with a **PATCH** request.

 `https://mc.adobe.io/<ORGANIZATION>/campaign/<apiName>/<resourceName>/<PKEY>`

1. The first step is to **retrieve the profile**.

1. In a second request, perform a **PATCH request** on the profile with the completed information in the payload.

1. To check if the PATCH request has updated the profile, we can perform a final GET request.

<br/>

***Sample request***

Sample GET request to retrieve a profile.

```

-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/<PKEY>\
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
            "firstName": "Amy",
            "lastName":"Dakota",
            "birthDate": "1980-10-24",
            ...
        }
    ]
}

```

PATCH request to update the "phone" attribute.

```

-X PATCH https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/<PKEY> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>' \
-d '{"phone":"3301020304"}'

```

It returns the PKEY and URL to retrieve the updated profile.

```

{
    "PKey": "<PKEY>",
    "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/@2v1dr3ZKJveMDhAdh0MPnh9hNQQ93qb7AW6BNVVKknjwXvTZRBAgUqz1SNcB4ZndgjqOofx3BwBZYBftlmObISoM3rs"
}

```
