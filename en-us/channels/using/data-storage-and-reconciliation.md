---
title: Data storage and reconciliation
seo-title: Data storage and reconciliation
description: Data storage and reconciliation
seo-description: Adobe Campaign allows you to define how the data entered in the landing page is managed once submitted by a user.
uuid: 2304b350-3fa6-428c-9569-ef613c97e7cd
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/channels/using/data-storage-and-reconciliation
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-30T04 54 13.701-0400
cq-lastreplicated: 2018-07-23T06 03 18.697-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: landing-pages
cq-template: /apps/help/templates/article-3
discoiquuid: 317b637f-bb97-4708-868c-d60cceccf354
firstPublishExternalDate: 2018-07-23T06:03:18.664-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 17.382-0400
jcr-createdby: admin
jcr-description: Data storage and reconciliation
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T06:03:18.664-0400
lochandoffdate: 2018-07-30T04 54 13.701-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Data storage and reconciliation
publishexternaldate: 2018-07-23T06 03 18.664-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/channels/using/data-storage-and-reconciliation.html
sha1: 86966030747ffedad956a760c01f236bf6ace595
topicBrowsingSortDate: 2018-07-23T06:03:18.664-0400
index: y
internal: n
snippet: y
---

# Data storage and reconciliation

Data storage and reconciliation

Data reconciliation parameters allow you to define how the data entered in the landing page is managed once it has been submitted by a user.

To do this:

1. Edit the landing page properties accessed via the  ![](assets/edit_darkgrey-24px.png) icon in the landing page dashboard, and display the **Job** parameters.

   ![](assets/lp_parameters_4.png)

1. Select the **Reconciliation key**: these database fields (for example: email, first name, last name) are used to determine whether the visitor has a profile that is already known in the Adobe Campaign database. This allows you to update or create a profile, according to the update strategy parameters defined.
1. Define the **Form parameter mapping**: this section allows you to map the landing page field parameters and those used in the reconciliation key.
1. Select the **Update strategy**: if the reconciliation key recovers an existing database profile, you can choose for this profile to be updated with the data entered in the form or instead prevent this update.

