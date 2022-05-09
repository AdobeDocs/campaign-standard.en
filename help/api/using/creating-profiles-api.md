---
title: Creating profiles with APIs
description: Learn more how to create profiles with APIs.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
feature: API
role: Data Engineer
level: Experienced
exl-id: 69e8d034-6bdd-4b82-bcd7-1ef4be0a59b3
---
# Creating profiles with APIs {#creating-profiles-api}

Creating profiles is performed with a **POST** request on the profile resource.

>[!CAUTION]
>
>If you want to associate an <b>orgUnit</b> to the created profile, you need to extend the profile resource with this field and, after the publication of the extension, perform a POST request on the <b>ProfileAndServicesExt</b> endpoint.
>
>For more on the profile's resource extension, refer to the <a href="https://helpx.adobe.com/campaign/standard/administration/using/organizational-units.html#partitioning-profiles">Campaign documentation</a>.

<br/>

***Sample request***

Sample POST request to create a profile with the email "john.doe@mail.com".

```

-X POST https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>' \
-i
-d '{"email":"john.doe@mail.com"}'

```

It returns the newly created profile, with the "john.doe@mail.com" email address.

```

{
    "PKey": "<PKEY>",
    "firstName": "John",
    "lastName":"Doe",
    "birthDate": "1980-10-24",
    "email": "john.doe@mail.com",
    ...
}

```
