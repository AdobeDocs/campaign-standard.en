---
title: "Step 2: Publish the extension"
seo-title: "Step 2: Publish the extension"
description: "Step 2: Publish the extension"
seo-description: 
uuid: 0d173805-b9f7-423a-92a8-403533436707
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/developing/using/step-2--publish-the-extension
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-26T02 53 37.125-0400
cq-lastreplicated: 2018-07-23T05 59 16.741-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: use-case--extending-the-api
cq-template: /apps/help/templates/article-3
discoiquuid: 9e439196-5aee-48f3-b66b-d74196db2027
firstPublishExternalDate: 2018-07-23T05:59:16.711-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 17.997-0400
jcr-createdby: admin
jcr-description: Step 2  Publish the extension
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T05:59:16.711-0400
lochandoffdate: 2018-07-26T02 53 37.125-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: "Step 2: Publish the extension"
publishexternaldate: 2018-07-23T05 59 16.711-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/developing/using/step-2--publish-the-extension.html
sha1: 931ad8df80455c7d75a03991bae8adc77fe72403
topicBrowsingSortDate: 2018-07-23T05:59:16.711-0400
index: y
internal: n
snippet: y
---

# Step 2: Publish the extension

Step 2: Publish the extension

1. From the advanced menu, via the Adobe Campaign logo, select **Administration** > **Development**, then **Publication**.
1. Click on the **Prepare Publication** button.
1. Select the **Update the Profiles & Services API** option.

   ![](assets/extendPandSAPI.png)

   >[!CAUTION]
   >
   >The API definition needs to be updated to match changes in the data model. Before publishing, make sure that the changes will not cause any errors with the integration. Otherwise, update the client code before updating the API.

1. Click the **Profiles & Services API Preview** tab.

   This will show you the changes that the publication of the API will apply to the current version of the profilesAndServicesExt API.

   Here, the Promo Code field (ID: cusBrand) will be inserted into the API.

   ![](assets/extendPandSAPI_diff.png)

1. Click the **Publish** button.

