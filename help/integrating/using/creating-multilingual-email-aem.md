---
solution: Campaign Standard
product: campaign
title: Creating a multilingual email with the Adobe Experience Manager integration.
description: With the Adobe Experience Manager integration, you can create content directly in AEM and use it later on in Adobe Campaign.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-experience-manager

---

# Creating a multilingual email with the Adobe Experience Manager integration {#creating-multilingual-email-aem}

Using this document, you will learn how to create and manage email contents in Adobe Experience Manager, then use them for your marketing campaigns by importing them in your emails into Adobe Campaign Standard.

The prerequisites are:

* Access to an AEM instance configured for the integration.
* Access to an Adobe Campaign instance configured for the integration.
* An Adobe Campaign email template configured to receive AEM content.

## Accessing emails in Adobe Experience Manager {#email-content-aem}

Log in to your Adobe Experience Manager authoring instance and browse your site to access the folder containing your email contents.

>[!VIDEO](https://video.tv.adobe.com/v/29996)

## Creating new email content in Adobe Experience Manager {#creating-email-content-aem}

Several templates specific to Adobe Campaign are available. You must use one of these templates as they contain predefined components supported by Adobe Campaign.

By default, two predefined templates allow you to create email contents for Adobe Campaign.

* **[!UICONTROL Adobe Campaign Email]**: this template contains a standard content that you can personalize. You can choose between Adobe Campaign Email (AC6.1) and Adobe Campaign Email (ACS).
* **[!UICONTROL Importer Page]**: this template lets you import a ZIP file containing an HTML file with content that you will then be able to personalize.

1. In Adobe Experience Manager, create a new **[!UICONTROL Page]**.

1. Select the **[!UICONTROL Adobe Campaign Email]** template. Refer to the following video for the detailed steps.
    >[!VIDEO](https://video.tv.adobe.com/v/29997)

1. Open your new email content.

1. In the **[!UICONTROL Page properties]**, set **[!UICONTROL Adobe Campaign]** as the **[!UICONTROL Cloud Service Configuration]**. This enables communication between your content and your Adobe Campaign instance.

    For more information, watch the following video:

    >[!VIDEO](https://video.tv.adobe.com/v/29999)

## Creating language copies {#creating-language-copies}

## Approve your email content in Adobe Experience Manager {#approval-workflow}

## Creating your multilingual content in Adobe Campaign Standard {#multilingual-acs}

1. Create email Campaign
1. Select template AEM multilingual email
1. Properties
1. Select audience
1. Click Create
1. In the Edit properties, from the Content drop-down, select which Adobe Experience Manager account you want to use for this email.
1. Access the email designer.
1. Click Use Adobe Experience Manager content.
1. Select your previously created email content.
1. Edit your email as needed. For more information, refer to this page.
1. Click Save & Close.
1. Click Language copy creation.
1. Select your previously created Adobe Experience Manager content and click Confirm. Be careful with your content path. Content needs to be approved for this to work.
1. 
