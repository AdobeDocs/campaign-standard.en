---
title: "Step 3: Update profiles and prepare an email"
seo-title: "Step 3: Update profiles and prepare an email"
description: "Step 3: Update profiles and prepare an email"
seo-description: Learn how to update the data model and work with the extende field in a message.
uuid: 99d874f5-e2bb-418b-ad98-79bb30b06fe1
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: use-case--extending-profiles
discoiquuid: 773cfbd1-fc4e-4215-8862-600273b8f8dc
isreadyforlocalization: false
index: y
internal: n
snippet: y
---

# Step 3: Update profiles and prepare an email{#step-update-profiles-and-prepare-an-email}

Step 3: Update profiles and prepare an email

1. From the advanced menu, via the Adobe Campaign logo, select **[!UICONTROL Profiles & audiences > Profiles]** .
1. Complete or create profiles, then complete the new **[!UICONTROL Promo code]** field.

   ![](assets/schema_extension_UC3.png)

1. Select **[!UICONTROL Profiles & Audiences > Test profiles]** in the navigation pane.
1. Complete or create a new test profile, then complete the new **[!UICONTROL Promo code]** field.

   ![](assets/schema_extension_UC4.png)

1. Create a **[!UICONTROL new email]** in a marketing campaign.
1. Create an **[!UICONTROL Audience]** from a **[!UICONTROL simple rule]** : **[!UICONTROL Promo code is not empty]** . This rule is valid for the main target as well as for the test profiles.
1. Insert the **[!UICONTROL Promo code]** field into the email content. 
1. Send the email to the test profiles selected by the audience.
1. Send the email to the profiles selected by the audience.

The values of the **[!UICONTROL Promo code]** personalized field are contextualized by profile type when the email is sent.
