---
title: Defining dynamic content in an email
seo-title: Defining dynamic content in an email
description: Defining dynamic content in an email
seo-description: Follow these steps to display different contents dynamically in an email according to the conditions defined through the Adobe Campaign expression editor.
uuid: 1fa39743-0b8e-4f5d-a632-a415e09961ec
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: defining-conditional-content
discoiquuid: fb894e71-e1a2-4aed-b89e-072c75bc8288
index: y
internal: n
snippet: y
---

# Defining dynamic content in an email{#defining-dynamic-content-in-an-email}

Defining dynamic content in an email

In an email, you can define different contents which will be displayed dynamically to the recipients according to the conditions defined via the expression editor. For example, from the same email, you can ensure that each profile receives a different message according to their age range.

Defining dynamic content is different from [defining visibility conditions](../../designing/using/defining-a-visibility-condition.md).

1. Select a fragment, a component or an element. In this example, select an image.
1. Click the **[!UICONTROL Dynamic content]** icon from the contextual toolbar.

   ![](assets/dynamic_content_2.png)

   The **[!UICONTROL Dynamic content]** section appears in the palette on the left.

   ![](assets/dynamic_content_3.png)

   By default, this section contains two elements: the default variant and a new variant.

   >[!NOTE]
   >
   >The content must always have a default variant. You cannot delete it.

1. Click the **[!UICONTROL Edit]** button to define the display conditions for the first alternative variant.

   ![](assets/dynamic_content_4.png)

1. Specify a label and select the fields that you want to set as conditions. For example, from the **[!UICONTROL General]** node, select the **[!UICONTROL Age]** field

   ![](assets/dynamic_content_5.png)

1. Set the filtering conditions. For example, you want a different content to be displayed to people aged between 18 and 25 years old.

   ![](assets/dynamic_content_6.png)

1. Once all the conditions are set, define the order of priority in which the condition will be applied and save your changes.

   ![](assets/dynamic_content_7.png)

   The contents will be displayed in the palette in order of priority, from top to bottom. For more on priorities, refer to [this section](../../designing/using/defining-dynamic-content-in-an-email.md#order-of-priority).

1. Upload a new image for the variant you just defined.

   ![](assets/dynamic_content_8.png)

   The recipients aged between 18 and 25 years old will see the new image.

   ![](assets/dynamic_content_10.png)

1. Click **[!UICONTROL Add a condition]** to add a new content and its linked rule.

   ![](assets/dynamic_content_9.png)

   For example, you can add a different image to be displayed to people aged between 26 and 35 years old.

1. Proceed similarly for any other element of your email that you want to be displayed dynamically. It can be text, button, fragment, etc. Save your changes.

>[!CAUTION]
>
>Once you have prepared your message and before sending it, test it using a proof. If you do not do this, some errors may not be detected and the email may not be sent.

**Related topics:**

* [Sending proofs](../../sending/using/managing-test-profiles-and-sending-proofs.md#sending-proofs)
* [Advanced expression editing](../../automating/using/editing-queries.md#about-query-editor)

## Order of priority {#order-of-priority}

In the expression editor, when you define a dynamic content, the order of priority is as follows.

1. You define two different dynamic contents with **two different conditions**, for example:

   **Condition 1:** the gender of the profile is masculine,

   **Condition 2:** the profile is between 20 and 30 years old.

   ![](assets/delivery_content_61.png)

   Some profiles in your database correspond to the two conditions but only one email with one dynamic content can be sent.

1. You therefore have to define the priority for the dynamic contents. A condition with an order of priority of **1** (and therefore the corresponding dynamic content) will be sent to a profile even if another condition whose priority order is **2** or **3** is also met by this profile.

   ![](assets/delivery_content_62.png)

You can only define one order of priority per dynamic content.
