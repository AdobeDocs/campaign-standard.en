---
title: Intersection
seo-title: Intersection
description: Intersection
seo-description: The Intersection activity allows you to keep only the elements common to the different inbound populations in the activity.
uuid: f7d322bb-f533-4223-950e-a1d80e6b6ebb
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/automating/using/intersection
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-10T07 24 53.709-0400
cq-lastreplicated: 2018-09-07T14 53 07.740-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: targeting-activities
cq-template: /apps/help/templates/article-3
discoiquuid: 3d884497-af61-4e32-89f6-02c411a7e438
firstPublishExternalDate: 2018-09-07T14:53:05.163-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 10.042-0400
jcr-createdby: admin
jcr-description: Intersection
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T14:53:05.163-0400
lochandoffdate: 2018-09-10T07 24 53.707-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Intersection
publishexternaldate: 2018-09-07T14 53 05.163-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/automating/using/intersection.html
sha1: 0192dd4cb6870475d015f9535421b0c333084fb5
topicBrowsingSortDate: 2018-09-07T14:53:05.163-0400
index: y
internal: n
snippet: y
---

# Intersection

Intersection

## Description

![](assets/intersection.png)

The **Intersection** activity allows you to keep only the elements common to the different inbound populations in the activity.

## Context of use

The **Intersection** activity is generally used to carry out additional filtering on populations from inbound transitions.

## Configuration

1. Drag and drop an **Intersection** activity into your workflow.
1. Connect it to the other activities that come before it, such as queries.
1. Select the activity, then open it using the  ![](assets/edit_darkgrey-24px.png)

   button from the quick actions that appear.
1. Select the **Reconciliation type**:

    * **Keys only**: Default mode. The activity only keeps one element when elements from the different inbound transitions have the same key.
    * **All shared columns**: The data is reconciled on the basis of columns in common with the inbound transitions. Therefore, you have to select the primary set that will serve as a basis for comparison. This option can be used if the inbound population targeting dimensions are different.
    * **A selection of columns**: Select this option to define the list of columns on which the data reconciliation will be applied. You must first select the primary set (the one which contains the source data), then specify the fields to use for the join.

1. Check the **Use common additional data only** box if you would like to keep only the additional data that is in all inbound transitions.
1. If needed, manage the activity's [Transitions](../../automating/using/executing-a-workflow.md#managing-an-activity-s-outbound-transitions) to access the advanced options for the outbound population.
1. Confirm the configuration of your activity and save your workflow.

## Example

The following example shows the intersection between two query activities. It is being used here to look into the Adobe Campaign database and retrieve profiles who are between 18 to 27 years old and profiles whose email address has been provided respectively.

![](assets/wkf_intersection_example.png)

