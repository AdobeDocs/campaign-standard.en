---
title: Importing content from a URL
seo-title: Importing content from a URL
description: Importing content from a URL
seo-description: Learn how to load content from an existing URL when creating an email.
uuid: 9e4b7d33-61ac-48f8-be10-8fb389c0246f
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: loading-content
discoiquuid: e2b948e0-2d42-416b-a328-4a45cde97712
isreadyforlocalization: false
index: y
internal: n
snippet: y
---

# Importing content from a URL{#importing-content-from-a-url}

Importing content from a URL

Before importing content from a URL, make sure it follows the requirements below:

* The content needs to be publicly available via this URL.
* For security reasons, only URLs beginning with **[!UICONTROL https]** are allowed.
* Make sure that all resources (images, CSS) are set in absolute links and in HTTPS. Otherwise, after sending the email, the mirror page would be displayed without its resources. Here is an example of an absolute link definition:

  ```
  <a href="https://www.mywebsite.com/images/myimage.png">
  ```

>[!NOTE]
>
>Loading content from a URL is available for the email channel only.

To retrieve existing content form a URL, follow the steps below:

1. Click the **[!UICONTROL Change content]** icon, then select the **[!UICONTROL From URL]** element.

   ![](assets/email_designer_importfromurl.png)

1. Define the URL from which the content will be retrieved, then click **[!UICONTROL Confirm]** .

   ![](assets/email_designer_importfromurl1.png)

## Retrieving content from a URL automatically at preparation time {#retrieving-content-from-a-url-automatically-at-preparation-time}

Importing content from a URL during message preparation enables you to retrieve the latest HTML content each time the email is prepared. This way, the content of recurring emails is always up-to-date at the time of their sending. This feature also enables you to create a message scheduled at a specific date, even if the content is not ready yet.

To retrieve content at preparation time, follow the steps below:

1. Select the **[!UICONTROL Content imported during preparation]** option.

   ![](assets/email_designer_importfromurl2.png)

1. The URL content displays in the editor as read-only.

   >[!CAUTION]
   >
   >At this step, the HTML display in the content editor should not be taken into account. It will be retrieved at the preparation phase.

1. To preview the URL content that has been retrieved, open the message once it is created then click the **[!UICONTROL Preview]** button.

It is possible to personalize the remote URL from which the content will be retrieved. To do this, follow the steps below:

1. Click the **[!UICONTROL Email properties]** button, then edit the **[!UICONTROL Remote URL]** field.

   ![](assets/email_designer_importfromurl4.png)

1. Insert the desired personalization field, content block or dynamic text then click **[!UICONTROL Save]** .

   The **[!UICONTROL Current date - YYYYMMDD]** content block, for example, enables you to insert the date of the day.

   >[!NOTE]
   >
   >The available personalization fields are linked to **Delivery** attributes only (email creation date, status, campaign label...).

   ![](assets/email_designer_importfromurl5.png)

