---
title: Data model best practices in Adobe Campaign Standard
description: Learn about the Adobe Campaign Standard data model best practices.
page-status-flag: never-activated
uuid: cacd563f-6936-4b3e-83e3-5d4ae31d44e8
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: about-custom-resources
discoiquuid: 4e0468da-3052-4ce5-8174-45aba1f5c4ed
context-tags: cusResource,overview;eventCusResource,overview
internal: n
snippet: y
---

# Data model best practices{#data-model-best-practices}

This document outlines key recommendations while designing the data model.

## Overview {#overview}

Adobe Campaign system is extremely flexible and can be extended beyond the initial implementation. However, while possibilities are infinite, it is critical to make wise decisions and build strong foundations to start designing your data model.

This document will provide common use case and best practices to learn how to architect properly you Adobe Campaign tool.

## Data model architecture {data-model-architecture}

Adobe Campaign Standard is a powerful cross-channel campaign management tool that can help you align your online and offline strategies to create personalized customer experiences.

### Customer-centric approach {#customer-centric-approach}

While most Email Service Providers are communicating to customers via a list-centric approach, Adobe Campaign relies on a relational database in order to leverage a broader view of the customers and their attributes.

This customer-centric approach is shown on the chart below. The **[!UICONTROL Profile]** table in grey represents the main customer table around which everything is being built:

![](assets/customer-centric-data-model.png)

The Adobe Campaign default data model is presented in this [section](../../developing/using/datamodel-introduction.md).

You can find a datamodel representation for the out-of-the-box resources [here](../../developing/using/datamodel-introduction.md).

<!--### What is a customer? {#customer-definition}

If you have customer data in more than one system, you need to determine which solution will allow you to identify records as one person. This work might require rules, eventually a match and merge processes to determine the master record. This master record should be the one sent to Adobe Campaign.

While some of this data cleansing might be performed in Adobe Campaign, the recommendation is to run these processes outside and only import clean data in Adobe Campaign. You should keep Campaign as a marketing solution more than a data cleansing tool.

Be able to provide a master customer record which will be sent to Adobe Campaign.-->

### Data for Adobe Campaign {#data-for-campaign}

What data should be sent to Adobe Campaign? It is critical to determine the data required for your marketing activities.

>[!NOTE]
>
>Adobe Campaign is neither a data warehouse or a reporting tool. This means that you should not try to import all possible customers and their associated information into Campaign, or import data which will only be used to build reports.

To make the decision whether an attribute would be needed or not in Adobe Campaign, determine whether it would fall under one of these categories:
* Attribute used for **segmentation**
* Attribute used for **data management processes** (aggregate calculation for example)
* Attribute used for **personalization**

If an attribute does not fall into any of these, you are most likely not going to need this in the platform.

### Data types {#data-types}

The following best practices around the type of data set up in Campaign can help to ensure a good architecture and performances of your system:
* Length for a **string** field should always be defined with the column. By default, Adobe Campaign will consider a length of 255, but we recommend keeping the field shorter if you already know that the size would not exceed a shorter length.
* It is acceptable to have a field shorter in Adobe Campaign than it is in the source system if there is a confirmation that the size in the source system was over estimated and would not be reached. This could mean a short string or smaller integer in Adobe Campaign.

## Best practices when building new resources?

### Identifiers and keys {identifiers-and-keys}

>[!IMPORTANT]
>
>No table should be defined in Adobe Campaign without setting up primary keys.

Adobe Campaign out-of-the-box tables have three identifiers. The following table describe them and their purpose.
Note: Identifier – Display name is the name of the field while it is displayed to the user via ACS user interface. Identifier – Technical name is the actual field name in the resource definition (and table column name).

| Identifier – Display name | Identifier – Technical name | Description |
|--- |--- |--- |
|  | PKey | The id is usually the physical primary key of an Adobe Campaign table.<br> An id is usually unique to a specific Adobe Campaign instance. A record/object deployment would generate a different id in the destination instance of Adobe Campaign.<br>In Adobe Campaign Standard, this value is not visible to the end-user. Via the API system, it is possible to retrieve a PKey value (which is a generated/hashed value, not the physical id) and it is not recommended to use it for anything else than retrieving/updating/deleting records via API.|
| ID | name or internalName | <ul><li>Often called “internal name” this information is a unique identifier of a record in a table. However, this value can be manually updated, with usually a generated name.</li><li>This identifier is keeping its value when being deployed in a different instance of Adobe Campaign. It will be required for the object to have a different name than the generated value to be exportable via a package.</li><li>An end user will see “ID” for the field, but it is not the actual primary key of the table.</li></ul> |
| Label | label | Business identifier of an object/record in Adobe Campaign. This object allows spaces and special characters but does not guarantee uniqueness of a record.|

For the “Profile” table, an additional “id” can be added: acsId. As the PKey should not be used in ACS, this is a solution to obtain a unique value generated during the insertion of a profile record.

The value will only be generated if the option is enabled in the profile extension resource before a record gets inserted in ACS. This UUID can be used as a reconciliation key.

