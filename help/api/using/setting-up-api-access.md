---
title: Setting-up API access
description: Learn how to set up access to Campaign Standard APIs.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis

feature: API
role: Data Engineer
level: Experienced
exl-id: efbbd0cd-9c56-4ad0-8bcb-efba4b63c28b
---
# Setting up API access {#setting-up-api-access}

Adobe Campaign Standard API access is set up through the steps below. Each of these steps is detailed in the [Adobe Developer documentation](https://developer.adobe.com/developer-console/docs/guides/#!AdobeDocs/adobeio-auth/master/AuthenticationOverview/ServiceAccountIntegration.md).

>[!IMPORTANT]
>
>To manage certificates in [Adobe Developer](https://developer.adobe.com/), make sure you have **System administrator** rights on the organization or a [developer account](https://helpx.adobe.com/enterprise/using/manage-developers.html) in the Admin Console.

1. **Check you have a digital certificate**, or create one if necessary. The public and private keys provided with the certificate are needed in the following steps.
1. **Create a new integration to Adobe Campaign Service** in [Adobe Developer](https://developer.adobe.com/) and configure it. Your credentials will then be generated (API Key, Client secret...).
1. **Create a JSON Web Token (JWT)** from the credentials previously generated and sign it with your private key. The JWT encodes all of the identity and security information that is needed by Adobe to verify your identity and grant you access to the API.

    >[!AVAILABILITY]
    >
    >JWT (JSON Web Tokens) is currently in the process of depreciation and is being replaced with OAuth. The transition is being carried out progressively within Campaign's upcoming releases and documentation will be updated to reflect these updates.

1. **Exchange your JWT for an Access Token** through a POST request. This Access Token will have to be used in each header of your API requests.

To establish a secure service-to-service Adobe I/O API session, every request to an Adobe service must include in the Authorization header the information below.

```

-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'

```

* **&lt;ORGANIZATION&gt;**: This is your personal ORGANIZATION ID, one ORGANIZATION ID is provided by Adobe for each of your instances :

    * &lt;ORGANIZATION&gt; : your production instance,
    * &lt;ORGANIZATION-mkt-stage&gt;: your stage instance.

    To obtain your ORGANIZATION ID value, refer to your administrator or your Adobe technical contact. You can also retrieve it into Adobe I/O when creating a new integration, in the licenses list (see the <a href="https://developer.adobe.com/developer-console/docs/guides/authentication/">Adobe Developer documentation</a>).

* **<ACCESS_TOKEN>**: Your personal access token, that was retrieved when exchanging your JSON Web Token through a POST request.

* **<API_KEY>**: your personal API Key. It is provided in Adobe I/O after creating a new integration to Adobe Campaign Service.

    ![alt text](assets/tenant.png)
    
## Troubleshooting

During AdobeIO integration, if the following error appears:

```

{ 
"code": 502, 
"message": "Oops. Something went wrong. Check your URI and try again." 
}

```


Refer to your administrator or your Adobe technical contact to check if the CNAME parameter is created correctly.
