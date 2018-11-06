---
title: About audiences
seo-title: About audiences
description: About audiences
seo-description: Learn how to build audiences from a query, a list or a file, and how to import them from Adobe Experience Cloud.
uuid: 1579bba7-b408-41ca-bd52-779b829f183f
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/audiences/using/about-audiences
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-10T07 22 50.159-0400
cq-lastreplicated: 2018-09-07T14 45 53.631-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: audiences
content-type: reference
topic-tags: managing-audiences
cq-template: /apps/help/templates/article-3
discoiquuid: 92078bf7-0ad8-4c2f-b8b1-a0e44421ee5b
firstPublishExternalDate: 2018-09-07T14:45:51.489-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 01 23.017-0400
jcr-createdby: admin
jcr-description: About audiences
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T14:45:51.489-0400
lochandoffdate: 2018-09-10T07 22 50.157-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: About audiences
publishexternaldate: 2018-09-07T14 45 51.489-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/audiences/using/about-audiences.html
sha1: 44d13c6e0f8101e4e1db9155df9f55c7a2ae2d12
topicBrowsingSortDate: 2018-09-07T14:45:51.489-0400
index: y
internal: n
snippet: y
---

# About audiences

About audiences

An audience is a list of profiles based on rules and attributes.

Adobe Campaign allows you to create your audiences manually using queries or automatically using dedicated workflows. You can also use shared audiences from the Adobe Experience Cloud. All of the audiences are regrouped into a list that can be accessed via the **Audiences** card on the Adobe Campaign home page or from the **Audiences** link.

![](assets/audience_1.png)

You can manipulate different audience types in Adobe Campaign. The type of an audience corresponds to the way in which it was created:

* **Query**: indicates that the audience was created from a [query](../../automating/using/editing-queries.md#about-query-editor) on data from the Adobe Campaign database from the list of audiences. Audiences defined by a query are recomputed at each further use.
* **List**: indicates that the audience is a fixed list of profiles. These lists are created in a [workflow](../../automating/using/discovering-workflows.md), where the data dimension is known when saving the audience. For example, after targeting activities (especially **Query**) or after the reconciliation of data imported from a file.
* **File**: indicates that the audience has been created directly from a [file import](../../automating/using/load-file.md) workflow and that the data dimension was unknown when saving the audience.
* **Experience Cloud**: indicates that the audience was imported from the Adobe Experience Cloud. This option is only available if the audience sharing functionality has been configured. For more information, see [Importing an audience from the Adobe Experience Cloud](../../integrating/using/sharing-audiences-with-audience-manager-or-people-core-service.md#importing-an-audience).

![](assets/audience_type_selection.png)

