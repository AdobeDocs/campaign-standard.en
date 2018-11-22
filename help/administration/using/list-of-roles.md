---
title: List of roles
seo-title: List of roles
description: List of roles
seo-description: Find out the list of roles that you can assign to your users.
page-status-flag: never-activated
uuid: 223b58f0-e143-4723-ab36-d5e47104409d
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/administration/using/list-of-roles
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: users-e-security
discoiquuid: 46da502b-1b89-4c79-9b87-48efb5ea0b14
isreadyforlocalization: false
navTitle: List of roles
publishexternaldate: 2018-11-20
sha1: c2f0b40b2a07bce5a0afab58b0cb4b814fe2e929
index: y
internal: n
snippet: y
---

# List of roles{#list-of-roles}

List of roles

By default, Adobe Campaign offers a set of roles which allows you to define unitary authorizations assigned to users and user groups. Combined with organizational units, roles give users a filtered view of the interface and define their access to the different features. For more on this, refer to the [Roles and permissions table](https://docs.campaign.adobe.com/doc/standard/en/Technotes/AdobeCampaign-ACSRights.pdf).

![](assets/user_management_3.png)

Roles can be managed from the **Administration > Users & Security > Roles** menu.

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

