---
title: Defining the direct mail content
seo-title: Defining the direct mail content
description: Defining the direct mail content
seo-description: Learn how to define the content for your direct mail delivery.
uuid: 20cf19f3-c84c-42d5-a822-efc67c9e5a28
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/channels/using/defining-the-direct-mail-content
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-08T08 23 17.320-0400
cq-lastreplicated: 2018-09-07T15 12 27.085-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: direct-mail
cq-template: /apps/help/templates/article-3
discoiquuid: e2f27d55-61e2-407a-9cdf-268d92a06d57
firstPublishExternalDate: 2018-09-07T15:12:27.047-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 07.731-0400
jcr-createdby: admin
jcr-description: Defining the direct mail content
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T15:12:27.047-0400
lochandoffdate: 2018-09-08T08 23 17.319-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Defining the direct mail content
publishexternaldate: 2018-09-07T15 12 27.047-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/channels/using/defining-the-direct-mail-content.html
sha1: fb0d1d42586136b5413f17108103c8488d8af87d
topicBrowsingSortDate: 2018-09-07T15:12:27.047-0400
index: y
internal: n
snippet: y
---

# Defining the direct mail content

Defining the direct mail content

You can either define the content in the last screen of the creation wizard or by clicking on the **Content** section of the delivery dashboard.

![](assets/direct_mail_6.png)

The **Content** definition screen is specific to the direct mail channel. It is divided into four tabs: **Extraction**, **File structure**, **Header** and **Footer**.

![](assets/direct_mail_11.png)

## Defining the extraction

1. Start by defining the name of the extraction file. Click on the button to the right of the **Output file** field and enter the desired label. You can use personalization fields, content blocks and dynamic text (see [Defining content](../../designing/using/example--email-personalization.md)). For example, you can complete the label with the delivery ID or the extraction date. 

   ![](assets/direct_mail_12.png)

1. Click the **+** or **Add an element** button to add an output column. The **Output columns** let you define the profile information (columns) to be exported into the output file.

   >[!CAUTION]
   >
   >Make sure that your profiles include a postal address as this information is essential to the direct mail provider. Also make sure you have checked the **Address specified** box in your profiles' information. See [Recommendations](../../channels/using/about-direct-mail.md#recommendations).

   ![](assets/direct_mail_13.png)

1. Create as many columns as you need. You can edit columns by clicking their expressions and labels.

>[!NOTE]
>
>For more information on output column definition, refer to the [Extract file](../../automating/using/extract-file.md) workflow activity section.

## Defining the file structure

The **File structure** tab allows you to configure the output, date, and number formats for the file that will be exported.

![](assets/direct_mail_14.png)

>[!NOTE]
>
>The available options are detailed in the [Extract file](../../automating/using/extract-file.md) workflow activity sections.

## Defining the header and footer

Sometimes you may need to add information at the beginning or at the end of the extraction file. For this, use the **Header** and **Footer** tabs of the **Content** configuration screen. 

![](assets/direct_mail_7.png)

For example, you might want to include, for the direct mail provider, the sender information in the header of the file. It is possible to personalize the footer and header with information available in the context of the delivery. See [Defining content](../../designing/using/example--email-personalization.md).

The sender address is defined in the **Send** section of the direct mail properties or at the template level.

![](assets/direct_mail_24.png)

