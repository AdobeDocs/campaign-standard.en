---
title: Wait
seo-title: Wait
description: Wait
seo-description: The Wait activity momentarily suspends executing a part of a workflow.
uuid: e9176d08-0aef-4649-951e-bb3fb805c317
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/automating/using/wait
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-25T09 29 37.962-0400
cq-lastreplicated: 2018-07-23T05 57 16.490-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: execution-activities
cq-template: /apps/help/templates/article-3
discoiquuid: 172b963d-2179-4974-a402-f054505165eb
firstPublishExternalDate: 2018-07-23T05:57:16.449-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 35.929-0400
jcr-createdby: admin
jcr-description: Wait
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T05:57:16.449-0400
lochandoffdate: 2018-07-25T09 29 37.961-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Wait
publishexternaldate: 2018-07-23T05 57 16.449-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/automating/using/wait.html
sha1: 4f4e5519a09c1e448da9972db3e71cba7e0371e2
topicBrowsingSortDate: 2018-07-23T05:57:16.449-0400
index: y
internal: n
snippet: y
---

# Wait

Wait

## Description

![](assets/wait.png)

The **Wait** activity momentarily suspends executing a part of a workflow. It activates its outbound transition after a delay that may range from a few seconds to several months, which executes the activities placed afterwards.

## Context of use

The **Wait** activity is used to allow a certain amount of time to pass between two activities being executed. For example, to wait several days after an email delivery activity then analyze the opens and clicks generated during this period before performing any follow-up operations (reminder email, creating an audience, etc.).

## Configuration

1. Drag and drop a **Wait** activity into your workflow.
1. Select the activity, then open it using the  ![](assets/edit_darkgrey-24px.png)

   button from the quick actions that appear.
1. Specify the **Duration** of the wait between when the inbound and outbound transitions of the activity are activated.

   You can manually enter the duration or use the selector available in the field.

   ![](assets/wait_duration.png)

1. Confirm the configuration of your activity and save your workflow.

## Example

The following example illustrates the **Wait** activity in a typical use case. An email invitation to an event is sent. 24 hours after it was sent, the email delivery logs are analyzed and a reminder email is sent to the people who received the first email but did not sign up.

The workflow is presented as follows:

![](assets/wait_example_workflow.png)

* A first **Query** targets the profiles that will be sent the email invitation.
* An **Email delivery** sends the invitation for the first time to the profiles selected.
* A **Wait** activity of 24h places a pause between when the invitation was sent and the rest of the workflow.
* A second **Query** targets the profiles that received the first email but did not click on the subscription link inside.
* A second **Email delivery** sends a reminder of the invitation to the people selected.

