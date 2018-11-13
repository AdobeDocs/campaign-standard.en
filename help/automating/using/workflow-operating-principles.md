---
title: Workflow operating principles
seo-title: Workflow operating principles
description: Workflow operating principles
seo-description: Learn the main aspects of workflows.
uuid: 972fd244-8a7c-4e9c-8212-9749fe4299cd
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/automating/using/workflow-operating-principles
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-10T07 22 28.082-0400
cq-lastreplicated: 2018-09-07T14 43 53.067-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: about-workflows-and-data-management
cq-template: /apps/help/templates/article-3
discoiquuid: 0e1912a7-f7de-443e-ba44-d4e0dcf51f6e
firstPublishExternalDate: 2018-09-07T14:43:51.031-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 18.766-0400
jcr-createdby: admin
jcr-description: Workflow operating principles
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T14:43:51.031-0400
lochandoffdate: 2018-09-10T07 22 28.080-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Workflow operating principles
publishexternaldate: 2018-09-07T14 43 51.031-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/automating/using/workflow-operating-principles.html
sha1: 7fd14d9b84015576e65de5f2cd0dc6f3a7d53e20
topicBrowsingSortDate: 2018-09-07T14:43:51.031-0400
index: y
internal: n
snippet: y
---

# Workflow operating principles{#workflow-operating-principles}

Workflow operating principles

A workflow is a **sequence of configurable activities**. Each activity has a specific role in the process. The result of each activity is forwarded to the following activity by a **transition**, represented by an arrow.

The type of data exchanged between one activity and another can affect the way the following activities are configured. For example, if a population is established before email delivery activity, it can serve as the target for the email in question.

You can open activities to check or edit parameters before or after executing the workflow.

You can open transitions to check that the data sent is correct during or after executing the workflow. To access the detail view of the transitions, you have to check the **Keep interim results** option in the **Execution** section of the workflow properties.

![](assets/workflow_overview.png)

