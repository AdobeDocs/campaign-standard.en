---
title: Creating profiles
seo-title: Creating profiles
description: Creating profiles
seo-description: Learn how to create profiles and collect data on your contacts, using APIs, import capabilities, online acquisition, automatic or manual updates.
page-status-flag: never-activated
uuid: a5f5a58a-e798-400f-8648-05dc843d5557
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: audiences
content-type: reference
topic-tags: managing-profiles
discoiquuid: 4ab8a984-f898-4fff-ad8c-ed8f95362f96
index: y
internal: n
snippet: y
---

# Creating profiles{#creating-profiles}

In Adobe Campaign, profiles are used by default to define the main target of messages.

To create or update a profile in Campaign, you can:

* Import a profile list from a file, via a [workflow](https://helpx.adobe.com/campaign/kt/acs/using/acs-importing-profiles-feature-video-using.html)
* Collect data online, via [landing pages](https://docs.campaign.adobe.com/doc/standard/getting_started/en/ACS_CreateLandingPage.html)
* Create bulk via [REST API](http://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html)
* Enter data using the graphical interface screens, as explained below

As an example, to create a new profile directly in the user interface, follow the steps below:

1. From the Adobe Campaign home page, click the **Customer Profiles** card or the **Profiles** tab to access the list of profiles.

   ![](assets/profile_creation_1.png)

1. Then click **[!UICONTROL Create]** .

   ![](assets/profile_creation.png)

1. Enter the profile data.

   ![](assets/profile_creation1.png)

    * The contact information, such as first name, last name, gender, date of birth, photo, preferred language (for [multilingual emails](../../channels/using/creating-a-multilingual-email.md)) helps better personalize deliveries.
    * The profile's **[!UICONTROL Time zone]** is used to send deliveries at the profile's time zone. For more on this, refer to this [section](../../sending/using/sending-messages-at-the-recipient-s-time-zone.md). 
    * The **[!UICONTROL Channels]** category, which contains the email address, mobile phone number, opt-out information, lets you know on which channel the profile is reachable.
    * The **[!UICONTROL No longer contact]** category is updated as soon as the profile unsubscribe to a channel.
    * The **[!UICONTROL Address]** category contains the postal address that needs to be filled along with the **[!UICONTROL Address specified]** option to send [direct mail](../../channels/using/about-direct-mail.md) to this profile. If the **[!UICONTROL Address specified]** option is not checked, this profile will be excluded from every direct mail delivery. 
    * The **[!UICONTROL Access authorization]** category indicates the profile's organizational units (to [manage permissions](../../administration/using/about-access-management.md)). See also [Partitioning profiles](../../administration/using/organizational-units.md#partitioning-profiles).
    * The **[!UICONTROL Traceability]** category automatically updates with information concerning the user who created or modified the profile.

1. Click **[!UICONTROL Create]** to save the profile.

The profile will now appear in the list.

>[!NOTE]
>
>Profiles creation is also possible using the Adobe Campaign Standard API. For more on this, refer to the [dedicated documentation](https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#creating-profiles) .

Profiles can also be partitioned depending on their organizational units. To add the organizational fields to your profiles, refer to the [Partitioning profiles](../../administration/using/organizational-units.md#partitioning-profiles) section.

>[!NOTE]
>
>The preferred language field is used to select the language when sending multilingual messages. For more information about the multilingual messages [refer to this page](../../channels/using/creating-a-multilingual-email.md).

**Related topics:**

* [Creating a landing page](https://docs.campaign.adobe.com/doc/standard/getting_started/en/ACS_CreateLandingPage.html) step-by-step guide
* [Importing profiles](https://helpx.adobe.com/campaign/kt/acs/using/acs-importing-profiles-feature-video-using.html)

