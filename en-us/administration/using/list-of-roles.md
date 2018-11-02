---
title: List of roles
seo-title: List of roles
description: List of roles
seo-description: Find out the list of roles that you can assign to your users.
uuid: f592648e-9973-406e-9ebd-d7c4418f5ce7
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/administration/using/list-of-roles
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-25T09 29 14.976-0400
cq-lastreplicated: 2018-07-23T05 53 25.333-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: users-e-security
cq-template: /apps/help/templates/article-3
discoiquuid: 1d1c285e-3634-4609-b113-e38b70094c92
firstPublishExternalDate: 2018-07-23T05:53:25.294-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-02-16T08 01 35.478-0500
jcr-createdby: admin
jcr-description: List of roles
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T05:53:25.294-0400
lochandoffdate: 2018-07-25T09 29 14.976-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: List of roles
publishexternaldate: 2018-07-23T05 53 25.294-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/administration/using/list-of-roles.html
sha1: 90d808b233b3f6613914c68b57bb02ed2559cea6
topicBrowsingSortDate: 2018-07-23T05:53:25.294-0400
index: y
internal: n
snippet: y
---

# List of roles

List of roles

By default, Adobe Campaign offers a set of roles which allows you to define unitary authorizations assigned to users and user groups. Combined with organizational and geographical units, roles give users a filtered view of the interface and define their access to the different features. For more on this, refer to this [page](https://docs.campaign.adobe.com/doc/standard/en/Technotes/AdobeCampaign-ACSRights.pdf).

Roles can be managed from the **Administration > Users & Security > Roles** menu.

![](assets/user_management_3.png)

Default rights are:

* ADMINISTRATION: Generic administration right.
* DATAMODEL: Right to run publications and create custom resources.
* EXPORT: Right to export data.
* GENERIC IMPORT: Right to run a generic import on data. For this to work, you need to link the **Generic import** role to the **Workflow** role.
* PREPARE DELIVERIES: Right to create, edit, start delivery preparation and send proofs.
* START DELIVERIES: Right to validate previously prepared deliveries.
* WORKFLOW: Right to use workflows.

>[!CAUTION]
>
>The DELIVERABILITY role is for Adobe administrators internal use only. It must not be granted to a user.

**Related topics:**

* [About access management](../../administration/using/about-access-management.md)
* [Managing groups and users](../../administration/using/managing-groups-and-users.md)

