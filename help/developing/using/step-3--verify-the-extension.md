---
title: "Step 3: Verify the extension"
seo-title: "Step 3: Verify the extension"
description: "Step 3: Verify the extension"
seo-description: Learn how to access to the extended field with the Rest API.
uuid: d510be6e-c80b-4add-86e8-5e0779eabfdf
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: use-case--extending-the-api
discoiquuid: 4a538d72-2b0b-4dd0-bb14-b0e315c05d09
isreadyforlocalization: false
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

