---
solution: Campaign Standard
product: campaign
title: "Step 3: Verify the extension"
description: Learn how to access to the extended field with the Rest API.
audience: developing
content-type: reference
topic-tags: use-case--extending-the-api

---

# Step 3: Verify the extension{#step-verify-the-extension}

1. Make a GET operation on the metadata of the Profiles & Services Extension API to check if the field added in the Profiles custom resource is now available.

   ```
   GET profileAndServicesExt/resourceType/profile
   ```

1. It returns:

   ![](assets/extendpandsapiview.png)

   The field is now available for further developments and integrations.

