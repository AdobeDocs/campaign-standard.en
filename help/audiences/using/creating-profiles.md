---
title: Creating profiles
seo-title: Creating profiles
description: Creating profiles
seo-description: Learn how to create profiles and collect data on your contacts, using APIs, import capabilities, online acquisition, automatic or manual updates.
uuid: 37b4e739-a16d-46d5-8eb8-f9f17caabf3a
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/audiences/using/creating-profiles
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-10T07 22 21.245-0400
cq-lastreplicated: 2018-09-07T14 42 54.966-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: audiences
content-type: reference
topic-tags: managing-profiles
cq-template: /apps/help/templates/article-3
discoiquuid: 5904e102-b8f6-4829-8172-2a7afb222a22
firstPublishExternalDate: 2018-09-07T14:42:52.588-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 01 37.426-0400
jcr-createdby: admin
jcr-description: Creating profiles
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T14:42:52.588-0400
lochandoffdate: 2018-09-10T07 22 21.243-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Creating profiles
publishexternaldate: 2018-09-07T14 42 52.588-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/audiences/using/creating-profiles.html
sha1: c81cb50c21a69c8ea3d3f6e842b81bfc4da7b2bf
topicBrowsingSortDate: 2018-09-07T14:42:52.588-0400
index: y
internal: n
snippet: y
---

# Creating profiles{#creating-profiles}

Creating profiles

In Adobe Campaign, profiles are used by default to define the main target of messages.

To create or update a profile in Campaign, you can:

* Import a profile list from a file, via a [workflow](https://docs.campaign.adobe.com/doc/standard/en/Videos/importing_profiles.mp4)
* Collect data online, via [landing pages](https://docs.campaign.adobe.com/doc/standard/getting_started/en/ACS_CreateLandingPage.html)
* Create bulk via [REST API](http://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html)
* Enter data using the graphical interface screens, as explained below

As an example, to create a new profile directly in the user interface, follow the steps below:

1. From the Adobe Campaign home page, click the **Customer Profiles** card or the **Profiles** tab to access the list of profiles.

   ![](assets/profile_creation_1.png)

1. Then click **Create**.

   ![](assets/profile_creation.png)

1. Enter the profile data.

   ![](assets/profile_creation1.png)

    * The contact information, such as first name, last name, gender, date of birth, photo, preferred language (for [multilingual emails](../../channels/using/creating-a-multilingual-email.md)) helps better personalize deliveries.
    * The **Channels** category, which contains the email address, mobile phone number, opt-out information, lets you know on which channel the profile is reachable.
    * The **No longer contact** category is updated as soon as the profile unsubscribe to a channel.
    * The **Address** category contains the postal address that needs to be filled along with the **Address specified** option to send [direct mail](../../channels/using/about-direct-mail.md) to this profile. If the **Address specified **option is not checked, this profile will be excluded from every direct mail delivery.

      The profile's **Time zone** is used to send deliveries at the profile's time zone. For more on this, refer to this [section](../../sending/using/sending-messages-at-the-recipient-s-time-zone.md). 
    
    * The **Access authorization** category indicates the profile's geographical and organizational units (to [manage permissions](../../administration/using/about-access-management.md)). See also [Partitioning profiles](../../administration/using/organizational-and-geographical-units.md#partitioning-profiles).
    * The **Traceability** category automatically updates with information concerning the user who created or modified the profile.

1. Click **Create** to save the profile.

The profile will now appear in the list.

Profiles can also be partitioned depending on their organizational and geographical units. To add the organizational and geographical fields to your profiles, refer to the [Partitioning profiles](../../administration/using/organizational-and-geographical-units.md#partitioning-profiles) section.

>[!NOTE]
>
>The preferred language field is used to select the language when sending multilingual messages. For more information about the multilingual messages [refer to this page](../../channels/using/creating-a-multilingual-email.md).

**Related topics:**

* [Creating a landing page](https://docs.campaign.adobe.com/doc/standard/getting_started/en/ACS_CreateLandingPage.html) step-by-step guide
* [Importing profiles](https://docs.campaign.adobe.com/doc/standard/en/Videos/importing_profiles.mp4)
* [Adobe Campaign REST API Documentation](http://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html) (**Quick Starts** > **How to create a profile**)

