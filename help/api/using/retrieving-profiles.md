---
title: Retrieving profiles
description: Learn more how to retrieve profiles with APIs
feature: API
role: Data Engineer
level: Experienced
exl-id: 19679804-f728-49fa-b26e-8f31b67c29bf
---
# Retrieving profiles with APIs {#retrieving-profiles}

Retrieving profiles is performed with a **GET** request.

You can then refine your search by using filters, ordering and pagination. For more on this, refer to the [Additional operations](../../api/using/sorting.md) section.

Additionally, Campaign Standard APIs allow you to search for profiles based on one of these fields: email, first name, last name or any custom field. For more on this, refer to [this section](#searching-field).

<br/>

***Sample requests***

* Sample GET request to retrieve all profiles.

    ```

    -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile \
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
                "firstName": "John",
                "lastName":"Doe",
                "birthDate": "1980-10-24",
                ...
            },
            ...
    }

    ```

* Sample GET request to retrieve the first 10 email values.

    ```

    -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/email?_lineCount=10 \
    -H 'Content-Type: application/json' \
    -H 'Authorization: Bearer <ACCESS_TOKEN>' \
    -H 'Cache-Control: no-cache' \
    -H 'X-Api-Key: <API_KEY>'

    ```

    Response to the request. The "next" node returns the URL that gives you access to the 10 next email values.

    ```

    {
    "content": [
        "amy.dakota@mail.com",
        "kristen.smith@mail.com",
        "omalley@mail.com",
        "xander.harrys@mail.com",
        "jane.summer@mail.com",
        "gloria.boston@mail.com",
        "edward.snow@mail.com",
        "dorian.simons@mail.com",
        "peter.paolini@mail.com",
        "mingam+test08@adobe.com"
    ],
    "next": {
        "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/email?_lineCount=10&_
        lineStart=@Qy2MRJCS67PFf8soTf4BzF7BXsq1Gbkp_e5lLj1TbE7HJKqc"
    }
    }

    ```

## Searching for profiles based on a field {#searching-field}

The **[!UICONTROL filterType]** parameter allows you to retrieve profiles based on one of these fields: email, first name, last name or any custom field that has been added in Advanced filtering when extending the profile resource.

>[!NOTE]
>
>Searches are case-sensitive and performed on prefixes only. For example, you will not be able to look up for a profile using their last name's last letters.

***Sample requests***

* Sample request to filter profiles on the basis of first name.

    ```

    -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/byText?text=John&filterType=firstName \
    -H 'Content-Type: application/json' \
    -H 'Authorization: Bearer <ACCESS_TOKEN>' \
    -H 'Cache-Control: no-cache' \
    -H 'X-Api-Key: <API_KEY>'

    ```

* Sample request to filter profiles on the basis of last name.

    ```

    -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/byText?text=Miller&filterType=lastName \
    -H 'Content-Type: application/json' \
    -H 'Authorization: Bearer <ACCESS_TOKEN>' \
    -H 'Cache-Control: no-cache' \
    -H 'X-Api-Key: <API_KEY>'

    ```

* Sample request to filter profiles on the basis of email.

    ```

    -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/byText?text=John%40gmail.com&filterType=email \
    -H 'Content-Type: application/json' \
    -H 'Authorization: Bearer <ACCESS_TOKEN>' \
    -H 'Cache-Control: no-cache' \
    -H 'X-Api-Key: <API_KEY>'

    ```

* Sample request to filter profiles based on the "Hobby" custom field.

    ```

    -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/profile/byText?cusHobby=Dancing&filterType=Hobby \
    -H 'Content-Type: application/json' \
    -H 'Authorization: Bearer <ACCESS_TOKEN>' \
    -H 'Cache-Control: no-cache' \
    -H 'X-Api-Key: <API_KEY>'

    ```
