---
title: Mapping definition
description: Learn how to map a Campaign Standard field with an Experience Data Model (XDM) field.
page-status-flag: never-activated
uuid: 867b1c4b-4c79-4c52-9d0a-ef71993e50a2
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: configuring-channels
discoiquuid: 406c955a-b2d2-4099-9918-95f5fa966067

internal: n
snippet: y
---

# Mapping definition {#mapping-definition}

In this section, you will discover how to map a Campaign Standard field with an an Experience Data Model (XDM) field.

Note:

To perform this task, the prerequisites are:

an XDM Schema definition via the interface or by using the REST API associated to XDM
a Dataset creation based on the XDM schema definition
Go to Administration > Development > Platform and choose the Data mappings entry.

Click on Create to start a new XDM mapping.

Create a new mapping
Complete the mandatory fields and select:

a targeting dimension: this is the Campaign Standard schema to map

a dataset: this is the data package associated to an XDM schema in Adobe Experience Platform

Note:

If the dataset you select is already being used in an existing data mapping, a warning appears to inform you that your data may be overwritten on Adobe Experience Platform. This may happen when there are some common recipients in datamappings using a same dataset.

The following screen presents the Field mappings section where you can create a new mapping for each field in the Campaign Standard schema.

Create mapping
The Create new field mapping button allows you to select the Campaign Standard field and the corresponding field path expression in the XDM schema.

If you are unable to find an Campaign Standard field, you can use the search field to search for the field. Currently, search only works for fields which are open in hierarchy.

Map fields
NOTE - The extended resources defined in Campaign Standard are mapped liked all native fields. They are defined into the _customer/default extension in XDM.

Custom mapping
You can customize the XDM extension via the API and define your own extension allowing you a better control on mapping.

See Schema Registry API tutorial for more details on XDM API.

NOTE - To map an enumeration field, you need to use the expression editor to define each enumeration value corresponding to the XDM value. For example, the postalAdressfield needs to be defined as:

Enumeration
If the XDM value is defined as an enumeration in the XDM Schema, you can use the native EXDM function that will automatically replace the Iif syntax.

Enum mapping EXDM
To edit a XDM mapping, open it, modify the desired information then save it.

WARNING - For now, if you edit a value in the Field mappings section then click outside of the field, your change does not display in the interface until you click the Save button. This behaviour occurs only once, when the edit on Field Mappings is the first edit on the page.

Edit mapping
