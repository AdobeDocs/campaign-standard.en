---
solution: Campaign Standard
product: campaign
title: Early Release Notes
description: Early Release Notes
feature: Overview
role: Business Practitioner
level: Beginner
hide: yes
hidefromtoc: yes
---
# Early release notes {#new-release}

This page describes new features, improvements and fixes included in the next Campaign Standard release.

>[!CAUTION]
>
> This content is subject to changes without prior notice until the stage environments upgrade date. Learn more in the [release planning page](../../rn/using/release-planning.md).
>

## Release 21.2 - June 2021 {#release-21-2---june-2021}

**Improvements**

* When designing a landing page, you can now add a mandatory checkbox that profiles are required to select before submitting the form. 

* For the Triggers integration, the error message displayed when there is no reconciliation data coming in the trigger payload has been improved: "Alias data missing from payload".

* Performance to retrieve push notifications from the queue has been improved.

**Other changes**

* The URL signature mechanism for tracking links has been disabled to prevent an issue that was causing some valid, signed tracking links to be incorrectly blocked after being modified by third-party security tools.

* In multi-variant deliveries, users can no longer create language copies if the default variant has been deleted. A message is now displayed during language copy creation. (CAMP-48235)

* The 2-step profile deletion process (deprecated starting Campaign 19.4 release) is now disabled by default. Previously it had to be manually disabled from the Campaign interface before using the Privacy Core Service. Not doing so would cause Delete requests to remain in pending state without completing.

* A new 'StringAgg' aggregate function has been introduced to concatenate the values of a string type column. (CAMP-47077)

* In Dynamic reports, the **Exclude Proof** segment has been removed. (CAMP-46161)

* A new warning message has been added to inform the user when an iOS certificate is uploaded without the platformPrincipal value in the Campaign application.

* The maximum size of an email is now set to 100 MB by default. This limit enables to prevent any error that could indefinitely increase the size of an email, which can lead to a system crash. (CAMP-47445)

* The Asset Core Service integration with the Email designer can now be used by Standard Users.  

* A new message has been added to confirm a successful migration from a v4 push application to a v5 push application.

**Patches**

* Fixed an issue which prevented the expiry option for the batch process log table (**xtkjoblog**) table from being applied. This prevented the table from being correctly purged.

* Fixed an issue which prevented you from changing the order of filters in a **Segmentation** workflow activity. (CAMP-48357)

* Fixed a regression from 20.4 that could lead to deliveries failing with a null value error. (CAMP-48591)

* Fixed an issue which prevented you from sending a report through the **Share** > **Send Report Now** or **Send Report on Schedule** menu. (CAMP-47798)

* Fixed a regression which could lead to incorrect open rates for Gmail due to the filtering of tracking events received from Gmail accounts. (CAMP-46504)

* Fixed various issues causing data discrepancy between reports in Adobe Campaign Standard and reports in Adobe Analytics. (CAMP-47671, CAMP-47296)

* Fixed an issue that prevented you from accessing the delivery logs after preparation had failed. (CAMP-48296)

* Fixed an issue which could display an error message when trying to edit, delete or send a custom report. (CAMP-47789, CAMP-47798)

* Fixed an issue causing the APIs calls to fail when creating a new custom resource and enabling the **Do not synchronize** option. (CAMP-48014)

* Fixed an issue where custom resources with the **Do not synchronize** option enabled could reference a schema that had been redrafted or deleted. This issue was causing an error when publishing the custom resources.

* Fixed an SMS opt-out issue when using multiple short codes on the same external account.

* Fixed an issue which prevented you from accessing a new delivery alerting criterion ("the resource you are trying to access is unreachable") after publishing the database. (CAMP-48221)

* Fixed an issue where tracking logs were missing in some instances. A new technical workflow has been added (**trackingLogRecovery**) to restore these lost tracking logs and should be used by Adobe internal only.

* Fixed an issue where no delivery data was displayed in Dynamic reports. Reports were set to 0. (CAMP-47480)

* Fixed an issue which prevented the Server JavaScript HTTP Client from connecting to external URL.

* Fixed an issue which reset an **Incremental query** activity after changing the internal name of the workflow. This occurred when a date field was used as incremental mode. (CAMP-47674)

* Fixed an issue which prevented the preview thumbnail from displaying in the delivery summary, when creating a multilingual email with the Adobe Experience Manager integration. This issue occurred when using the **Language copy creation** button to create the email variants. (CAMP-47810)

* Fixed an issue which prevented users from accessing the parent delivery from the Email or SMS child delivery. (CAMP-47986)

* Fixed an issue which could cause excess CPU and memory consumption when sending transactional messages via the REST API with a missing custom event. (CAMP-47147)

* Fixed an error with the Transactional Messaging API which sometimes prevented realtime messages from being sent.

* Fixed an issue where reports were not received after using the **Send report on schedule** option. (CAMP-48583)

* Fixed an issue where reports received after using the **Send report now option** were incomplete and missing data. (CAMP-48583)

* Fixed an issue with the **Send report on schedule** option in Dynamics report where the built-in **Instant Report Sharing** (reportSendingNow) workflow was failing to generate reports. (CAMP-47786)

* Fixed an issue with the Email Designer where an image's dimensions were narrowed down when uploading an image. (CAMP-47017)

* Fixed an issue which prevented every available Experience Manager template from being displayed when creating a delivery. (CAMP-48132)

* Fixed an error which prevented the Campaign link in the Summary page of a sent delivery from redirecting the users to the related campaign. (CAMP-48012)

* Fixed an issue in the Email Designer where the Asset Core Service integration kept failing when trying to select an asset. (CAMP-47446)

* Fixed an issue that blocked some Journey Orchestration deliveries due to Campaign not supporting timestamps with an exact value (i.e. ending with 00) sent by events from Journey Orchestration.

* The updateDeliveryIndicators technical workflow has been optimized. Delivery IDs which have the same broadlog/trackinglog schema are now grouped together. This limits the number of queries thus improving performance.
