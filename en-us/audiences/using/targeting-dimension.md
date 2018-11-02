---
title: Targeting dimension
seo-title: Targeting dimension
description: Targeting dimension
seo-description: Learn about target mapping selection, creation and management in Adobe Campaign.
page-status-flag: never-activated
uuid: d9644190-1db3-415c-9655-8595a160e040
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/audiences/using/targeting-dimension
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-01-10T15 16 25.872-0500
products: SG_CAMPAIGN/STANDARD
audience: audiences
content-type: reference
topic-tags: managing-audiences
cq-template: /apps/help/templates/article-3
discoiquuid: 56db1883-eeab-41ee-b1e1-4fcbb3b46c21
firstPublishExternalDate: 2018-01-10T15:16:25.862-0500
herogradient: light
jcr-created: 2018-01-11T19 01 25.593-0500
jcr-createdby: admin
jcr-description: Targeting dimension
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-01-10T15:16:25.862-0500
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Targeting dimension
publishexternaldate: 2018-01-10T15 16 25.862-0500
publishExternalURL: https://helpx.adobe.com/campaign/standard/audiences/using/targeting-dimension.html
sha1: 9d9e8be6b27dc2bc584239a9239bfd440ee08e1b
topicBrowsingSortDate: 2018-01-10T15:16:25.862-0500
index: y
internal: n
snippet: y
---

# Targeting dimension

Targeting dimension

You can create audiences from different resources available in Adobe Campaign. However, each audience is made up of a single targeting dimension. For example, you cannot create an audience made up of both profiles, test profiles and subscribers for example.

Targeting dimensions are defined in target mappings and stored under **Administration** > **Application settings** > **Target mappings**, accessible from the Adobe Campaign logo.

* **File** audiences (created directly from a [file import](../../automating/using/use-case--importing-profiles.md)) are not linked to an Adobe Campaign targeting dimension.
* [Profiles](../../audiences/using/about-profiles.md): audiences of identified profiles are particularly used to define the main targets for your messages, groups to exclude in your sends, etc.
* [Test profiles (seedMember)](../../sending/using/managing-test-profiles-and-sending-proofs.md#about-test-profiles): test profile audiences are particularly used to establish trap addresses, proof targets, etc.
* **Delivery**: deliveries (emails) created or sent with Adobe Campaign.

![](assets/audience_resource_selection.png)

