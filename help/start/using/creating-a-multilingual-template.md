---
title: Creating a multilingual template
seo-title: Creating a multilingual template
description: Creating a multilingual template
seo-description: Learn how to define and execute multilingual Email/SMS deliveries through a single delivery based on your automatically segmented customers' preferred language. Report on the performance of every delivery down to the language and individual levels.
uuid: 4267e832-4d9a-4d9c-95d4-557ebebb3fa8
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/start/using/creating-a-multilingual-template
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-08T08 23 09.701-0400
cq-lastreplicated: 2018-09-07T15 08 46.586-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: start
content-type: reference
topic-tags: managing-templates
cq-template: /apps/help/templates/article-3
discoiquuid: d890eb7e-c09c-4238-8dba-a01f230f5b95
firstPublishExternalDate: 2018-09-07T15:08:46.399-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 01 50.380-0400
jcr-createdby: admin
jcr-description: Creating a multilingual template
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T15:08:46.399-0400
lochandoffdate: 2018-09-08T08 23 09.701-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Creating a multilingual template
publishexternaldate: 2018-09-07T15 08 46.399-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/start/using/creating-a-multilingual-template.html
sha1: 2f2a0e2012d8ff0b76a5a338ecfdb9785e89a324
topicBrowsingSortDate: 2018-09-07T15:08:46.399-0400
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

