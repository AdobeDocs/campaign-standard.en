---
title: "Example: Email personalization"
seo-title: "Example: Email personalization"
description: "Example: Email personalization"
seo-description: See a full example of personalizing an email with dynamic content and text according to the profiles' ages.
uuid: a51a44da-c2db-4596-86de-57a4b7084358
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: personalizing-content
discoiquuid: a7f76948-6fff-482c-8c83-8abf6c84a1e4
index: y
internal: n
snippet: y
---

# Example: Email personalization{#example-email-personalization}

Example: Email personalization

In this example, a member of the marketing service team has created an email to inform some of his clients that there is a special offer just for them. The team member decided to personalize the email according to the clients' respective ages. Clients aged between 18 and 27 years old will receive an email containing a different image and slogan to those that the clients older than 27 will receive.

The email is created as follows:

* Dynamic contents are applied to the image and these dynamic contents are configured according to age range.

  ![](assets/delivery_content_43.png)

  Adding and configuring dynamic content is detailed in the [Defining dynamic content in an email](../../designing/using/defining-dynamic-content-in-an-email.md) section.

* Personalization fields and dynamic contents are applied to the text. Depending on the age range of the profile, the email starts with either the profile's first name, or the profile's title and last name.

  ![](assets/delivery_content_44.png)

  Adding and configuring the personalization fields is detailed in the [Inserting a personalization field](../../designing/using/inserting-a-personalization-field.md) section.

## Configuring images {#configuring-images}

In this example, the dynamic contents applied to the images are configured as follows:

**To target 18-27-year-old:**

1. Select the dynamic content in the **[!UICONTROL Properties]** palette and click the **[!UICONTROL Edit]** button.

   ![](assets/delivery_content_48.png)

1. Edit the label then select the **[!UICONTROL Age]** field from the **[!UICONTROL Profile]** node.

   ![](assets/delivery_content_49.png)

1. Select the **Greater than or equal to** operator then enter **18** to create the **older than 18** expression.

   ![](assets/delivery_content_50.png)

1. Add a new **[!UICONTROL Age]** condition.

   Select the **Less than or equal to** operator followed by 27 in the value field to create the **younger than 27** expression.

   ![](assets/delivery_content_51.png)

1. Confirm your changes.

**To target profiles aged 27 and above:**

1. Select the dynamic content from the palette and edit it.
1. Edit the label then select the **[!UICONTROL Age]** field from the **[!UICONTROL Profile]** node.
1. Add the **Greater than** operator followed by 27 in the value field to create the **older than 27** expression.

   ![](assets/delivery_content_52.png)

1. Confirm your changes.

Your dynamic contents are correctly configured.

## Configuring text {#configuring-text}

In this example, the dynamic contents applied to the texts are configured as follows:

**To target profiles aged between 18-27:**

1. Select the structure component you want and add a dynamic content.
1. Edit the dynamic content and configure the targeting expressions. Refer to [Configuring images](../../designing/using/example--email-personalization.md#configuring-images).
1. In the structure component, at the desired position, click the **[!UICONTROL Personalize]** icon from the contextual toolbar and select **[!UICONTROL Insert personalization field]** .

   ![](assets/delivery_content_53.png)

1. In the list that appears, select the **[!UICONTROL First name]** field and confirm.

   ![](assets/delivery_content_54.png)

1. Your personalization field is then perfectly inserted into the dynamic content selected.

**To target profiles aged 27 and above:**

1. Select the structure component you want and add a dynamic content.
1. Edit the dynamic content and configure the targeting expressions. Refer to [Configuring images](../../designing/using/example--email-personalization.md#configuring-images).
1. In the structure component, at the desired position, click the **[!UICONTROL Personalize]** icon from the contextual toolbar and select **[!UICONTROL Insert personalization field]** .
1. Select **[!UICONTROL Title]** from the drop-down list.
1. Proceed similarly to add the **[!UICONTROL Last name]** field.

   ![](assets/delivery_content_56.png)

Your personalization fields should now be perfectly inserted into the chosen dynamic content.

## Previewing emails {#previewing-emails}

Previewing allows you to check that the personalization fields and the dynamic contents are configured correctly before sending the **[!UICONTROL Proofs]** . During the preview, you can select different test profiles corresponding to the email targets.

Without test profiles, the email that appears by default is:

![](assets/delivery_content_45.png)

The email does not have personalization fields in the slogan, and the default image is used.

The first test profile corresponds to a client aged between 18 and 27. By selecting this profile, the following email appears:

![](assets/delivery_content_46.png)

The personalization field that corresponds to the 18-27-year-old expression, specifically the profile's first name, is configured correctly and the image has also changed according to the profile.

The second profile corresponds to a client aged over 27 and generates the following email:

![](assets/delivery_content_47.png)

The image has changed thanks to the dynamic content, and the slogan that appears is the more formal slogan defined for this targeted public.

**Related topics:**

* [Creating audiences](../../audiences/using/creating-audiences.md)
* [Preparing the send](../../sending/using/preparing-the-send.md)

