---
title: List of roles
description: Find out the list of roles that you can assign to your users.
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

By default, Adobe Campaign offers a set of roles which allows you to define unitary authorizations assigned to users and user groups.

Combined with organizational units, roles give users a filtered view of the interface and define their access to the different features.

For more on this, refer to the [Roles and permissions table](/help/administration/using/assets/acs_rights.pdf), which details the functions available in the interface depending on the selected authorizations.

   ![](assets/user_management_3.png)

Roles can be managed from the **[!UICONTROL Administration > Users & Security > Roles]** menu.

Default rights are:

* **[!UICONTROL Administration]**: Generic administration right.
* **[!UICONTROL Datamodel]**: Right to run publications and create custom resources.
* **[!UICONTROL Generic import]**: Right to run a generic import on data. For this to work, you need to link the **[!UICONTROL Generic import]** role to the **[!UICONTROL Workflow]** role.
* **[!UICONTROL Prepare deliveries]**: Right to create, modify, prepare and delete deliveries. Users with this role can prepare the delivery but not send it.
* **[!UICONTROL Start deliveries]**: Right to create, modify, prepare, send, and delete deliveries.
* **[!UICONTROL Workflow]**: Right to manage the execution of workflows (start, stop, pause etc.). Users with this role can not send a delivery even in a workflow.

**Related topics:**

* [About access management](../../administration/using/about-access-management.md)
* [Managing groups and users](../../administration/using/managing-groups-and-users.md)
