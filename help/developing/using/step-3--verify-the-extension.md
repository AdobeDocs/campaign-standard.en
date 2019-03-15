---
title: "Step 3: Verify the extension"
seo-title: "Step 3: Verify the extension"
description: "Step 3: Verify the extension"
seo-description: Learn how to access to the extended field with the Rest API.
uuid: c420da3c-a258-4c2b-ab35-7fdbd73f52b5
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: use-case--extending-the-api
discoiquuid: fa09861f-278f-4a98-a16d-f85a001896bf
index: y
internal: n
snippet: y
---

# Step 3: Verify the extension{#step-verify-the-extension}

1. Make a GET operation on the metadata of the Profiles & Services Extension API to check if the field added in the Profiles custom resource is now available.

   ```
   GET profileAndServicesExt/resourceType/profile
   ```

1. It returns:

   ![](assets/extendpandsapiview.png)

   The field is now available for further developments and integrations.

