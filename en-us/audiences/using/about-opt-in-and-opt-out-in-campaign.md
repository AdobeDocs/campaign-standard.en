---
title: About opt-in and opt-out in Campaign
seo-title: About opt-in and opt-out in Campaign
description: About opt-in and opt-out in Campaign
seo-description: Opt-out (or blacklist) results in a profile no longer being targeted by any delivery or by deliveries from a specific channel.
uuid: 71d3f17d-1a01-4817-8324-5528a17f978d
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/audiences/using/about-opt-in-and-opt-out-in-campaign
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-25T09 29 19.518-0400
cq-lastreplicated: 2018-07-23T05 55 34.320-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: audiences
content-type: reference
topic-tags: understanding-opt-in-and-opt-out-processes
cq-template: /apps/help/templates/article-3
discoiquuid: 5771e9dd-6b55-4a8f-a03d-47ed1ddd540a
firstPublishExternalDate: 2018-07-23T05:55:34.189-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-05-07T07 29 07.735-0400
jcr-createdby: admin
jcr-description: About opt-in and opt-out in Campaign
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T05:55:34.189-0400
lochandoffdate: 2018-07-25T09 29 19.517-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: About opt-in and opt-out in Campaign
publishexternaldate: 2018-07-23T05 55 34.189-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/audiences/using/about-opt-in-and-opt-out-in-campaign.html
sha1: 755ee1ac530e2a40f1ea4dffaf976df74bb1f38a
topicBrowsingSortDate: 2018-07-23T05:55:34.189-0400
index: y
internal: n
snippet: y
---

# About opt-in and opt-out in Campaign

About opt-in and opt-out in Campaign

Opt-out (or blacklist) results in a profile no longer being targeted by any delivery or by deliveries from a specific channel.

To give profiles the ability to opt in or opt out, you have to create a dedicated landing page. For more on this, refer to [Setting up opt-in and opt-out landing pages](../../audiences/using/managing-opt-in-and-opt-out-in-campaign.md#setting-up-opt-in-and-opt-out-landing-pages).

Profiles can also be opted in or out manually by an operator. For more on this, refer to [Managing opt-in and opt-out from a profile](../../audiences/using/managing-opt-in-and-opt-out-in-campaign.md#managing-opt-in-and-opt-out-from-a-profile).

Opt-out profiles are automatically excluded during the delivery analysis in order to speed up deliveries (the error rate has a significant effect on delivery speed).

>[!NOTE]
>
>Opt-out applies to **Profiles**, as opposed to quarantine which is linked to an **email address** or **phone number**. Opting out a profile will therefore exclude from deliveries all the addresses linked to it. If a user has two profiles in the database, he will still be targeted by deliveries as only one of his profiles is opt-out. To make sure all his adresses are excluded, add them to the quarantines addresses. For more on this, refer to [this page](../../sending/using/understanding-quarantine-management.md#identifying-quarantined-addresses-for-the-entire-platform).

For more on services subscriptions, refer to [this page](../../audiences/using/about-subscriptions.md).
