---
title: Campaign dimensions and metrics in Analytics
seo-title: Campaign dimensions and metrics in Analytics
description: Campaign dimensions and metrics in Analytics
seo-description: Learn the different dimensions that you can find in Adobe Analytics to start tracking your email deliveries from Adobe Campaign.
page-status-flag: never-activated
uuid: 83d36180-d1e2-4012-a31e-96a9dcf917ac
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/integrating/using/campaign-dimensions-and-metrics-in-analytics
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-analytics
discoiquuid: aa58c0ad-a0c0-4f62-91d6-0ab42d429af5
isreadyforlocalization: false
navTitle: Campaign dimensions and metrics in Analytics
publishexternaldate: 2018-11-20
sha1: 9846d68e3b14094179603e0063002597967e1bba
index: y
internal: n
snippet: y
---

# Campaign dimensions and metrics in Analytics{#campaign-dimensions-and-metrics-in-analytics}

Campaign dimensions and metrics in Analytics

Adobe Campaign and Adobe Analytics integration lets you track the success of your email deliveries directly in Adobe Analytics.

Campaign **dimensions** found in Analytics are listed below:

<table> 
 <thead> 
  <tr> 
   <th> Dimension<br /> </th> 
   <th> Definition<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Campaign ID<br /> </td> 
   <td> Campaign's internal name as seen in Campaign<br /> </td> 
  </tr> 
  <tr> 
   <td> Campaign label<br /> </td> 
   <td> Campaign's label as seen in Campaign<br /> </td> 
  </tr> 
  <tr> 
   <td> Delivery ID<br /> </td> 
   <td> Delivery's internal name as seen in Campaign.<br /> For example, DM1 is a recurring delivery scheduled to send child deliveries every week. DM2, DM3 and DM4 are sent the first three weeks. The Delivery ID dimension will then display the results for every delivery, namely DM1 to DM4. <br /> </td> 
  </tr> 
  <tr> 
   <td> Delivery label<br /> </td> 
   <td> Delivery's label as seen in Campaign<br /> </td> 
  </tr> 
  <tr> 
   <td> Executed delivery ID<br /> </td> 
   <td> Delivery's internal name as seen in Campaign. This only concerns delivery in execution in Campaign.<br /> For example, DM1 is a recurring delivery scheduled to send child deliveries every week. DM2, DM3 and DM4 are sent the first three weeks. The Executed delivery ID dimension will then display the results for the executed deliveries, namely the child deliveries DM2, DM3 and DM4. <br /> </td> 
  </tr> 
  <tr> 
   <td> Executed delivery label<br /> </td> 
   <td> Delivery's label as seen in Campaign. This only concerns delivery in execution in Campaign.<br /> </td> 
  </tr> 
 </tbody> 
</table>

Campaign **metrics** found in Analytics are listed below:

<table> 
 <thead> 
  <tr> 
   <th> Metric<br /> </th> 
   <th> Definition<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Clicked<br /> </td> 
   <td> Number of times a content was clicked in a delivery.<br /> </td> 
  </tr> 
  <tr> 
   <td> Delivered<br /> </td> 
   <td> Number of messages successfully sent, in relation to the total number of sent messages.<br /> </td> 
  </tr> 
  <tr> 
   <td> Opened<br /> </td> 
   <td> Number of times a message was opened in a delivery.<br /> </td> 
  </tr> 
  <tr> 
   <td> Sent<br /> </td> 
   <td> Total number of sends for the delivery.<br /> </td> 
  </tr> 
  <tr> 
   <td> Total Bounces<br /> </td> 
   <td> Total of errors cumulated during delivery and automatic return processing in relation to the total number of sent messages.<br /> </td> 
  </tr> 
  <tr> 
   <td> Unique Open<br /> </td> 
   <td> Number of recipients who opened the delivery.<br /> </td> 
  </tr> 
  <tr> 
   <td> Unique Click<br /> </td> 
   <td> Number of recipients who clicked on a content in a delivery.<br /> </td> 
  </tr> 
  <tr> 
   <td> Unsubscribed<br /> </td> 
   <td> Number of clicks on the unsubscription link.<br /> </td> 
  </tr> 
 </tbody> 
</table>

