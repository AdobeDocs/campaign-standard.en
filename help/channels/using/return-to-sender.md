---
title: Return to sender
description: Learn how to be notified of an incorrect address and exclude it from future communications.
audience: channels
content-type: reference
topic-tags: direct-mail
feature: Direct Mail
role: User
level: Intermediate
exl-id: 6783aa68-7fd7-4f53-86bf-853c0fea5899
TQID: https://experienceleague.adobe.com/g-0yLI3-qYRfbF-gXuO8AtyCI3Qr5F7an5hqVzaQCE8
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
---
# Return to sender{#return-to-sender}

Flat file exchanges with Direct Mail providers incorporating Return to Sender information are supported. This allows corresponding postal addresses to be excluded from future communications. This also allows you to be notified of an incorrect address and engage with the customer through other channels or to encourage them to update their postal address.

For example, a contact has moved to a new place and did not provide you with their new postal address. The provider retrieves the list of erroneous addresses and sends this information to Adobe Campaign which automatically denylists the erroneous addresses.

In order for this functionality to work, the direct mail default delivery template includes, in the content, the delivery log ID. Thus, Adobe Campaign will be able to synchronize the profile and delivery data with the information returned by the provider.

![](assets/direct_mail_return_sender_1.png)

An import template is available under **[!UICONTROL Adobe Campaign > Resources > Templates > Import templates > Update Direct Mail quarantines and delivery logs]**. Duplicate this template to create your own. For more on using import templates, refer to [Using import templates](../../automating/using/importing-data-with-import-templates.md#setting-up-import-templates).

![](assets/direct_mail_return_sender_2.png)

When the import is done, Adobe Campaign automatically performs the following actions:

* Incorrect addresses are added to denylist at the profile level
* The delivery main indicators (KPIs) are updated
* The delivery logs are updated
