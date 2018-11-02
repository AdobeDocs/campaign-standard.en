---
title: Step 3: Verify the extension
seo-title: Step 3: Verify the extension
description: Step 3: Verify the extension
seo-description: Learn how to access to the extended field with the Rest API.
uuid: ba4e354b-2f05-44d6-9222-da2f32967bb8
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/developing/using/step-3--verify-the-extension
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-26T02 53 37.964-0400
cq-lastreplicated: 2018-07-23T05 59 17.664-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: use-case--extending-the-api
cq-template: /apps/help/templates/article-3
discoiquuid: 85b00eb8-6766-4158-a4b3-1f4ccdbbdc88
firstPublishExternalDate: 2018-07-23T05:59:17.622-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 01 58.684-0400
jcr-createdby: admin
jcr-description: Step 3  Verify the extension
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T05:59:17.622-0400
lochandoffdate: 2018-07-26T02 53 37.964-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Step 3: Verify the extension
publishexternaldate: 2018-07-23T05 59 17.622-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/developing/using/step-3--verify-the-extension.html
sha1: 4a5579107fd89bb25820b6f41471367c98e8900d
topicBrowsingSortDate: 2018-07-23T05:59:17.622-0400
index: y
internal: n
snippet: y
---

# Step 3: Verify the extension

Step 3: Verify the extension

1. Make a GET operation on the metadata of the Profiles & Services Extension API to check if the field added in the Profiles custom resource is now available.

   ```
   GET profileAndServicesExt/resourceType/profile
   ```

1. It returns:

   ![](assets/extendPandSAPIview.png)

   The field is now available for further developments and integrations.

