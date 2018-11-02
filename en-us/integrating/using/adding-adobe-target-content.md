---
title: Adding Adobe Target content
seo-title: Adding Adobe Target content
description: Adding Adobe Target content
seo-description: Learn how to add Adobe Target dynamic content in one of your Adobe Campaign delivery.
page-status-flag: never-activated
uuid: 2cc877d4-b3fe-44f5-8f3c-23748d2a4aeb
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/integrating/using/adding-adobe-target-content
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-01-10T15 24 03.766-0500
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: adobe-target-integration
cq-template: /apps/help/templates/article-3
discoiquuid: ab636b92-e12f-4136-b7f8-3938121c929e
firstPublishExternalDate: 2018-01-10T15:24:03.758-0500
herogradient: light
jcr-created: 2018-01-11T19 02 13.424-0500
jcr-createdby: admin
jcr-description: Adding Adobe Target content
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-01-10T15:24:03.758-0500
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Adding Adobe Target content
publishexternaldate: 2018-01-10T15 24 03.758-0500
publishExternalURL: https://helpx.adobe.com/campaign/standard/integrating/using/adding-adobe-target-content.html
sha1: 7dc47ed1888ff4a62c3370a340986f59dc9b6852
topicBrowsingSortDate: 2018-01-10T15:24:03.758-0500
index: y
internal: n
snippet: y
---

# Adding Adobe Target content

Adding Adobe Target content

With Adobe Target integration, dynamic images can be added into a delivery to personalize your content depending of experiences.

While editing an email, you can insert a dynamic image from Adobe Target which will change depending of the recipients.

Before accessing the image in Adobe Campaign, the following tasks must first be performed in Adobe Target:

* Create one or several [redirect offers](https://marketing.adobe.com/resources/help/en_US/tnt/help/t_Creating_a_Redirect_Offer.html), in which you must specify the URL of the image you will be using.
* Create one or several [audiences](https://marketing.adobe.com/resources/help/en_US/target/ov/c_about_segments.html), to define the target of your activity.
* Create a [Form-based experience composer](https://marketing.adobe.com/resources/help/en_US/target/target/t_form_experience_composer.html) activity, in which you have to select a rawbox and specify several experiences, depending on the number of redirect offers created. For each experience, you must select one of the redirect offers created.
* Create segments using information from Adobe Campaign to specify experiences. To use data from Adobe Campaign in the offer's selection rules, you must specify the data in the rawbox in Adobe Target.

1. Create an email delivery.
1. When editing the content of an email or a landing page, go to an image block, then select **Dynamic image from Adobe Target** via the contextual menu.

   ![](assets/tar_insert_dynamic_image.png)

1. Select the image that will appear by default in the email. You can directly specify the image URL or select an image shared via [Assets](../../integrating/using/assets-core-service-integration.md).

   The integration only supports static images. The rest of the content is not customizable.

1. Enter the name of the rawbox specified in Adobe Target.
1. In **Additional decision parameters**, specify the mapping between the fields defined in the Adobe Target segments and the Adobe Campaign fields.

   The Adobe Campaign fields used must have been specified in the rawbox. Here, we will define different experiences depending of the recipient's gender.

   ![](assets/tar_additional_decisionning_parameters.png)

1. Preview your email to see if, when selecting different profiles, the image inserted changes depending on the parameters specified in the Adobe Target activity and in Adobe Campaign.

Your delivery containing the dynamic image can now be send. Its results can be found in Adobe Target.

**Related topics:**

* [Adobe Target Portal](https://marketing.adobe.com/resources/help/en_US/target/a4t/c_campaign_and_target.html)
* [Define email content](../../designing/using/example--email-personalization.md)
* [Personalize Email Images in Real-Time](https://helpx.adobe.com/marketing-cloud/how-to/email-marketing.html) video

