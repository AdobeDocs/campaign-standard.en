---
title: Creating a Campaign form in Experience Manager 
seo-title: Creating a Campaign form in Experience Manager 
description: Creating a Campaign form in Experience Manager 
seo-description: With the Adobe Experience Manager integration, you can create forms directly in AEM to create and update profiles or manage subscriptions.
uuid: b182dc46-4948-4b8b-9926-eb03e996817b
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/integrating/using/creating-a-campaign-form-in-experience-manager-
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-27T03 26 25.389-0400
cq-lastmodifiedby: mancini
cq-lastreplicated: 2018-07-23T05 59 29.754-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-experience-manager
cq-template: /apps/help/templates/article-3
discoiquuid: ebfb6528-673b-41a7-821f-ab12e0d78de2
firstPublishExternalDate: 2018-07-23T05:59:29.699-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 16.446-0400
jcr-createdby: admin
jcr-description: Creating a Campaign form in Experience Manager 
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T05:59:29.699-0400
lochandoffdate: 2018-07-27T03 26 25.388-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
moreHelpPaths: /content/help/en/campaign/standard/integrating/morehelp/working-with-campaign-and-experience-manager;/content/help/en/campaign/standard/integrating/morehelp/working-with-campaign-and-experience-manager
navTitle: Creating a Campaign form in Experience Manager 
publishexternaldate: 2018-07-23T05 59 29.699-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/integrating/using/creating-a-campaign-form-in-experience-manager-.html
sha1: c71b6262d5f422b85fb1ef8dd29c3dec5cd22545
topicBrowsingSortDate: 2018-07-23T05:59:29.699-0400
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
