---
title: "Step 2: Publish the extension"
seo-title: "Step 2: Publish the extension"
description: "Step 2: Publish the extension"
seo-description: 
uuid: afeadd44-0b31-4aed-9d7a-b9c92bbbebbb
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: use-case--extending-the-api
discoiquuid: 0ecc6a3e-5cbc-4020-bf3f-966d576239a1
index: y
internal: n
snippet: y
---

# Step 2: Publish the extension{#step-publish-the-extension}

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

