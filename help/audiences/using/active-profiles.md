---
solution: Campaign Standard
product: campaign
title: Campaign Active profiles
description: Learn how to access customer metrics and  active profiles
feature: Profiles
role: Business Practitioner
level: Intermediate
exl-id: 22516348-7695-4579-99eb-480e5b723ccc
---
# Customer metrics {#customer-metrics}

Campaign functional administrators can access the **[!UICONTROL Customer metrics]** report from **[!UICONTROL Administration > Customer metrics]**. 

![](assets/audience_active_profiles1.png)

Thie report displays:

* the Experience Cloud ID
* the IMS Organization ID
* the number of **active profiles** 
* the list of targeting dimensions available in the instance

This report is generated every month by the **[!UICONTROL Billing]** technical workflow. 

## Active profiles{#active-profiles}

According to your contract, each of your Campaign instances is provisioned with a specific number of active profiles. Please refer to your licence agreement for reference on number of purchased active profiles.

>[!NOTE]
>
>As an Admin user, you can also monitor the number of active profiles used on your instances directly from the Control Panel. For more on this, refer to the [Control Panel documentation](https://experienceleague.adobe.com/docs/control-panel/using/performance-monitoring/active-profiles-monitoring.html).
>

A “Profile” is a record of information representing an end-customer, prospect, or lead. Profiles are considered **active** if they have been targeted by a Campaign delivery within the past 12 months via any channel. The profiles that were excluded during delivery preparation (by typology rules or quarantine mechanism for example) are not taken into account. A profile that has been targeted by several deliveries will only be counted once. This report is only informative, it doesn't have a direct impact on billing. 

![](assets/audience_active_profiles2.png)

At the bottom of the report, you will find the list of active profiles for each targeting dimension. It shows the number of active profiles that were targeted during the last 12-month rolling period. 

* The **[!UICONTROL NmsRecipient]** source includes all profiles that were contacted using information from their Campaign Standard profile.

* The  customers **[!UICONTROL anonymous]** source shows the number of profiles that were targeted using a specific piece of information only (email address, phone number), with no relation to their Campaign profile.
