---
title: Creating a Campaign form in Experience Manager 
seo-title: Creating a Campaign form in Experience Manager 
description: Creating a Campaign form in Experience Manager 
seo-description: With the Adobe Experience Manager integration, you can create forms directly in AEM to create and update profiles or manage subscriptions.
uuid: bd38ae95-9ff1-4084-8cfa-fefdb23a06cc
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-experience-manager
discoiquuid: aece902d-2cfd-4257-8dc2-bc357466add9
isreadyforlocalization: false
index: y
internal: n
snippet: y
---

# Creating a Campaign form in Experience Manager {#creating-a-campaign-form-in-experience-manager}

Creating a Campaign form in Experience Manager 

You can create "forms" on your AEM sites and map the fields in a form to the fields in the Adobe Campaign database. This allows you to create and update profiles or manage the subscriptions to a service.

To create an Adobe Campaign form on your AEM site:

1. In your AEM site, create a new page based on the **Adobe Campaign Profile ** template.

   ![](assets/aem_content_forms.png)

1. In the page properties, select the **[!UICONTROL Cloud Service]** corresponding to your Adobe Campaign instance.

   ![](assets/aem_content_forms_2.png)

1. Select the form type from the **[!UICONTROL Form Start]** component:

    * **Adobe Campaign: Save profile**
    * **Adobe Campaign: Subscribe to Services**
    * **Adobe Campaign: Unsubscribe from Services**

1. Edit the content of the form by adding different fields and components that you can map to the Adobe Campaign database fields.
1. Test and publish the form to make it accessible on your AEM site.

For more information, refer to the [detailed documentation](https://docs.adobe.com/docs/en/aem/6-2/author/personalization/adobe-campaign/adobe-campaign-forms.html).
