---
title: Custom resources
description: Learn more about custom resources management with APIs/
audience: developing
content-type: reference
topic-tags: campaign-standard-apis

feature: API
role: Data Engineer
level: Experienced
exl-id: d7b2231d-46ff-4966-9ea7-27a775e5236b
---
# Custom resources {#custom-resources}

Adobe Campaign comes with a pre-defined data model, where data is defined through different resources. You can enrich the data model that is provided by extending the resources to add your own custom fields or custom tables, such as purchase or product tables.

Custom resources are accessible through APIs using the **/profileAndServicesExt** endpoint, and the custom resource name.

`https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/<resourceName>/`

>[!NOTE]
>
>For resources that are not out-of-the-box, always use the <b>"cus"</b> prefix before the resource's name.

You can perform any operation with custom resources, as long as they are linked to the Profile table. For example, let's consider the tables structure below:

![alt text](assets/cusresources.png)

In that case, all resources from the **Transaction**, **TransactionDetails** and **Product** tables are available as long as they are linked to the **Profile** table.

<br/>

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
    ...
}

```

For more information on data model extension, refer to the Campaign documentation:

* [Data model concepts](../../developing/using/data-model-concepts.md)
* [Extending the API](../../developing/using/about-extending-the-api.md)
* [Defining links with other resources](https://helpx.adobe.com/campaign/standard/developing/using/configuring-the-resource-s-data-structure.html#defining-links-with-other-resources)
