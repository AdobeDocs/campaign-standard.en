---
title: Managing links
seo-title: Managing links
description: Managing links
seo-description: Discover the different links you can insert into any page element.
uuid: 13afe23c-6536-4300-a352-0f49f2befa58
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/designing/using/managing-links
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-06-25T08 45 08.718-0400
cq-lastreplicated: 2018-06-14T08 43 42.980-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: editing-message-and-landing-page-content
cq-template: /apps/help/templates/article-3
discoiquuid: 11bcdfcd-3d01-494c-969d-d89b6c9cbb53
firstPublishExternalDate: 2018-06-14T08:43:42.955-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-05-07T07 29 22.079-0400
jcr-createdby: admin
jcr-description: Managing links
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-06-14T08:43:42.955-0400
lochandoffdate: 2018-06-25T08 45 08.718-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Managing links
publishexternaldate: 2018-06-14T08 43 42.955-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/designing/using/managing-links.html
sha1: 3267e7a2fb554b57818d3c95509f751694a05d2e
topicBrowsingSortDate: 2018-06-14T08:43:42.955-0400
index: y
internal: n
snippet: y
---

# Managing links

Managing links

You can insert a link into any page element: image, word, group of words, block of text, etc.

There are several types of links:

* Link to an external URL: allows you to add a link to a URL. You can define personalization for your URLs, as detailed in [this section](../../designing/using/managing-links.md#personalizing-urls).
* Link that defines an action: allows you to define an action when an element in the landing page is clicked.

  >[!NOTE]
  >
  >This type of link is only available for landing pages.

* Link to a landing page: allows you to access an Adobe Campaign landing page.
* Subscription link: allows you to insert a link to subscribe to an Adobe Campaign service.
* Unsubscription link: allows you to insert a link to unsubscribe from an Adobe Campaign service.

## Adding a link

1. Select the element then use the corresponding button in the toolbar. Refer to [Toolbar](../../designing/using/content-editor-interface.md#toolbar).

   ![](assets/delivery_content_13.png)

1. Enter the link parameters:

   ![](assets/delivery_content_14.png)

    * Label
    * Link target: URL, action, landing page, or service

## Personalizing URLs

Adobe Campaign allows you to personalize one or several URLs in your delivery by adding personalization fields, content blocks, or dynamic content to them. To do this:

* Insert an external URL and specify its parameters.
* Click the **URL** button to access the personalization options.

  ![](assets/delivery_content_57.png)

* Add the personalization fields, content blocks, and dynamic contents that you want to use.

  ![](assets/delivery_content_58.png)

* Confirm your changes.

>[!NOTE]
>
>Personalizing URLs cannot be applied to the domain name, nor to the URL extension. An error message will be displayed during delivery analysis if personalization is incorrect.

To change a personalized URL, select it and use the **URL** button in the palette on the left-hand side.

The **Encoded value** option is checked by default. It allows for special characters to be encoded if they are present in the personalization field's value. We advise you to leave this option unchecked to avoid incorrect URL encoding.

![](assets/delivery_content_59.png) 

## Inserting tracking links

The content editor allows you to personalize your email by inserting links into the HTML content elements.

The following types of links are available:

* Link to an external URL
* Link to a landing page
* Subscription link
* Unsubscription link

>[!NOTE]
>
>The creation and configuration of these links are detailed in the section.

![](assets/delivery_content_edition4.png)

The **Tracked URLs** icon in the action bar automatically displays the list of all the URLs included in the content.

Tracking is activated by default.

![](assets/delivery_content_edition13.png)

>[!NOTE]
>
>This functionality is only available if tracking has been activated in Adobe Campaign.

The list of tracked URLs is divided into two zones:

* HTML, for the tracked URLs in the HTML content.
* Text, for the tracked URLs in the text content.

The label and the category of each URL can be modified directly from the list.

![](assets/delivery_content_edition14.png)

For each tracked URL you can activate or deactivate tracking.

![](assets/delivery_content_edition15.png)

>[!NOTE]
>
>The URLs are detected by Adobe Campaign if they start with: "&lt;%@" "&lt;!--" "[protocol]://"

You can regroup your URLs by editing the **Category** field, depending on the URLs used in the delivery. 

![](assets/delivery_content_edition18.png)

