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

| Objects | Existing Behavior | Future Behavior |
|:-----: | :-----: | :----:|
|mc Child Deliveries| Child deliveries right now have orgUnit mcExec | Child deliveries will have the orgUnit of the user who have created the message template|
|mc Message Template| Message Template are made with org unit mcExec | Message Template will be made with the org unit of the user creating them|
|mcExec Campaign| mcExec Campaign right now have orgUnit mcExec | The Campaign's org unit will be changed to all so that all the child deliveries that are made can be put into this campaign.Now, all users will have access to see the reporting of the child deliveries albeit they will have read-only access to the deliveries themselves|
|Transactional Events| Only Administrator role users have access to create and publish events | The rights to create and publish events will be role based so any group can have the access|
|Transactional Message Template| Message Template are made with org and geo unit all | Message Template will be made with the org unit of the user creating them|

