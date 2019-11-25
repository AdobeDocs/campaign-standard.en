---
title: About APIs use cases
description: Learn more on how use cases you can perform with APIs.
page-status-flag: never-activated
uuid: c7b9c171-0409-4707-9d45-3fa72aee8008
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
discoiquuid: 304e7779-42d2-430a-9704-8c599a4eb1da

internal: n
snippet: y
---

# About Campaign Standard APIs use cases {#about-apis-use-cases}

In this section, you will find various use cases you can perform Campaign Standard APIs.

Moreover, a collection of requests is available to help you familiarize yourself with Campaign Standard APIs requests. This collection in JSON format provides pre-designed API requests representing common use cases.

The steps below describe a step-by-step use case to import and use the collection to create a profile in Campaign Standard database.

>[!NOTE]
>
>Our example uses Postman. However, feel free to use your favorite REST client.

1. Download the JSON collection by clicking [here](https://helpx.adobe.com/content/dam/help/en/campaign/kb/working-with-acs-api/_jcr_content/main-pars/download_section/download-1/KB_postman_collection.json.zip).

1. Open Postman, then select the **File** / **Import** menu.

1. Drag and drop the downloaded file into the window. Pre-designed API requests display, ready to be used.

    ![alt text](assets/postman_collection.png)

1. Select the **Creating a profile** request, then update the POST request and the **Headers** tab with your own information (&lt;ORGANIZATION&gt;, &lt;API_KEY&gt;, &lt;ACCESS_TOKEN&gt;). For more on this, refer to [this section](../../api/using/setting-up-api-access.md).

    ![alt text](assets/postman_uc1.png)

1. Fill in the **Body** tab with the information you want to add to the new profile, then click the **Send** button to execute the request.

    ![alt text](assets/postman_uc2.png)

1. Once an object created, a primary key (PKey) is associated to it. It is visible in the resquest response, as well as other attributes.

    ![alt text](assets/postman_uc3.png)

1. Open your Campaign Standard instance, then check that the profile is created, with all the information from the payload.

    ![alt text](assets/postman_uc4.png)
