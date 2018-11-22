---
title: Creating a multilingual email
seo-title: Creating a multilingual email
description: Creating a multilingual email
seo-description: Follow these steps to create a multilingual email targeting recipients with different preferred languages.
page-status-flag: never-activated
uuid: 93c48f83-bc97-4e92-9b7a-78b06fca4fb3
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/channels/using/creating-a-multilingual-email
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: email-messages
discoiquuid: 7724fb10-281b-401d-806e-8d09cbe2868c
isreadyforlocalization: false
navTitle: Creating a multilingual email
publishexternaldate: 2018-11-20
sha1: 3ede805ba06826605ed7b6f6d5e13a25f16fa071
index: y
internal: n
snippet: y
---

# Creating a multilingual email{#creating-a-multilingual-email}

Creating a multilingual email

You can send a multilingual email to profiles with different preferred languages: each profile will receive a variant of the email in his preferred language.

To do this, check that you have a multilingual email template available. If not, learn how to create one in [this section](../../start/using/creating-a-multilingual-template.md).

The audience is based on profiles with a completed preferred language information.

1. Create a new email based on a [multilingual template](../../start/using/creating-a-multilingual-template.md).

   ![](assets/multi_create1.png)

1. Define the general properties and the target audience of the email, just as for a standard email. Refer to the [Creating audiences](../../audiences/using/creating-audiences.md) section.
1. At the fourth step in the creation wizard, define the variant options. If the [multilingual template](../../start/using/creating-a-multilingual-template.md) already contains all the right parameters, you can directly click on the **Create** button.

   ![](assets/multi_create4.png)

   If needed, add variants using the **Add an element** button. **Default** variant must not be deleted. When set to **default**, [the profile's preferred language](../../audiences/using/creating-profiles.md) is used to choose the variant. You can also set the **Default** variant to any other language.

1. Confirm email creation: the email dashboard will then be displayed.
1. Define the email content for each variant. Depending on the template that you have chosen, you can define several subjects, several sender names, or several different contents. Use the drop-down menu to navigate between the different variants of the element. For more information, consult the [content editor](../../designing/using/about-email-content-design.md) section.

   ![](assets/multi_selectcontent.png)

1. Test and validate your message. Refer to the [Sending proof](../../sending/using/managing-test-profiles-and-sending-proofs.md#sending-proofs) section.
1. Schedule the send with the **Send after confirmation option**.
1. Once your email is sent, you can access its logs and reports to measure the success of your campaign. For more on reporting, refer to [this section](../../reporting/using/about-dynamic-reports.md).

