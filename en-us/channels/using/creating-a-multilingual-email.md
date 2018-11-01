---
title: Creating a multilingual email
seo-title: Creating a multilingual email
description: Creating a multilingual email
seo-description: Follow these steps to create a multilingual email targeting recipients with different preferred languages.
uuid: 515f0d0c-4335-4984-980b-1403026271b8
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/channels/using/creating-a-multilingual-email
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-30T04 53 49.614-0400
cq-lastreplicated: 2018-07-23T06 02 44.248-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: email-messages
cq-template: /apps/help/templates/article-3
discoiquuid: 112b99ba-27c6-4882-9546-e47dbbfa826e
firstPublishExternalDate: 2018-07-23T06:02:44.215-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 01 20.103-0400
jcr-createdby: admin
jcr-description: Creating a multilingual email
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T06:02:44.215-0400
lochandoffdate: 2018-07-30T04 53 49.614-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Creating a multilingual email
publishexternaldate: 2018-07-23T06 02 44.215-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/channels/using/creating-a-multilingual-email.html
sha1: 0e5e38968113510cffa55dbc55ee218be749e9be
topicBrowsingSortDate: 2018-07-23T06:02:44.215-0400
index: y
internal: n
snippet: y
---

# Creating a multilingual email

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

