---
title: Personalizing an email
seo-title: Personalizing an email
description: Personalizing an email
seo-description: Learn how to insert a personalization field and how to define dynamic content.
uuid: 129660c5-be8e-4243-94d6-bd76b2106c34
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/designing/using/personalizing-an-email
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-06-25T08 45 21.483-0400
cq-lastreplicated: 2018-06-14T08 43 52.882-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: designing-email-content
cq-template: /apps/help/templates/article-3
discoiquuid: c7c0fb2e-33e1-40d6-a378-6b575aac929f
firstPublishExternalDate: 2018-06-14T08:43:52.860-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-27T07 29 06.348-0400
jcr-createdby: admin
jcr-description: Personalizing an email
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-06-14T08:43:52.860-0400
lochandoffdate: 2018-06-25T08 45 21.483-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Personalizing an email
publishexternaldate: 2018-06-14T08 43 52.860-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/designing/using/personalizing-an-email.html
sha1: af153f6ab0da2f953248eb2a21f820cd4f534504
topicBrowsingSortDate: 2018-06-14T08:43:52.860-0400
index: y
internal: n
snippet: y
---

# Personalizing an email

Personalizing an email

## Inserting a personalization field

Adobe Campaign allows you to insert a field from the database into your page such as the recipient's first name.

To add a personalization field to the content:

1. Click inside a text block and select **Insert personalization field**. 
1. Select the field that you would like to insert into your page content.

   If the email is created from a workflow, the additional data computed in the workflow is also available in the personalization fields. For more information about adding additional data from a workflow, refer to the [Enriching data](../../automating/using/targeting-data.md#enriching-data) section.

The field name appears in the editor and it is highlighted.

Once personalization is generated (when previewing and preparing the email for example), this field will be replaced by the value corresponding to the targeted recipient.

## Personalizing an email with dynamic content

You can define different contents which will be displayed dynamically to the user according to the conditions defined via the expression editor. For example, from the same email, you can ensure that the recipients receive a different message according to their age range.

Defining dynamic content is different from defining visibility conditions, which can be done by [editing the settings of a fragment.](../../designing/using/customizing-the-display-and-style-of-an-element.md)

1. Select a fragment.
1. Select the **Dynamic content** icon.

   The **Dynamic content** section then appears in the palette.

   By default, this section contains two elements: the default content and a new content.

   You cannot delete the default content. The content must always have a default variant.

1. Click the **Edit** button to define the first alternative variant or **Add variant** to add a new content and its linked rule.
1. To define a content's display conditions, select the variant, then use the **Edit** button to open the expression editor and define a condition.

   For each content, you can specify a label and define the order of priority in which the condition will be applied. The contents will be displayed in the palette in order of priority, from left to right. For more on order of priority, refer to [this section](../../designing/using/personalizing-an-email.md#order-of-priority). 

   ![](assets/email_designer_dynamic_content.png)

1. Once you have entered and confirmed an expression, you can make any changes you would like to the corresponding block in the editing zone.

>[!CAUTION]
>
>Once you have prepared your message and before sending it, don't forget to test it using a proof. If you do not do this, any errors may not be detected and the email may not be sent.

**Related topics:**

* [Sending proofs](../../sending/using/managing-test-profiles-and-sending-proofs.md#sending-proofs)
* [Advanced expression editing](../../automating/using/editing-queries.md#about-query-editor)

### Order of priority

In the expression editor, when you define a dynamic content, the order of priority works as follows:

1. You define two different dynamic contents with **two different conditions**, for example:

   **Condition 1:** the gender of the profile is masculine,

   **Condition 2:** the profile is between 20 and 30 years old.

   Some profiles in your database correspond to the two conditions but only one email with one dynamic content can be sent.

1. You therefore have to define the priority for the dynamic contents. A condition with an order of priority of **1** (and therefore the corresponding dynamic content) will be sent to a profile even if another condition whose priority order is **2** or **3** is also met by this profile.

You can only define one order of priority per dynamic content.

## Personalizing the subject line of an email

### Personalizing an email subject

The message subject is mandatory to prepare and send the message. It can be configured by clicking on the email label.

![](assets/email_designer_subject.png)

By clicking the **Edit** button, you can also add personalization fields and dynamic content to the subject line.
