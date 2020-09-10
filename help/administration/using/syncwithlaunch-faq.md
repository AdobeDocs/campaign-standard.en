---
title: Sync with Launch technical workflow FAQ
description: Common questions about Launch technical workflow.
page-status-flag: never-activated
uuid: 4f538452-cc67-4e03-9e2f-2d9eecc081c7
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: users-and-security
discoiquuid: 54028f63-c9ca-4397-a079-e27e0cfdebf6
internal: n
snippet: y
---

# Adobe Launch Synchronization FAQ {#syncwithlaunch-faq}

You can import Adobe Launch mobile properties into Adobe Campaign Standard through the **[!UICONTROL Sync with Launch]** dedicated technical workflow. For more information, refer to this [page](../../administration/using/technical-workflows.md)

The section below lists common questions about this synchronization.

>[!NOTE]
>
>You will need to submit a ticket to Adobe Customer Care (either directly or through your Adobe contact) to have the **[!UICONTROL syncWithLaunch]** technical workflow enabled in your Campaign instance.

## I created a property in [!DNL Launch] (non-admin of Org-unit ALL). My application is in Ready to Configure state in Adobe Campaign but I am unable to open/configure it. {#configuring-property}

Only administrator of organizational unit ALL can configure mobile applications in Adobe Campaign Standard. Once configured, only users of the assigned organizational unit can edit the 
application. For more information on organizational unit, refer to this [page](../../administration/using/organizational-units.md).

## I am unable to edit a configured mobile application in Adobe Campaign Standard and mobile applications are in Read-mode only. {#read-mode-mobile-app}

Check the organizational unit of the mobile application in the **[!UICONTROL Access Authorization ]** section. Only users of the assigned organizational unit can edit the mobile application.

For more information on organizational unit, refer to this [page](../../administration/using/organizational-units.md).

## I am an administrator with organization unit ALL in Adobe Campaign Standard but I cannot configure mobile application. {#org-unit-mobile}

An administrator with organization unit set to ALL should have rights to all mobile properties in [!DNL Launch] to configure the mobile application.

For more information on organizational unit, refer to this [page](../../administration/using/organizational-units.md).

## I created a mobile property in [!DNL Launch] but my property is not visible in Adobe Campaign Standard. {#visibility-mobile-property}

1. Check that the Adobe Campaign Standard extension is installed in mobile property in [!DNL Launch].

1. Verify that the endpoints of instance are correctly configured in the extension.

1. Check that 'Launch_URL_Campaign' or 'NmsServer_URL' are correct.

1. Then, check that the sync between [!DNL Launch] and Adobe Campaign is completed with the **[!UICONTROL syncWithLaunch]** technical workflow.

## How to check if the sync between Adobe Campaign and Launch has been completed? {#sync-campaign-launch}

1. In Adobe Campaign Standard, from the advanced menu, select **[!UICONTROL Administration]** > **[!UICONTROL Application Settings]** > **[!UICONTROL Workflows]**. 

1. Open the **[!UICONTROL syncWithLaunch]** workflow.

1. Check if the workflow has ended without error.

1. Check in the logs that the workflow sync is enabled and successfully completed.

## I reset the pkey for a configured mobile application in Launch. How to reconfigure the pkey again in Launch? {#configuring-pkey}

1. Open the mobile property in Adobe Launch.

1. Set a new URL in the Adobe Campaign Standard extension for which the PKey was reset.

1. Save it and let the workflow sync between Adobe Campaign and [!DNL Launch].

1. After sync is completed, open the mobile property in [!DNL Launch].

1. Set the correct URL in the Adobe Campaign Standard extension for which PKey was reset.

1. Save it and let the workflow sync run again.

1. Only then the property will appear in **[!UICONTROL Ready to Configure]** state in Adobe Campaign and can now be configured.

## I want to configure a mobile property in Adobe Campaign. Will I have to wait for the technical workflow to sync between Adobe Launch and Adobe Campaign?

You can do immediate execution of the workflow:

1. In Adobe Campaign Standard, from the advanced menu, select **[!UICONTROL Administration]** > **[!UICONTROL Application Settings]** > **[!UICONTROL Workflows]**. 

1. Open the **[!UICONTROL syncWithLaunch]** workflow.

1. Click on the **[!UICONTROL Scheduler]** activity and select **[!UICONTROL Immediate execution]**.
