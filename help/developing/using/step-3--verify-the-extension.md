---
title: "Step 3: Verify the extension"
seo-title: "Step 3: Verify the extension"
description: "Step 3: Verify the extension"
seo-description: Learn how to access to the extended field with the Rest API.
page-status-flag: never-activated
uuid: 478a379d-99ba-4d38-bf8f-63c6b0b4e836
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: use-case--extending-the-api
discoiquuid: 4ef0ea87-cbde-4e90-b6d3-50ed8462b082
isreadyforlocalization: true
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

