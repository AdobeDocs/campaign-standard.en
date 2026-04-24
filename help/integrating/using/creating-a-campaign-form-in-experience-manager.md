---
title: Creating a Campaign form in Experience Manager
description: With the Adobe Experience Manager integration, you can create forms directly in AEM to create and update profiles or manage subscriptions.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-experience-manager
feature: Triggers
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: 61683639-3f71-4652-a138-acfc0e91e868
TQID: https://experienceleague.adobe.com/5wklRtwZ6Wubvyo-yu2ogEHufoqYBh6cvaJEoBC-Lkk
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
---
# Creating a Campaign form in Experience Manager {#creating-a-campaign-form-in-experience-manager}

You can create "forms" on your AEM sites and map the fields in a form to the fields in the Adobe Campaign database. This allows you to create and update profiles or manage the subscriptions to a service.

To create an Adobe Campaign form on your AEM site:

1. In your AEM site, create a new page based on the **Adobe Campaign Profile** template.

   ![](assets/aem_content_forms.png)

1. In the page properties, select the **[!UICONTROL Cloud Service]** corresponding to your Adobe Campaign instance.

   ![](assets/aem_content_forms_2.png)

1. Select the form type from the **[!UICONTROL Form Start]** component:

    * **Adobe Campaign: Save profile**
    * **Adobe Campaign: Subscribe to Services**
    * **Adobe Campaign: Unsubscribe from Services**

1. Edit the content of the form by adding different fields and components that you can map to the Adobe Campaign database fields.
1. Test and publish the form to make it accessible on your AEM site.

For more information, refer to the [detailed documentation](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/aem-adobe-campaign/adobe-campaign-forms.html).
