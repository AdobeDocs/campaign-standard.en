---
title: "Step 3: Update profiles and prepare an email"
seo-title: "Step 3: Update profiles and prepare an email"
description: "Step 3: Update profiles and prepare an email"
seo-description: Learn how to update the data model and work with the extende field in a message.
page-status-flag: never-activated
uuid: fc2d4852-ece6-4113-9072-05cfde7ee2b3
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/developing/using/step-3--update-profiles-and-prepare-an-email
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: use-case--extending-profiles
discoiquuid: d4acb02b-9aca-4c85-93f4-45a216f4b10c
isreadyforlocalization: false
navTitle: "Step 3: Update profiles and prepare an email"
publishexternaldate: 2018-11-20
sha1: c708dce2fae767b65110d14b98c6481ff03203f8
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
