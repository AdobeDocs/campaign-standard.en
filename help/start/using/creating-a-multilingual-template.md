---
title: Creating a multilingual template
seo-title: Creating a multilingual template
description: Creating a multilingual template
seo-description: Learn how to define and execute multilingual Email/SMS deliveries through a single delivery based on your automatically segmented customers' preferred language. Report on the performance of every delivery down to the language and individual levels.
page-status-flag: never-activated
uuid: b7d7633a-3cb9-4381-8068-79b781b069e4
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/start/using/creating-a-multilingual-template
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: start
content-type: reference
topic-tags: managing-templates
discoiquuid: 35b22567-cb7e-4176-b4e5-2bc078b1f739
isreadyforlocalization: false
navTitle: Creating a multilingual template
publishexternaldate: 2018-11-20
sha1: e5cddc217bcaa1c12f8fb3dd7a4e9338392994c9
index: y
internal: n
snippet: y
---

# Creating a multilingual template{#creating-a-multilingual-template}

Creating a multilingual template

A multilingual template is a specific template to manage multilingual messages.

This kind of template is available for **Email and SMS messages** and useable in standalone mode, within a workflow or in a recurring delivery.

In the multilingual feature templates, the language management is based on variants. **Each variant represents one language.**

Adobe Campaign Standard is able to set up a maximum of 40 variants.

A default language is mandatory. By default, for all instances, the sending language is US.

During the template creation, you can add the number of variants corresponding to the number of needed languages in the message.

To perform the creation of SMS or email template, follow the steps:

1. Duplicate an existing multilingual template (SMS or Email).

   ![](assets/multi_template_duplicate.png)

   >[!NOTE]
   >
   >You can also modify an existing standard template in a multilingual template by clicking on the **Initialize content variant** button in the template properties.

1. Modify the properties to customize label, tracking, etc.
1. Modify the number of desired variants by clicking on the variants tile. The variants window is displayed

   ![](assets/multi_template_variants.png)

   You can add or remove variants. To add a variant, complete the **New content variant** window.

   ![](assets/multi_template_newvariant.png)

   >[!NOTE]
   >
   >Do not delete the "default" variant as it is the variant sent to profiles without a completed preferred language parameter.

1. Customize label variant if needed and click on confirm.
1. You can also directly add the content for each variant.

You are now ready to create an email or an SMS message based on this multilingual template.

**Related topics:**

* [Creating a multilingual email](../../channels/using/creating-a-multilingual-email.md)
* [Creating profiles](../../audiences/using/creating-profiles.md)

