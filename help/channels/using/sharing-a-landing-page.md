---
title: Sharing a landing page
seo-title: Sharing a landing page
description: Sharing a landing page
seo-description: Learn how to test and publish a landing page in Adobe Campaign.
uuid: d792aaa6-3396-4811-9946-6c76a999d46a
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/channels/using/sharing-a-landing-page
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-08T08 23 23.433-0400
cq-lastreplicated: 2018-09-07T15 12 36.297-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: landing-pages
cq-template: /apps/help/templates/article-3
discoiquuid: 1268306a-639e-46fe-83bb-1b53394f690f
firstPublishExternalDate: 2018-09-07T15:12:36.257-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 35.668-0400
jcr-createdby: admin
jcr-description: Sharing a landing page
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T15:12:36.257-0400
lochandoffdate: 2018-09-08T08 23 23.432-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Sharing a landing page
publishexternaldate: 2018-09-07T15 12 36.257-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/channels/using/sharing-a-landing-page.html
sha1: 233c64868035ba14494fb4d949a4ae7a1b158782
topicBrowsingSortDate: 2018-09-07T15:12:36.257-0400
index: y
internal: n
snippet: y
---

# Sharing a landing page

Sharing a landing page

## About landing page publication

Before publishing a landing page, you need to perform tests: validate the execution, configure access and set up your landing page end-of-life. These steps are prerequisites and need to be executed with caution.

## Testing the landing page

As the landing page will impact your platform and data, you need to test carefully its execution. To do this:

1. Click the **Test** button in the action bar of the landing page.
1. From the test screen, select a test profile, and a test service if the landing page is to manage subscriptions.

   ![](assets/lp_test_2.png)

1. Enter data in the fields, and select options. 
1. Submit the landing page and check updates in the database.

   >[!CAUTION]
   >
   >When the form is submitted, service and profile used are updated.

1. Repeat this with various profiles and data.

   You can also generate the landing page thumbnail from this screen.

## Setting up validity parameters

Before publishing, for security reasons and platform performances, we highly recommend you to set an expiration date in the landing page properties. On the selected date, the landing page is automatically unpublished. To do this:

1. Edit the landing page properties accessed via the  ![](assets/edit_darkgrey-24px.png)

   button in the landing page dashboard.

   ![](assets/lp_edit_properties_button.png)

1. Set up expiration date and time in the **Publication** section: the landing page will automatically be unpublished on the specified date and therefore no longer be available.

   You can select the time zone to be taken into account for this date and time.

1. Define a redirection URL to redirect the visitors when trying to access a non-active landing page.

   ![](assets/lp_settings_general.png)

>[!CAUTION]
>
>You can also define a deployment date and time: the landing page will then be automatically published on the specified date.

## Publishing a landing page

When you publish a landing page, it goes live and can be accessed by your visitors.

You can unpublish or update and republish your landing page at any time, via the **Publish** button. However, if republishing fails and you have not yet unpublished your landing page, the first version will remain online.
