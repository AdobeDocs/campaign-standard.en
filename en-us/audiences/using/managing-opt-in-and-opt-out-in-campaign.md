---
title: Managing opt-in and opt-out in Campaign
seo-title: Managing opt-in and opt-out in Campaign
description: Managing opt-in and opt-out in Campaign
seo-description: Understand how opt-in and opt-out are managed in Adobe Campaign.
uuid: f8e2e2d2-1586-4424-8bb4-126c28085dbb
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/audiences/using/managing-opt-in-and-opt-out-in-campaign
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-25T09 29 19.717-0400
cq-lastreplicated: 2018-07-23T05 55 35.713-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: audiences
content-type: reference
topic-tags: understanding-opt-in-and-opt-out-processes
cq-template: /apps/help/templates/article-3
discoiquuid: 90823f06-7c35-48c1-9bd0-76cf343b40f9
firstPublishExternalDate: 2018-07-23T05:55:35.613-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-05-07T07 29 07.776-0400
jcr-createdby: admin
jcr-description: Managing opt-in and opt-out in Campaign
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T05:55:35.613-0400
lochandoffdate: 2018-07-25T09 29 19.716-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Managing opt-in and opt-out in Campaign
publishexternaldate: 2018-07-23T05 55 35.613-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/audiences/using/managing-opt-in-and-opt-out-in-campaign.html
sha1: 378b0f2c04365bbfcc963148f0c26c48279b2793
topicBrowsingSortDate: 2018-07-23T05:55:35.613-0400
index: y
internal: n
snippet: y
---

# Managing opt-in and opt-out in Campaign

Managing opt-in and opt-out in Campaign

## Managing opt-in and opt-out from a profile

Users can be opted in or out by an operator directly from the profile **General** tab.

In the **No longer contact (blacklist)** section, the selected checkboxes correspond to the channels from which the user chose to opt out. Select the channels according to the user's needs.

![](assets/optIn_landingPage_3.png)

## Setting up opt-in and opt-out landing pages

To give users the ability to opt in or opt out, you have to create and publish a **Profile acquisition** landing page. They will then be able to select the channels according to their needs. To do this, follow the steps below.

You can also set up a **BlackList** landing page that will enable users to opt out from all deliveries. For more on this, refer to [Setting up a landing page to opt out from all deliveries](../../audiences/using/managing-opt-in-and-opt-out-in-campaign.md#setting-up-a-landing-page-to-opt-out-from-all-deliveries).

>[!NOTE]
>
>Landing pages can also be used to enable services subscription. For more on this, refer to [this page](../../channels/using/designing-a-landing-page.md#linking-a-form-to-a-service).

1. Create a **Profile acquisition** landing page (see [this section](../../channels/using/about-landing-pages.md)).
1. Add a checkbox in the landing page content for each desired channel, then link it to the corresponding field from the Campaign database.

   ![](assets/optIn_landingPage_1.png)

1. Save the landing page and publish it.
1. In the landing page, the checkboxes are already selected according to the profile **General** tab. The user can select or unselect the channels according to his needs and submit the form.

   ![](assets/optIn_landingPage_2.png)

1. Once the form submitted, the profile **General** tab is updated according to the user's selection.

   ![](assets/optIn_landingPage_3.png)

### Setting up a landing page to opt out from all deliveries

To give users the ability to opt out from all deliveries, you have to create and publish a **BlackList** landing page. For more on landing pages creation, refer to [this page](../../channels/using/about-landing-pages.md).

Once a user clicks on the landing page link, the **No longer contact (by any channel)** option in the profile is automatically selected.

![](assets/blacklisting_allChannels.png)

