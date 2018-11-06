---
title: Tracking messages
seo-title: Tracking messages
description: Tracking messages
seo-description: Learn how to track the behavior of your delivery recipients.
uuid: c230a43b-f05a-4218-b241-bf50d49e9e84
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/sending/using/tracking-messages
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-30T04 53 56.139-0400
cq-lastreplicated: 2018-07-23T06 02 25.570-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: sending-and-tracking-messages
cq-template: /apps/help/templates/article-3
discoiquuid: d8973611-1240-464a-a82d-8a7a6369fa8e
firstPublishExternalDate: 2018-07-23T06:02:25.531-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 01 51.016-0400
jcr-createdby: admin
jcr-description: Tracking messages
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T06:02:25.531-0400
lochandoffdate: 2018-07-30T04 53 56.138-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Tracking messages
publishexternaldate: 2018-07-23T06 02 25.531-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/sending/using/tracking-messages.html
sha1: 9f7a4ee053ec1b8a7faab6151e5c0921a60c47d1
topicBrowsingSortDate: 2018-07-23T06:02:25.531-0400
index: y
internal: n
snippet: y
---

# Tracking messages

Tracking messages

## About tracking

Thanks to its tracking functionalities, Adobe Campaign enables you to track the behavior of your delivery recipients. To do this, Adobe Campaign uses session cookies and permanent cookies.

You can inform users that your sites are equipped with web tracking tools via an authorization request (that comes up over the page, for example) with a checkbox to authorize the use of cookies, or add a banner at the top of the first page they land on, etc. Pop-up windows should be avoided as they are often blocked by browsers.

Adobe Campaign uses two types of cookies:

* A session cookie (nlid). This contains the identifier of the email sent to the contact (broadlogId) and the identifier of the message template (deliveryId). It is added when the contact clicks a URL included in an email sent by Adobe Campaign and enables you to track their behavior on the web. This session cookie is erased automatically when the browser is closed. The contact can configure their browser to refuse cookies.
* A cookie shared between Adobe Experience Cloud solutions. This enables you to identify the users who interact with the Experience Cloud solutions when they visit a website. The description of this cookie is available here: [https://marketing.adobe.com/resources/help/en_US/whitepapers/cookies/cookies_mc.html](https://marketing.adobe.com/resources/help/en_US/whitepapers/cookies/cookies_mc.html).

Tracking information are available for each contact of your database into **integrated customer profiles**. For more on this, refer to [this section](../../audiences/using/integrated-customer-profile.md).

## Tracking logs

The **Tracking logs** tab lists the tracking history for this delivery. This tab displays the tracking information for the sent messages, such as all the URLs which have been tracked by Adobe Campaign. Tracking information in this tab is updated every 10 minutes.

>[!NOTE]
>
>If tracking is not enabled for a delivery, this tab is not displayed. Tracking logs are available for the **email** and **push notification** channels only.

![](assets/tracking_logs.png)

In the example above, the recipient:

* Opened the message.
* Clicked on the "LEARN MORE" custom link.
* Clicked on the unsubscription and the mirror page link.

In the **Type** column, the possible values are:

* **Email click**: the recipients clicked on a custom link. 
* **Mirror page**: the recipient clicked on a link to the mirror page. 
* **Open**: the recipient opened the email.
* **Opt-out**: the recipient clicked on an unsubscription link.

>[!NOTE]
>
>For the **push notification** channel, only clicks on mobile notifications are tracked. In that case, the value will be **Click on mobile notification**.

For more on how to insert tracking links, refer to [this page](../../designing/using/inserting-a-link.md).

## Tracked URLs

The **Tracked URLs** tab regroups the URLs contained in the sent message, including their URL type and their source URL.

![](assets/sending_delivery6.png)

For more on tracking links, refer to [this section](../../designing/using/about-tracked-urls.md).
