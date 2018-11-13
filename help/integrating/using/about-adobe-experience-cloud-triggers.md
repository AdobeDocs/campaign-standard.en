---
title: About Adobe Experience Cloud Triggers
seo-title: About Adobe Experience Cloud Triggers
description: About Adobe Experience Cloud Triggers
seo-description: By tracking specific behaviors from customers with Adobe Analytics, you can now send personalized emails to your customers in Adobe Campaign.
uuid: 3d71a4f0-ed86-449c-aba4-10cd367bb3be
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/integrating/using/about-adobe-experience-cloud-triggers
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-10T02 19 13.101-0400
cq-lastreplicated: 2018-09-07T15 08 14.360-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-triggers
cq-template: /apps/help/templates/article-3
discoiquuid: 3d29cca8-2508-45d8-bb38-36a523c8da42
firstPublishExternalDate: 2018-09-07T15:08:14.015-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 01 59.216-0400
jcr-createdby: admin
jcr-description: About Adobe Experience Cloud Triggers
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T15:08:14.015-0400
lochandoffdate: 2018-09-10T02 19 13.100-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: About Adobe Experience Cloud Triggers
publishexternaldate: 2018-09-07T15 08 14.015-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/integrating/using/about-adobe-experience-cloud-triggers.html
sha1: 8fb02a4d9a234d12cbbc39862dbdb9a404ac6a08
topicBrowsingSortDate: 2018-09-07T15:08:14.015-0400
index: y
internal: n
snippet: y
---

# About Adobe Experience Cloud Triggers{#about-adobe-experience-cloud-triggers}

About Adobe Experience Cloud Triggers

Integration between the Experience Cloud Activation core service **Triggers** and Adobe Campaign allows you to send personalized emails to your customers as a reaction to specific behaviors that are tracked on your website by Adobe Analytics (within 15 minutes).

In Adobe Experience Cloud, you define the different triggers, that is to say, the customer behaviors that you would like to monitor, such as all of the clients who abandoned their visit on your website, made a search on your website, but didn't make a purchase, or even the clients whose session expired. When creating a trigger, you define the trigger's condition and the data that will be sent in the event (pload) to Adobe Campaign.

In Adobe Campaign, you select the trigger that was previously created, you enrich the event data with datamart data and you define a transactional message template linked to that trigger. For example, when a client abandons his visit on your website, an event is sent to Adobe Campaign which can then leverage this event via a remarketing email that is sent to the client within 15 minutes.

Related topics:

* Learn about the different types of triggers: [Adobe Experience Cloud documentation](https://marketing.adobe.com/resources/help/en_US/mcloud/triggers.html).
* Watch the [Trigger Remarketing Messages based on Site Activity](https://helpx.adobe.com/marketing-cloud/how-to/email-marketing.html#step-two) video.
* Discover our two [Abandonment Triggers use cases](../../integrating/using/abandonment-triggers-use-cases.md).

## Triggers user process {#triggers-user-process}

>[!CAUTION]
>
>Before executing the main user steps, the functionality needs to be configured. For more on this refer to [Activating the functionality](../../integrating/using/configuring-triggers-in-experience-cloud.md#activating-the-functionality), [Configuring solutions and services](../../integrating/using/configuring-triggers-in-experience-cloud.md#configuring-solutions-and-services) and [Creating a mapped trigger in Campaign](../../integrating/using/using-triggers-in-campaign.md#creating-a-mapped-trigger-in-campaign).

The main steps of the user process, in Adobe Campaign, are:

1. Create a trigger event linked to an existing Adobe Experience Cloud trigger.
1. Publish the trigger event.
1. Define the content of the transactional message template.
1. Test the template (create a test profile and send a proof).
1. Publish the transactional message template.

Complete use cases are described in [this section](../../integrating/using/abandonment-triggers-use-cases.md).

## Important notes {#important-notes}

Here are some important notes to take into account before using the Triggers - Campaign integration:

* Push notifications are not supported for triggers. Only Email and SMS are supported.
* You can enrich the trigger with meta data captured through Analytics such as email ID, page name, etc.
* You can reconcile the trigger to a profile stored in Campaign Standard and use the profile's fields to personalize the message.
* As soon a trigger is received, it is processed and reconciled and sent out. It takes about 5 to 15 minutes depending on the volume of triggers received, the number of personalization fields used in template.

>[!NOTE]
>
>For more on best practices and technical limitations, refer to [Triggers best practices and limitations](../../integrating/using/configuring-triggers-in-experience-cloud.md#triggers-best-practices-and-limitations).

