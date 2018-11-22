---
title: Creating a Campaign form in Experience Manager 
seo-title: Creating a Campaign form in Experience Manager 
description: Creating a Campaign form in Experience Manager 
seo-description: With the Adobe Experience Manager integration, you can create forms directly in AEM to create and update profiles or manage subscriptions.
page-status-flag: never-activated
uuid: 05cc54ea-3a0d-4005-bd15-aed228d2cab3
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/integrating/using/creating-a-campaign-form-in-experience-manager-
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-experience-manager
discoiquuid: 16602f50-6954-4aa0-99ae-a8a9288aeeef
isreadyforlocalization: false
navTitle: Creating a Campaign form in Experience Manager 
publishexternaldate: 2018-11-20
sha1: fa2e5715f0eb5e52516a4555ed4300d2b2fac9bd
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

1. In the page properties, select the **Cloud Service** corresponding to your Adobe Campaign instance.

   ![](assets/aem_content_forms_2.png)

1. Select the form type from the **Form Start** component:

    * **Adobe Campaign: Save profile**
    * **Adobe Campaign: Subscribe to Services**
    * **Adobe Campaign: Unsubscribe from Services**

1. Edit the content of the form by adding different fields and components that you can map to the Adobe Campaign database fields.
1. Test and publish the form to make it accessible on your AEM site.

For more information, refer to the [detailed documentation](https://docs.adobe.com/docs/en/aem/6-2/author/personalization/adobe-campaign/adobe-campaign-forms.html).
