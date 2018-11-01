---
title: Start and end
seo-title: Start and end
description: Start and end
seo-description: The Start and End activities allow you to clearly mark where your workflow starts and ends.
uuid: 2ec3045e-af7d-4ded-b897-bc5c8aa49085
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/automating/using/start-and-end
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-25T09 29 35.809-0400
cq-lastreplicated: 2018-07-23T05 57 11.741-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: execution-activities
cq-template: /apps/help/templates/article-3
discoiquuid: ce7ef3af-50e7-4e2b-a59a-e3c2c58dd640
firstPublishExternalDate: 2018-07-23T05:57:11.698-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 01 52.636-0400
jcr-createdby: admin
jcr-description: Start and end
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T05:57:11.698-0400
lochandoffdate: 2018-07-25T09 29 35.809-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Start and end
publishexternaldate: 2018-07-23T05 57 11.698-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/automating/using/start-and-end.html
sha1: 4cecc1f5e80e65721576bd6076aae959b7342624
topicBrowsingSortDate: 2018-07-23T05:57:11.698-0400
index: y
internal: n
snippet: y
---

# Start and end

Start and end

## <p>Description</p>

![](assets/start.png) ![](assets/end.png)

The **Start** and **End** activities allow you to clearly mark where your workflow starts and ends.

## <p>Context of use</p>

Executing a workflow starts with activities without an inbound transition, and stops when there are no longer any tasks in progress. Nevertheless, you can add **Start** and **End** activities to clearly mark the starting and ending points of a workflow. This is especially helpful for relatively complex workflows.

It is a best practice to use an **End** activity instead of leaving the last transition of a workflow on its own to ensure that the workflow properly ends.

## <p>Configuration</p>

1. Drag and drop a **Start** or **End** activity into your workflow.
1. Put the **Start ** activity in front of other activities such as queries, and the **End** activity after a series of activities.
1. Select the activity, then open it using the  ![](assets/edit_darkgrey-24px.png)

   button from the quick actions that appear.
1. You can configure the **End** object so that it interrupts all of the workflow's ongoing tasks, including those that have not finished. To do this, select the corresponding option.
1. Confirm the configuration of your activity and save your workflow.

## <p>Triggering another workflow</p>

Using the **External signal** tab of an **End** activity, you can trigger another workflow. Refer to the [External signal](../../automating/using/external-signal.md) section.

## <p>Example</p>

The following example shows how a complex workflow is executed with a **Start** activity and several **End** activities. The **Stop all tasks in progress** box has been checked for the first **End** activity. Once the corresponding task is finished, the entire workflow will be stopped: it will have the same effect as if the  ![](assets/stop_darkgrey-24px.png) button had been selected (refer to the [Action bar](../../automating/using/workflow-interface.md#action-bar) section)

![](assets/wkf_start_end_example.png)

