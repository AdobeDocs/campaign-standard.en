---
title: Inserting images
seo-title: Inserting images
description: Inserting images
seo-description: Learn how to add images to your content.
page-status-flag: never-activated
uuid: 3bb32cf6-e49c-48b2-8a09-cd0f37f65755
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/designing/using/inserting-images
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: using-images
discoiquuid: ae3816d7-0395-47b9-813b-05180bf7e47d
isreadyforlocalization: false
navTitle: Inserting images
publishexternaldate: 2018-11-20
sha1: 82994d65a54060fe46215675de115c7c4a252e1e
index: y
internal: n
snippet: y
---

# Inserting images{#inserting-images}

Inserting images

You can insert images in your emails and landing pages.

The following types of images are available, depending on your configuration:

* Local images
* Images shared from Adobe Experience Cloud - refer to [Working with Campaign and Assets Core Service](../../integrating/using/working-with-campaign-and-assets-core-service.md) / Assets On Demand
* Dynamic images from Adobe Target - refer to [Working with Campaign and Target](../../integrating/using/about-campaign-target-integration.md)

If enabled, you can modify images with the Adobe Creative SDK. See [Modifying images with the Adobe Creative SDK](../../designing/using/modifying-images-with-the-adobe-creative-sdk.md).

>[!CAUTION]
>
>If you choose to add an image directly by editing the HTML version of the email, you must not call up **external files in a &lt;script&gt; tag** of the HTML page. These files will not be imported onto the Adobe Campaign server.

## Inserting images in an email {#inserting-images-in-an-email}

1. Add a structure component. For more on this, see [Editing the email structure](../../designing/using/defining-the-email-structure.md#editing-the-email-structure).
1. Inside this structure component, add an **Image** content component.

   ![](assets/des_insert_images_1.png)

1. Click **Browse**. Drag and drop an image or click to select a file from your computer.

   ![](assets/des_insert_images_2.png)

1. Select the content component that you just added.
1. Check the image properties and adjust them if needed.

   ![](assets/des_insert_images_3.png)

## Inserting images in a landing page {#inserting-images-in-a-landing-page}

1. In a landing page content, select a block containing an image.
1. Select the **Insert** button.

   ![](assets/des_insert_images_LP_1.png)

1. Choose **Local image** from the contextual toolbar.

   ![](assets/des_insert_images_LP_2.png)

1. Select a file.

   ![](assets/des_insert_images_LP_3.png)

1. Adjust the image properties as needed.

   ![](assets/des_insert_images_LP_4.png)

