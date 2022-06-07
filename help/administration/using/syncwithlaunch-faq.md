---
title: Sync with Launch technical workflow FAQ
description: Common questions about Adobe Launch technical workflow
audience: administration
feature: Instance Settings
role: Admin
level: Experienced
exl-id: aaaceb3a-5e54-47da-9be4-b70747282830
---
# Tags in Adobe Experience Platform synchronization FAQ {#syncwithlaunch-faq}

You can import tag mobile properties into Adobe Campaign Standard through the **[!UICONTROL Sync with Launch]** dedicated technical workflow. For more information, refer to this [page](../../administration/using/technical-workflows.md)

The section below lists common questions about this synchronization.

## I created a tag property (non-admin of Org-unit ALL). My application is in Ready to Configure state in Adobe Campaign but I am unable to open/configure it. {#configuring-property}

Only administrator of organizational unit ALL can configure mobile applications in Adobe Campaign Standard. Once configured, only users of the assigned organizational unit can edit the 
application. For more information on organizational unit, refer to this [page](../../administration/using/organizational-units.md).

## I am unable to edit a configured mobile application in Adobe Campaign Standard and mobile applications are in Read-mode only. {#read-mode-mobile-app}

Check the organizational unit of the mobile application in the **[!UICONTROL Access Authorization]** section. Only users of the assigned organizational unit can edit the mobile application.

For more information on organizational unit, refer to this [page](../../administration/using/organizational-units.md).

## I am an administrator with organization unit ALL in Adobe Campaign Standard but I cannot configure mobile application. {#org-unit-mobile}

An administrator with organization unit set to ALL should have rights to all tag mobile properties to configure the mobile application.

For more information on organizational unit, refer to this [page](../../administration/using/organizational-units.md).

## I created a tag mobile property but my property is not visible in Adobe Campaign Standard. {#visibility-mobile-property}

1. Check that the Adobe Campaign Standard extension is installed in mobile property in the Data Collection UI.

1. Verify that the endpoints of instance are correctly configured in the extension.

1. Check that 'Launch_URL_Campaign' or 'NmsServer_URL' are correct.

1. Then, check that the sync is completed with the **[!UICONTROL syncWithLaunch]** technical workflow.

## How to check if the sync between Adobe Campaign and Tags in Adobe Experience Platform has been completed? {#sync-campaign-launch}

1. In Adobe Campaign Standard, from the advanced menu, select **[!UICONTROL Administration]** > **[!UICONTROL Application Settings]** > **[!UICONTROL Workflows]**. 

1. Open the **[!UICONTROL syncWithLaunch]** workflow.

1. Check if the workflow has ended without error.

1. Check in the logs that the workflow sync is enabled and successfully completed.

## I reset the pkey for a configured tag mobile application. How to reconfigure the pkey again in Data Collection UI? {#configuring-pkey}

1. Open the mobile property in the Data Collection UI.

1. Set a new URL in the Adobe Campaign Standard extension for which the PKey was reset.

1. Save it and let the workflow sync.

1. After sync is completed, open the mobile property in in the Data Collection UI.

1. Set the correct URL in the Adobe Campaign Standard extension for which PKey was reset.

1. Save it and let the workflow sync run again.

1. Only then the property will appear in **[!UICONTROL Ready to Configure]** state in Adobe Campaign and can now be configured.

## I want to configure a mobile property in Adobe Campaign. Will I have to wait for the technical workflow to sync between Tags in Adobe Experience Platform and Adobe Campaign?

You can do immediate execution of the workflow:

1. In Adobe Campaign Standard, from the advanced menu, select **[!UICONTROL Administration]** > **[!UICONTROL Application Settings]** > **[!UICONTROL Workflows]**. 

1. Open the **[!UICONTROL syncWithLaunch]** workflow.

1. Click on the **[!UICONTROL Scheduler]** activity and select **[!UICONTROL Immediate execution]**.
