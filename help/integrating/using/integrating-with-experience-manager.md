---
solution: Campaign Standard
product: campaign
title: About Campaign-Experience Manager integration
description: With the Adobe Experience Manager integration, you can create content directly in AEM and use it later on in Adobe Campaign.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-experience-manager

feature: Triggers
role: Data Architect
level: Intermediate
exl-id: ff94f69b-3036-4103-a841-6b85feb0eb7e
---
# About Campaign-Experience Manager integration{#integrating-with-experience-manager}

This integration between Adobe Campaign Standard and Adobe Experience Manager allows you to use content created in Adobe Experience Manager in your Adobe Campaign emails.

You can therefore make the most of the Adobe Experience Manager content editing functionalities as well as Adobe Campaign's delivery and data management capabilities. Please note that you cannot perform A/B tests for contents imported from Adobe Experience Manager.

Adobe Campaign Standard is compatible with Adobe Experience Manager 6.1, 6.2, 6.3, 6.4 and 6.5. The following sections present an overview of the actions you can execute. For more information, refer to the sections dedicated to [configuration](https://docs.adobe.com/content/help/en/experience-manager-65/administering/integration/campaignstandard.html) and the [use](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/aem-adobe-campaign/campaign.html) of the integration.

>[!NOTE]
>
> Adobe Campaign Standard templates are no longer available with Adobe Experience Manager 6.5.

## Tips on how to use Campaign-Experience Manager integration {#tips-aem}

* **Know which template to use with the integration**

    Since email templates are editable within Adobe Experience Manager, it might look easier to edit any template in Adobe Experience Manager. But certain templates are not easily accommodated. Individualized templates specific to one customer are not recommended for this integration and should be edited directly in Adobe Campaign Standard.

    For more information on templates, refer to this [page](https://docs.adobe.com/content/help/en/experience-manager-65/developing/platform/templates/templates.html).

* **Make sure the Externalizer was configured during implementation**

    Configuring the Externalizer while implementing Experience Manager for Adobe Campaign Standard makes it possible to transform a resource path into a URL. This allows you to make your images visible on the page. If the Externalizer is not configured properly, your emails will contain broken images.
    
    To learn how to configure the Externalizer, refer to this [page](https://docs.adobe.com/content/help/en/experience-manager-65/developing/platform/externalizer.html).

* **Organize your email templates to avoid misuse.**

    Keeping templates organized ensures that the appropriate templates are in the appropriate folders and to not choose the wrong ones by mistake. During implementation, paths should be created to save templates in the right places.

    For more information on templates, refer to this [page](https://docs.adobe.com/content/help/en/experience-manager-65/developing/platform/templates/templates.html#template-availability).

* **Get quickly started with out-of-the-box components.**

    Out-of-the-box components in Adobe Experience Manager for Adobe Campaign Standard can help you get quickly started if your templates are not complex.
    There are seven out-of-the-box components in Experience Manager that you can start using:
    
    * Heading
    * Image
    * Link
    * Scene7 Image Template
    * Targeted Reference
    * Text & Image
    * Text & Personalization

* **HTML for emails is different from HTML for web**

    It is important to understand that you can’t use the same components used in your web content for email templates. Using out-of-the-box components ensures that your components will be email-compatible.

* **Unlink content from templates and reuse them again and again.**

    When setting up your emails in Campaign Standard and selecting an Experience Manager template, you can only choose one that has not already been linked to another campaign. Otherwise, if you change the content in Adobe Experience Manager for one campaign and refresh, you can unintentionally impact the content in the other campaign.
    To avoid this, once you’ve finished using your template, you can unlink it to use it again. You just have to select the template and click **[!UICONTROL Delete the link with Adobe Experience Manager content]**.

* **Use Adobe Experience Manager to create variations of emails for Adobe Campaign Standard.**

    This integration allows you to easily turn one email into several versions with the segmentation.
    To learn how to set up segmentation in Adobe Experience Manager and how to create email with targeted content, refer to this [page](https://docs.adobe.com/help/en/experience-manager-65/authoring/aem-adobe-campaign/target-adobe-campaign.html#setting-up-segmentation-in-aem).

* **For a successful sync, the segment name in Experience Manager has to match the segment name in Campaign exact.**
