---
title: Exclusion
seo-title: Exclusion
description: Exclusion
seo-description: The Exclusion  activity allows you to exclude elements from one population according to certain criteria.
uuid: 4ecabd67-bae3-4859-8724-86726c69a6c5
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/automating/using/exclusion
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-25T09 29 27.169-0400
cq-lastreplicated: 2018-07-23T05 57 03.367-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: targeting-activities
cq-template: /apps/help/templates/article-3
discoiquuid: e87b689c-0e24-4a23-803d-4008895a6d9d
firstPublishExternalDate: 2018-07-23T05:57:03.300-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 09.176-0400
jcr-createdby: admin
jcr-description: Exclusion
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T05:57:03.300-0400
lochandoffdate: 2018-07-25T09 29 27.169-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Exclusion
publishexternaldate: 2018-07-23T05 57 03.300-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/automating/using/exclusion.html
sha1: bbc5a19c25b0706e266dc5225c7d0935e30ea051
topicBrowsingSortDate: 2018-07-23T05:57:03.300-0400
index: y
internal: n
snippet: y
---

# Exclusion

Exclusion

## Description

![](assets/exclusion.png)

The **Exclusion ** activity allows you to exclude elements from one population according to certain criteria.

## Context of use

The **Exclusion** activity is used essentially to carry out additional filtering on inbound transition populations.

A primary set is defined amongst inbound transitions. Members of other inbound transitions are excluded from the primary set. The outbound transition of the exclusion activity only contains the members of the primary set that were not encountered in the other inbound transitions.

## Configuration

1. Drag and drop an **Exclusion** activity into your workflow.
1. Select the activity, then open it using the  ![](assets/edit_darkgrey-24px.png)

   button from the quick actions that appear.
1. Select the **Primary set** from the inbound transitions. This is the set from which elements are excluded. The other sets match elements before being excluded from the primary set.

   >[!NOTE]
   >
   >The inbound transitions have to contain the same type of population. For example, if the primary set contains test profiles, the other transitions have to also contain test profiles.

1. If needed, manage the activity's [Transitions](../../automating/using/executing-a-workflow.md#managing-an-activity-s-outbound-transitions) to access the advanced options for the outbound population.
1. Confirm the configuration of your activity and save your workflow.

## Example

The following example shows two query activities configured to filter profiles from the Adobe Campaign database who are between 18 and 27 years old and have an invalid email address. The profiles with invalid email addresses are then excluded from the first set. This allows you to then send an email for example.

![](assets/wkf_exclusion_example.png)

