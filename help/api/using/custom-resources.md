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

# Custom resources {#custom-resources}

Adobe Campaign comes with a pre-defined data model, where data is defined through different resources. You can enrich the data model that is provided by extending the resources to add your own custom fields, such as purchase or product tables.

For more information on data model extension, refer to the Campaign documentation:

* [Data model concepts](https://docs.adobe.com/content/help/en/campaign-standard/using/developing/about-custom-resources/data-model-concepts.html)
* [Extending the API](https://helpx.adobe.com/campaign/standard/developing/using/about-extending-the-api.html)
* [Defining links with other resources](https://helpx.adobe.com/campaign/standard/developing/using/configuring-the-resource-s-data-structure.html#defining-links-with-other-resources)

Custom resources are accessible using the **/profileAndServicesExt** endpoint, and the custom resource name.

`https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/<resourceName>/`

>[!NOTE]
>
>For resources that are not out-of-the-box, always use the <b>"cus"</b> prefix before the resource's name.

You can perform any operation with custom resources, as long as they are linked to the Profile table.

For example, let's consider the tables structure below:

![alt text](assets/cusresources.png)

In that case, all resources from the **Transaction**, **TransactionDetails** and **Product** tables are available as long as they are linked to the **Profile** table.

***Sample request***

Sample GET request to access the extended profileAndServicesExt resource.

```

-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/\
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>' \

```

It returns the list of all linked custom resources. You can then use the resources URLs to perform any API task described in this documentation.

```

{
"apiName": "resourceType",
"cusProduct": {
        "content": ...,
        "data": "/profileAndServicesExt/cusProduct/",
        "help": "Product",
        "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/cusProduct/metadata",
        "name": "cusProduct",
        "type": "collection"
    },
"cusTransaction": {
        "content": ...,
        "data": "/profileAndServicesExt/cusTransaction/",
        "help": "Product",
        "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/cusTransaction/metadata",
        "name": "cusProduct",
        "type": "collection"
    },
"cusTransactionDetails": {
        "content": ...,
        "data": "/profileAndServicesExt/cusTransactionDetails/",
        "help": "Product",
        "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/cusTransactionDetails/metadata",
        "name": "cusProduct",
        "type": "collection"
    },
}

```
