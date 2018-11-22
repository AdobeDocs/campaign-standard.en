---
title: "Step 3: Verify the extension"
seo-title: "Step 3: Verify the extension"
description: "Step 3: Verify the extension"
seo-description: Learn how to access to the extended field with the Rest API.
page-status-flag: never-activated
uuid: 34758fbb-ef68-4e10-a939-6dad94682602
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/developing/using/step-3--verify-the-extension
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: use-case--extending-the-api
discoiquuid: da9a631a-2ec9-498f-8153-adcf8666ffe2
isreadyforlocalization: false
navTitle: "Step 3: Verify the extension"
publishexternaldate: 2018-11-20
sha1: 117cbf27564c75a38f0e7aed388b5783effe7a80
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

