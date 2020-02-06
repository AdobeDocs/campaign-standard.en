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

While most Email service providers are communicating to customers via a list-centric approach, Adobe Campaign relies on a relational database in order to leverage a broader view of the customers and their attributes.

This customer-centric approach is shown on the chart below. The **Profile** table in grey represents the main customer table around which everything is being built:

![](assets/customer-centric-data-model.png)

The Adobe Campaign default data model is presented in this [section](../../developing/using/datamodel-introduction.md).

<!--You can find a datamodel representation for the out-of-the-box resources [here](../../developing/using/datamodel-introduction.md).-->

<!--### What is a customer? {#customer-definition}

If you have customer data in more than one system, you need to determine which solution will allow you to identify records as one person. This work might require rules, eventually a match and merge processes to determine the master record. This master record should be the one sent to Adobe Campaign.

While some of this data cleansing might be performed in Adobe Campaign, the recommendation is to run these processes outside and only import clean data in Adobe Campaign. You should keep Campaign as a marketing solution more than a data cleansing tool.

Be able to provide a master customer record which will be sent to Adobe Campaign.-->

### Data for Adobe Campaign {#data-for-campaign}

What data should be sent to Adobe Campaign? It is critical to determine the data required for your marketing activities.

>[!NOTE]
>
>Adobe Campaign is neither a data warehouse or a reporting tool. Therefore, do not try to import all possible customers and their associated information into Adobe Campaign, or import data which will only be used to build reports.

To make the decision whether an attribute would be needed or not in Adobe Campaign, determine whether it would fall under one of these categories:
* Attribute used for **segmentation**
* Attribute used for **data management processes** (aggregate calculation for example)
* Attribute used for **personalization**

If an attribute does not fall into any of these, you are most likely not going to need this in the platform.

### Data types {#data-types}

To ensure good architecture and performance of your system, follow the best practices below to set up data in Adobe Campaign:
* The length for a **string** field should always be defined with the column. By default, the maximum length in Adobe Campaign is 255, but Adobe recommends keeping the field shorter if you already know that the size will not exceed a shorter length.
* It is acceptable to have a field shorter in Adobe Campaign than it is in the source system if there is a confirmation that the size in the source system was overestimated and would not be reached. This could mean a shorter string or smaller integer in Adobe Campaign.

## Best practices when configuring a resource's data structure

### Identifiers and keys {identifiers-and-keys}

<!-->>[!IMPORTANT]
>
>No table should be defined in Adobe Campaign without setting up primary keys. => on ne peut pas en fait et on ne parle pas de pkey car pas dans l'UI donc...-->

Adobe Campaign out-of-the-box tables have three identifiers. It is also possible to add an additional identifier.

The following table describe these identifiers and their purpose.

>[!NOTE]
>
>The display name is the name of the field while displayed to the user via the Adobe Campaign user interface. The technical name is the actual field name in the resource definition (and the table column name).

| Display name | Technical name | Description |
|--- |--- |--- |
|  | PKey | <ul><li>The id is usually the physical primary key of an Adobe Campaign table.</li><li>An id is usually unique to a specific Adobe Campaign instance. A record/object deployment would generate a different id in the destination instance of Adobe Campaign.</li><li>In Adobe Campaign Standard, this value is not visible to the end-user. Via the API system, it is possible to retrieve a PKey value (which is a generated/hashed value, not the physical id) and it is not recommended to use it for anything else than retrieving/updating/deleting records via API.|
| ID | name or internalName | <ul><li>Often called “internal name” this information is a unique identifier of a record in a table. However, this value can be manually updated, with usually a generated name.</li><li>This identifier is keeping its value when being deployed in a different instance of Adobe Campaign. It will be required for the object to have a different name than the generated value to be exportable via a package.</li><li>An end user will see “ID” for the field, but it is not the actual primary key of the table.</li></ul> |
| Label | label | <ul><li>Business identifier of an object/record in Adobe Campaign.</li><li>This object allows spaces and special characters but does not guarantee uniqueness of a record.|
| ACS ID |  acsId | <ul><li>An additional identifier can be added: the ACS ID. As the PKey should not be used in ACS, this is a solution to obtain a unique value generated during the insertion of a profile record.</li><li>The value can only be automatically generated if the option is enabled in the profile extension resource before a record gets inserted into Adobe Campaign. This UUID can be used as a reconciliation key.</li><li>For more on this, see [Generating a unique ID for profiles and custom resources](../../developing/using/configuring-the-resource-s-data-structure.md#generating-a-unique-id-for-profiles-and-custom-resources).</li></ul> |

**Best practices when creating IDs:**
* It is recommended to rename the record name generated by Adobe Campaign if the object is meant to be deployed from an environment to another. If the object is created under “business-as-usual” activity on production, there is no need to manually rename it unless it helps the IT or user groups with Adobe Campaign maintenance and usability.
* Any technical object created as a core functionality for a customer implementation of Adobe Campaign (think about data import workflows for example) should be renamed and a convention should be determined for the object name.
* Do not use special characters as space “ “, semi-column “:” or hyphen “-“. All these characters would be replaced by an underscore “_” (allowed character). While “abc-def” and “abc:def” should be different, they would be stored as “abc_def” and overwrite each other.

**Best practices when creating labels**:

It is recommended to determine a structure for your object labels as this will be the most user-friendly solution to identify a record or object for an Adobe Campaign user.

**Custom “internal key”**

Most organizations are importing records from external systems. While the physical key of the Profile table is behind the “PKey” attribute, it is possible to determine a custom key in addition.

This custom key is the actual record primary key in the external system feeding Adobe Campaign.

When an out-of-the-box table has both an ID (internal auto-generated) and internal key, the internal key will be set as a unique index in the physical database table (from Customer data).

Creating a custom table, you have two options:
* Combination of auto-generated key (id) and internal key (custom). This option is interesting if your system key is a composite key or not an integer. Integers will provide higher performances in big tables and joining with other tables.
* Primary key as the external system primary key. In most cases, we would prefer this solution. This simplifies the approach to import/export data, with a consistent key between different systems.
Takeaway: Primary keys are required for every table created in Adobe Campaign. An autopk should not be used as a reference in workflows.