---
title: "Step 3: Verify the extension"
seo-title: "Step 3: Verify the extension"
description: "Step 3: Verify the extension"
seo-description: Learn how to access to the extended field with the Rest API.
uuid: d713a985-208e-4382-bc9b-dacdfb2d6a30
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/developing/using/step-3--verify-the-extension
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-10T02 19 14.918-0400
cq-lastreplicated: 2018-09-07T14 58 08.726-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: use-case--extending-the-api
cq-template: /apps/help/templates/article-3
discoiquuid: 0a868a06-ec89-4734-9f85-4713a40318cb
firstPublishExternalDate: 2018-09-07T14:58:05.816-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 01 58.684-0400
jcr-createdby: admin
jcr-description: Step 3  Verify the extension
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T14:58:05.816-0400
lochandoffdate: 2018-09-10T02 19 14.917-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: "Step 3: Verify the extension"
publishexternaldate: 2018-09-07T14 58 05.816-0400
publishExternalURL: "https://helpx.adobe.com/campaign/standard/developing/using/step-3--verify-the-extension.html"
sha1: 79ba052d50b06d5dd389e6d52c9fd32d2f98aab6
topicBrowsingSortDate: 2018-09-07T14:58:05.816-0400
index: y
internal: n
snippet: y
---

# Step 3: Verify the extension{#step-verify-the-extension}

Step 3: Verify the extension

1. Make a GET operation on the metadata of the Profiles & Services Extension API to check if the field added in the Profiles custom resource is now available.

   ```
   GET profileAndServicesExt/resourceType/profile
   ```

1. It returns:

   ![](assets/extendPandSAPIview.png)

   The field is now available for further developments and integrations.

