---
title: Adobe Campaign notifications
seo-title: Adobe Campaign notifications
description: Adobe Campaign notifications
seo-description: Learn how to send real-time system notifications to your Adobe Campaign users.
uuid: 39ac38cd-54a3-49dc-8380-fe383f4baced
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/administration/using/adobe-campaign-notifications
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-10T07 26 53.763-0400
cq-lastreplicated: 2018-09-07T15 06 35.642-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: application-settings
cq-template: /apps/help/templates/article-3
discoiquuid: 6ec658d7-37c9-4809-a176-c04817310ce1
firstPublishExternalDate: 2018-09-07T15:06:34.360-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-02-16T08 01 36.554-0500
jcr-createdby: admin
jcr-description: Adobe Campaign notifications
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T15:06:34.360-0400
lochandoffdate: 2018-09-10T07 26 53.762-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Adobe Campaign notifications
publishexternaldate: 2018-09-07T15 06 34.360-0400
publishExternalURL: "https://helpx.adobe.com/campaign/standard/administration/using/adobe-campaign-notifications.html"
sha1: ecdb17a5a7efc8e81a18d14f64f6311bf3cd3a30
topicBrowsingSortDate: 2018-09-07T15:06:34.360-0400
index: y
internal: n
snippet: y
---

# Adobe Campaign notifications{#adobe-campaign-notifications}

Adobe Campaign notifications

Adobe Campaign gives you the possibility to receive notifications regarding important system activities directly within the application. Real-time notifications keep relevant stakeholders informed and provide users with the ability to immediately and directly act on activity notifications from within the application. The result for teams is advanced agility, efficiency and smoother execution of campaigns.

![](assets/pulse_3.png)

You can configure notifications for the following objects:

* **A/B Test emails**: the email creator and modifier(s) are notified that a variant has been chosen (automatic mode) or that a variant needs to be chosen (manual mode). Clicking on the notification displays the corresponding email. Notifications are activated by default in the out-of-the-box A/B Test template. If you want to deactivate them, edit the properties of the email or the email template and uncheck the box located under **General > Notifications**. For more information on A/B Test emails, refer to [Creating an AB Test](../../channels/using/designing-an-a-b-test-email.md). For more on email properties, refer to [List of email properties](../../administration/using/configuring-email-channel.md#list-of-email-properties).

  ![](assets/pulse_2.png)

* **Workflows**: each member of the selected security group are notified (email and in-app notification) whenever a workflow is in error. Clicking on the notification or on the email link displays the corresponding workflow. Notifications are deactivated by default in the out-of-the-box workflow template. If you want to activate them, edit the properties of the workflow or workflow template and add a security group under **General > Execution > Error management > Supervisors**. For more information on security groups, refer to [Managing groups and users](../../administration/using/managing-groups-and-users.md). For more on workflow properties, refer to [Workflow properties](../../automating/using/executing-a-workflow.md#workflow-properties).

  ![](assets/pulse_1.png)

