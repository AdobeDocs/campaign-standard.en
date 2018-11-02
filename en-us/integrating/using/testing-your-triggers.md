---
title: Testing your triggers
seo-title: Testing your triggers
description: Testing your triggers
seo-description: 
uuid: 5dc98f70-6045-4673-b9b0-99abdf849a03
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/integrating/using/testing-your-triggers
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-27T03 27 37.572-0400
cq-lastreplicated: 2018-07-23T05 59 50.574-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-triggers
cq-template: /apps/help/templates/article-3
discoiquuid: 953000b3-6831-4214-8118-a1fb353b88cb
firstPublishExternalDate: 2018-07-23T05:59:50.531-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-06-15T07 29 54.569-0400
jcr-createdby: admin
jcr-description: Testing your triggers
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T05:59:50.531-0400
lochandoffdate: 2018-07-27T03 27 37.571-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Testing your triggers
publishexternaldate: 2018-07-23T05 59 50.531-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/integrating/using/testing-your-triggers.html
sha1: 5be88b5a53bbee885c98f459696e774c35250457
topicBrowsingSortDate: 2018-07-23T05:59:50.531-0400
index: y
internal: n
snippet: y
---

# Testing your triggers

Testing your triggers

The following troubleshooting tips will help you solve the most common problems you may encounter when using Triggers with Adobe Campaign:

**Is the functionality activated?**

To check if the Triggers - Campaign integration is activated, click the Adobe Campaign logo, in the top left corner, then select **Marketing plans** > **Transactional messages**. You should see the **Experience Cloud Triggers** item.

If you see it, move on to the next step.

If not, contact your Adobe account executive or professional services partner. See [Activating the functionality](../../integrating/using/configuring-triggers-in-experience-cloud.md#activating-the-functionality).

**Try creating a trigger**

Follow the steps described in [Creating a mapped trigger in Campaign](../../integrating/using/using-triggers-in-campaign.md#creating-a-mapped-trigger-in-campaign) to create a trigger.

If the trigger is created, move on to the next step. If not, it means that the trigger end point connection failed. Check if Triggers is provisioned in Experience Cloud (Activation services). If it is not, contact your Adobe account executive or professional services partner. The following information is required:

* Marketing Cloud Company Name
* IMS ORG ID
* Analytics Login Company (can be the same as the Marketing Cloud Company Name)

**Try publishing the trigger**

Follow the steps described in [Creating a mapped trigger in Campaign](../../integrating/using/using-triggers-in-campaign.md#creating-a-mapped-trigger-in-campaign) to publish the trigger.

If the publication succeeded, move on to the next step. If not, contact Adobe to restart your instance and try again.

**Generate the trigger from the website**

Follow the steps described in [Editing the transactional message template](../../integrating/using/using-triggers-in-campaign.md#editing-the-transactional-message-template) to edit and publish the transactional template. Then, test the generation of the trigger from the website.

If the trigger is received by Analytics, move on to the next step. If not, check the following items:

* Trigger is enabled for Analytics
* The website used MCID and Analytics is enabled in DTM
* The correct Analytics report suite is used while creating triggers

**Is the trigger received by Campaign?**

If not, check if the trigger is received from the pipeline.

If not, contact Adobe to check the configuration of the pipeline end points.

If it is, follow these guide lines:

* Check the reconciliation ID type in Campaign datasource.
* CustomerId Datasource is created via Customer Attributes.
* Check the Datasource ID.
* Ask Adobe to restart the Campaign instance after the Datasource configuration. 
* Check trigger parsing issues in the trigger report.

**Is the trigger in pending status?**

If not, move on to the next step. If it is, follow these guide lines:

* Check that the transactional template is published.
* If the propensityScore threshold is enabled for Campaign, check the trigger's propensity score from the pipeline.
* Check that the profile is not blacklisted.
* Check the application of typology rules.
* Check the transactional message's logs.

**Is the message valid?**

If the message is not valid, check the following items:

* For trigger enrichment personalization fields marked as invalid, validate the transactional template from the associated eventCusResource collections.
* Validate the message format

