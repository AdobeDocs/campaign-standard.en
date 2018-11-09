---
title: Creating an email
seo-title: Creating an email
description: Creating an email
seo-description: Follow these steps to create a single-send email in Adobe Campaign.
uuid: 547b56bf-da32-4169-9e7e-345df7bae087
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/channels/using/creating-an-email
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-08T08 23 03.413-0400
cq-lastreplicated: 2018-09-07T15 11 38.705-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: email-messages
cq-template: /apps/help/templates/article-3
discoiquuid: d589f0c6-e6c4-4402-bece-1097cc2da2db
firstPublishExternalDate: 2018-09-07T15:11:38.457-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 01 08.365-0400
jcr-createdby: admin
jcr-description: Creating an email
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T15:11:38.457-0400
lochandoffdate: 2018-09-08T08 23 03.413-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Creating an email
publishexternaldate: 2018-09-07T15 11 38.457-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/channels/using/creating-an-email.html
sha1: 2af7841f7b53e8cb78930b42bb8c61aacb722b01
topicBrowsingSortDate: 2018-09-07T15:11:38.457-0400
index: y
internal: n
snippet: y
---

# Creating an email{#creating-an-email}

Creating an email

You can create an email from a [campaign](../../start/using/marketing-activities.md#creating-a-marketing-activity), from the Adobe Campaign [home page](../../start/using/interface-description.md#home-page), or in the [marketing activity list](../../start/using/programs-and-campaigns.md#creating-a-campaign). You can also create single-send and recurring emails from a workflow.

1. Once you have started creating an email marketing activity, select the template you would like to use.

   By default, you can choose from several templates for each marketing activity. This allows you to pre-configure certain parameters according to your needs and also assign a brand to your delivery, see the [Managing templates](../../start/using/about-templates.md) section. 

   ![](assets/email_creation_1.png)

   >[!NOTE]
   >
   >Follow-up and A/B test templates are hidden by default. Check the boxes on the left side (**Filter** lateral panel) if you want to display them.

1. Enter the email's general properties. You can enter a name in the **Label** field and edit the ID. Both the activity name and its ID appear in the interface, but they are not visible to the message recipients.

   You can add a description that the user can see in the campaign content.

   ![](assets/email_creation_2.png)

   >[!NOTE]
   >
   >You can create your email within a parent campaign from the home page or the list of marketing activities. Select it from the campaigns that have already been created.

1. Define the target of your message based on your business criteria, see the [Managing profiles](../../audiences/using/about-profiles.md) section. You also define the test profiles who will validate the message, see the [Managing test profiles](../../sending/using/managing-test-profiles-and-sending-proofs.md#managing-test-profiles) section.

   ![](assets/email_creation_3.png)

1. Define and personalize the message content, sender name and subject. Then preview your message.

   At this stage in the creation wizard, you can choose to use the default editor or to try the Creative Designer for email ("Beta"). To be able to try the [Creative Designer](../../designing/using/about-email-content-design.md#using-the-creative-designer), you need to read and accept the terms and conditions displayed when choosing this option.

   You can design your message directly using a pre-defined content template or by using DreamWeaver or Adobe Experience Manager. If you don't feel like a designer, you can also upload a content that has been prepared for you, or import an existing content from a URL. See the [Loading an existing content](../../designing/using/selecting-an-existing-content.md) section.

   ![](assets/email_creation_4.png)

1. Confirm creating the email. The email dashboard is then displayed, see [Approving messages](../../sending/using/preparing-the-send.md) section.

   ![](assets/delivery_dashboard_2.png)

1. Schedule the sending, see the [Scheduling messages](../../sending/using/about-scheduling-messages.md) guide.

   ![](assets/delivery_planning.png)

1. Prepare your message to analyze its target, see the [Preparing the send](../../sending/using/confirming-the-send.md) section.

   ![](assets/preparing_delivery_2.png)

   >[!NOTE]
   >
   >You can set global cross-channel fatigue rules that will automatically exclude oversollicited profiles from campaigns. See [Fatigue rules](../../administration/using/fatigue-rules.md).

1. Send proofs to check and validate your message and monitor its inbox rendering, see the [Sending proof](../../sending/using/managing-test-profiles-and-sending-proofs.md#sending-proofs) section.

   ![](assets/bat_select.png)

1. Send the message and check its delivery through the message dashboard and logs, see the [Sending messages](../../sending/using/confirming-the-send.md) section.

   ![](assets/confirm_delivery.png)

1. Measure the impact of your message with delivery reports. For more on reporting, refer to [this section](../../reporting/using/about-dynamic-reports.md).

**Related topics**:

* [Creating an email](https://docs.campaign.adobe.com/doc/standard/en/Videos/email_creation.mp4) video
* [Adobe Campaign and Dreamweaver integration](https://docs.campaign.adobe.com/doc/standard/en/Videos/ACS_Dreamweaver.mp4) video
* [Using Adobe Experience Manager](../../integrating/using/integrating-with-experience-manager.md)
* [Integrating Adobe Target](../../integrating/using/configuring-the-campaign-target-integration.md)

