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

Currently, users without administrative privileges in Adobe Campaign Standard cannot access, create, or publish events, which is causing issues for business users who need to configure and publish events but lack admin rights. To address this, a new role will be created in Adobe Campaign Standard  that allows non-admin users to handle transactional events. This new role will give standard users the ability to access, create, and publish events, and also allow them to unpublish existing events and messages, bringing them on par with admin users.

The table provided below outlines the impact of this feature on access control:

| Objects | Existing Behavior | Future Behavior |
|:-----: | :-----: | :----:|
| Child Deliveries| Child deliveries right now have the Organizational unit of the Message Center agent security group.| Child deliveries will have the Organizational unit of the user who have created the message template|
|Message Template| Message Template are set with the Organizational unit of the Message Center agents. | Message Template will be made with the the Organizational unit of the user creating them.|
|Campaign| Campaign right now have the Message Center agents.| The Campaign's org unit will be changed to all so that all the child deliveries that are made can be put into this campaign. Now, all users will have access to see the reporting of the child deliveries albeit they will have read-only access to the deliveries themselves|
|Transactional Events| Only Administrator role users have access to create and publish events | The rights to create and publish events will be role based so any group can have the access|
|Transactional Message Template| Message Template are made with org and geo unit all | Message Template will be made with the org unit of the user creating them|

