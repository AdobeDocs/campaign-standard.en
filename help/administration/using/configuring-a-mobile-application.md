---
title: Configuring a mobile application
description: Discover how to configure Adobe Campaign to send push notifications or In-App messages using SDK V4 or Experience Platform SDK.
page-status-flag: never-activated
uuid: 63e1476a-7875-4f48-ba9e-97f1a0007e42
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: configuring-channels
discoiquuid: 2a14500f-5ede-4131-8b1a-b7fd65b7e3aa

internal: n
snippet: y
---

# Configuring a mobile application{#configuring-a-mobile-application}

## Configuring a mobile application using Adobe Experience Platform SDKs {#using-adobe-experience-platform-sdk}

>[!IMPORTANT]
>
>Push notification and In-App implementations have to be performed by expert users. If you need to be assisted, contact your Adobe Account executive or Professional services partner.

To send push notifications and In-App messages with Experience Platform SDK application, a mobile application has to be set up in Adobe Experience Platform Experience Platform Experience Platform Launch and configured in Adobe Campaign.

Once a mobile application is set up, you can retrieve the PII data it collected to create or update profiles from your database. For more on this, refer to this section: [Creating and updating profile information based on mobile application data](../../channels/using/updating-profile-with-mobile-app-data.md).

To learn more on the different mobile use cases supported in Adobe Campaign Standard by using the Adobe Experience Platform SDKs, refer to this [page](https://helpx.adobe.com/campaign/kb/configure-launch-rules-acs-use-cases.html).

To complete the configuration, complete the following steps:

1. In Adobe Campaign, ensure that you can access the following:
   * Push notification
   * In-App message
   * Adobe Places (Beta)

   If not, contact your account team.

1. Check that your user has the necessary permissions in Adobe Campaign Standard and Experience Platform Launch.
   * In Adobe Campaign Standard, ensure that the IMS user is part of the Standard User and Administrator Product Profiles. This step allows the user to log in to Adobe Campaign Standard, navigate to the Experience Platform SDK mobile app page, and view the mobile app properties that you created in Experience Platform Launch.

   * In Experience Platform Launch, ensure that your IMS user is part of a Experience Platform Launch product profile.
   This step allows the user to log in to Experience Platform Launch to create and view the properties. For more information about product profiles in Experience Platform Launch, see Create your product profile. In the product profile, there should be no permissions set on the company or the properties, but the user should be able to still log in.

   To complete additional tasks like installing an extension, publishing an app, configuring environments, and so on, you need to set permissions in the product profile.

1. In Experience Platform Launch, create a mobile property. For more information, see [Set up a mobile property](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property).

1. In Experience Platform Launch, click the Extensions tab, go to Catalog, and search for the Adobe Campaign Standard extension. For more information, see [Adobe Campaign Standard](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard).

1. To support location use cases in Campaign Standard, install the Places extension and the Places Monitor extension.
   * Install Places extension in Experience Platform Launch. Refer to this [page](https://docs.adobe.com/content/help/en/places/using/places-ext-aep-sdks/places-extension/places-extension.html).
   * Install the Places Monitor extension in Experience Platform Launch. Refer to this [page](https://docs.adobe.com/content/help/en/places/using/places-ext-aep-sdks/places-monitor-extension/using-places-monitor-extension.html)

1. In Adobe Campaign Standard, configure the mobile property that you created in Experience Platform Launch. Refer to this section.

1. Add the channel-specific configuration to your mobile application set up.
   For more information, see Channel-specific application configuration in Adobe Campaign.

1. If required, you can delete your Experience Platform Launch property.
   For more information, see Deleting your Experience Platform Launch application.

## Setting up your Adobe Experience Platform Launch application in Adobe Campaign {#set-up-Campaign}

To use an Experience Platform Launch mobile property in Campaign, you also need to configure this property in Adobe Campaign. In Adobe Campaign, ensure that the IMS user is part of the Standard User and Administrator Product Profiles.

For users with the syncWithLaunch technical workflow feature flag, you will need to wait for the technical workflow to run and sync the Launch mobile property to Adobe Campaign. You can then configure it in Adobe Campaign.

For more information on syncWithLaunch technical workflow feature flag, refer to this page.

>[!NOTE]
>
>By default, administrators with organizational unit set to ALL can edit the mobile application. 

1. From the advanced menu, select Administration > Channels > Mobile app (AEP SDK).

1. Select the mobile application that you created in Experience Platform Launch.
   Its Property Status should be Ready to configure.
   
   >[!NOTE]
   >
   >By default, to retrieve the list of mobile applications created in Adobe Launch, Campaign Standard uses the value defined in the NmsServer_URL option to look for matching properties.
   In some cases, the Campaign endpoint for a mobile application may be different from the one defined in NmsServer_URL. In that case, define the endpoint in the Launch_URL_Campaign option. Campaign will use the value from this option to look for matching properties in Adobe Launch..

1. You can change the organizational unit of your mobile application under the Access Authorization section to limit access to this mobile application to specific organization units. For more information, refer to this page.

   Here, the administrator can assign sub organizational units by selecting them from the drop-down. 

1. To make the connection between Campaign and Experience Platform Launch, click Save.

1. Verify that the status of the mobile app has changed from Ready to Configure to Configured.

When the Experience Platform Launch Campaign extension shows that the pkey has been set up successfully, you can also verify that the property has been set up successfully in Campaign.

1. For this configuration to take effect, the changes need to be published in Experience Platform Launch.

For more information, see Publish configuration.
