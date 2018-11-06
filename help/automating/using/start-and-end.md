---
title: Start and end
seo-title: Start and end
description: Start and end
seo-description: The Start and End activities allow you to clearly mark where your workflow starts and ends.
uuid: 84d2f7fb-4947-4021-bf3d-1e6a21f7960c
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/automating/using/start-and-end
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-10T07 26 08.290-0400
cq-lastreplicated: 2018-09-07T14 58 16.813-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: execution-activities
cq-template: /apps/help/templates/article-3
discoiquuid: a064d6ee-1d2e-4a0e-97e9-da250535af03
firstPublishExternalDate: 2018-09-07T14:58:14.075-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 01 52.636-0400
jcr-createdby: admin
jcr-description: Start and end
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T14:58:14.075-0400
lochandoffdate: 2018-09-10T07 26 08.288-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Start and end
publishexternaldate: 2018-09-07T14 58 14.075-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/automating/using/start-and-end.html
sha1: f69836fdc84b99f5c24ae238c26aeaf1e51557e3
topicBrowsingSortDate: 2018-09-07T14:58:14.075-0400
index: y
internal: n
snippet: y
---

# Start and end

Start and end

## Description

![](assets/start.png) ![](assets/end.png)

The **Start** and **End** activities allow you to clearly mark where your workflow starts and ends.

## Context of use

Executing a workflow starts with activities without an inbound transition, and stops when there are no longer any tasks in progress. Nevertheless, you can add **Start** and **End** activities to clearly mark the starting and ending points of a workflow. This is especially helpful for relatively complex workflows.

It is a best practice to use an **End** activity instead of leaving the last transition of a workflow on its own to ensure that the workflow properly ends.

## Configuration

1. Drag and drop a **Start** or **End** activity into your workflow.
1. Put the **Start ** activity in front of other activities such as queries, and the **End** activity after a series of activities.
1. Select the activity, then open it using the  ![](assets/edit_darkgrey-24px.png)

   button from the quick actions that appear.
1. You can configure the **End** object so that it interrupts all of the workflow's ongoing tasks, including those that have not finished. To do this, select the corresponding option.
1. Confirm the configuration of your activity and save your workflow.

## Triggering another workflow

Using the **External signal** tab of an **End** activity, you can trigger another workflow. Refer to the [External signal](../../automating/using/external-signal.md) section.

## Example

The following example shows how a complex workflow is executed with a **Start** activity and several **End** activities. The **Stop all tasks in progress** box has been checked for the first **End** activity. Once the corresponding task is finished, the entire workflow will be stopped: it will have the same effect as if the  ![](assets/stop_darkgrey-24px.png) button had been selected (refer to the [Action bar](../../automating/using/workflow-interface.md#action-bar) section)

![](assets/wkf_start_end_example.png)

