---
title: Email rendering
seo-title: Email rendering
description: Email rendering
seo-description: Discover the email rendering feature.
uuid: d6c543f1-5ba8-4bb7-a4a7-9caa99e7365a
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/sending/using/email-rendering
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-08T08 23 04.383-0400
cq-lastreplicated: 2018-09-07T15 11 17.371-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: preparing-and-testing-messages
cq-template: /apps/help/templates/article-3
discoiquuid: 1ed3f1af-737c-40b8-81b9-244b8115c418
firstPublishExternalDate: 2018-09-07T15:11:17.306-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 01 40.105-0400
jcr-createdby: admin
jcr-description: Email rendering
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T15:11:17.306-0400
lochandoffdate: 2018-09-08T08 23 04.383-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Email rendering
publishexternaldate: 2018-09-07T15 11 17.306-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/sending/using/email-rendering.html
sha1: d6d87ae464bcf601f13415cd8670a046ba840b3a
topicBrowsingSortDate: 2018-09-07T15:11:17.306-0400
index: y
internal: n
snippet: y
---

# Email rendering

Email rendering

Before hitting the **Send** button, make sure that your message will be displayed in an optimal way on a variety of web clients, web mails and devices.

To allow this, Adobe Campaign captures the rendering and makes it available in a dedicated report. This enables you to preview the sent message in the different contexts in which it may be received.

The mobile, messaging and webmail clients available for **Email rendering** in Adobe Campaign are listed on the Litmus [website](https://litmus.com/email-testing) (click **View all email clients**).

## Checking the Email rendering report

Once you have created your email delivery and defined its content as well as the targeted population, follow the steps below.

1. Click **Audience** to access the **Test profiles** tab.

   ![](assets/email_rendering_05.png)

1. Use the query editor to define the test profiles that you want to use, including the test profiles that are for **Email rendering** use. See [About test profiles](../../sending/using/managing-test-profiles-and-sending-proofs.md#about-test-profiles).

   ![](assets/email_rendering_06.png)

1. Check and confirm your query, then save your changes.
1. Click the **Test** button in the action bar.

   ![](assets/email_rendering_07.png)

1. Select the **Email rendering** option then click **OK**.

   ![](assets/email_rendering_08.png)

   >[!NOTE]
   >
   >The **Proof + Email rendering** option enables you to send a proof and use the email rendering feature simultaneously. You can have your message approved by the proof recipients and at the same time you can test the way your message will be received depending on the inboxes targeted. In this case, you also need to select Proof test profiles. See [About test profiles](../../sending/using/managing-test-profiles-and-sending-proofs.md#about-test-profiles).

   The test delivery is sent.

1. The rendering thumbnails are available a few minutes after sending the messages. To access them, select **Proofs** in the **Summary** drop-down list.

   ![](assets/email_rendering_03.png)

1. From the **Proofs** list, click the **Access email rendering** icon.

   ![](assets/email_rendering_04.png)

The dedicated email rendering report is displayed. See [Email rendering report description](../../sending/using/email-rendering.md#email-rendering-report-description).

**Related topics**:

* [Creating an email](../../channels/using/creating-an-email.md)
* [Managing test profiles and sending proofs](../../sending/using/managing-test-profiles-and-sending-proofs.md)
* [Query editor](../../automating/using/editing-queries.md#about-query-editor)

## Email rendering report description

This report presents the email renderings as they appear to the recipient. Email renderings can differ based upon how the recipient opens the email delivery: in a browser, on a mobile device, or via an email application.

>[!NOTE]
>
>The number of available renderings is listed in your license agreement. Each delivery with **Email rendering** enabled decreases your available renderings (known as tokens) by one. If you are a Litmus client, you can use your own Litmus account to provision and use Email rendering in Adobe Campaign. For more on this, contact your Adobe account executive.

The report summary presents the number of messages received, unwanted (spam), not received, or pending reception.

![](assets/inbox_rendering_report.png)

The report is divided into three parts: **Mobile**, **Messaging clients**, and **Webmails**. Scroll down the report to display all the renderings grouped into these three categories.

![](assets/inbox_rendering_report_3.png)

To get the details for each report, click the corresponding card. The rendering is displayed for the reception method selected.

![](assets/inbox_rendering_report_2.png)

The **Technical data** tab allows you to get more information, such as the receiving and capture dates, and the complete headers of emails.
