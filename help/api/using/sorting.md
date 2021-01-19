---
solution: Campaign Standard
product: campaign
title: Sorting
description: Learn more how to perform sorting operations
audience: developing
content-type: reference
topic-tags: campaign-standard-apis

---

# Sorting

Sorting is available in ascending or descending order. To do this, use the **%20desc** or **%20asc** parameter to your request.

To know if a field can be sorted, check the "sortable" parameter into the resource metadata. For more on this, refer to [this section](../../api/using/metadata-mechanism.md).

<br/>

***Sample requests***

* Sample GET request to retrieve emails in the database alphabetically ordered.

    ```

    -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/email/email?_order=email \
    -H 'Content-Type: application/json' \
    -H 'Authorization: Bearer <ACCESS_TOKEN>' \
    -H 'Cache-Control: no-cache' \
    -H 'X-Api-Key: <API_KEY>'

    ```

    Response to the request.

    ```

    {
    "content": [
        "adam@email.com",
        "allison.durance@example.com",
        "amy.dakota@mail.com",
        "andrea.johnson@mail.com",
        ...
    ]
    ...
    }

    ```

* Sample GET request to retrieve the email in the database in a descending alpha order.

    ```

    -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/email?_order=email%20desc \
    -H 'Content-Type: application/json' \
    -H 'Authorization: Bearer <ACCESS_TOKEN>' \
    -H 'Cache-Control: no-cache' \
    -H 'X-Api-Key: <API_KEY>'

    ```

    Response to the request.

    ```

    {
    "content": [
        "tombinder@example.com",
        "tombinder@example.com",
        "timross@example.com",
        "john.smith@example.com",
        ...
    ]
    }

    ```
