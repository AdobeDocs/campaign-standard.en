---
title: "Step 2: Publish the extension"
seo-title: "Step 2: Publish the extension"
description: "Step 2: Publish the extension"
seo-description: 
uuid: 19aa9992-ee54-46da-ae35-2fc297f4ed18
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: use-case--extending-the-api
discoiquuid: 9ca4f06e-9f46-4407-b46e-b99a83f47946
index: y
internal: n
snippet: y
---

# Step 2: Publish the extension{#step-publish-the-extension}

Step 2: Publish the extension

1. From the advanced menu, via the Adobe Campaign logo, select **[!UICONTROL Administration]** > **[!UICONTROL Development]** , then **[!UICONTROL Publication]** .
1. Click on the **[!UICONTROL Prepare Publication]** button.
1. Select the **[!UICONTROL Update the Profiles & Services API]** option.

   ![](assets/extendpandsapi.png)

   >[!CAUTION]
   >
   >The API definition needs to be updated to match changes in the data model. Before publishing, make sure that the changes will not cause any errors with the integration. Otherwise, update the client code before updating the API.

1. Click the **[!UICONTROL Profiles & Services API Preview]** tab.

   This will show you the changes that the publication of the API will apply to the current version of the profilesAndServicesExt API.

   Here, the Promo Code field (ID: cusBrand) will be inserted into the API.

   ![](assets/extendpandsapi_diff.png)

1. Click the **[!UICONTROL Publish]** button.

