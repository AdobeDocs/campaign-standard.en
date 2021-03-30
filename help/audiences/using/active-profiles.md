---
solution: Campaign Standard
product: campaign
title: Active profiles
description: You can access a dedicated report on customer metrics and visualize active profiles in your Campaign database.
audience: audiences
content-type: reference
topic-tags: managing-profiles

feature: Profiles
role: Business Practitioner
level: Intermediate
---

# Active profiles{#active-profiles}

Adobe Campaign provides a report that displays the number of active profiles. This report is only informative, it doesn't have a direct impact on billing. Only administrators can access this report, under **[!UICONTROL Administration > Customer metrics]**.

![](assets/audience_active_profiles1.png)

>[!NOTE]
>
>If you are using Campaign Standard from build 10368, you can also monitor the number of active profiles used on your instances directly from the Control Panel. For more on this, refer to the [Control Panel documentation](https://docs.adobe.com/content/help/en/control-panel/using/performance-monitoring/active-profiles-monitoring.html).
>
>Note that Active profiles metric is available and relevant for **Marketing instances** only. It is not neither applicable nor available for Execution instances, meaning MID (mid sourcing) and RT (Message Center / Real-time messaging) instances.

The profiles that were excluded during delivery preparation (typology rules, quarantines, control groups) are not taken into account. A profile that has been targeted by several deliveries will only be counted once. At the bottom of the report, you will find the list of active profiles for each targeting dimension.

This report is generated every month by the **[!UICONTROL Billing]** technical workflow. It contains the number of active profiles that were targeted during the last 12-month rolling period.

Note that the profiles that were excluded during delivery preparation (typology rules, quarantines) are not taken into account. Moreover, a profile that has been targeted by several deliveries will only be counted once.

![](assets/audience_active_profiles2.png)

At the bottom of the report, you will find the list of active profiles processed by the billing workflow:

* The **[!UICONTROL NmsRecipient]** source includes all customers that were contacted using information from their Campaign Standard profile.

* On the other hand, customers that were targeted using a specific piece of information only (email address, phone number), with no relation to their Campaign profile, will come under the **[!UICONTROL anonymous]** source.
