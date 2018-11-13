---
title: Data storage and reconciliation
seo-title: Data storage and reconciliation
description: Data storage and reconciliation
seo-description: Adobe Campaign allows you to define how the data entered in the landing page is managed once submitted by a user.
uuid: 6fb4cf25-ed2b-481a-b4a8-4ee05c589940
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/channels/using/data-storage-and-reconciliation
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-08T08 23 23.703-0400
cq-lastreplicated: 2018-09-07T15 12 37.283-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: landing-pages
cq-template: /apps/help/templates/article-3
discoiquuid: 5ec1d23c-843a-4a6e-a10e-87b0c23b4b87
firstPublishExternalDate: 2018-09-07T15:12:37.249-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 17.382-0400
jcr-createdby: admin
jcr-description: Data storage and reconciliation
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T15:12:37.249-0400
lochandoffdate: 2018-09-08T08 23 23.703-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Data storage and reconciliation
publishexternaldate: 2018-09-07T15 12 37.249-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/channels/using/data-storage-and-reconciliation.html
sha1: cfb67778751cc497fe187d2aaaba48d21d43d4a3
topicBrowsingSortDate: 2018-09-07T15:12:37.249-0400
index: y
internal: n
snippet: y
---

# Data storage and reconciliation{#data-storage-and-reconciliation}

Data storage and reconciliation

Data reconciliation parameters allow you to define how the data entered in the landing page is managed once it has been submitted by a user.

To do this:

1. Edit the landing page properties accessed via the  ![](assets/edit_darkgrey-24px.png) icon in the landing page dashboard, and display the **Job** parameters.

   ![](assets/lp_parameters_4.png)

1. Select the **Reconciliation key**: these database fields (for example: email, first name, last name) are used to determine whether the visitor has a profile that is already known in the Adobe Campaign database. This allows you to update or create a profile, according to the update strategy parameters defined.
1. Define the **Form parameter mapping**: this section allows you to map the landing page field parameters and those used in the reconciliation key.
1. Select the **Update strategy**: if the reconciliation key recovers an existing database profile, you can choose for this profile to be updated with the data entered in the form or instead prevent this update.

