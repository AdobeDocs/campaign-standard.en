---
title: Importing content from a URL
seo-title: Importing content from a URL
description: Importing content from a URL
seo-description: 
uuid: 8a842d50-250a-48b3-9e51-74c4a61b0757
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/designing/using/importing-content-from-a-url
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-26T02 53 40.607-0400
cq-lastmodifiedby: mancini
cq-lastreplicated: 2018-07-23T08 13 39.613-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: loading-content
cq-template: /apps/help/templates/article-3
discoiquuid: 7e78c7d0-1ec0-4ebe-8800-46a524cc8488
firstPublishExternalDate: 2018-07-23T05:58:19.358-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-07-23T07 30 15.414-0400
jcr-createdby: admin
jcr-description: Importing content from a URL
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T08:13:39.572-0400
lochandoffdate: 2018-07-26T02 53 40.606-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
moreHelpPaths: /content/help/en/campaign/standard/designing/morehelp/loading-content;/content/help/en/campaign/standard/designing/morehelp/loading-content
navTitle: Importing content from a URL
publishexternaldate: 2018-07-23T08 13 39.572-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/designing/using/importing-content-from-a-url.html
sha1: 92538b99fb8ad30d3504ed32f692d425b5cd633d
topicBrowsingSortDate: 2018-07-23T08:13:39.572-0400
index: y
internal: n
snippet: y
---

# Importing content from a URL

Importing content from a URL

Before importing content from a URL, make sure it follows the requirements below:

* The content needs to be publicly available via this URL.
* For security reasons, only URLs beginning with **https** are allowed.
* Make sure that all resources (images, CSS) are set in absolute links and in HTTPS. Otherwise, after sending the email, the mirror page would be displayed without its resources. Here is an example of an absolute link definition:

  ```
  <a href="https://www.mywebsite.com/images/myimage.png">
  ```

To retrieve existing content form a URL, follow the steps below:

1. Click the **From URL** element.
1. Define the URL from which the content will be retrieved, then confirm.

   ![](assets/email_designer_importfromurl.png)

## Retrieving content from a URL automatically at preparation time

Importing content from a URL at the delivery preparation phase enables you to retrieve the latest HTML content each time the delivery is prepared. This way, the content of recurring emails is always up-to-date at the time of their sending. This feature also enables you to create a delivery scheduled at a specific date, even if the content is not ready yet.

>[!NOTE]
>
>This feature is only available for now in email deliveries that are created within the [content editor](../../designing/using/about-email-content-design.md#using-the-email-content-editor). It is not yet available in the [Creative Designer](../../designing/using/about-email-content-design.md#using-the-creative-designer).

To retrieve content at the delivery preparation phase, follow the steps below:

1. Select the **Content imported during preparation** option.

   ![](assets/email_designer_importfromurl2.png)

1. The URL content displays in the editor as read-only.

   ![](assets/email_designer_importfromurl3.png)

   >[!CAUTION]
   >
   >At this step, the HTML display in the content editor should not be taken into account. It will be retrieved at the delivery preparation phase.

1. To preview the URL content that has been retrieved, open the delivery once it is created then click the **Preview** button.

It is possible to personalize the remote URL from which the content will be retrieved. To do this, follow the steps below:

1. Click the **Remote URL** field button.

   ![](assets/email_designer_importfromurl4.png)

1. Insert the desired personalization field, content block or dynamic text then click **Confirm**.

   The **Current date - YYYYMMDD** content block, for example, enables you to insert the date of the day.

   >[!NOTE]
   >
   >The available personalization fields are linked to **Delivery** attributes only (delivery creation date, status, campaign label...).

   ![](assets/email_designer_importfromurl5.png)

