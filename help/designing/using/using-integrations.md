---
title: Designing emails through Adobe Campaign integrations 
description: Discover how to design emails through Adobe Campaign integrations in the Email Designer.
page-status-flag: never-activated
uuid: 571ffc01-6e41-4501-9094-2f812b041a10
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: editing-email-content
discoiquuid: 39b86fda-7766-4e5f-ab48-bcc536ab66b3

internal: n
snippet: y
---

# Multi-solution email design {#multi-solution-email-design}

Adobe Campaign offers several email authoring options. You can use solutions such as Dreamweaver to edit your email content and create responsive messages in the Email Designer. You can also email content with Adobe Experience Manager and use it in your emails in Adobe Campaign Standard.

## Editing content in Dreamweaver {#editing-content-in-dreamweaver}

The Adobe Campaign Standard integration with Dreamweaver lets you edit an email's content in the Dreamweaver interface. You have access to the powerful interface of Dreamweaver to design and develop responsive email content.

* **Bidirectional syncing**

  Whenever an edit is made in one product, it is updated in real time in the other. If you want to change the color of text in Dreamweaver, as soon as you make that edit, the color of the text is live in Campaign. Additionally, when you select code in either Dreamweaver or Campaign, since the line numbers are the same, the selection remains between the two products, which is very useful when looking for something specific in the code.

* **Upload local images to Adobe Campaign through Dreamweaver**

  When creating or editing an email within Dreamweaver, you can simply select an image from your desktop or local machine. While Dreamweaver has always allowed you to do this, when Dreamweaver and Campaign are connected, the local file is immediately uploaded to the Adobe Campaign server: no need to manually upload images as content changes. Additionally, it ensures that the latest images are always live in Campaign.

* **Add Campaign personalization in Dreamweaver**

  For the email developer there is no longer a need to add text like `[[FIRSTNAME_PLACEHOLDER]]` nor to look up the syntax of your data model’s tables. The Campaign toolbar in Dreamweaver connects directly to your Campaign instance's data model. That means you can pull in any data you want for personalization from something like First Name to Address. If you’ve created Content Blocks within Campaign, you can also pull those directly into Dreamweaver.

This capability is detailed in the Dreamweaver Documentation accessible [here](https://helpx.adobe.com/dreamweaver/using/working-with-dreamweaver-and-campaign.html). A demonstration [video](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/designing-content/email-designer/dreamweaver-integration.html) is also available.

## Editing content in Experience Manager {#editing-content-in-experience-manager}

Email content can be edited in Experience Manager and then used for one or several email messages in Adobe Campaign Standard. Refer to [this document](../../integrating/using/integrating-with-experience-manager.md).

## Product listings {#product-listing}

>[!CONTEXTUALHELP]
>id="ac_product_listing"
>title="Using product listings"
>abstract="The product listings allows you to reference a data collection and display it in the email content."

The product listings allows you to reference one or more data collections in the email content. These listings are available for transactional emails. A dedicated section for this feature is available [here](../../channels/using/event-transactional-messages.md#using-product-listings-in-a-transactional-message).

## Email design options comparison {#email-design-options-comparison}

Adobe Campaign offers several email authoring options. The table below shows the main possibilities, benefits and limitations for each of them.

<table> 
 <thead> 
  <tr> 
   <th> </th> 
   <th> Email Designer<br /> </th> 
   <th> Experience Manager<br /> </th> 
   <th> Dreamweaver<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <strong>Start blank email</strong><br /> </td> 
   <td> Supported<br /> </td> 
   <td> Supported<br /> </td> 
   <td> Supported<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Write HTML</strong><br /> </td> 
   <td> Supported<br /> </td> 
   <td> Not supported<br /> </td> 
   <td> Supported<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Update HTML</strong><br /> </td> 
   <td> Only inside an HTML component<br /> </td> 
   <td> Not supported<br /> </td> 
   <td> Supported<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Basic personalization</strong><br /> </td> 
   <td> Supported<br /> </td> 
   <td> Supported<br /> </td> 
   <td> Supported<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Advanced personalization</strong><br /> </td> 
   <td> Supported<br /> </td> 
   <td> Not supported<br /> </td> 
   <td> Not supported<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Proof/Preview</strong><br /> </td> 
   <td> Supported<br /> </td> 
   <td> Preview in AEM<br /> Proof in Campaign<br /> </td> 
   <td> Preview and proof in Campaign<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Product listings</strong><br /> </td> 
   <td> Supported in email transactional messages<br /> </td> 
   <td> Not supported<br /> </td> 
   <td> Not supported<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Benefits</strong><br /> </td> 
   <td> 
     <p>- Easy email building through drag-and-drop experience</p>
     <p>- Functionalities similar to legacy content editor</p>
     <p>- Reusable content with fragments</p>
  </td> 
   <td> 
     <p>- Reusing assets from website in emails</p>
     <p>- Leveraging the power of Experience Manager in email contents</p>
    </td> 
   <td> 
    <p>- Capability for a developer to directly code an email</p>
    <p>- Bi-directional synchronization</p>
    <p>- Editing offline in Dreamweaver and synchronizing later</p>
    <p>- Uploading images to Adobe Campaign through Dreamweaver</p>
  </td> 
  </tr> 
  <tr> 
   <td> <strong>Limitations</strong><br /> </td> 
   <td> 
     <p>- No conditional content within fragments</p>
     <p>- Using Experience Manager fragments not possible</p>
  </td> 
   <td> 
     <p>- Advanced personalization difficult to implement</p>
     <p>- Need to send tests in Adobe Campaign</p>
  </td> 
   <td> Dynamic content not supported<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Audience</strong><br /> </td> 
   <td> Marketers who want to keep the flexibility to use HTML components in combination with drag-and-drop features<br /> </td> 
   <td> Marketers already using Experience Manager who want to use standard email templates with little personalization<br /> </td> 
   <td> Developers who want to code email contents and integrate directly with Adobe Campaign<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>To learn more</strong><br /> </td> 
   <td> See <a href="../../designing/using/designing-content-in-adobe-campaign.md">About the Email Designer</a>.<br /> </td> 
   <td> See <a href="../../integrating/using/integrating-with-experience-manager.md">Integrating with Experience Manager</a>.<br /> </td> 
   <td> See <a href="https://helpx.adobe.com/dreamweaver/using/working-with-dreamweaver-and-campaign.html">Dreamweaver and Campaign</a> and watch this <a href="https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/designing-content/email-designer/dreamweaver-integration.html">video</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>
