---
title: Creating the direct mail
seo-title: Creating the direct mail
description: Creating the direct mail
seo-description: Follow these steps to create a direct mail delivery in Adobe Campaign.
page-status-flag: never-activated
uuid: 07cd7b9e-8224-474e-9e24-c441245cf6dc
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/channels/using/creating-the-direct-mail
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: direct-mail
discoiquuid: 58ec0331-ce32-45aa-a6f4-08909a43f7ee
isreadyforlocalization: false
navTitle: Creating the direct mail
publishexternaldate: 2018-11-20
sha1: 4cdc271ec6e21188fd218b2c7097c91fd14b4a62
index: y
internal: n
snippet: y
---

# Creating the direct mail{#creating-the-direct-mail}

Creating the direct mail

Creating a direct mail delivery is very similar to creating a regular email. The following steps describe the configuration that is specific to this channel. Refer to [Creating an email](../../channels/using/creating-an-email.md) for more information on other options.

1. Create a new direct mail delivery. You can create one from the Adobe Campaign [home page](../../start/using/interface-description.md#home-page), in a [campaign](../../start/using/marketing-activities.md#creating-a-marketing-activity) or in a [marketing activity list](../../start/using/programs-and-campaigns.md#creating-a-campaign).

   >[!NOTE]
   >
   >You can also add a direct mail activity in a workflow. For more on this, refer to the [Workflows](../../automating/using/direct-mail-delivery.md) guide.

   ![](assets/direct_mail_1.png)

1. Choose either the out-of-the-box **Direct mail** template or one of your own templates. For more information on templates, refer to the [Managing templates](../../start/using/about-templates.md) section.

   ![](assets/direct_mail_2.png)

1. Enter the general properties of the delivery.

   ![](assets/direct_mail_3.png)

1. Define the audience you wish to include in the extraction file as well as the test and trap profiles. See [Defining the direct mail audience](../../channels/using/defining-the-direct-mail-audience.md). 

   ![](assets/direct_mail_4.png)

   >[!NOTE]
   >
   >The audience definition is very similar to defining a regular email audience. See [Creating audiences](../../audiences/using/creating-audiences.md).

1. Edit the content of your file: columns to include for each profile, file structure, header and footer. See [Defining the direct mail content](../../channels/using/defining-the-direct-mail-content.md).

   ![](assets/direct_mail_5.png)

1. Click on the **Schedule** section of the delivery dashboard to define the contact date. For direct mail, the contact date is mandatory. For more information, refer to [Scheduling the send](../../sending/using/about-scheduling-messages.md).

   ![](assets/direct_mail_8.png)

1. If you added test profiles (refer to [Adding test and trap profiles](../../channels/using/defining-the-direct-mail-audience.md#adding-test-and-trap-profiles)), you can test your delivery before preparing the final file. It allows you to create a sample file containing only the test profiles selected.

   Click on **Test** to generate the sample file. Click on **Summary**, in the top left corner, then select **Proofs**. On the left part of the screen, select the proof and click on **Download file**.

   >[!NOTE]
   >
   >The **Export** role is required to allow Adobe Campaign to export the file and make it available for download. Please contact your administrator.

   ![](assets/direct_mail_19.png)

1. Once you have defined your delivery content, audience and contact date, click on the **Prepare** button, on the delivery dashboard.

   ![](assets/direct_mail_16.png)

   Typology rules are applied. For example, all unspecified postal addresses are excluded from the target. This is why you need to make sure you have checked the **Address specified** box in your profiles' information (see [Recommendations](../../channels/using/about-direct-mail.md#recommendations)). If you have defined a **Maximum volume of message** in the direct mail properties or at the template level, it will also be applied here.

   ![](assets/direct_mail_25.png)

   >[!NOTE]
   >
   >You can set global cross-channel fatigue rules that will automatically exclude oversollicited profiles from campaigns. See [Fatigue rules](../../administration/using/fatigue-rules.md).

1. Click on **Explore file** to preview the first 100 lines of the file. 

   ![](assets/direct_mail_18.png)

   The complete file is accessible for local download in the left part of the screen. Downloading the file generates a log entry in the **Export audits** menu. For more information on export audits, refer to the [Auditing exports](../../administration/using/auditing-export-logs.md) section.

   >[!NOTE]
   >
   >The **Export** role is required to allow Adobe Campaign to export the file and make it available for download. Please contact your administrator.

   If you need to change the delivery content, you only have to click on the **Regenerate file** button to take the change into account. No need to go through the preparation again. 

   ![](assets/direct_mail_21.png)

1. To confirm that the file is final, click on **Confirm** in the delivery dashboard.

   ![](assets/direct_mail_20.png)

You are now ready to send the extraction file to your direct mail provider. For this, you have several options:

* Send it via a regular email, with the file attached
* Send it via Campaign: perform your direct mail within a campaign [workflow](../../automating/using/direct-mail-delivery.md) and add a **Transfer file** to send the file via FTP for example. See [Transfer file](../../automating/using/transfer-file.md).

The provider retrieves the list of erroneous addresses and sends this information to Adobe Campaign which automatically blacklists the erroneous addresses. See [Return to sender](../../channels/using/return-to-sender.md).
