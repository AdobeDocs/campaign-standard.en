---
title: About the Audience Destinations service
description: Learn more about the Audience Destinations service.
page-status-flag: never-activated
uuid: b3996642-96ec-489e-b146-c8c2cb52aa32
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: audiences
content-type: reference
topic-tags: managing-audiences
discoiquuid: 750ecd8d-67a5-4180-bfec-2a8e3098c812
context-tags: audience,wizard;audience,overview;delivery,audience,back
internal: n
snippet: y
---

# About the Audience Destinations service {#about-audiences}

>[!IMPORTANT]
>
>This capability is currently in beta, and subject to frequent updates and modifications without notice. Data mapping is based on Adobe Experience Platform and requires a specific configuration. Please reach out to Adobe Customer Care if you plan to implement this capability.

The **Audience Destinations service** allows you to build highly targeted audiences based on large, complex datasets and share these segments near real-time with other Adobe Experience Cloud solutions.

The [Adobe Experience Platform](https://www.adobe.io/apis/experienceplatform/home.html) consolidates profile, behavioral and multi-entity data to help you build a 360 view of your customer, enabling you to effectively manage your customer experiences.

Campaign Standard allows you to work with Adobe Experience Platform, in order to identify collections of profiles, known as **Audiences**. They are created by building **segments**, which are rules including profile attributes and event data originating from Adobe Experience Platform.

Global concepts on Unified Profile & Segmentation Services can be referenced in [these dedicated documents](https://www.adobe.io/apis/experienceplatform/home/profile-identity-segmentation.html).

Once an audience has been created, you can activate it for a delivery in [Campaign Standard workflows](../../automating/using/aep-targeting-audiences.md). Additionally, you can use contextual data from the Adobe Experience Platform to [personalize](../../automating/using/aep-personalizing-campaigns.md) and add dynamic content to your campaigns, if desired.

Terms used in these sections:

* **Profile**: Profile is an Experience Platform standard data model used to define attributes of consumers. A profile can also be an aggregate of event data and attributes related to a person and or device.

    Example: "John Doe is a 55 years old male.”

* **Segment**: A set of rules that defines a subset of profiles from your database, using both attributes and event data.

    Example: “Males > 50 years old.”

* **Audience**: A collection of profiles that meet segment rules.

    Example: List of profiles corresponding to all males > 50 years old in your database.
