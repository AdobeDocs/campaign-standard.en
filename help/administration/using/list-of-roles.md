---
title: List of roles
description: Find out the list of roles that you can assign to your users
audience: administration
feature: Access Management
role: Admin
level: Experienced
exl-id: 00714c80-bdaf-4241-bf2f-51498ca1dbef
TQID: https://experienceleague.adobe.com/HvLFiLS2GV0iJODsGL3AMMWd-lXbvDXYyLSJ8Mj20-w
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
feature_v2:
  - id: c5474392-5419-4296-9e41-f6f4ce4f6e9b
    internal-label: Administration
subfeature_v2:
  - id: e3988c18-3cfa-4f16-b812-ac2d2b1056fa
    internal-label: Permissions
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# List of roles{#list-of-roles}

By default, Adobe Campaign offers a set of roles which allows you to define unitary authorizations assigned to users and user groups.

Combined with organizational units, roles give users a filtered view of the interface and define their access to the different features.

Roles can be managed from the **[!UICONTROL Administration > Users & Security > Roles]** menu.

Default rights are:

* **[!UICONTROL Administration]**: Generic administration right.

    >[!NOTE]
    >
    >If you work with Experience Cloud Triggers, you need the **[!UICONTROL Administration]** right to be able to access the Experience Cloud Triggers menu. For more information on Experience Cloud Triggers, refer to this [page](../../integrating/using/about-adobe-experience-cloud-triggers.md).

* **[!UICONTROL Datamodel]**: Right to run publications and create custom resources.
* **[!UICONTROL Generic import]**: Right to run a generic import on data. For this to work, you must link the **[!UICONTROL Generic import]** role to the **[!UICONTROL Workflow]** role.
* **[!UICONTROL Prepare deliveries]**: Right to create, modify, prepare and delete deliveries. Users with this role can prepare the delivery but not send it.
* **[!UICONTROL Start deliveries]**: Right to create, modify, prepare, send, and delete deliveries.
* **[!UICONTROL Workflow]**: Right to manage the execution of workflows (start, stop, pause etc.). Users with this role can not send a delivery even in a workflow.

For more on this, refer to the [Roles and permissions table](/help/administration/using/assets/acs_rights.pdf), which details the functions available in the interface depending on the selected authorizations.

[![image](assets/user_management_3.png)](https://experienceleague.adobe.com/docs/campaign-standard/assets/acs_rights.pdf)

**Related topics:**

* [About access management](../../administration/using/about-access-management.md)
* [Managing groups and users](../../administration/using/managing-groups-and-users.md)
