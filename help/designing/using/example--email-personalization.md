---
title: "Example: Email personalization"
seo-title: "Example: Email personalization"
description: "Example: Email personalization"
seo-description: See a full example of personalizing an email with dynamic content and text according to the recipients' ages.
uuid: 226e2458-15d5-47e2-8d72-35fff8c3cc06
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/designing/using/example--email-personalization
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-10T07 25 28.819-0400
cq-lastreplicated: 2018-09-07T15 03 22.627-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: personalizing-content
cq-template: /apps/help/templates/article-3
discoiquuid: 320405ff-cbcd-4fa9-89c5-393af5ceddd7
firstPublishExternalDate: 2018-09-07T15:03:19.887-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 02.752-0400
jcr-createdby: admin
jcr-description: Example  Email personalization
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T15:03:19.887-0400
lochandoffdate: 2018-09-10T07 25 28.817-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: "Example: Email personalization"
publishexternaldate: 2018-09-07T15 03 19.887-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/designing/using/example--email-personalization.html
sha1: 25ee2deff484385dd6e9953b5f80678be4ba5791
topicBrowsingSortDate: 2018-09-07T15:03:19.887-0400
index: y
internal: n
snippet: y
---

# Example: Email personalization{#example-email-personalization}

Example: Email personalization

In this example, a member of the marketing service team has created an email to inform some of his clients that there is a special offer just for them. The team member decided to personalize the email according to the clients' respective ages. Clients aged between 18 and 27 years old will receive an email containing a different image and slogan to those that the clients that are older than 27 will receive.

>[!NOTE]
>
>The images below show how to personalize an email using the [content editor](../../designing/using/about-email-content-design.md#using-the-email-content-editor).

The email is created as follows:

* Dynamic contents are applied to the image and these dynamic contents are configured according to age range.

  Adding and configuring dynamic content is detailed in the [Defining dynamic content in a landing page](../../designing/using/defining-dynamic-content-in-a-landing-page.md) section.

  ![](assets/delivery_content_43.png)

* Personalization fields and dynamic contents are applied to the text. Depending on the age range of the recipient, the email starts with either the title and last name of the recipient, or by the recipient's first name.

  Adding and configuring the personalization fields is detailed in the [Inserting a personalization field](../../designing/using/inserting-a-personalization-field.md) section.

  ![](assets/delivery_content_44.png)

## Configuring images {#configuring-images}

In this example, the dynamic contents applied to the images are configured as follows:

**To target 18-27-year-old:**

1. Select the dynamic content in the **Properties** palette and click the **Edit** button.

   ![](assets/delivery_content_48.png)

1. Edit the label then select the **Age** field from the **Profile** node.

   ![](assets/delivery_content_49.png)

1. Select the **Greater than or equal to** operator then enter **18** to create the **older than 18** expression.

   ![](assets/delivery_content_50.png)

1. Add a new **Age** condition.

   Select the **Less than or equal to** operator followed by 27 in the value field to create the **younger than 27** expression.

   ![](assets/delivery_content_51.png)

1. Confirm your changes.

**To target profiles aged 27 and above:**

1. Select the dynamic content from the palette and edit it.
1. Edit the label then select the **Age** field from the **Profile** node.
1. Add the **Greater than** operator followed by 27 in the value field to create the **older than 27** expression.

   ![](assets/delivery_content_52.png)

1. Confirm your changes.

Your dynamic contents are correctly configured.

## Configuring text {#configuring-text}

In this example, the dynamic contents applied to the texts are configured as follows:

**To target profiles aged between 18-27:**

1. Select the text block you want and add a dynamic content.
1. Edit the dynamic content and configure the targeting expressions. Refer to [Configuring images](../../designing/using/example--email-personalization.md#configuring-images).
1. Select the text block again, and hover the cursor over the start of the sentence. Click the **Insert personalization field** option.

   ![](assets/delivery_content_53.png)

1. In the list that appears, select the **First name** field and confirm.

   ![](assets/delivery_content_54.png)

1. Your personalization field is then perfectly inserted into the dynamic content selected.

**To target recipients aged 27 and above:**

1. Select the text block you want and add a dynamic content.
1. Edit the dynamic content and configure the targeting expressions. Refer to [Configuring images](../../designing/using/example--email-personalization.md#configuring-images).
1. In the text block, hover the cursor over where you would like to add the personalization field.
1. Click the **Insert personalization field** option.
1. Select **Title** from the drop-down list.
1. Confirm and then click the **Insert personalization field** option again to add the **Last name** field.

   ![](assets/delivery_content_56.png)

Your personalization fields should now be perfectly inserted into the chosen dynamic content.

## Previewing emails {#previewing-emails}

Previewing allows you to check that the personalization fields and the dynamic contents are configured correctly before sending the **Proofs**. During the preview, you can select different test profiles corresponding to the email targets.

Without test profiles, the email that appears by default is:

![](assets/delivery_content_45.png)

The email does not have personalization fields in the slogan, and the default image is used.

The first test profile corresponds to a client aged between 18 and 27. By selecting this profile, the following email appears:

![](assets/delivery_content_46.png)

The personalization field that corresponds to the 18-27-year-old expression, specifically the recipient's first name, is configured correctly and the image has also changed according to the profile.

The second profile corresponds to a client aged over 27 and generates the following email:

![](assets/delivery_content_47.png)

The image has changed thanks to the dynamic content, and the slogan that appears is the more formal slogan defined for this targeted public.

**Related topics:**

* [Creating audiences](../../audiences/using/creating-audiences.md)
* [Preparing the send](../../sending/using/preparing-the-send.md)

