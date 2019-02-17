---
title: "Step 3: Verify the extension"
seo-title: "Step 3: Verify the extension"
description: "Step 3: Verify the extension"
seo-description: Learn how to access to the extended field with the Rest API.
uuid: 08466bcc-ac1a-4181-b982-ea455bcd6b55
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: use-case--extending-the-api
discoiquuid: 976f41bb-62cd-46d4-a411-fe8913c02eb1
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

   ![](assets/extendpandsapiview.png)

   The field is now available for further developments and integrations.

