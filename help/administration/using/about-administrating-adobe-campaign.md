---
title: Get started with Campaign Standard administration
description: Adobe Campaign provides you with a complete set of administration tools. Learn how to manage your users and configure your channels.
page-status-flag: never-activated
uuid: 64c34729-5c98-4db0-9131-af6dd0e78fb4
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: about-administrating-adobe-campaign
discoiquuid: 5587530a-2308-4be1-9f56-19eeb7a924d5

internal: n
snippet: y
---

# Get started with Campaign Standard administration {#about-administrating-adobe-campaign}

As a cloud-based solution, Adobe Campaign offers administrators different ways to configure the application. Though the infrastructure configuration is performed by Adobe, functional administrators can perform various configuration operations detailed below.

>[!NOTE]
>
>If you have questions or requests about implementation and configuration matters, contact your Adobe account executive.

<table>
<tr><td><img src="assets/do-not-localize/icon_menu.svg" width="60px"></td><td><img src="assets/do-not-localize/icon_users.svg"  width="60px"></td><td><img src="assets/do-not-localize/icon_channels.svg"  width="60px"></td><td><img src="assets/do-not-localize/icon_settings.svg" width="60px"></td></tr>
<tr><td><a href="#administration-menu">Administration menu</a></td><td><a href="#users-security">Users and security</a></td><td><a href="#channels-configuration">Channels configuration</a></td><td><a href="#application-settings">Application settings</a></td></tr>
</table>

## Administration menu {#administration-menu}

The different Adobe Campaign admin operations are carried out via the **[!UICONTROL Administration]** menu accessible when clicking the Adobe Campaign logo in the top left-hand corner. This part of the interface can only be accessed by functional administrators of the platform.

![](assets/admin_overview2.png)

The different menus available are:

* [Users & Security](../../administration/using/about-access-management.md): This menu allows you to manage access to the platform (users, roles, security groups, units). 
* [Channels](../../administration/using/about-channel-configuration.md): This menu regroups the technical parameters linked to the different platform channels (Email, SMS) as well as typology and quarantine management. 
* [Application settings](../../administration/using/external-accounts.md): This menu allows you to configure different application elements (external accounts, options, technical workflows).
* [Development](../../developing/using/data-model-concepts.md): This menu allows you to manage your custom resources and access diagnostic tools.
* [Instance settings](../../administration/using/branding.md): This menu is where you define your different brands and configure their settings (logo, manage tracking, URL domain to access the landing pages, etc.).
* [Deployment](../../automating/using/managing-packages.md): This menu regroups the package import and export options.
* [Customer metrics](../../audiences/using/active-profiles.md): Adobe Campaign provides a report that displays the number of active profiles. This report is only informative, it doesn't have a direct impact on billing. 
* [Privacy Tools](https://docs.campaign.adobe.com/doc/standard/getting_started/en/ACS_GDPR.html): This menu allows you to create GDPR access and delete requests and track their evolution.

## Users and security {#users-security}

Invite users to access the application and manage **security groups**, which are sets of users hsaring the same roles and rights within your organization. By default, Adobe Campaign offers a set of **roles** which allows you to define unitary authorizations assigned to users and user groups. Combined with **organizational units**, roles give users a filtered view of the interface and define their access to the different features.

Campaign standard also allows you to monitor security-related information:

* Retrieve information regarding data exports performed by users through the **[!UICONTROL Export audits]** screen.
* Leverage the **[!UICONTROL Licenses]** screen to monitor all the installed Campaign licenses within your organization, as well as different information such as the build number, release version and terms of agreement.

Read more:

* [Users management](administration/using/users-management.md)
* [Organizational units](administration/using/organizational-units.md)
* [List of roles](administration/using/list-of-roles.md)
* [Managing groups and users](administration/using/managing-groups-and-users.md)
* [Auditing export logs](administration/using/auditing-export-logs.md)
* [Licenses](administration/using/licenses.md)

## Channels configuration {#channels-configuration}

All communication channels in Adobe Campaign must be correctly configured to be able to effectively send messages.

The **[!UICONTROL Channel]**  menu allows you to manage the technical parameters linked to the different channels:

* Configure various email parameters: processing rules for bounce, quarantines, email properties and routing parameters, typoly rules...
* Define routing configurations and properties of the SMS channel, as well as SMS encoding and formats.
* Configure mobile applications in order to be able to send in-app messages and push bnotifications using Adobe Experience Platform SDKs.
* Configure transactional messaging by creating and setting up events.

Read more:

* [About channel configuration](administration/using/about-channel-configuration.md)
* [Configuring email channel](administration/using/configuring-email-channel.md)
* [Configuring SMS channel](administration/using/configuring-sms-channel.md)
* [Configuring a mobile application](administration/using/configuring-a-mobile-application.md)
* [Configuring transactional messaging](administration/using/configuring-transactional-messaging.md)

## Application settings {#application-settings}

Campaign Standard comes with different application elements that can be configured to match your needs.

* Set up external accounts, which are used to connect Adobe Campaign to external servers.
* Access Campaign Standard target mappings.
* Monitor your platform using technical workflows.
* Define one or several brands for your organization and link them to messages or landing pages.
* Configure the sending of real-time notifications within the application in case of important system activities.

Read more:

* [About Campaign Standard settings](administration/using/about-campaign-standard-settings.md)
* [External accounts](administration/using/external-accounts.md)
* [Target mappings in Campaign](administration/using/target-mappings-in-campaign.md)
* [Technical workflows](administration/using/technical-workflows.md)
* [Branding](administration/using/branding.md)
* [Sending internal notifications](administration/using/sending-internal-notifications.md)
