---
title: Managing incoming SMS
seo-title: Managing incoming SMS
description: Managing incoming SMS
seo-description: Learn how to manage STOP SMS and store incoming SMS in Adobe Campaign.
uuid: 2f4e544e-bfa8-441e-af77-5b009602ccc2
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/channels/using/managing-incoming-sms
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-30T04 53 53.745-0400
cq-lastreplicated: 2018-07-23T06 02 48.090-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: sms-messages
cq-template: /apps/help/templates/article-3
discoiquuid: 01f83aba-7af3-44a5-9e81-1ea941ce4253
firstPublishExternalDate: 2018-07-23T06:02:47.995-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 14.075-0400
jcr-createdby: admin
jcr-description: Managing incoming SMS
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T06:02:47.995-0400
lochandoffdate: 2018-07-30T04 53 53.745-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Managing incoming SMS
publishexternaldate: 2018-07-23T06 02 47.995-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/channels/using/managing-incoming-sms.html
sha1: 4dae22a839f58ddafd0975ed688feb3b8d1a145d
topicBrowsingSortDate: 2018-07-23T06:02:47.995-0400
index: y
internal: n
snippet: y
---

# Managing incoming SMS

Managing incoming SMS

## Managing STOP SMS

When a profile replies to an SMS message which was sent via Campaign, you can configure messages which are automatically sent back to him as well as the action to perform.

This configuration is defined in the **Automatic reply sent to the MO** section of the [SMS Routing external account](../../administration/using/configuring-sms-channel.md#defining-an-sms-routing). MO stands for 'Mobile Originated', which means that you can configure an auto-reply to the mobile who sent the SMS.

To do so:

1. From the advanced menu, via the Adobe Campaign logo, select **Administration > Application settings > External accounts** then the **SMS routing via SMPP** external account.
1. Under the **Automatic reply sent to the MO** category, click **Create element** to start configuring your automatic reply.

   ![](assets/sms_mo_1.png)

1. Choose the keyword that will trigger this automatic reply. The keywords are not case-sensitive. For example, here, if recipients send the keyword "STOP", they will receive the automatic reply.

   Leave this column empty if you want to send the same reply no matter what the keyword is.

   ![](assets/sms_mo_2.png)

1. In the **Short code** field, specify a number that is usually used to send deliveries and will serve as a sender name. You can also decide to leave the **Short code** column empty, to send the same reply no matter what the short code.

   ![](assets/sms_mo_4.png)

1. Type in the answer you want to send to your recipients in the field **Answer**.

   To carry out an action without sending a reply, leave the **Answer** column empty. For example, this allows you to remove from quarantine the phone number of a user who replies with a message other than "STOP".

   ![](assets/sms_mo_3.png)

1. In the **Additional action** field, link an action to your automatic reply:

    * The **Blacklist** action automatically quarantines the profile phone number.
    * The **Unblacklist** action removes the profile phone number from quarantine.
    * The **None** action allows you to only send the message to your recipients without carrying an action.

   For example, in the configuration below, if recipients send the keyword "STOP", they will automatically receive an unsubscription confirmation and their phone number will be sent to quarantine with the **Blacklisted** status. This status refers to the phone number only, the profile is not blacklisted so that the user continues receiving email messages.

   ![](assets/sms_mo.png)

Your recipients can now be automatically unsubscribed to your messages and sent to quarantine with this automatic reply. The quarantined recipients are listed in the **Addresses** table available through the **Administration** > **Channels** > **Quarantines** menu. For more information on quarantines, refer to this [section](../../sending/using/understanding-quarantine-management.md).

These incoming SMS can be stored if needed. For more information on this, refer to this [section](../../channels/using/managing-incoming-sms.md#storing-incoming-sms).

## Storing incoming SMS

In the **SMS routing via SMPP** external account, you can choose to store incoming messages for example when a subscriber replies "STOP" to an SMS message in order to be removed from your recipient lists.

![](assets/sms_config_mo_1.png)

By checking **Store incoming MO in the database** in the **SMPP channel settings** category, all SMS will be stored in the inSMS table and can be retrieved via a query activity in a workflow.

To do so:

1. In the **SMPP channel settings** field, check **Store incoming MO in the database**.

   ![](assets/sms_config_mo_2.png)

1. In the **Marketing activities** tab, click **Create** then select **Workflow**.

   ![](assets/sms_config_mo_3.png)

1. Select your workflow type.
1. Edit the properties of your workflow, then click **Create**. For more on workflows creation, refer to this [section](../../automating/using/building-a-workflow.md).
1. Drag and drop a **Query** activity and double-click the activity.
1. In the **Properties** tab of the query, choose **Incoming SMS (inSMS)** in the **Resource** field.

   ![](assets/sms_config_mo_4.png)

1. Then, in the **Target** tab, drag and drop the **Incoming SMS attributes** rule.

   ![](assets/sms_config_mo_5.png)

1. Here, we want to target every incoming message from the day before. In the **Field** category, select **Creation date (created)**.
1. In **Filter type**, select **Relative** then in **Level of precision**, choose **Day**.

   ![](assets/sms_config_mo_6.png)

1. You can then choose to retrieve data from today, the day before or the last few days. Click **Confirm** when your query is configured.

This query will retrieve every STOP message received depending on the chosen time range.

The activity allows you for example to build a population and better personalize your deliveries.
