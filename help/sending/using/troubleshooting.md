---
title: Troubleshooting deliverability issues in Adobe Campaign Standard
description: Learn what to do when experiencing deliverability issues with Adobe Campaign Standard.
page-status-flag: never-activated
uuid: 286fceee-65a9-4cb9-b205-9ce5d024675c
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: sheduling-messages
discoiquuid: 9c7fd670-bba9-4f3c-8cb1-87397a1acd27
context-tags: delivery,schedule,back
internal: n
snippet: y
---

# Troubleshooting{#troubleshooting}

Are you experiencing a deliverability problem? You may find the solution here.

## Same error message for an ISP {#same-error-for-an-isp}

**Why do I always get the same error message for a particular ISP?**

If you always get the same error message for an ISP, your email or IP may have been detected as faulty by the ISP. Carry out the following recommendations:
* Check whether you receive a large percentage of failures linked to inexistent email addresses (**User unknown** failures).
* Update your subscription forms to detect any errors in the domain names entered (for example: gmaul.com or yaho.com).
* If you notice errors stating that your messages are declared as spam, or that your messages are constantly blocked, try excluding the recipients that have not opened or clicked in one of your messages in the last 12 months from the target.

If the problem persists, contact the commercial or deliverability services, or Adobe Campaign support.

## Blacklisting versus quarantine {#blacklisting-versus-quarantine}

* **What is the difference between a blacklisted email address and a quarantined email address?**

    * The status **[!UICONTROL Blacklisted]** is a result of a feedback loop (when a person reports a message as spam).

    * The status **[!UICONTROL Quarantined]** is a result of a soft or hard bounce. For more on this, see this [section](../../sending/using/understanding-quarantine-management.md#quarantine-vs-blacklisting).

* **What do the different quarantine error reasons mean?**

    Here are 10 possible reasons: not defined, user unknown, invalid domain, blacklisted address, refused, error ignored, unreachable, account disabled, mailbox full, not connected.
    
    For more on this, see [Understanding quarantine management](../../sending/using/understanding-quarantine-management.md).

## Unblacklisting {#unblacklisting}

* **One of my recipients was blacklisted by mistake. How do I unblacklist them so that I can start sending them messages again?**

    * Go to **[!UICONTROL Administration > Channels > Quarantines > Addresses]**.
    * In the details of the corresponding record, set the value of the **[!UICONTROL Status]** field to **[!UICONTROL Valid]**.
    * Save the record.

* **How can I find out whether one of my IPs is blacklisted? How do I unblacklist my IP(s)?**

    To check whether your IP address is blacklisted, you can use various web sites to verify it:
    * https://mxtoolbox.com/
    * https://whatismyipaddress.com/blacklist-check
    * https://www.blacklistalert.org/

    Generally, the result of the IP address check will return a list that contains details of the blacklist and also the name of the web site that blacklisted the IP address.

    By clicking the corresponding link, you can access the web site details.

    Then, you can request that your web site be delisted from the web site that blacklisted the IP address.

    >[!NOTE]
    >
    >The delisting process may vary depending on the web site. Some sites require you to create an account, while others just need you to provide the IP address.
