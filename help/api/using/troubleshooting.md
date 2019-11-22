---
title: Troubleshooting
description: Learn more about  common issues related Campaign Standard APIs.
page-status-flag: never-activated
uuid: c7b9c171-0409-4707-9d45-3fa72aee8008
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: use-case--extending-the-api
discoiquuid: 304e7779-42d2-430a-9704-8c599a4eb1da

internal: n
snippet: y
---

# Troubleshooting {#troubleshooting}

```

-X GET https://mc.adobe.io/{ORGANIZATION}/campaign/profileAndServices/profile \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'

```

It returns the following error.

```

{"error_code":"403023","message":"Profile is not valid"}

```

>Check your IMS profile with this request.

```

-X GET https://ims-na1.adobelogin.com/ims/profile/v1 \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'

```

In the response, the ORGANIZATION_ID value must be the same in your first GET request.

```

{
  "countryCode": "FR",
  "mrktPermEmail": null,
  "projectedProductContext": [
    {
    "prodCtx": {
      "statusCode": "ACTIVE",
      "ident": "ZQ9FRQK7BF09YXAESFY9DDQP1G",
      "modDts": 1448307260000,
      "organization_id": "actest",
      "owningEntity": "6096892F54B5819E0A4C98A2@AdobeOrg",
      "serviceCode": "dma_tartan",
      "label": "Adobe Marketing Cloud",
      "serviceLevel": "standard",
      "createDts": 1421181343000,
      "deal_id": " "
      }
    }
  ]
}

```

* **When going to the Adobe.io Console you get the following error: "The Adobe I/O console is only available to select members of enterprise accounts. If you believe you should have access, please contact your System Administrator."**

You can only create API Keys for the IMS organizations you are admin of. If this message is displayed and you want to create API Keys and you want to ask one of the administrator of the IMS organization.

* **When doing a request to Adobe.io you get {"error_code":"403023","message":"Profile is not valid"}**

This means that there is an issue with the IMS provisioning of your specific Campaign product: the IMS team needs to fix it.

To get more details you can call the IMS API with your token to see what your IMS profile looks like: You need to have a prodCtx where the organization_id is the same as the one you put in you URL for Adobe.io to be able to route your request.
If it is missing the IMS provisioning needs to be fixed.

* **When doing a request to Adobe.io you get {"code":500, "message":"Oops. Something went wrong. Check your URI and try again."}**

Adobe.io declares your unvalid URI: most likely the URI you are requesting is not valid. On Adobe.io when you select the Campaign service you get a picker with a list of possible organization_ids. You need to check that the one you choose is the one you put in your URL.

* **When doing a request to Adobe.io you get {"error_code":"401013","message":"Oauth token is not valid"}**

Either your token is invalid (improper IMS call used to generate a token) or your token has expired.

* **I don't see my profile after creation**

Depending on the instance configuration, the created profile needs to be associated to an **orgUnit**. To understand how to add this field in your creation, consult [this section](#creating-profiles).
