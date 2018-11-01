---
title: Adding links and URL tracking
seo-title: Adding links and URL tracking
description: Adding links and URL tracking
seo-description: Learn how to add links to the HTML content elements of an email.
uuid: d0835346-528d-4e71-860d-abb1bf75097b
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/designing/using/adding-links-and-url-tracking
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-06-25T08 45 21.973-0400
cq-lastreplicated: 2018-06-14T08 43 53.585-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: designing-email-content
cq-template: /apps/help/templates/article-3
discoiquuid: d3bc6f76-3b21-4ba6-8917-3a17d0d97748
firstPublishExternalDate: 2018-06-14T08:43:53.561-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-27T07 29 05.497-0400
jcr-createdby: admin
jcr-description: Adding links and URL tracking
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-06-14T08:43:53.561-0400
lochandoffdate: 2018-06-25T08 45 21.973-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Adding links and URL tracking
publishexternaldate: 2018-06-14T08 43 53.561-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/designing/using/adding-links-and-url-tracking.html
sha1: 0d3ab36ee5c6d85bc14d61b27ed56090370f9639
topicBrowsingSortDate: 2018-06-14T08:43:53.561-0400
index: y
internal: n
snippet: y
---

# Adding links and URL tracking

Adding links and URL tracking

The editor allows you to personalize your email by inserting links into the HTML content elements. A menu summarizes all the URLs of your email that will be tracked.

## <p>Inserting a link</p>

You can insert a link into any page element: image, word, group of words, block of text, etc.

1. Select **Link** in the toolbar.
1. Choose the type of link you want to create:

    * Link to an external URL: allows you to add a link to a URL.
    * Link to a landing page: allows you to access an Adobe Campaign landing page.
    * Subscription link: allows you to insert a link to subscribe to an Adobe Campaign service.
    * Unsubscription link: allows you to insert a link to unsubscribe from an Adobe Campaign service.

1. Enter the link parameters:

    * Label: text displayed to the profile.
    * Link target: URL, action, landing page, or service

   ![](assets/email_designer_createlink.png)

1. Validate the link creation.

Once the link is created, you can still modify it by selecting it and re-opening the link popup, by editing the link target directly in the settings of the element displayed next to the email, or from the **Tracked URLs** overview, as described below.

## <p>About tracked URLs</p>

The **Tracked URLs** icon in the action bar automatically displays the list of all the URLs included in the content.

Tracking is activated by default.

>[!NOTE]
>
>This functionality is only available if tracking has been activated in Adobe Campaign.

The label, category, URL and tracking type of each link can be modified directly from this list.

For each tracked URL you can activate or deactivate tracking.

![](assets/email_designer_trackedurls.png)

>[!NOTE]
>
>The URLs are detected by Adobe Campaign if they start with: "&lt;%@" "&lt;!--" "[protocol]://"

You can regroup your URLs by editing the **Category** field, depending on the URLs used in the delivery. 
