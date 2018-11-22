---
title: Data model concepts
seo-title: Data model concepts
description: Data model concepts
seo-description: 
page-status-flag: never-activated
uuid: f1236053-b821-4811-8f50-076a3c884f3b
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/developing/using/data-model-concepts
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: about-custom-resources
discoiquuid: a1610b0e-93ed-4547-afb5-bbb1d06e4e84
isreadyforlocalization: false
navTitle: Data model concepts
publishexternaldate: 2018-11-20
sha1: 2f79e5c0ac8de2b9ac66f802c908cd38e1b7a2e2
index: y
internal: n
snippet: y
---

# Data model concepts{#data-model-concepts}

Data model concepts

Adobe Campaign comes with a pre-defined data model. This data model can be modified by administrators with new resources or extensions to existing resources.

The **Administration** > **Development** menu, accessed via the Adobe Campaign logo, allows you to manage your **custom resources**, **publish** them, and **access the diagnostic tools**.

The data used by Adobe Campaign is defined through different resources.

You can **enrich the data template** that is provided by creating your own custom resources, such as purchase or product tables.

Out-of-the-box resources (such as campaigns, emails, or audiences) cannot be modified. However, custom resources can be extended to add new fields.

>[!NOTE]
>
>You can find a datamodel representation for the out-of-the-box resources [here](https://docs.campaign.adobe.com/doc/standard/en/datamodel/datamodel.html).

You can also **configure the navigation** in the screens corresponding to the resource created.

Extension fields are generated with a prefix so that they never conflict with the out-of-the-box fields.
