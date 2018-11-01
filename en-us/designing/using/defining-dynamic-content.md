---
title: Defining dynamic content
seo-title: Defining dynamic content
description: Defining dynamic content
seo-description: Follow these steps to display different contents dynamically to the user according to the conditions defined through the Adobe Campaign expression editor.
uuid: 8de622c8-3b45-41f4-afed-197aeb8005b5
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/designing/using/defining-dynamic-content
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-06-25T08 45 12.478-0400
cq-lastreplicated: 2018-06-14T08 43 46.260-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: editing-message-and-landing-page-content
cq-template: /apps/help/templates/article-3
discoiquuid: 53542981-a98d-4bd9-8f1b-aea0c1a48334
firstPublishExternalDate: 2018-06-14T08:43:46.226-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 13.738-0400
jcr-createdby: admin
jcr-description: Defining dynamic content
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-06-14T08:43:46.226-0400
lochandoffdate: 2018-06-25T08 45 12.478-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Defining dynamic content
publishexternaldate: 2018-06-14T08 43 46.226-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/designing/using/defining-dynamic-content.html
sha1: f96a56603c44c6d23ca9f47de4db8819b67e8b13
topicBrowsingSortDate: 2018-06-14T08:43:46.226-0400
index: y
internal: n
snippet: y
---

# Defining dynamic content

Defining dynamic content

You can define different contents which will be displayed dynamically to the user according to the conditions defined via the expression editor. For example, from the same email, you can ensure that the recipients receive a different message according to their age range.

1. Select a block using the breadcrumb or by directly clicking an element.

   >[!NOTE]
   >
   >Certain blocks, such as images, cannot be directly selected. In this case, select the parent block using the breadcrumb. You can then modify all of the elements included in this parent element, including images. The condition will be applied to all child elements within the parent block. The breadcrumb is presented in the [Managing blocks](../../designing/using/managing-content-structure-and-style.md) section.

   ![](assets/delivery_content_32.png)

1. Select the **Dynamic content** icon.

   ![](assets/delivery_content_25.png)

1. The **Dynamic content** section then appears in the palette.

   By default, this section contains two elements: the default content and a new content.

   You cannot delete the default content. The content editor must always have a default variant.

   ![](assets/delivery_content_26.png)

   >[!NOTE]
   >
   >If an element is outlined in red, this means that an expression has not yet been defined.

1. Click the **Create** button to add a new content and its linked rule.

   ![](assets/delivery_content_34.png)

1. To define a content's display conditions, click it. A contextual menu is displayed.

   ![](assets/delivery_content_27.png)

1. Use the **Edit** button to open the expression editor and define a condition.

   ![](assets/delivery_content_28.png)

   For each content, you can specify a label and define the order of priority in which the condition will be applied. The contents will be displayed in the palette in order of priority, from left to right. For more on order of priority, refer to [this section](../../designing/using/defining-dynamic-content.md#order-of-priority). 

1. Once you have entered and confirmed an expression, you can make any changes you would like to the corresponding block in the editing zone.

   ![](assets/delivery_content_33.png)

>[!CAUTION]
>
>In this case, once you have prepared your message and before sending it, don't forget to test it using a proof. If you do not do this, any errors may not be detected and the email may not be sent.

**Related topics:**

* [Sending proofs](../../sending/using/managing-test-profiles-and-sending-proofs.md#sending-proofs)
* [Advanced expression editing](../../automating/using/editing-queries.md#about-query-editor)

## <p>Previewing dynamic contents</p>

You can navigate between the different dynamic contents of an image block or a block of text. To do this:

* Select the content block.

  Arrows appear on the right- and left-hand sides of the image.

  ![](assets/delivery_content_35.png)

* Click the right arrow to browse through the available dynamic contents.

  ![](assets/delivery_content_36.png)

  The arrows on each side dim according to whether you have reached the last or first available dynamic contents.

  ![](assets/delivery_content_37.png)

In the palette:

* The contents which have an expression entered are no longer outlined in red, they are shown in gray.
* If a label was defined for a content, that label then replaces the word "Label" and the new label name also appears whenever the content is hovered over.
* The content that is currently selected appears in blue.

![](assets/delivery_content_31.png)

To delete all the conditions applied to a block, select the block in question and click the **Dynamic content** icon.

A new window appears. From this window you can select the dynamic content that you would like to keep.

![](assets/delivery_content_38.png)

## <p>Order of priority</p>

In the expression editor, when you define a dynamic content, the order of priority works as follows:

1. You define two different dynamic contents with **two different conditions**, for example:

   **Condition 1:** the gender of the profile is masculine,

   **Condition 2:** the profile is between 20 and 30 years old.

   ![](assets/delivery_content_61.png)

   Some profiles in your database correspond to the two conditions but only one email with one dynamic content can be sent.

1. You therefore have to define the priority for the dynamic contents. A condition with an order of priority of **1** (and therefore the corresponding dynamic content) will be sent to a profile even if another condition whose priority order is **2** or **3** is also met by this profile.

   ![](assets/delivery_content_62.png)

>[!CAUTION]
>
>You can only define one order of priority per dynamic content.

## <p>Defining dynamic text</p>

Dynamic text functions in the same way as **dynamic content**. Refer to the section.

You can define dynamic text

* in an email subject,
* in HTML mode,
* in text mode.

To define dynamic text:

1. Select text in the body of your email.

   ![](assets/delivery_content_39.png)

1. Click **Enable dynamic text**.

   ![](assets/delivery_content_40.png)

   The **Dynamic text** option then appears in the palette.

   It is configured in the same way as dynamic content.

   ![](assets/delivery_content_41.png)

   A purple frame appears around dynamic text in the body of the email.

   ![](assets/delivery_content_42.png)

