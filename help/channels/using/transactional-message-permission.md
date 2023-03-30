---
title: Transactional messaging permission
description: Learn about permissions linked to transactional events.
audience: channels
content-type: reference
topic-tags: transactional-messaging
context-tags: 
feature: Transactional Messaging
role: User
level: Intermediate
---
# Transactional messaging permission {#transactional-message-permission}

Currently, in Adobe Campaign Standard, users without the Administrator security group cannot access, create, or publish events, causing issues for business users who need to configure and publish events but lack Administrator rights.

We have implemented the following improvements to transactional messaging access control:

* A new **[!UICONTROL Role]**, called **MC user**, has been added to allow non-administrator users to manage transactional events. The **MC user** role grants these users the ability to access, create, publish, and unpublish transactional events and messages.

* Child deliveries are now set to the **[!UICONTROL Organizational unit]** of the user who creates the message template, rather than being restricted to the **[!UICONTROL Organizational unit]** of the **Message Center agent (mcExec)** security group.

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
| Child Deliveries| Child deliveries are set to the **Organizational unit** of the **Message Center agent (mcExec)** security group.| Child deliveries will be set to the **Organizational unit** of the user creating the message template.|
|Message Template| Message Templates are set to the **Organizational unit** of the**Message Center agent (mcExec)** security group. | Message Templates will be set to the the **Organizational unit** of the user creating them.|
|Transactional Events| Only users within the **Administrator** security group can create and publish events. | The **MC user** role allows users to create and publish events.|
|Transactional Message Templates| Message templates are set to the Organizational unit **All**. | Message Template are set to the **Organizational unit** of the user creating them.|