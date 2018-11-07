---
title: Step 3 Update profiles and prepare an email
seo-title: Step 3 Update profiles and prepare an email
description: Step 3 Update profiles and prepare an email
seo-description: Learn how to update the data model and work with the extende field in a message.
uuid: 2a4c07f1-d4fe-4158-b9e9-93dab801fe5d
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/developing/using/step-3--update-profiles-and-prepare-an-email
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-10T02 19 22.646-0400
cq-lastreplicated: 2018-09-07T15 01 10.585-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: use-case--extending-profiles
cq-template: /apps/help/templates/article-3
discoiquuid: b92bbcce-07e7-403e-863d-a8adac6bca3b
firstPublishExternalDate: 2018-09-07T15:01:07.667-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 21.218-0400
jcr-createdby: admin
jcr-description: Step 3  Update profiles and prepare an email
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T15:01:07.667-0400
lochandoffdate: 2018-09-10T02 19 22.645-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Step 3 Update profiles and prepare an email
publishexternaldate: 2018-09-07T15 01 07.667-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/developing/using/step-3--update-profiles-and-prepare-an-email.html
sha1: f6785b3ac3c9117e1b50b368a3e0122b6934a970
topicBrowsingSortDate: 2018-09-07T15:01:07.667-0400
index: y
internal: n
snippet: y
---

# Step 3: Update profiles and prepare an email

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
