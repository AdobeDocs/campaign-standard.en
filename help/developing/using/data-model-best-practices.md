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

This document outlines key recommendations while designing the data model: what to be and what not to be followed, data type decisions, and other data model related topics are discussed.

Adobe Campaign comes with a pre-defined data model. This data model can be modified by [administrators](../../administration/using/users-management.md#functional-administrators) who are able to add new resources or extensions to existing resources.

>[!CAUTION]
>
>xxxx.

The **[!UICONTROL Administration]** > **[!UICONTROL Development]** menu, accessed via the Adobe Campaign logo, allows you to manage your **custom resources**, **publish** them, and **access the diagnostic tools**.


>[!NOTE]
>
>You can find a datamodel representation for the out-of-the-box resources [here](https://docs.campaign.adobe.com/doc/standard/en/datamodel/datamodel.html).

## Data model architecture {data-model-architecture}

Adobe Campaign relies on a relational database.

While most ESPs are communicating to customers via a list-centric approach, this is not the case with Adobe Campaign. Instead, the objective is to leverage a broader view of the customer and his/her attributes. In the Entity Relationship Diagram above, you can see this customer-centric approach with a Profile table in grey representing the main customer table around which everything is being built.

## Data for Adobe Campaign

What data should be sent to Adobe Campaign? A simple question which requires deep investigation.
Adobe Campaign offers a marketing database and not a data warehouse. This means that you should not try to import all possible customers and their associated information into Campaign.
Adobe Campaign is not a reporting tool either. While you will get reporting opportunities in Campaign, you do not want to import data which will only be used to build reports.
To make the decision whether an attribute would be needed or not in Adobe Campaign, determine whether it would fall under one of these categories:
• Attribute used for segmentation
• Attribute used for data management processes (aggregate calculation for example)
• Attribute used for personalization
If an attribute does not fall into any of these, you are most likely not going to need this in the platform.

## Data types

The following best practices around the type of data set up in Campaign can help to ensure a good architecture and performances of your system:
• Length for a string field should always be defined with the column. By default, Adobe Campaign will consider a length of 255, but we recommend keeping the field shorter if you already know that the size would not exceed a shorter length.
• It is acceptable to have a field shorter in Adobe Campaign than it is in the source system if there is a confirmation that the size in the source system was over estimated and would not be reached. This could mean a short string or smaller integer in Adobe Campaign.