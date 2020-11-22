---
solution: Campaign Standard
product: campaign
title: Starting a new platform with Adobe Campaign Standard
description: Learn how to set up a new platform while maintaining your domain and IP address reputation with Adobe Campaign Standard.
audience: sending
content-type: reference
topic-tags: sheduling-messages
context-tags: delivery,schedule,back
---

# Starting a new platform{#starting-new-platform}

Maintaining your domain and IP address reputation is essential. Here is some advice for setting up a new platform.

Starting to send emails on a new platform is a sensitive step because the platform does not have any history of use and no reputation (when the sending IPs have never been used for this purpose). ISPs are naturally suspicious of IP addresses that have never been used to send email and that suddenly start to send large volumes of email traffic. In effect, spammers generally use "unknown" IP addresses (addresses that have never been added to the denylist) to send the largest possible number of messages before detection.

You cannot expect to reach operational speed in terms of output at the very start of the production phase. Furthermore, you should not attempt to send messages at this rate as it might lead the ISPs to block the sending addresses and to severely compromise the rest of the start-up phase.

Starting a platform often happens when using a list of addresses for the first time and which may not be fully qualified. If you send to invalid addresses or to honeypot addresses this will contribute to diminishing the reputation of the platform.
* If you have a list of invalid addresses, it is in your best interests to import it into the quarantine table (**[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Quarantines]** > **[!UICONTROL Addresses]**) before sending for the first times. For more on this, see this [section](../../sending/using/understanding-quarantine-management.md#identifying-quarantined-addresses-for-the-entire-platform).
* If, all the same, you wish to requalify the invalid addresses, it is by far preferable to do this once the reputation of the platform is established and bit by bit in order to "dilute" the use of bad addresses over time.

To summarize the principles to be followed when starting up:
* **Configure a dedicated subdomain** to work with Campaign that is specific to email campaigns sent from Adobe.
* **Import invalid/inactive addresses into the quarantine table** (if you have this information).
* **Limit the delivery throughput** rate (technical setting: limiting the number of mtachilds).
* **Progressively increase the volumes sent**: do not target the whole database from the very start, but rather add an extra fraction of the list each time you send. This should enable you to increase the volume at each step while reducing the overall rate of invalid addresses.
* **Send messages regularly**: to a certain extent it is better to send small shots regularly rather than large campaigns sporadically.
* **Closely monitor the delivery reports**: high error indicators can mean a technical setting is badly configured.
