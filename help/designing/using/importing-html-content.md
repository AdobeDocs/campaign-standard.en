---
title: Importing HTML content
seo-title: Importing HTML content
description: Importing HTML content
seo-description: Learn how to select or import content for your messages with Adobe Campaign.
uuid: 05f76765-e556-4805-b902-4eb36a83f928
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/designing/using/importing-html-content
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-06-25T08 45 01.814-0400
cq-lastreplicated: 2018-06-14T08 43 39.158-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: editing-message-and-landing-page-content
cq-template: /apps/help/templates/article-3
discoiquuid: baf9f6f5-c7c9-4152-8dc7-e3b6cb91a72a
firstPublishExternalDate: 2018-06-14T08:43:39.127-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 01 35.646-0400
jcr-createdby: admin
jcr-description: Importing HTML content
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-06-14T08:43:39.127-0400
lochandoffdate: 2018-06-25T08 45 01.814-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Importing HTML content
publishexternaldate: 2018-06-14T08 43 39.127-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/designing/using/importing-html-content.html
sha1: 8c5fa31749638d250f0d0ffd6eb1f7a051390195
topicBrowsingSortDate: 2018-06-14T08:43:39.127-0400
index: y
internal: n
snippet: y
---

# Importing HTML content

Importing HTML content

Adobe Campaign comes with a set of predefined contents to help you get started. You can use one of these or, if the content of the message you need to send is being prepared outside of Adobe Campaign, you can import it from your computer or a URL.

The content of the message can be changed from the content editor.

>[!CAUTION]
>
>The selected content replaces the current content. Make sure the HTML content is valid before importing (text layout, image location for example): Adobe Campaign will not perform any validation.

1. Click the **Change content** button in the action bar.

   ![](assets/delivery_content_edition.png)

1. Choose the type of content you want to import, then confirm.

    * [Out-of-the-box templates](../../start/using/about-templates.md#content-templates)
    * [Content from your computer as a ZIP or HTML file](../../designing/using/importing-html-content.md#importing-content-from-a-file)
    * [Content from an existing URL](../../designing/using/importing-html-content.md#importing-content-from-a-url)

   ![](assets/delivery_content_edition1.png)

1. The HTML template is uploaded in the content editing zone. Once imported, the content can be edited and personalized as usual.

   ![](assets/delivery_content_edition2.png)

**Related topics:**

* [Creating an email](../../channels/using/creating-an-email.md)
* [Managing landing pages](../../channels/using/about-landing-pages.md)
* [Content templates](../../start/using/about-templates.md#content-templates)

## Importing content from a file

Click the **From a file** element to upload a file from your computer, then confirm.

There are no constraints on the zip file structure. However, referencing HTML files has to be relative and respect the tree structure of the zip folder.

The following formats are supported for import:

* an HTML file with an incorporated style sheet
* a .zip folder containing the HTML file, the style sheet (.CSS) and the images

>[!NOTE]
>
>For email content, we recommend that you import single HTML files with an incorporated style sheet.

![](assets/delivery_content_edition1_fromFile.png) 

## Importing content from a URL

Click the **From URL** element to import HTML content from an existing URL, then confirm.

![](assets/delivery_content_edition1_fromURL.png)

>[!CAUTION]
>
>The content needs to be publicly available via this URL. For security reasons, only URLs beginning with **https** are allowed.

Make sure that all resources (images, CSS) are set in absolute links and in HTTPS. Otherwise, after sending the email, the mirror page would be displayed without its resources. Here is an example of an absolute link definition:

```
<a href="https://www.mywebsite.com/images/myimage.png">
```

![](assets/delivery_content_edition_importURL.png)

