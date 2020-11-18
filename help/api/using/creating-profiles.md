---
title: Creating profiles
description: Learn more how to create profiles with APIs.
page-status-flag: never-activated
uuid: c7b9c171-0409-4707-9d45-3fa72aee8008
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
discoiquuid: 304e7779-42d2-430a-9704-8c599a4eb1da

---

# Creating profiles {#creating-profiles}

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
