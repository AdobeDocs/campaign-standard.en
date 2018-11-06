---
title: Loading an existing content
seo-title: Loading an existing content
description: Loading an existing content
seo-description: Learn how to select or import content for your messages with Adobe Campaign.
uuid: cfe0ae2d-36d7-43f7-bea0-d8ff10b7cc0b
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/designing/using/loading-an-existing-content
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-06-25T08 45 16.577-0400
cq-lastreplicated: 2018-06-14T08 43 48.620-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: designing-email-content
cq-template: /apps/help/templates/article-3
discoiquuid: 19bc520a-2d5b-446d-b810-6f2be859cacc
firstPublishExternalDate: 2018-06-14T08:43:48.542-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-27T07 29 06.045-0400
jcr-createdby: admin
jcr-description: Loading an existing content
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-06-14T08:43:48.542-0400
lochandoffdate: 2018-06-25T08 45 16.576-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Loading an existing content
publishexternaldate: 2018-06-14T08 43 48.542-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/designing/using/loading-an-existing-content.html
sha1: 6b2652f65906a13e8c2417a906893c8716f2ff99
topicBrowsingSortDate: 2018-06-14T08:43:48.542-0400
index: y
internal: n
snippet: y
---

# Loading an existing content

Loading an existing content

When creating an email, you can choose between starting from a blank content and loading an existing content from another source.

1. Open the Creative Designer.
1. Select **Change content**.
1. Select the source of the content you want to load:

    * [Content templates](../../start/using/about-templates.md#content-templates)
    * [Content from your computer as a ZIP or HTML file](../../designing/using/loading-an-existing-content.md#importing-content-from-a-file)
    * [Content from an existing URL](../../designing/using/loading-an-existing-content.md#importing-content-from-a-url)
    * Content from scratch, to start fresh.

1. Load the content. The selected content replaces the current content.

   Once imported, the content can be edited and personalized.

   >[!NOTE]
   >
   >The Creative Designer uses specific tagging. Standard HTML content uploaded to Campaign have to match the expected tagging to be fully compatible and editable from the Creative Designer. If not matching, your content is uploaded in [compatibility mode](../../designing/using/about-the-creative-designer.md#about-compatibility-mode).

## Importing content from a file

Click the **From a file** element to upload a file from your computer, then confirm.

There are no constraints on the zip file structure. However, referencing HTML files has to be relative and respect the tree structure of the zip folder.

The following formats are supported for import:

* an HTML file with an incorporated style sheet.
* a .zip folder containing the HTML file, the style sheet (.CSS) and the images.

>[!NOTE]
>
>For email content, we recommend that you import single HTML files with an incorporated style sheet.

## Importing content from a URL

Click the **From URL** element to import HTML content from an existing URL, then confirm.

>[!CAUTION]
>
>The content needs to be publicly available via this URL. For security reasons, only URLs beginning with **https** are allowed.

Make sure that all resources (images, CSS) are set in absolute links and in HTTPS. Otherwise, after sending the email, the mirror page would be displayed without its resources. Here is an example of an absolute link definition:

```
<a href="https://www.mywebsite.com/images/myimage.png">
```

![](assets/email_designer_importfromurl.png)

