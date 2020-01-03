---
title: About Campaign-Experience Manager integration
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

# About Campaign-Experience Manager integration{#integrating-with-experience-manager}

This integration between Adobe Campaign Standard and Adobe Experience Manager allows you to use content created in Adobe Experience Manager in your Adobe Campaign emails.

You can therefore make the most of the Adobe Experience Manager content editing functionalities as well as Adobe Campaign's delivery and data management capabilities.

>[!NOTE]
>
>You cannot perform A/B tests for contents imported from Adobe Experience Manager.

Adobe Campaign Standard is compatible with Adobe Experience Manager 6.1, 6.2, 6.3 and 6.4. The following sections present an overview of the actions you can execute. For more information, refer to the sections dedicated to [configuration](https://helpx.adobe.com/experience-manager/6-4/sites/administering/using/campaignstandard.html) and the [use](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/campaign.html) of the integration.

## Tips on how to use Campaign-Experience Manager integration {#tips-aem}

* **Know when to use the integration and when not to**

    Since email templates are editable from within Experience Manager, it might seem like best practice to edit any template, regardless of complexity, in Experience Manager. The reality is that there are certain templates that Experience Manager can’t easily accommodate. Personalization templates, ones in which the name of the customer changes but the rest of the content stays the same, work well with the Experience Manager for Campaign integration. Individualized templates on the other hand, ones in which the email content is specific to one customer and contains a variety of moving parts, are not recommended for this integration and should be edited directly in Campaign.

* **Make sure the Externalizer was configured during implementation**

    Configuring the Externalizer while implementing Experience Manager for Campaign makes it possible to transform a resource path into a URL. This allows you to make your images visible on the page. If the Externalizer is not configured properly, your emails will contain broken images.
    
    To learn how to configure the Externalizer, refer to this [page](https://docs.adobe.com/content/help/en/experience-manager-64/developing/platform/externalizer.html)

* **Make sure your email templates are organized properly to avoid misuse.**
    Say your organization is a national corporation with several brands in your portfolio. But to the general public, some of your brands appear to be competitors. If Brand A accidentally sends an email to Brand B customers, complete with personal information only Brand B should have, the reputation of both brands could suffer. 
    Keeping templates organized ensures that the appropriate templates are in the appropriate folders, so content authors don’t choose the wrong ones by mistake. During implementation, the implementer should have created paths that guide authors to save templates in the right places. But if not, it can be done afterward. It’s just a matter of adding or customizing the “allowedPaths” property /content/campaigns/brandA/(/[^/]*)in Experience Manager Sites.

* **Get quickly started with out-of-the-box components.**
    Out-of-the-box components in Experience Manager for Campaign can help you get quickly started if your templates are simple and not overly complex. 
    There are seven out-of-the-box components in Experience Manager for Campaign that you can start using: 
    1. Heading 
    1. Image
    1. Link
    1. Scene7 Image Template
    1. Targeted Reference
    1. Text and Image
    1. Text and Personalization

*  HTML for emails is different from HTML for web, it is important to understand that you can’t use the same components used in your web content for email templates. Using out-of-the-box components ensures that your components will be email-compatible.

* **Unlink content from templates and reuse them again and again.**

    When setting up your emails in Campaign, you’ll see that when selecting an Experience Manager template, you can only choose one that has not already been linked to another campaign. That’s because if you change the content in Experience Manager for one campaign and hit refresh, you can unintentionally impact the content in the other campaign. However, once you’ve finished with the template, you can unlink it and use it again. Simply select the template and click “Delete the link with Adobe Experience Manager content.”

* **Use Experience Manager to create variations of emails for Campaign.**

* **In order to enable a successful sync, the segment name in Experience Manager has to match the segment name in Campaign exact**