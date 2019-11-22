---
title: Privacy management
description: Learn more about privacy management with APIs
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

# Privacy management {#privacy-management}

Campaign Standard APIs provides features that allow the automatic process of requests related to privacy regulations such as GDPR and CCPA.

The actions you can perform are as follows:

* Create a new privacy request,
* Monitor a privacy request,
* Retrieve a privacy data file,
* Manage a profile's CCPA opt-out status.

The privacy API endpoint is **/privacy/privacyTool**. PrivacyTool resource description and associated filters are available in the resource metadata. See [Metadata Mechanism](#metadata-mechanism).

CCPA opt-out is managed using the **ccpaOptOut** profile attribute.

For more on Adobe Campaign Standard and privacy compliance, refer to the [dedicated documentation](https://helpx.adobe.com/campaign/kb/acs-privacy.html).

## Creating a privacy request

>[!CAUTION]
>
>The [Privacy Core Service](https://adobe.io/apis/cloudplatform/gdpr.html) Integration is the method you should use for all access and delete requests. Starting 19.4, the use of the Campaign API and interface for access and delete requests is deprecated. For more on Campaign Standard deprecated and removed features, refer to [this page](https://helpx.adobe.com/campaign/kb/acs-deprecated-and-removed-features.html).

Privacy requests are created using a **POST** request.

Before creating requests, you need to define the namespace you will use. For more on this, refer the [Privacy management documentation](https://helpx.adobe.com/campaign/kb/acs-privacy.html#ManagingPrivacyRequests).

The payload must contain the following parameters:

* **name**: a unique internal name
* **namespace**: the namespace name configured in Campaign Standard interface
* **reconciliationValue**: the reconciliation value based on the reconciliation key defined in the namespace
* **label**: the request label
* **type**: the request type. Accepted values are "access" or "delete".
* **regulation**: the regulation type. Example: "GDPR", "CCPA". This parameter is mandatory, and available starting Campaign Standard 19.4 release. If you are on an older build, you do not need to add it to your payload.

***Sample request***

This POST request creates a privacy request based on a email reconciliation key defined in the namespace AMCDS2:

```

-X POST https://mc.adobe.io/<ORGANIZATION>/campaign/privacy/privacyTool \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>' \
-H 'Content-Type: application/json;charset=utf-8'

{
"name":"PT11832",
"namespaceName": "AMCDS2",
"reconciliationValue": "customers@adobe.com",
"regulation": "gdpr",
"label":"Delete customers",
"type":"delete"
}

```

Response to the POST request.

```

{
    "PKey": "<PKEY>",
    "audit": "",
    "created": "2018-03-21 10:41:58.570Z",
    "desc": "",
    "gdprRequestData": {
        "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/head/privacyTool/<PKEY>/gdprRequestData/"
    },
    "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/privacy/privacyTool/<PKEY>",
    "label": "Delete customers",
    "lastModified": "2018-03-21 10:41:58.570Z",
    "name": "PT11832",
    "namespace": {
        "PKey": "<PKEY>",
        "title": "Doc (AMCDS2)"
    },
    "namespaceName": "AMCDS2",
    "reconciliationValue": "customers@adobe.com",
    "regulation": "gdpr",
    "retryCount": 0,
    "status": "new",
    "title": "Delete customers (PT11832)",
    "type": "delete"
}

```

## Monitoring a privacy request

You can monitor information about a created privacy request using a **GET** request.

The status list description is available in the [Privacy management documentation](https://helpx.adobe.com/campaign/kb/acs-privacy.html#ManagingPrivacyRequests).

***Sample request***

```

-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/privacy/privacyTool \
-H 'Authorization: Bearer <ACCESS_TOKEN>' 
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>' \
-H 'Content-Type: application/json;charset=utf-8'

```

Response to the GET request.

```

{
            "PKey": "<PKEY>",
            "audit": "",
            "created": "2018-03-09 12:28:37.319Z",
            "desc": "",
            "gdprRequestData": {
                "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/privacy/privacyTool/<PKEY>/gdprRequestData/"
            },
            "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/privacy/privacyTool/<PKEY>",
            "label": "Delete customer profile",
            "lastModified": "2018-03-09 12:39:21.232Z",
            "name": "GDPR6",
            "namespace": {
                "PKey": "<PKEY>",
                "title": "Email (defaultNamespace1)"
            },
            "namespaceName": "defaultNamespace1",
            "reconciliationValue": "customers@adobe.com",
            "regulation": "gdpr",
            "retryCount": 0,
            "status": "errorDataNotFound",
            "title": "Delete customer profile (GDPR6)",
            "type": "delete"
        }

```

## Retrieving a privacy data file

>[!CAUTION]
>
>The [Privacy Core Service](https://adobe.io/apis/cloudplatform/gdpr.html) Integration is the method you should use for all access and delete requests. Starting 19.4, the use of the Campaign API and interface for access and delete requests is deprecated. For more on Campaign Standard deprecated and removed features, refer to [this page](https://helpx.adobe.com/campaign/kb/acs-deprecated-and-removed-features.html).

To retrieve the file that contains all the information associated to a reconciliation value, follow this three-steps procedure:

1. Perform a **POST** request to create a new request with the attribute **type="access"**, see [Creating a new privacy request](#creating-a-privacy-request).

1. Perform a **GET** request to retrieve information about the request.

1. Retrieve the data file by performing a **POST** request on the returned **privacyRequestData** URL, with the privacy request internal name inside the payload. For example: {"name":"PT17"}.

***Sample request***

Create a privacy request with the type="access" attribute.

```

-X POST https://mc.adobe.io/<ORGANIZATION>/campaign/privacy/privacyTool \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>' \
-H 'Content-Type: application/json;charset=utf-8'

{
"name":"PT11832",
"namespaceName": "AMCDS2",
"reconciliationValue": "customers@adobe.com",
"regulation": "gdpr",
"label":"Delete customers",
"type":"access"
}

```

<!-- + réponse -->

Perform a GET request to retrieve information about the request.

```

-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/privacy/privacyTool \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>' \
-H 'Content-Type: application/json;charset=utf-8'

```

It returns the privacyRequestData attribute with an associated URL.

```

{
    ...
    "name": "PR2",
    "namespace": ...,
    "namespaceName": "defaultNamespace1",
    "privacyRequestData": {
        "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/privacy/privacyTool/<PKEY>/privacyRequestData/"
    },
    "reconciliationValue": "johndoe@mail.com",
    "regulation": "gdpr",
    "retryCount": 0,
    "status": "complete",
    "title": "EPR (PR2)",
    "type": "access"
    ...
},

```

Perform a POST request on the privacyRequestData URL, with the request internal name inside the payload.

```

-X POST https://mc.adobe.io/<ORGANIZATION>/campaign/privacy/privacyTool/<PKEY>/privacyRequestData \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>' \
-H 'Content-Type: application/json;charset=utf-8'
-d '{"name": "PR1"}'

```

It returns the file content.

```

"{data:<gdprRequestData _cs=\" ()\" id=\"8565163\" reconciliationValue=\"'customer@adobe.com'\">\n  <table name=\"nms:recipient\">\n    <rowId='8569152'\n\t\tlastName='customer'\n\t\tfirstName='customer'\n\t\tgender='1'\n\t\temail='customer@adobe.com'\n\t\tcreatedBy-id='8565162'\n\t\tmodifiedBy-id='8565162'\n\t\tlastModified='2018-03-15 13:54:28.708Z'\n\t\tcreated='2018-03-15 13:54:28.708Z'\n\t\tthumbnail='/nl/img/thumbnails/defaultProfil.png'\n\t\temailFormat='2'</row>\n  </table>\n  <table name=\"nms:broadLogRcp\">\n    <row>deliveryLabel='Send via email'\n\t\tdeliveryType='0'\n\t\tcontactDate='2018-03-15 13:58:31.667Z'\n\t\tid='8003'\n\t\taddress='customer@adobe.com'\n\t\tstatus='1'\n\t\tmsg-id='1194'\n\t\teventDate='2018-03-15 13:58:34.726Z'\n\t\tlastModified='2018-03-15 13:59:02.008Z'\n\t\tvariant='default'\n\t\tdelivery-id='8569153'\n\t\tpublicId='1'\n\t\tprofile-id='8569152'</row>\n  </table>\n  <table name=\"nms:trackingLogRcp\">\n    <row>deliveryLabel='Send via email'\n\t\tdeliveryType='0'\n\t\tcontactDate='2018-03-15 13:58:31.667Z'\n\t\turlLabel='Open'\n\t\turlSource=''\n\t\tuserAgent='-1178080215'\n\t\ttrackedDevice='pc'\n\t\tid='5000'\n\t\tlogDate='2018-03-15 14:00:51.650Z'\n\t\tsourceType='html'\n\t\tuserAgent='-1178080215'\n\t\turl-id='1'\n\t\tdelivery-id='8569153'\n\t\tbroadLog-id='8003'\n\t\trecipient-id='8569152'</row>\n    <row>deliveryLabel='Send via email'\n\t\tdeliveryType='0'\n\t\tcontactDate='2018-03-15 13:58:31.667Z'\n\t\turlLabel='Open'\n\t\turlSource=''\n\t\tuserAgent='0'\n\t\ttrackedDevice=''\n\t\tid='6000'\n\t\tlogDate='2018-03-15 16:00:41.110Z'\n\t\tsourceType='html'\n\t\turl-id='1'\n\t\tdelivery-id='8569153'\n\t\tbroadLog-id='8003'\n\t\trecipient-id='8569152'</row>\n  </table>\n</gdprRequestData>}"

```

## Managing CCPA opt-out

A profile's CCPA opt-out status can be monitored and managed using the **ccpaOptOut** profile attribute and the "true" or "false" values:

`"ccpaOptOut": <value>`

* **true**:  forbids the sale of personal information.
* **false**: authorizes the sale of personal information.

>[!CAUTION]
>
>The “CCPA Opt-Out” attribute is only available starting 19.4. For 19.3 environments, you need to extend the Profiles resource and add a boolean field. This field will be added to the API with the chosen label. We suggest you use “Opt-Out for CCPA”.
>
>For more on this, refer to the [Privacy management documentation](https://helpx.adobe.com/campaign/kb/acs-privacy.html#ccpa).

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
