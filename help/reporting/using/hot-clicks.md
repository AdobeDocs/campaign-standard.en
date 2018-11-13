---
title: Hot clicks
seo-title: Hot clicks
description: Hot clicks
seo-description: With the Hot clicks out-of-the-box report, learn where your customer clicked on your delivery.
uuid: 0f39796f-4cba-4a68-86dd-56cfd1618cb4
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/reporting/using/hot-clicks
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-10T02 19 10.052-0400
cq-lastreplicated: 2018-09-07T15 08 39.446-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: reporting
content-type: reference
topic-tags: list-of-reports
cq-template: /apps/help/templates/article-3
discoiquuid: a141a4d1-c150-48ac-8771-657771121be2
firstPublishExternalDate: 2018-09-07T15:08:38.537-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 00.205-0400
jcr-createdby: admin
jcr-description: Hot clicks
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T15:08:38.537-0400
lochandoffdate: 2018-09-10T02 19 10.051-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Hot clicks
publishexternaldate: 2018-09-07T15 08 38.537-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/reporting/using/hot-clicks.html
sha1: e0179556de5124f6a6f901fdf46b82226924fc4a
topicBrowsingSortDate: 2018-09-07T15:08:38.537-0400
index: y
internal: n
snippet: y
---

# Hot clicks{#hot-clicks}

Hot clicks

This report can be accessed from the **Reports** button in each delivery or transactional message.

![](assets/delivery_reports_hot-clicks_4.png)

It presents the message content (HTML and/or text) with the percentage of clicks on each link.

![](assets/delivery_reports_10.png)

If you created dynamic content for your delivery, you can view the percentages for each condition that you defined. For more on inserting conditional content in a delivery, see [Defining dynamic content](../../designing/using/defining-dynamic-content-in-a-landing-page.md).

For example, imagine you created a delivery with the following conditions:

* The link on the main image is different if the recipient is a man or a woman.
* You also added a link to a special offer that is only visible to recipients over 25.

Once your message is sent, select **Reports** > **Hot clicks** from the delivery dashboard.

By default, no profile is selected. Only clicks for recipients whose gender is unknown and for recipients who are under 25 or whose age is unknown are displayed.

![](assets/delivery_reports_hot-clicks_1.png)

To display clicks for women, click the **Change profile** button and select a female test profile. To display clicks for men, proceed similarly and select a male test profile.

![](assets/delivery_reports_hot-clicks_2.png)

To display clicks for recipients over 25, click the **Change profile** button and select a test profile whose birth date is matching this condition.

For more on test profiles, see [About test profiles](../../sending/using/managing-test-profiles-and-sending-proofs.md#about-test-profiles).

>[!NOTE]
>
>The number of clicks on a specific link is a percentage of the total clicks for all conditional contents in a delivery. Therefore, if you defined dynamic content, the total of the percentages displayed for a specific test profile might not equal 100.

Similarly, for recurring deliveries and transactional messages, you can select the test profile corresponding to the dynamic content that you want to display, but you can also view the click percentages according to the selected execution delivery.

An execution delivery is a non-actionable and non-functional technical message that is created in the following cases:

* Each time a recurring delivery is executed or updated.

  For example, if the workflow managing this delivery is executed once a month, there will be one execution delivery per month. In addition to this, each time the content of the delivery is updated, an additional execution delivery is created.

  For more on recurring email deliveries, see [Email delivery](../../automating/using/email-delivery.md).

* By default once a month for transactional messages, and each time a transactional message is edited and published again.

  For more on transactional messages, see [About transactional messaging](../../channels/using/about-transactional-messaging.md).

>[!NOTE]
>
>Because the tracked URLs' IDs are different for each execution, the hot clicks data cannot be aggregated for all the execution deliveries of a given message. It can only be displayed for one execution delivery at a time.

Once your message is sent, select **Reports** > **Hot clicks** from the delivery dashboard.

By default, the last execution delivery is selected. Click the **Change execution delivery** button to select another one.

![](assets/delivery_reports_hot-clicks_3.png)

Only the click percentages for the selected delivery execution are displayed.
