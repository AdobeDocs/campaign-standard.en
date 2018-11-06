---
title: Indicator calculation
seo-title: Indicator calculation
description: Indicator calculation
seo-description: Understand the results of your reports with a list of every metric's formula.
uuid: 8da68d13-c722-41d4-9034-71d865c4684a
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/reporting/using/indicator-calculation
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-10T02 18 43.667-0400
cq-lastreplicated: 2018-09-07T15 03 21.992-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: reporting
content-type: reference
topic-tags: about-reporting
cq-template: /apps/help/templates/article-3
discoiquuid: 45d6bcc8-6ca5-4bdf-a5b7-c37cace9e74c
firstPublishExternalDate: 2018-09-07T15:03:19.185-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 03 01.935-0400
jcr-createdby: admin
jcr-description: Indicator calculation
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T15:03:19.185-0400
lochandoffdate: 2018-09-10T02 18 43.667-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Indicator calculation
publishexternaldate: 2018-09-07T15 03 19.185-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/reporting/using/indicator-calculation.html
sha1: 2ad61f3ca9cb86d54fb414d7191e4731e0e7bf8d
topicBrowsingSortDate: 2018-09-07T15:03:19.185-0400
index: y
internal: n
snippet: y
---

# Indicator calculation

Indicator calculation

The table below gives you the list of indicators used in the different reports and their calculation formula.

>[!NOTE]
>
>Unique clicks is calculated using ThetaSketch concepts.

<table> 
 <thead> 
  <tr> 
   <th> <strong>Label</strong> <br /> </th> 
   <th> <strong>Field name</strong> <br /> </th> 
   <th> <strong>Indicator description</strong> <br /> </th> 
   <th> <strong>Indicator calculation formula</strong> <br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Account disabled<br /> </td> 
   <td> @disabled<br /> </td> 
   <td> Count of all messages with a status equal to "Failed" and a reason equal to "Account disabled".<br /> </td> 
   <td> count(@failureReason=4)<br /> </td> 
  </tr> 
  <tr> 
   <td> Blacklisted<br /> </td> 
   <td> @blacklisted<br /> </td> 
   <td> Number of messages that are marked as spam by recipients, also includes the number of recipients who clicked on the mail-client generated unsubscription link.<br /> </td> 
   <td> count(@failureReason=8, @failureType=2)<br /> </td> 
  </tr> 
  <tr> 
   <td> Blacklisted rate<br /> </td> 
   <td> @rateBlacklisted<br /> </td> 
   <td> Rate of broadlogs marked as blacklisted.<br /> </td> 
   <td> @blacklisted/@sent<br /> </td> 
  </tr> 
  <tr> 
   <td> Bounces + Errors<br /> </td> 
   <td> @bounces<br /> </td> 
   <td> Sum of bounces following a delivery.<br /> </td> 
   <td> count(@status=2)<br /> </td> 
  </tr> 
  <tr> 
   <td> Bounce + Error rate<br /> </td> 
   <td> @rateBounces<br /> </td> 
   <td> Rate of deliveries that bounced in relation to the total number of sent messages.<br /> </td> 
   <td> @bounces/@sent<br /> </td> 
  </tr> 
  <tr> 
   <td> Click<br /> </td> 
   <td> @clicks<br /> </td> 
   <td> Number of times a content was clicked in a delivery.<br /> </td> 
   <td> count(@trackingUrlType=1 or 10)<br /> </td> 
  </tr> 
  <tr> 
   <td> Delivered<br /> </td> 
   <td> @delivered<br /> </td> 
   <td> Number of messages processed successfully.<br /> </td> 
   <td> count(@status=1)<br /> </td> 
  </tr> 
  <tr> 
   <td> Delivered rate<br /> </td> 
   <td> @rateDelivered<br /> </td> 
   <td> Rate of deliveries successfully sent.<br /> </td> 
   <td> @delivered/@sent<br /> </td> 
  </tr> 
  <tr> 
   <td> Hard bounces<br /> </td> 
   <td> @hardBounces<br /> </td> 
   <td> Total number of permanent errors.<br /> </td> 
   <td> count(@failureType=2 AND @failureReason=8)<br /> </td> 
  </tr> 
  <tr> 
   <td> Hard bounces rate<br /> </td> 
   <td> @rateHardBounces<br /> </td> 
   <td> Rate of deliveries that failed due to permanent reason.<br /> </td> 
   <td> @hardBounces/@sent<br /> </td> 
  </tr> 
  <tr> 
   <td> Invalid domain<br /> </td> 
   <td> @invalidDomain<br /> </td> 
   <td> Count of all messages with a status equal to "Failed" and a reason equal to "Invalid domain". <br /> </td> 
   <td> count(@failureReason=2)<br /> </td> 
  </tr> 
  <tr> 
   <td> Mailbox full<br /> </td> 
   <td> @mailBoxFull<br /> </td> 
   <td> Count of all messages with a status equal to "Failed" and a reason equal to "Inbox full". <br /> </td> 
   <td> count(@failureReason=5)<br /> </td> 
  </tr> 
  <tr> 
   <td> Mirror page<br /> </td> 
   <td> @mirrorPage<br /> </td> 
   <td> Number of recipients who clicked on the mirror page link.<br /> </td> 
   <td> count(@trackingUrlType=6)<br /> </td> 
  </tr> 
  <tr> 
   <td> Mirror page rate<br /> </td> 
   <td> @rateMirrorPage<br /> </td> 
   <td> Number of clicks on the mirror page link in relation to the total number of delivered messages.<br /> </td> 
   <td> @mirrorPage/@delivered<br /> </td> 
  </tr> 
  <tr> 
   <td> Not connected<br /> </td> 
   <td> @notConnected<br /> </td> 
   <td> Count of all messages with a status equal to "Failed" and a reason equal to "Not connected". <br /> </td> 
   <td> count(@failureReason=6)<br /> </td> 
  </tr> 
  <tr> 
   <td> Opens<br /> </td> 
   <td> @opens<br /> </td> 
   <td> Sum of each time a recipient opened a delivery.<br /> </td> 
   <td> count(@trackingUrlType=2 + unique(@trackingUrlType=1,2,3,6,10,11) - unique(@trackingUrlType=2))<br /> </td> 
  </tr> 
  <tr> 
   <td> Opens rate<br /> </td> 
   <td> @rateOpens<br /> </td> 
   <td> Rate of deliveries opened by recipients.<br /> </td> 
   <td> @opens/@delivered<br /> </td> 
  </tr> 
  <tr> 
   <td> Quarantine<br /> </td> 
   <td> @quarantine<br /> </td> 
   <td> Number of recipients that were quarantined.<br /> </td> 
   <td> isQuarantine=true<br /> </td> 
  </tr> 
  <tr> 
   <td> Quarantine rate<br /> </td> 
   <td> @rateQuarantine<br /> </td> 
   <td> Rate of quarantines in relation to the total number of sent messages.<br /> </td> 
   <td> @quarantine/@sent<br /> </td> 
  </tr> 
  <tr> 
   <td> Refused<br /> </td> 
   <td> @refused<br /> </td> 
   <td> Count of all messages with a status equal to "Failed" and a reason equal to "Refused". <br /> </td> 
   <td> count(@failureReason=20)<br /> </td> 
  </tr> 
  <tr> 
   <td> Rejected<br /> </td> 
   <td> @rejected<br /> </td> 
   <td> Number of deliveries automatically declared as spam by the SMTP servers.<br /> </td> 
   <td> count(@failureReason=20, @failureType=2)<br /> </td> 
  </tr> 
  <tr> 
   <td> Rejected rate<br /> </td> 
   <td> @rateRejected<br /> </td> 
   <td> Rate of broadlogs marked as rejected.<br /> </td> 
   <td> @rejected/@sent<br /> </td> 
  </tr> 
  <tr> 
   <td> Sent<br /> </td> 
   <td> @sent<br /> </td> 
   <td> Number of sends for the delivery.<br /> </td> 
   <td> @delivered + @bounces<br /> </td> 
  </tr> 
  <tr> 
   <td> Soft bounces<br /> </td> 
   <td> @softBounces<br /> </td> 
   <td> Total number of temporary errors.<br /> </td> 
   <td> count(@failureType=1)<br /> </td> 
  </tr> 
  <tr> 
   <td> Soft bounces rate<br /> </td> 
   <td> @rateSoftBounces<br /> </td> 
   <td> Rate of deliveries that failed due to temporary reason.<br /> </td> 
   <td> @softBounces/@sent<br /> </td> 
  </tr> 
  <tr> 
   <td> Unique opens<br /> </td> 
   <td> @uniqueopens<br /> </td> 
   <td> Number of opens by a unique recipient.<br /> </td> 
   <td> unique(@trackingUrlType=1,2,3,6,10,11)<br /> </td> 
  </tr> 
  <tr> 
   <td> Unreachable <br /> </td> 
   <td> @unreachable<br /> </td> 
   <td> Count of all messages with a status equal to "Failed" and a reason equal to "Unreachable". <br /> </td> 
   <td> count(@failureReason=3)<br /> </td> 
  </tr> 
  <tr> 
   <td> Unsubscribe<br /> </td> 
   <td> @unsubscribes<br /> </td> 
   <td> Number of recipients who clicked on the Unsubscription link.<br /> </td> 
   <td> count(@trackingUrlType=3)<br /> </td> 
  </tr> 
  <tr> 
   <td> Unsubscribe rate<br /> </td> 
   <td> @rateUnsubscribes<br /> </td> 
   <td> Rate of unsubscriptions in relation to the total number of messages delivered.<br /> </td> 
   <td> @unsubscribes/@delivered<br /> </td> 
  </tr> 
  <tr> 
   <td> User unknown<br /> </td> 
   <td> @unknownUser<br /> </td> 
   <td> Count of all messages with a status equal to "Failed" and a reason equal to "User unknown". <br /> </td> 
   <td> count(@failureReason=1)<br /> </td> 
  </tr> 
 </tbody> 
</table>

