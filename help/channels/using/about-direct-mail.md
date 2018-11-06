---
title: About direct mail
seo-title: About direct mail
description: About direct mail
seo-description: Discover the main specificities of the direct mail channel in Adobe Campaign.
uuid: 4b3b7c58-a900-49aa-bd0b-aa370c557dc3
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/channels/using/about-direct-mail
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-08T08 23 16.131-0400
cq-lastreplicated: 2018-09-07T15 12 23.659-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: direct-mail
cq-template: /apps/help/templates/article-3
discoiquuid: 9e4106aa-790f-40b0-9b87-f2fc8eec4f19
firstPublishExternalDate: 2018-09-07T15:12:23.625-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 08.709-0400
jcr-createdby: admin
jcr-description: About direct mail
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T15:12:23.625-0400
lochandoffdate: 2018-09-08T08 23 16.131-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: About direct mail
publishexternaldate: 2018-09-07T15 12 23.625-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/channels/using/about-direct-mail.html
sha1: fbd1e535d65a7d217c13c2d38264bc6561645243
topicBrowsingSortDate: 2018-09-07T15:12:23.625-0400
index: y
internal: n
snippet: y
---

# About direct mail

About direct mail

Direct mail is an offline channel that allows you to personalize and generate the file required by direct mail providers. It gives you the possibility to mix online and offline channels in your customer journeys.

>[!NOTE]
>
>This feature is optional. Please check your license agreement. The **Export** role is required to use direct mail. Please contact your administrator.

Online channels allow you to create your messages (email, SMS, mobile app delivery, etc.) and send them to your audience directly from Adobe Campaign. With offline channels, it is different. When you prepare a direct mail delivery, Adobe Campaign generates a file including all the targeted profiles and the chosen contact information (postal address for example). You will then be able to send this file to your direct mail provider who will take care of the actual sending.

The following section explains how to create and generate a one-shot direct mail delivery. You also have the possibility to include a direct mail activity in a workflow to orchestrate campaigns combining online and offline channels. For more on this, refer to the [Workflows](../../automating/using/about-data-and-processes.md) guide.

The user process in Adobe Campaign is as follows:

1. Creating the delivery
1. Choosing the audience
1. Defining the content
1. Setting the contact date
1. Generating the file

## Recommendations

### Direct mail providers

First of all, you need to reach out to your direct mail provider and collect their recommendations. Identify what profile information needs to be included in the extraction file so that they can personalize the communication and send it to the audience. For example, the first and last name, the postal address, a promotion code, etc. These fields are the ones that you will add in the [Defining the extraction](../../channels/using/defining-the-direct-mail-content.md#defining-the-extraction) tab of the direct mail's content.

Make sure you have checked the **Address specified** box in your profiles' information. If this option is activated, the profile will be added to the target. It is not, it will excluded by a typology rule during the preparation phase (see [Creating the direct mail](../../channels/using/creating-the-direct-mail.md)). During profile import, do not forget to update this field.

![](assets/direct_mail_22.png)

### Postal addresses

When you add the fields to include in the extraction file, the postal address fields are available in the **Location** node.

Adobe Campaign offers you a set of predefined calculated fields that follow the most common postal address normalizations. The fields are available in the **Postal address **node.

An address can contain up to six lines by default: the first calculated field (**Line 1** contains the first name and last name, the next lines contain the postal address (road etc.), and the last line contains the ZIP/Postal code and town or city.

![](assets/direct_mail_23.png)

