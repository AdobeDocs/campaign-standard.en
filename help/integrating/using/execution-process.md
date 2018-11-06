---
title: Execution process
seo-title: Execution process
description: Execution process
seo-description: Learn the main steps of the execution process before using the Adobe Marketing Cloud Triggers integration.
page-status-flag: never-activated
uuid: 5c21426a-d78e-471b-9e01-e7197cc48c3b
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/integrating/using/execution-process
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-01-10T15 24 18.404-0500
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: marketing-cloud-triggers
cq-template: /apps/help/templates/article-3
discoiquuid: 6180c9e4-d67b-4108-bb12-bec877841633
firstPublishExternalDate: 2018-01-10T15:24:18.399-0500
herogradient: light
jcr-created: 2018-01-11T19 01 50.142-0500
jcr-createdby: admin
jcr-description: Execution process
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-01-10T15:24:18.399-0500
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Execution process
publishexternaldate: 2018-01-10T15 24 18.399-0500
publishExternalURL: https://helpx.adobe.com/campaign/standard/integrating/using/execution-process.html
sha1: 5dacae308316beb68a420ef8f5fb5844e2b7d16f
topicBrowsingSortDate: 2018-01-10T15:24:18.399-0500
index: y
internal: n
snippet: y
---

# Execution process

Execution process

The main steps of the execution process are (example: cart abandonment):

1. A client adds a product to their cart.
1. Adobe Analytics detects this behavior and, after a period of inactivity (up to 4 hours maximum), Adobe Marketing Cloud sends an event to Adobe Campaign.
1. Adobe Campaign receives the event.
1. Adobe Campaign reconciles the event with a profile to recover the email address. The event is then stored in the database.
1. Adobe Campaign sends the personalized transactional message associated with the client.

