---
title: Transactional messaging permission
description: Learn about permissions linked to transactional events.
audience: channels
content-type: reference
topic-tags: transactional-messaging
context-tags: null
hide: yes
hidefromtoc: yes
feature: Transactional Messaging
role: User
level: Intermediate
exl-id: 995da330-6c86-444b-86b2-61d887f37db4
---
# Transactional messaging permission {#transactional-message-permission}

Currently, in Adobe Campaign Standard, users without the Administrator security group cannot access, create, or publish events, causing issues for business users who need to configure and publish events but lack Administrator rights.

We have implemented the following improvements to transactional messaging access control:

* A new **[!UICONTROL Role]**, called **MC user**, has been added to allow non-administrator users to manage transactional events. The **MC user** role grants these users the ability to access, create, publish, and unpublish transactional events and messages.

* Child deliveries are now set to the **[!UICONTROL Organizational unit]** of the security group to which the user creating the message template belongs, rather than being restricted to the **[!UICONTROL Organizational unit]** of the **Message Center agent (mcExec)** security group.

* The default **Message Center Execution (mcExec)** campaign, which gathers the transactional messaging child deliveries, is now set to the organizational unit **All** allowing all users to view reports of child deliveries.

To assign the **MC user** role:

1. Create a new **[!UICONTROL Security group]** or update an existing one. [Learn more](../../administration/using/managing-groups-and-users.md).

1. Click **[!UICONTROL Create element]** to assign roles to your security group.

   ![](assets/event_access_1.png)

1. Select the MC user **[!UICONTROL Role]** and click **[!UICONTROL Confirm]**.

    >[!IMPORTANT]
    >
    > Proceed with caution when assigning the MC User role to operators, as this grants them the ability to unpublish events.

   ![](assets/event_access_2.png)

1. Once configured, click **[!UICONTROL Save]**.

Users linked to this **[!UICONTROL Security group]** can now access, create, and publish Transactional events and messages.

The table below outlines the impact of this feature on access control:

| Objects | Before this change | After this change |
|:-: | :--: | :-:|
|Message Center Execution (mcExec) campaign| **Message Center Execution (mcExec)** campaign is set to the Organizational unit of the **Message Center agent (mcExec)** security group.| **Message Center Execution (mcExec)** campaign is set to the Organizational unit **All** to allow all child deliveries to be associated with this campaign.</br> All users will be able to view reports of the child deliveries, but will only have read-only access to the delivery content.|
| Child Deliveries| Child deliveries are set to the **Organizational unit** of the **Message Center agent (mcExec)** security group.| Child deliveries will be set to the **Organizational unit** of the security group to which the user creating the message template belongs.|
|Message Template| Message Templates are set to the **Organizational unit** of the**Message Center agent (mcExec)** security group. | Message Templates will be set to the **Organizational unit** of the security group to which the user creating the message template belongs.|
|Transactional Events| Only users within the **Administrator** security group can create and publish events. | The **MC user** role allows users to create and publish events.|
|Transactional Message Templates| Transactional Message templates are set to the Organizational unit **All**. | Transaction Message Template will be set to the **Organizational unit** of the security group to which the user creating the message template belongs.|

## Duplicate transactional events

When the FEATUREFLAG_MC_DUPLICATE_EVENT feature flag is enabled, a user with the **Administrator** security group ([Functional administrators](../../administration/using/users-management.md#functional-administrators)?) can duplicate an event configuration if it has been published.

=> Is the FEATUREFLAG_MC_DUPLICATE_EVENT feature flag enabled for all customers or is it only on demand? If so, what's the process to request enablement? Shall we mention this process in core documentation and/or Release Notes?

If the feature flag FEATUREFLAT_MC_NONADMINACCESS is also turned on, non-administrator users with the **MC user** role can also access event configurations, but their permission is determined by the **Organizational unit** of the current user and the **Organizational unit** of the event configuration's creator.
If the user's **Organizational unit** and the creator's **Organizational unit** are in the same **Organizational unit** hierarchy, duplication is allowed.

For example:
* If an event configuration is created by a user whose **Organizational unit** is 'France Sales', another user whose **Organizational unit** is 'Paris Sales' will be able to duplicate the event configuration as 'Paris Sales' is part of the 'France Sales' **Organizational unit**.
* However, a user whose **Organizational unit** is 'San Francisco Sales' will not be able to do so as 'San Francisco Sales' is under the 'US Sales' **Organizational unit**, which is separate from the 'France Sales' **Organizational unit**.

=> Is the FEATUREFLAT_MC_NONADMINACCESS feature flag enabled for Microsoft only? Can it be enabled for other customers on demand? If so, what's the process to request enablement? Shall we mention this process in core documentation and/or Release Notes?