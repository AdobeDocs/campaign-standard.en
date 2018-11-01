---
title: Defining dynamic content in an email
seo-title: Defining dynamic content in an email
description: Defining dynamic content in an email
seo-description: Follow these steps to display different contents dynamically in an email according to the conditions defined through the Adobe Campaign expression editor.
uuid: 92555f07-4688-405a-8dfb-b4e50090a9b8
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/designing/using/defining-dynamic-content-in-an-email
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-26T02 53 58.952-0400
cq-lastreplicated: 2018-07-23T08 13 56.868-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: defining-conditional-content
cq-template: /apps/help/templates/article-3
discoiquuid: 98a3bd9b-c8b0-4e9a-8400-cbcf23e0de19
firstPublishExternalDate: 2018-07-23T05:58:44.123-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-07-23T07 30 16.779-0400
jcr-createdby: admin
jcr-description: Defining dynamic content in an email
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T08:13:56.803-0400
lochandoffdate: 2018-07-26T02 53 58.952-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Defining dynamic content in an email
publishexternaldate: 2018-07-23T08 13 56.803-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/designing/using/defining-dynamic-content-in-an-email.html
sha1: 08e823db085094bca0c9a2ae159e835dc64d2067
topicBrowsingSortDate: 2018-07-23T08:13:56.803-0400
index: y
internal: n
snippet: y
---

# Defining dynamic content in an email

Defining dynamic content in an email

In an email, you can define different contents which will be displayed dynamically to the user according to the conditions defined via the expression editor. For example, from the same email, you can ensure that the recipients receive a different message according to their age range.

Defining dynamic content is different from [defining visibility conditions](../../designing/using/defining-a-visibility-condition.md).

1. Select a fragment, a component or an element.
1. Select the **Dynamic content** icon from the contextual toolbar.

   The **Dynamic content** section then appears in the palette on the left.

   By default, this section contains two elements: the default content and a new content.

   You cannot delete the default content. The content must always have a default variant.

1. Click the **Edit** button to define the first alternative variant or **Add a condition** to add a new content and its linked rule.
1. To define a content's display conditions, select the variant, then use the **Edit** button to open the expression editor and define a condition.

   For each content, you can specify a label and define the order of priority in which the condition will be applied. The contents will be displayed in the palette in order of priority, from left to right. For more on order of priority, refer to [this section](../../designing/using/defining-dynamic-content-in-an-email.md#order-of-priority). 

   ![](assets/email_designer_dynamic_content.png)

1. Once you have entered and confirmed an expression, you can make any changes you would like to the corresponding block in the editing zone.

>[!CAUTION]
>
>Once you have prepared your message and before sending it, don't forget to test it using a proof. If you do not do this, any errors may not be detected and the email may not be sent.

**Related topics:**

* [Sending proofs](../../sending/using/managing-test-profiles-and-sending-proofs.md#sending-proofs)
* [Advanced expression editing](../../automating/using/editing-queries.md#about-query-editor)

## <p>Order of priority</p>

In the expression editor, when you define a dynamic content, the order of priority works as follows:

1. You define two different dynamic contents with **two different conditions**, for example:

   **Condition 1:** the gender of the profile is masculine,

   **Condition 2:** the profile is between 20 and 30 years old.

   ![](assets/delivery_content_61.png)

   Some profiles in your database correspond to the two conditions but only one email with one dynamic content can be sent.

1. You therefore have to define the priority for the dynamic contents. A condition with an order of priority of **1** (and therefore the corresponding dynamic content) will be sent to a profile even if another condition whose priority order is **2** or **3** is also met by this profile.

   ![](assets/delivery_content_62.png)

You can only define one order of priority per dynamic content.
