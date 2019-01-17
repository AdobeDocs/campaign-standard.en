---
title: Active profiles
seo-title: Active profiles
description: Active profiles
seo-description: You can access a dedicated report on customer metrics and visualize active profiles in your Campaign database.
uuid: 6118df31-4aba-4224-864c-273cdda8bd29
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: audiences
content-type: reference
topic-tags: managing-profiles
discoiquuid: 2d65711c-71a6-4a75-b2f0-937965fe121e
isreadyforlocalization: false
index: y
internal: n
snippet: y
---

# Active profiles{#active-profiles}

Active profiles

Adobe Campaign provides a report that displays the number of active profiles. This report is only informative, it doesn't have a direct impact on billing. Only administrators can access this report, under **[!UICONTROL Administration > Customer metrics]** . 

![](assets/audience_active_profiles1.png)

The **[!UICONTROL Billing]** technical workflow generates every month a report containing the number of active profiles that were targeted during the last 12-month rolling period.

The profiles that were excluded during delivery preparation (typology rules, quarantines) are not taken into account. A profile that has been targeted by several deliveries will only be counted once. At the bottom of the report, you will find the list of active profiles for each targeting dimension.

![](assets/audience_active_profiles2.png)

