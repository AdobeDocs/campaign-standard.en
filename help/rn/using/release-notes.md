---
title: Latest Release
description: This page details content of the latest Campaign Standard release
feature: Overview
role: User
level: Beginner
exl-id: e1f55a9b-be51-4f57-8719-fed7efc89113
---

# Latest Release{#latest-release}

![Control Panel](assets/do-not-localize/cp-icon.png) **New Control Panel release**. [Learn more](https://experienceleague.adobe.com/docs/control-panel/using/release-notes.html){target="_blank"}.


## Release 22.2 - June 2022 {#june-2022}

**Improvements**

* **Adobe Notification Service** - Campaign comes with Adobe Notification Service that allows Experience Cloud solutions to alert users across Experience Cloud on activities that are important for them to know. Starting 22.2 version, the user experience has been improved: notifications are prioritized and product-generated notifications are separated from Adobe status announcements. In addition, when the notification refers to a specific workflow, you can now access the corresponding workflow directly from the email or in-product notification.  For more on Adobe Campaign notifications, refer to [Adobe Campaign notifications](../../administration/using/sending-internal-notifications.md).

* **Optimization in Workflow startup** - Adobe has added a new capability which can tune the number of workflows that start around the same time. This would help prevent CPU spikes that could have led to service interruptions or downtime. Adobe would enable it after 22.2 release. There is no further action item on customer regarding the same.

* **Accessibility** - Adobe has made many accessibility fixes for improving the application’s overall ease of use. These features are currently enabled for a set of early adopters only, and they will be rolled out to all customers in the ACS 22.3 release. Examples of accessibility improvements include:

    * Ensuring that there is a visible focus indicator for focusable elements on each screen
    * Creating page landmarks for easier navigation
    * Adding the name, role, value, and state for many controls
    * Correcting issues encountered with dynamic focus order on main screens


**Patches**

* Fixed an issue on the Billing technical workflow due to a duplicate key error. (CAMP-51029)
* Added the missing Microsoft Edge browser category in tracking Reports. They were previously categorized with Microsoft Chrome opens. (CAMP-51165)
* Fixed an issue with GDPR requests which were not deleting data from child tables. (CAMP-48276)
* Fixed an issue in the Email Designer which caused the visibility condition of a fragment not to be saved, in a transactional message template. (CAMP-50338)
* Fixed an issue in Campaign Reports which caused the date range not to be taken into account. (CAMP-50991)
* Fixed an error which caused scheduled emails to fail: the delivery analysis could not start as the delivery was still in the 'Retry pending' status. (CAMP-50302)
* Fixed an issue in the Email Designer when previewing an email with a profile substitution. (CAMP-49312)
* Fixed an issue with empty value in custom enumerations: when creating a custom resource with a field which is a text enumeration and contains only one value, this value is set now by default, so that you can create a query on this field as a simple request. (CAMP-50606)

