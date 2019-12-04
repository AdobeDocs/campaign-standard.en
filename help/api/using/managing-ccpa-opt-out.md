---
title: Managing CCPA opt-out
description: Learn how to manage CCPA opt-out with APIs
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

# Managing CCPA opt-out {#managing-ccpa-optout}

A profile's CCPA opt-out status can be monitored and managed using the **ccpaOptOut** profile attribute and the "true" or "false" values:

`"ccpaOptOut": <value>`

* **true**:  forbids the sale of personal information.
* **false**: authorizes the sale of personal information.

>[!CAUTION]
>
>The “CCPA Opt-Out” attribute is only available starting 19.4. For 19.3 environments, you need to extend the Profiles resource and add a boolean field. This field will be added to the API with the chosen label. We suggest you use “Opt-Out for CCPA”.
>
>For more on this, refer to the [Privacy management documentation](https://helpx.adobe.com/campaign/kb/acs-privacy.html#ccpa).

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
