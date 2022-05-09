---
title: Creating a privacy request
description: Learn how to create a privacy request with APIs
audience: developing
content-type: reference
topic-tags: campaign-standard-apis

feature: API
role: Data Engineer
level: Experienced
exl-id: 06ad2e13-922b-4f35-8726-007427125c63
---
# Creating a privacy request {#creating-a-privacy-request}

>[!CAUTION]
>
>The [Privacy Core Service](https://developer.adobe.com/experience-platform-apis/references/privacy-service) Integration is the method you should use for all access and delete requests. <!--Starting 19.4, the use of the Campaign API and interface for access and delete requests is deprecated. For more on Campaign Standard deprecated and removed features, refer to [this page](../../rn/using/deprecated-features.md).-->

Privacy requests are created using a **POST** request.

Before creating requests, you need to define the namespace you will use. For more on this, refer the [Privacy management documentation](../../start/using/privacy-requests.md).

The payload must contain the following parameters:

* **name**: a unique internal name
* **namespace**: the namespace name configured in Campaign Standard interface
* **reconciliationValue**: the reconciliation value based on the reconciliation key defined in the namespace
* **label**: the request label
* **type**: the request type. Accepted values are "access" or "delete".
* **regulation**: the regulation type. Example: "GDPR", "CCPA". This parameter is mandatory, and available starting Campaign Standard 19.4 release. If you are on an older build, you do not need to add it to your payload.

<br/>

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
