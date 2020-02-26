---
title: Creating an email content in Adobe Experience Manager.
description: With the Adobe Experience Manager integration, you can create content directly in AEM and use it later on in Adobe Campaign.
page-status-flag: never-activated
uuid: ed6c1b76-87f7-4d23-b5e2-0765297a905c
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-experience-manager
discoiquuid: 6c0c3c5b-b596-459e-87dd-a06bb7d633d2

internal: n
snippet: y
---

# Importing an Adobe Experience Manager content into an Adobe Campaign email {#creating-email-aem}

Using this document, you will learn how to create and manage email contents in Adobe Experience Manager, then use them for your marketing campaigns by importing them in your emails into Adobe Campaign Standard.

The prerequisites are:

* Access to an AEM instance configured for the integration.
* Access to an Adobe Campaign instance configured for the integration.
* An Adobe Campaign email template configured to receive AEM content.

## Accessing email contents in Adobe Experience Manager {#email-content-aem}

>[!VIDEO](https://images-tv.adobe.com/mpcv3/2674d459-d57b-413b-9d34-9fd941666023_1575035768.854x480at800_h264.mp4)

## Creating new email content in Adobe Experience Manager {#creating-email-aem}

### Content templates and properties {#templates-properties}

Several templates specific to Adobe Campaign are available. You must use one of these templates as they contain predefined components supported by Adobe Campaign.

By default, two predefined templates allow you to create email contents for Adobe Campaign.

* **Adobe Campaign Email**: this template contains a standard content that you can personalize. You can choose between Adobe Campaign Email (AC6.1) and Adobe Campaign Email (ACS).
* **Importer Page**: this template lets you import a ZIP file containing an HTML file with content that you will then be able to personalize.

Open the new content and set the Adobe Campaign Cloud Service in the Page Properties, available from the sidekick. This enables communication between your content and your Adobe Campaign instance.
For more information, watch the following video:

>[!VIDEO](https://images-tv.adobe.com/mpcv3/923f1650-b359-4e90-9a90-f773b71b472d_1575035810.854x480at800_h264.mp4)

### Page properties {#page-properties-aem}

Selecting a Cloud Service provides you with access to personalization fields and other Adobe Campaign information that you will be able to access when editing your content.

>[!VIDEO](https://images-tv.adobe.com/mpcv3/38aedcab-a459-45bb-b8bd-ab22a457d0c6_1576057007.854x480at800_h264.mp4)

## Editing the email content in Adobe Experience Manager {#editing-email-aem}

You can edit the email content by adding components and assets. Personalization fields can be used to deliver a more relevant message based on the recipients' data in Adobe Campaign.

To create an email content in Adobe Experience Manager:

1. Edit the subject as well as the Plain text version of your email by accessing the Page properties > Email tab from the sidekick.

1. Personalization fields are available through the Text & Personalization component. By using it, you will be able to insert variables specific to the recipients.

1. Each component corresponds to a specific usage: inserting images, adding personalization, etc. The complete list of available components is detailed in the technical documentation.
For more information, watch the following video.
1. The validation workflow is available from the Workflow tab of the sidekick. You will not be able to send an email in Adobe Campaign if it uses a content that has not been approved.

## Sending the delivery {#sending-email-aem}

Once the content and sending parameters are defined, you can proceed to approving, preparing, and sending the email.

For more information, watch the following video: