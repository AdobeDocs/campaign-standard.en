---
title: "Step 3: Update profiles and prepare an email"
seo-title: "Step 3: Update profiles and prepare an email"
description: "Step 3: Update profiles and prepare an email"
seo-description: Learn how to update the data model and work with the extende field in a message.
page-status-flag: never-activated
uuid: 85fc6364-d6fc-4baa-9b1d-074269547349
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: use-case--extending-profiles
discoiquuid: e2ce4095-ad38-40e5-86e8-cff34af7e8b5
isreadyforlocalization: true
index: y
internal: n
snippet: y
---

# Step 3: Update profiles and prepare an email{#step-update-profiles-and-prepare-an-email}

Step 3: Update profiles and prepare an email

1. From the advanced menu, via the Adobe Campaign logo, select **Profiles & audiences > Profiles**.
1. Complete or create profiles, then complete the new **Promo code** field.

   ![](assets/schema_extension_UC3.png)

1. Select **Profiles & Audiences > Test profiles** in the navigation pane.
1. Complete or create a new test profile, then complete the new **Promo code** field.

   ![](assets/schema_extension_UC4.png)

1. Create a **new email** in a marketing campaign.
1. Create an **Audience** from a **simple rule**: **Promo code is not empty**. This rule is valid for the main target as well as for the test profiles.
1. Insert the **Promo code** field into the email content. 
1. Send the email to the test profiles selected by the audience.
1. Send the email to the profiles selected by the audience.

The values of the **Promo code** personalized field are contextualized by profile type when the email is sent.
