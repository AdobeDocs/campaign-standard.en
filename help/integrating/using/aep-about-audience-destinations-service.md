---
solution: Campaign Standard
product: campaign
title: About the Audience Destinations service
description: Learn more about the Audience Destinations service.
audience: audiences
content-type: reference
topic-tags: managing-audiences
context-tags: audience,wizard;audience,overview;delivery,audience,back
---

# About the Audience Destinations service {#about-audiences}

>[!IMPORTANT]
>
>Audience Destinations service is currently in beta, which may be subject to frequent updates without notice. Customers are required to be hosted on Azure (currently in beta for North America only) to access these capabilities. Please reach out to Adobe Customer Care if you would like access.

Empower your consumer experiences by leveraging the [Adobe Experience Platform](https://docs.adobe.com/content/help/en/experience-platform/landing/home.html) to build highly targeted audiences based on large, complex datasets. The Adobe Experience Platform consolidates profile, behavioral and multi-entity data across online and offline sources, including Adobe Analytics, to help you build a 360-degree view of your customer, enabling you to effectively manage your customer experiences.

Adobe Campaign Standard will then use the **Audience Destinations** service to retrieve a collection of profiles, known as **Audiences**, from Adobe Experience Platform for multi-step and/or cross-channel campaign programs.

**Audiences** are created by first building **segments**, which are essentially a set of rules based on virtually any variable (e.g., profile, event, multi-entity data) within a customer profile from Adobe Experience Platform to create a multidimensional target. Global concepts on Real-time Customer Profile & Segmentation Services are referenced in these dedicated documents:

* [Real-time Customer Profile overview](https://docs.adobe.com/content/help/en/experience-platform/profile/home.html)
* [Segmentation Service overview](https://docs.adobe.com/content/help/en/experience-platform/segmentation/home.html)

Once a segment has been created, you can then activate it as an audience for a delivery in [Campaign Standard workflows](../../integrating/using/aep-targeting-audiences.md). Additionally, you can use contextual data from the Adobe Experience Platform to [personalize](../../integrating/using/aep-personalizing-campaigns.md) and add dynamic content to your campaigns.

![](assets/do-not-localize/how-to-video.png) How-to videos are also available in [this section](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/profiles-and-audiences/audience-destinations/audience-destinations-overview.html).

Terms used in these sections:

* **Profile**: Profile is an Experience Platform standard data model used to define attributes of consumers. A profile can also be an aggregate of event data and attributes related to a person and or device.

    Example: "John Doe is a 55 years old male.”

* **Segment**: A set of rules that defines a subset of profiles from your database, using both attributes and event data.

    Example: “Males > 50 years old.”

* **Audience**: A collection of profiles that meet segment rules.

    Example: List of profiles corresponding to all males > 50 years old in your database.
