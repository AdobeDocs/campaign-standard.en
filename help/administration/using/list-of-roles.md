---
title: List of roles
seo-title: List of roles
description: List of roles
seo-description: Find out the list of roles that you can assign to your users.
page-status-flag: never-activated
uuid: 128aaf9b-9b7d-49f3-9e1f-72e79a29baa0
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: users-and-security
discoiquuid: ceaa3c94-9e1a-4271-b443-b00b4068929f
context-tags: role,overview;role,main
internal: n
snippet: y
---

# List of roles{#list-of-roles}

By default, Adobe Campaign offers a set of roles which allows you to define unitary authorizations assigned to users and user groups. Combined with organizational units, roles give users a filtered view of the interface and define their access to the different features. For more on this, refer to the [Roles and permissions table](https://docs.campaign.adobe.com/doc/standard/en/Technotes/AdobeCampaign-ACSRights.pdf).

[![image](/help/administration/using/assets/user_management_3.png)](https://docs.campaign.adobe.com/doc/standard/en/Technotes/AdobeCampaign-ACSRights.pdf)

Roles can be managed from the **[!UICONTROL Administration > Users & Security > Roles]** menu.

Default rights are:

* **[!UICONTROL Administration]**: Generic administration right.
* **[!UICONTROL Datamodel]**: Right to run publications and create custom resources.
* **[!UICONTROL Export]**: Right to export data.
* **[!UICONTROL Generic import]**: Right to run a generic import on data. For this to work, you need to link the **[!UICONTROL Generic import]** role to the **[!UICONTROL Workflow]** role.
* **[!UICONTROL Prepare deliveries]**: Right to create, edit, start delivery preparation, send deliveries and proofs.
* **[!UICONTROL Start deliveries]**: Right to create, edit and validate previously prepared deliveries. This role does not allow you to send delivery.
* **[!UICONTROL Workflow]**: Right to create, edit, start delivery preparation and workflows.

>[!CAUTION]
>
>The **[!UICONTROL Deliverability]**, **[!UICONTROL Command execution]**, **[!UICONTROL Export]**, **[!UICONTROL File access]** and **[!UICONTROL Message Center push]** roles are for Adobe administrators internal use only. They should not be granted to a user.

**Related topics:**

* [About access management](../../administration/using/about-access-management.md)
* [Managing groups and users](../../administration/using/managing-groups-and-users.md)

