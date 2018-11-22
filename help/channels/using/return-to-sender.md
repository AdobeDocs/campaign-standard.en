---
title: Return to sender
seo-title: Return to sender
description: Return to sender
seo-description: Learn how to be notified of an incorrect address and exclude it from future communications.
page-status-flag: never-activated
uuid: 6c529b5f-18d6-4e1b-9aee-2eec10fb3813
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/channels/using/return-to-sender
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: direct-mail
discoiquuid: 6e39a0d9-d9c3-4102-9bb9-ca15eb03ddff
isreadyforlocalization: false
navTitle: Return to sender
publishexternaldate: 2018-11-20
sha1: cda198400aba4db8e8aefb3478ee52d2d685849a
index: y
internal: n
snippet: y
---

# Return to sender{#return-to-sender}

Return to sender

Flat file exchanges with Direct Mail providers incorporating Return to Sender information are supported. This allows corresponding postal addresses to be excluded from future communications. This also allows you to be notified of an incorrect address and engage with the customer through other channels or to encourage him to update his postal address.

For example, a contact has moved to a new place and did not provide you with his new postal address. The provider retrieves the list of erroneous addresses and sends this information to Adobe Campaign which automatically blacklists the erroneous addresses.

In order for this functionality to work, the direct mail default delivery template includes, in the content, the delivery log ID. Thus, Adobe Campaign will be able to synchronize the profile and delivery data with the information returned by the provider.

![](assets/direct_mail_return_sender_1.png)

An import template is available under **Adobe Campaign > Resources > Templates > Import templates > Update Direct Mail quarantines and delivery logs**. Duplicate this template to create your own. For more on using import templates, refer to [Using import templates](../../automating/using/defining-import-templates.md).

![](assets/direct_mail_return_sender_2.png)

When the import is done, Adobe Campaign automatically performs the following actions:

* Incorrect addresses are blacklisted at the profile level
* The delivery main indicators (KPIs) are updated
* The delivery logs are updated

