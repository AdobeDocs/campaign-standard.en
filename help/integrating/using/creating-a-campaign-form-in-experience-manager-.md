---
title: Creating a Campaign form in Experience Manager 
seo-title: Creating a Campaign form in Experience Manager 
description: Creating a Campaign form in Experience Manager 
seo-description: With the Adobe Experience Manager integration, you can create forms directly in AEM to create and update profiles or manage subscriptions.
uuid: 58d3f355-55eb-4ebf-9b9a-ca7cf3a2715f
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/integrating/using/creating-a-campaign-form-in-experience-manager-
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-10T02 18 38.462-0400
cq-lastreplicated: 2018-09-07T14 59 28.306-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-experience-manager
cq-template: /apps/help/templates/article-3
discoiquuid: d1662970-0d6e-4e54-8f4c-9af1ca236437
firstPublishExternalDate: 2018-09-07T14:59:26.173-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 16.446-0400
jcr-createdby: admin
jcr-description: Creating a Campaign form in Experience Manager 
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T14:59:26.173-0400
lochandoffdate: 2018-09-10T02 18 38.461-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Creating a Campaign form in Experience Manager 
publishexternaldate: 2018-09-07T14 59 26.173-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/integrating/using/creating-a-campaign-form-in-experience-manager-.html
sha1: 8a8e443c3e8a1c2293e80f271bce5cf6fd4bd480
topicBrowsingSortDate: 2018-09-07T14:59:26.173-0400
index: y
internal: n
snippet: y
---

# Creating a Campaign form in Experience Manager 

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
