---
title: Early Release Notes
description: Early Release Notes
feature: Overview
role: User
level: Beginner
hide: yes
hidefromtoc: yes
exl-id: 4b10eb63-3fea-438e-a1a7-25fbf7b0e5b0
---
# Early release notes {#new-release}

This page describes new features, improvements and fixes included in the next Campaign Standard release.

>[!CAUTION]
>
> This content is subject to changes without prior notice until the stage environments upgrade date. Learn more in the [release planning page](../../rn/using/release-planning.md).
>

## Release 22.2 - June 2022 {#rn-2022}

**Improvement**

* **Adobe Notification Service** - Campaign comes with Adobe Notification Service that allows Experience Cloud solutions to alert users across Experience Cloud on activities that are important for them to know. Starting 22.2 version, the user experience has been improved: notifications are prioritized and product-generated notifications are separated from Adobe status announcements. In addition, when the notification refers to a specific workflow, you can now access the corresponding workflow directly from the email or in-product notification.  For more on Adobe Campaign notifications, refer to [Adobe Campaign notifications](../../administration/using/sending-internal-notifications.md).

* **Optimization in Workflow startup** - Adobe has added a new capability which can tune the number of workflows that start around the same time. This would help prevent CPU spikes that could have led to service interruptions or downtime. Adobe would enable it after 22.2 release. There is no further action item on customer regarding the same.

**Security upgrade**

* Apache Tomcat has been upgraded from version 7 to version 8.5.

**Patches**

* Fixed an issue on the Billing technical workflow due to a duplicate key error. (CAMP-51029)
* Added the missing Microsoft Edge browser category in tracking Reports. They were previously categorized with Microsoft Chrome opens. (CAMP-51165)
* Fixed an issue with GDPR requests which were not deleting data from child tables. (CAMP-48276)
* Fixed an issue in the Email Designer which caused the visibility condition of a fragment not to be saved, in a transactional message template. (CAMP-50338)
* Fixed an issue in Campaign Reports which caused the date range not to be taken into account. (CAMP-50991)
* Fixed an error which caused scheduled emails to fail: the delivery analysis could not start as the delivery was still in the 'Retry pending' status. (CAMP-50302)
* Fixed an issue in the Email Designer when previewing an email with a profile substitution. (CAMP-49312)
* Fixed an issue with empty value in custom enumerations: when creating a custom resource with a field which is a text enumeration and contains only one value, this value is set now by default, so that you can create a query on this field as a simple request. (CAMP-50606)
