---
title: Fork
seo-title: Fork
description: Fork
seo-description: The Fork activity allows you to create outbound transitions to start several activities at the same time.
uuid: e4a4c03c-18ae-462f-84bb-af4ae2f84de3
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/automating/using/fork
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-25T09 29 36.448-0400
cq-lastreplicated: 2018-07-23T05 57 12.861-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: execution-activities
cq-template: /apps/help/templates/article-3
discoiquuid: 82cc659a-ebf2-40ee-a638-4e8afd13f14a
firstPublishExternalDate: 2018-07-23T05:57:12.826-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 16.995-0400
jcr-createdby: admin
jcr-description: Fork
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T05:57:12.826-0400
lochandoffdate: 2018-07-25T09 29 36.448-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Fork
publishexternaldate: 2018-07-23T05 57 12.826-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/automating/using/fork.html
sha1: 83dbf147488f7166c3da38241135822525343fa0
topicBrowsingSortDate: 2018-07-23T05:57:12.826-0400
index: y
internal: n
snippet: y
---

# Fork

Fork

## Description

![](assets/fork.png)

The **Fork** activity allows you to create outbound transitions to start several activities at the same time.

## Context of use

The **Fork** activity allows you to carry out several different activities independently within the same workflow.

## Configuration

1. Drag and drop a **Fork** activity into your workflow.
1. Connect it to the other activities that come before it, such as queries.
1. Select the activity, then open it using the  ![](assets/edit_darkgrey-24px.png)

   button from the quick actions that appear.
1. Specify the number of outbound transitions by creating, deleting or duplicating them. You can also attribute a name and a label to them.
1. Confirm the configuration of your activity and save your workflow.

## Example

The following example shows an intersection of two query activities that target profiles from the Adobe Campaign database, in this case, women living in Paris. The fork activity therefore allows you to use several activities at the same time: one that saves the audience to remember the calculated population, and another that segments the population to send two different emails with a targeted content for each segment. The first email is sent to Parisian women aged between 18 and 40 and another targeting Parisian women aged over 40.

![](assets/wkf_fork_example.png)

