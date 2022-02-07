---
title: Managing CCPA opt-out
description: Learn how to manage CCPA opt-out with APIs
audience: developing
content-type: reference
topic-tags: campaign-standard-apis

feature: API
role: Data Engineer
level: Experienced
exl-id: bfc52511-f66f-4948-a939-d0d77e8ef03c
---
# Managing CCPA opt-out {#managing-ccpa-optout}

A profile's CCPA opt-out status can be monitored and managed using the **ccpaOptOut** profile attribute and the "true" or "false" values:

`"ccpaOptOut": <value>`

* **true**:  forbids the sale of personal information.
* **false**: authorizes the sale of personal information.

<!--The “CCPA Opt-Out” attribute is only available starting 19.4. For 19.3 environments, you need to extend the Profiles resource and add a boolean field. This field will be added to the API with the chosen label. We suggest you use “Opt-Out for CCPA”.
>
>For more on this, refer to the [Managing Privacy requests documentation](../../start/using/privacy-requests.md#sale-of-personal-information-ccpa).-->

<br/>

***Sample requests***

* Sample GET request to retrieve a profile's CCPA opt-out status.

    ```

    -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profilesAndServices/profile/<PKEY> \
    -H 'Authorization: Bearer <ACCESS_TOKEN>' \
    -H 'Cache-Control: no-cache' \
    -H 'X-Api-Key: <API_KEY>' \
    -H 'Content-Type: application/json;charset=utf-8'

    ```

    Response to the GET request.

    ```

    {
    "PKey": "<PKEY>",
      "ccpaOptOut": false,
      "firstName": "John",
      "lastName": "Doe",
    ...
    }

    ```

* Sample POST request to mark a profile for CCPA opt-out.

    ```

    -X POST https://mc.adobe.io/<ORGANIZATION>/campaign/profilesAndServices/profile/ \
    -H 'Authorization: Bearer <ACCESS_TOKEN>' \
    -H 'Cache-Control: no-cache' \
    -H 'X-Api-Key: <API_KEY>' \
    -H 'Content-Type: application/json;charset=utf-8'
    -i
    -d {
    -d  "firstName": "John",
    -d  "lastName": "Doe",
    -d  "email": "jdoe@mail.com",
    -d  "ccpaOptOut": true
    -d }'

    ```

    Response to the GET request.

    ```

    {
        ...
        "email": "john.doe@mail.com",
        "firstName": "John",
        "lastName": "Doe",
        "ccpaOptOut": true,
        ...
    }

    ```

* Sample PATCH request to update a profile for CCPA opt-out.

    ```

    -X PATCH https://mc.adobe.io/<ORGANIZATION>/campaign/profilesAndServices/profile/<PKEY> \
    -H 'Authorization: Bearer <ACCESS_TOKEN>' \
    -H 'Cache-Control: no-cache' \
    -H 'X-Api-Key: <API_KEY>' \
    -H 'Content-Type: application/json;charset=utf-8'
    -i
    -d {
    -d  "ccpaOptOut": true
    -d }'

    ```

    Response to the GET request.

    ```

    {
        ...
        "email": "john.doe@mail.com",
        "firstName": "John",
        "lastName": "Doe",
        "ccpaOptOut": true,
        ...
    }

    ```
