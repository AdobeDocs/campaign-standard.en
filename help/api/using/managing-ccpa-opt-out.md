---
title: Managing CCPA opt-out
description: Learn how to manage CCPA opt-out with APIs
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
feature: API
old-role: Data Architect
role: Developer
level: Experienced
exl-id: bfc52511-f66f-4948-a939-d0d77e8ef03c
TQID: https://experienceleague.adobe.com/XcgCy73XQYn-JyB0N41X3n30nGGo1tHVzmn-UQ1TOJQ
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
feature_v2:
  - id: b12f6872-9271-4369-85e5-86969a0b99a2
    internal-label: APIs
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
---
# Managing CCPA opt-out {#managing-ccpa-optout}

A profile's CCPA opt-out status can be monitored and managed using the **ccpaOptOut** profile attribute and the "true" or "false" values:

`"ccpaOptOut": <value>`

* **true**:  forbids the sale of personal information.
* **false**: authorizes the sale of personal information.

<!--
The “CCPA Opt-Out” attribute is only available starting 19.4. For 19.3 environments, you need to extend the Profiles resource and add a boolean field. This field will be added to the API with the chosen label. We suggest you use “Opt-Out for CCPA”.
>
>For more on this, refer to the [Managing Privacy requests documentation](../../start/using/privacy-requests.md#sale-of-personal-information-ccpa).
-->

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
