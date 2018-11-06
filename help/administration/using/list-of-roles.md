---
title: List of roles
seo-title: List of roles
description: List of roles
seo-description: Find out the list of roles that you can assign to your users.
uuid: 2c8501ae-7030-48d1-acab-56c53bfe06bd
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/administration/using/list-of-roles
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-10-04T05 14 28.853-0400
cq-lastmodifiedby: beneat
cq-lastreplicated: 2018-10-04T05 14 28.912-0400
cq-lastreplicatedby: beneat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: users-e-security
cq-template: /apps/help/templates/article-3
discoiquuid: f88241cc-d0ae-48b2-a3d0-7d397cce1592
firstPublishExternalDate: 2018-09-07T14:41:21.936-0400
firstpublishinternaldate: 2018-10-04T05 14 28.839-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-02-16T08 01 35.478-0500
jcr-createdby: admin
jcr-description: List of roles
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-10-04T05:14:28.839-0400
lastpublishinternaldate: 2018-10-04T05 14 28.839-0400
lochandoffdate: 2018-09-10T07 23 04.045-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: beneat@adobe.com
moreHelpPaths: /content/help/en/campaign/standard/administration/morehelp/users-e-security;/content/help/en/campaign/standard/administration/morehelp/users-e-security
navTitle: List of roles
publishexternaldate: 2018-10-04T05 14 28.839-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/administration/using/list-of-roles.html
publishinternaldate: 2018-10-04T05 14 28.839-0400
publishinternalurl: https //helpx-internal.corp.adobe.com/content/help/en/campaign/standard/administration/using/list-of-roles.html
sha1: 212a40997c5f2313467837fd786a492adaf8fcf7
topicBrowsingSortDate: 2018-10-04T05:14:28.839-0400
index: y
internal: n
snippet: y
---

# List of roles

List of roles

By default, Adobe Campaign offers a set of roles which allows you to define unitary authorizations assigned to users and user groups. Combined with organizational and geographical units, roles give users a filtered view of the interface and define their access to the different features. For more on this, refer to this [page](https://docs.campaign.adobe.com/doc/standard/en/Technotes/AdobeCampaign-ACSRights.pdf).

Roles can be managed from the **Administration > Users & Security > Roles** menu.
[ ![](assets/user_management_3.png)](https://docs.campaign.adobe.com/doc/standard/en/Technotes/AdobeCampaign-ACSRights.pdf)Default rights are:

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

