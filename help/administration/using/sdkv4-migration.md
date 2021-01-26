---
solution: Campaign Standard
product: campaign
title: SDK v4 mobile application migration to Adobe Experience Platform SDK
description: This document allows you to migrate your mobile application from SDK v4 to Adobe Experience Platform SDK
audience: channels
content-type: reference
topic-tags: push-notifications
context-tags: mobileApp,overview
---

# How to migrate your mobile application from SDK v4 to Adobe Experience Platform SDK {#sdkv4-migration}

>[!IMPORTANT]
>
> The migration process is irreversible.
>
> Please read the document carefully before starting the migration of your mobile application SDK V4 to Adobe Experience Platform SDK.

## About the SDK V4 migration

Adobe Campaign Standard treats a mobile app using SDK V4 as a separate application from a mobile app using Adobe Experience Platform SDK.

Customers that upgrade the SDK version in their mobile applications do not consider their app a different app when they upgrade Adobe's SDK. Customers after the upgrading the Adobe SDK version (from v4 to Adobe Experience Platform/v5 ) in their mobile applications need to continue using their application subscriber data and campaigns as it. For this they need to migrate their v4 SDK application in Adobe Campaign Standard to Adobe Experience Platform SDK application.
This feature will enable them to do this by single click. The feature is migration of SDK v4 application to a fresh Adobe Experience Platform SDK application. Please do not consider it as the feature to merge any SDK v4 application with any Adobe Experience Platform SDK application.

| Things that will not change after migrating |
|:-:|
| There will no effect on the existing deliveries and campaigns using the application that is being migrated.  |
| The name of the mobile application will remain same. |
| The platform credentials for iOS and Android will be preserved.  |
| All the subscribers of the application and their data will be preserved. |
| The existing mobile application having v4 Adobe SDK will continue to send data (PII data/ subscriber & token information) to Adobe Campaign Standard and that data will continue to captured successfully at Adobe Campaign Standard.  |
| The **[!UICONTROL Organizational unit]** of the mobile application will remain same. |

| Things that will change after migrating  |
|:-:|
| The mobile application will be available in Administration > Channels > Mobile app (Adobe Experience Platform SDK). Before migration it was available in Administration > Channels > Mobile app (SDK v4).  |
| The 'Collect PII Endpoint' of the application will change. The older collect PII endpoint will continue to work and data sent to that will not loose. |
| The application will be tied to an Adobe Experience Platform Launch property and it will now be treated in manner similar to fresh application created in Adobe Experience Platform SDK.  |
|  The original Adobe Experience Platform SDK application used in migration will not exist as separate application. Only migrated SDK v4 application will be available. |

## Migrate your mobile application from SDK v4 to Adobe Experience Platform SDK {#how-to-migrate}

Before migrating

* The migration process is irreversible.
* It is advisable not to run migration of multiple application in parallel. Also make migration of same application is not triggered by multiple window at the same time.
* Before migration make sure that you have rights to **[!UICONTROL Organizational unit]** of application which you are migrating and the Adobe Experience Platform application which you are using for migration.
* The application will become a Adobe Experience Platform SDK application after migration and its changes will be linked to Launch Property.

1. Create a new mobile property in the Adobe Experience Platform Launch. For more information on this, refer to [Adobe Experience Platform Launch documentation](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property#create-a-mobile-property).
1. In Adobe Campaign Standard, from the advanced menu, select **[!UICONTROL Administration]** > **[!UICONTROL Application Settings]** > **[!UICONTROL Workflows]** and open the **[!UICONTROL syncWithLaunch]** workflow. Check if the workflow has ended without error.
1. After workflow completion, check if the mobile application is available in Adobe Campaign Standard and is in **[!UICONTROL Ready to Configure]** state.
1. Go to the v4 SDK application which you want to migrate.
1. Select the `Mobile application migration to Adobe Experience Platform SDK` tab.
1. From the list of available Adobe Experience Platform applications, select the application created in step 1-3.
1. Press the 'Migrate' button after selecting the Adobe Experience Platform SDK app from the list.
1. On pressing the 'Migrate' Button confirm dialog is shown. Press 'OK' on it.
The successful completion dialog is shown and press 'Go to Adobe Experience Platform SDK Channel list' button of the dialog.
On pressing 'Go to Adobe Experience Platform SDK channel list' Adobe Experience Platform SDK channel list page is opened where the migrated v4 app is visible in Ready To Configure state.
1. Open it and press save to complete the migration.

Additional good to have steps:

Both the old subscribers collected by v4 version of mobile application and the new subscribers collected by v5 version of mobile application will available under the single migrated application. There will no obvious way to distinguish between them. After migration customers may want to have some information to distinguish between the subscriber which are still on v4 version and which are using new version. For this they can implement a new custom field of type text in the 'Subscriptions to an application' as 'sdkversion' or 'appVersion' (any name of customer's choice). Configure the associated Launch property to send this custom field value in Collect Pii call. Change the mobile application implementation accordingly.

## FAQ {#faq}

### Q: On SDK v4 application 'Mobile application migration to Adobe Experience Platform SDK' tab is not visible? {#tab-not-visible}

A: From the advanced menu **[!UICONTROL Administration]** > **[!UICONTROL Application Settings]** > **[!UICONTROL Options]**, check the value of the **[!UICONTROL Enable migration of mobile app from SDK v4 to Adobe Experience Platform SDK option]** option. It should be set to 1 and enabled by default. Administrator may have disabled it manually.

![](assets/Adobe Experience Platform_v4_1.png)

### Q: 'No data' is shown on the opening the Adobe Experience Platform SDK mobile application list on 'Mobile application migration to Adobe Experience Platform SDK' tab? {#no-data}

A: Only eligible application of your **[!UICONTROL Organizational unit]** is shown in the list. Please make sure you have eligible Adobe Experience Platform application for merging. The **[!UICONTROL Property Status]** of your Adobe Experience Platform application should be set to **[!UICONTROL Ready to Configure]**  and the **[!UICONTROL Mobile app migration status]** set to **[!UICONTROL Not Migrated]**.

### Q: Why can't the Adobe Experience Platform SDK application with 'Configured' Property Status be used for migration? {#property-status}

A: Migration process retains the SDK v4 subscribers and attributes. It only keeps the Launch related information from Adobe Experience Platform SDK application and rest everything including subscribers and other data of Adobe Experience Platform SDK application is dropped. To avoid any data loss situation only Adobe Experience Platform SDK applications with the **[!UICONTROL Ready to Configure]** **[!UICONTROL Property Status]** are eligible for migration.

### Q. After migration is SDK v4 application is not visible? {#v4-app-not-visible}

A: The mobile application after migration will be visible in **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile app (Adobe Experience Platform SDK)]**.

### Q. After migration is Adobe Experience Platform SDK application is not visible? {#Adobe Experience Platform-not-visible}

A: The original Adobe Experience Platform SDK application used in migration will not exist as a separate application. Only migrated SDK v4 application will be available.

### Q. SDK v4 application is of Organizational unit A (child of Organizational unit ALL) and Adobe Experience Platform SDK is of Organizational unit ALL. How to do the merge? {#v4-org-unit}

A: Administrators of the **[!UICONTROL Organizational unit]** ALL will have rights to manage both mobile applications. They will be in charge of the migration.

### Q. SDK v4 application is of Organizational unit A and Adobe Experience Platform SDK application is of Organizational unit B (sibling of Organizational unit A). How to do the migration? {#Adobe Experience Platform-org-unit}

A: Adobe Experience Platform SDK application being the asset of sibling **[!UICONTROL Organizational unit]** will not be visible to the Administrator of **[!UICONTROL Organizational unit]** A. Though such migration option will be available to the Administrator of ALL but should not be attempted. Please migrate your mobile applications in a same **[!UICONTROL Organizational unit]** or with a parent tree path only.