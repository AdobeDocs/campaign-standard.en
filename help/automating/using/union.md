---
title: Union
seo-title: Union
description: Union
seo-description: The Union activity allows you to regroup the result of multiple activities into a single target.
uuid: 0fa14f06-5e4e-48c4-93c4-b7bd5566efec
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/automating/using/union
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-10T07 24 48.323-0400
cq-lastreplicated: 2018-09-07T14 52 29.279-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: targeting-activities
cq-template: /apps/help/templates/article-3
discoiquuid: 9b065dc5-c061-45df-bfcf-1d15c663ec36
firstPublishExternalDate: 2018-09-07T14:52:27.418-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 12.356-0400
jcr-createdby: admin
jcr-description: Union
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T14:52:27.418-0400
lochandoffdate: 2018-09-10T07 24 48.321-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Union
publishexternaldate: 2018-09-07T14 52 27.418-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/automating/using/union.html
sha1: 2521f2fee3df9b424f17dbb1858375b29f3022ba
topicBrowsingSortDate: 2018-09-07T14:52:27.418-0400
index: y
internal: n
snippet: y
---

# Union

Union

## Description

![](assets/union.png)

The **Union** activity allows you to regroup the result of multiple activities into a single target.

>[!NOTE]
>
>The sets do not necessarily need to be homogeneous.

## Context of use

The **Union** activity is used to combine the populations from inbound transitions when performing a segmentation, defining an audience, or when preparing the message target for example.

## Configuration

1. Drag and drop a **Union** activity into your workflow.
1. Connect it to the other activities that come before it, such as queries.
1. Select the activity, then open it using the  ![](assets/edit_darkgrey-24px.png)

   button from the quick actions that appear.
1. Select the **Reconciliation type** to define how duplicates are from the confrontation between inbound populations are handled:

    * **Keys only**: this is the default mode. The activity only keeps one element when elements from the different inbound transitions have the same key. This option can only be used if the inbound populations are homogeneous.
    * **All shared columns**: The data is reconciled on the basis of all the columns in common with the inbound transitions. Therefore, you have to select the primary set that will be kept in case of a duplicate. This option can be used if the inbound population targeting dimensions are different.
    * **A selection of columns**: select this option to define the list of columns on which the data reconciliation will be applied. You must first select the primary set (that which contains the source data), then the columns to use for the join.

1. Check the **Use common additional data only** box if you would like to keep only the additional data that is in all inbound transitions.
1. If you would like to limit the size of the final population, check the **Limit size of generated population** box. The size can be specified in the **Maximum number of records** field.
1. If needed, manage the activity's [Transitions](../../automating/using/executing-a-workflow.md#managing-an-activity-s-outbound-transitions) to access the advanced options for the calculated population.
1. Confirm the configuration of your activity and save your workflow.

## Example

The following example shows the result of two query activities that aim to regroup profiles from the Adobe Campaign database who are between 18 and 27 years old and those who are between 34 and 40 years old. The result contains all the profiles of the two queries or the maximum number of records, if applicable, as specified during the configuration.

![](assets/wkf_union_example.png)

