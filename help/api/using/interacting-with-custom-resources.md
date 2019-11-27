---
title: Custom resources
description: Learn more about custom resources management with APIs/
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

# Interacting with custom resources {#interacting-with-custom-resources}


The **/customResources** endpoint allows you to expose the ACS custom entities in REST. Based on this API, an integration between custom entities and external endpoints is available.

The /customResources has exactly the same behavior as /profileAndServices endpoint.

The custom entities that are exposed within this API are:

* all the entities linked to the profile entity
* all the entities linked to the profile entity's children
* all the entities that are not linked to profile and, for these entities, their children and grandchildren.

>[!NOTE]
>The custom entities that are available under /profileAndServicesExt are not exposed in the /customResources API.

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
