---
title: Monitoring a privacy request
description: Learn how to monitor a privacy request with APIs
audience: developing
content-type: reference
topic-tags: campaign-standard-apis

feature: API
role: Data Engineer
level: Experienced
exl-id: 63864f0f-2c22-4a65-86ae-21897031f30a
---
# Monitoring a privacy request {#monitoring-a-privacy-request}

You can monitor information about a created privacy request using a **GET** request.

The status list description is available in the [Privacy management documentation](../../start/using/privacy-requests.md).

<br/>

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
