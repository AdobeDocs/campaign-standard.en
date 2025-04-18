---
title: Data retention
description: Learn about the default retention values for standard tables
audience: administration
feature: Instance Settings
role: Admin
level: Experienced
exl-id: 01cfa2a0-4ff5-4520-a515-11676de82528
---
# Data retention{#data-retention} 

>[!NOTE]
>
>Data reporting is available for the last three years only. For more information about data retention periods, please contact Adobe consultants or your technical administrators.

Standard log tables in Campaign have pre-set retention periods on them limiting their data storage duration, to avoid overloading your system.

Data retention configuration is set by Adobe technical administrators during implementation and values may vary for each implementation, based on customer requirements.

Reach out to the Adobe consultants or technical administrators to learn more about retention periods which apply to your environment, or to set custom retention periods.

Note that using standard workflow functionality, it is possible to set up retention periods for any custom table.

Below are the default retention periods for standard tables. Whenever possible, and depending on your data usage, Adobe suggests you to move to the recommended retention periods to improve performances of your Campaign instance.

* **Consolidated tracking**: 6 months (recommended: 1 month)
* **Delivery logs**: 6 months (recommended: 1 month)
* **Tracking logs**: 6 months (recommended: 1 month)
* **Events**: 1 month
* **Statistics of event processing**: 6 months (recommended: 1 month)
* **Archived events**: 6 months (recommended: 1 month)
* **Temporary entities**: 7 days
* **Ignored pipeline events**: 1 month
* **Delivery alerts**: 1 month
* **Export audit**: 6 months (recommended: 1 month)
* **Deliveries**: 2 years

## Retention period for deliveries {#deliveries}

<!-- By default, the retention period for deliveries is unlimited.-->

Effective June 1st, 2025, only deliveries from the past two years will remain available in the system. You will find more details below:

* Any deliveries older than two years will be permanently removed and no longer accessible.
* This cleanup includes only sent and failed deliveries; recurring deliveries, draft deliveries and templates will not be affected.
* Once a delivery is removed, any linked tracking or sending information will also be permanently deleted.
* Marketing or transactional delivery templates will not be deleted.
* For recurring deliveries, child deliveries with aggregation period set as month or year will not be deleted.

In case you are looking to speed up processes such as the **[!UICONTROL Copy headers from delivery templates]** workflow, the delivery retention period can be decreased. To do so, please reach out to your Adobe representative.

<!--

However, if there is a high volume of deliveries on your instance, you can update the **NmsCleanup_DeliveryPurgeDelay** option available from the **[!UICONTROL Administration]** > **[!UICONTROL Application settings]** menu.

Each time the **[!UICONTROL Database cleanup]** workflow is run, the deliveries meeting the conditions set for this option will be deleted.

-->

<!--

When updating the **NmsCleanup_DeliveryPurgeDelay** option, it is recommended to proceed gradually with multiple iterations. For example, you can start by setting the value to 300 days, then 180 days, then 120 days, and so on - making sure iterations are at least 2 days apart. Otherwise, the **[!UICONTROL Database cleanup]** workflow may take much longer because of a large number of deliveries to delete.

This action can help speeding up processes such as the **[!UICONTROL Copy headers from delivery templates]** workflow. Learn more on technical workflows in [this section](technical-workflows.md).

The default value for the **NmsCleanup_DeliveryPurgeDelay** option is `-1`. In this case, no delivery is deleted.

For example, if you set it to `180`, any non-template deliveries that have not been updated in the last 180 days will be deleted when the **[!UICONTROL Database cleanup]** workflow is run.

-->


