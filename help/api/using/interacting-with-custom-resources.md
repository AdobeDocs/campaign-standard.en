---
solution: Campaign Standard
product: campaign
title: Custom resources
description: Learn more about custom resources management with APIs/
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
feature: API
role: Data Engineer
level: Experienced
---

# Interacting with custom resources {#interacting-with-custom-resources}

The **/customResources** endpoint allows you to expose the Campaign custom resources in REST. Based on this API, an integration between custom entities and external endpoints is available.

The /customResources endpoint has exactly the same behavior as /profileAndServices endpoint.

The custom resources that are exposed within this API are:

* all the entities linked to the profile entity
* all the entities linked to the profile entity's children
* all the entities that are not linked to profile and, for these entities, their children and grandchildren.

>[!NOTE]
>The custom resources that are available under /profileAndServicesExt are not exposed in the /customResources API.

Here is an example to retrieve the metadata from a custom resource:

```
GET /customResources/resourceType/<customResourceName>
```

To perform a creation, update or deletion, the GET, POST, PATCH, DELETE are used.

```
POST /customResources/<customResourceName>
```

>[!NOTE]
>The privacy API endpoint and workflows (/privacy/privacyTool) are not managing the custom resources that are not linked to the profile entity.
>You will have the responsibility to manage and clean up any PII for these custom resources. For more information on privacy tool, [click here](../../api/using/creating-a-privacy-request.md).

