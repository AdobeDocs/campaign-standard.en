---
title: Creating a service with APIs
description: Learn how to create a service with APIs
feature: API
role: Data Engineer
level: Experienced
exl-id: 91bbce9e-a618-4be2-840b-c7d021271f4e
---
# Creating a service with APIs{#creating-a-service-api}

Services creation is performed with a **POST** request on the service resource.

If you want to create the service with specific attributes, add them into the payload. Otherwise, the new service will be created with default ones.

<br/>

***Sample request***

Sample POST request to create a service with specific attributes.

```

-X POST https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/ \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
-i
-d {
-d "label": "My newsletter",
-d "messageType": "email",
-d "name": "email_newsletter",
-d "start": "2019-10-06"
-d }

```

It returns the newly created service with the updated attributes.

```

{
    "PKey": "<PKEY>",
    "builtIn": false,
    "created": "2019-09-26 12:00:37.005Z",
    "href": "https://mc.adobe.io/<ORGANIZATION>/profileAndServices/service/@NLscZuVHxdVu9rPftvrMWFfR1zRIxQGswSOmGLrK09JTF_iWhB0JCUHEndA_vvy__k9mzOYa5NVkcWDcrK8qGh0wygahX9kRcD44kiWWSEceShn3",
    "label": "My newsletter",
    ...
}

```
