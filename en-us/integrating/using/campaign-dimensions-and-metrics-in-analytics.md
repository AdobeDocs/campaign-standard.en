---
title: Campaign dimensions and metrics in Analytics
seo-title: Campaign dimensions and metrics in Analytics
description: Campaign dimensions and metrics in Analytics
seo-description: Learn the different dimensions that you can find in Adobe Analytics to start tracking your email deliveries from Adobe Campaign.
uuid: bfe0137e-541d-4a69-bada-f4465d7e3839
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/integrating/using/campaign-dimensions-and-metrics-in-analytics
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-27T03 26 46.032-0400
cq-lastreplicated: 2018-07-23T05 59 38.756-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-analytics
cq-template: /apps/help/templates/article-3
discoiquuid: 7253fc31-855a-41bd-95d3-be8879d81c02
firstPublishExternalDate: 2018-07-23T05:59:38.725-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-05-07T07 29 25.627-0400
jcr-createdby: admin
jcr-description: Campaign dimensions and metrics in Analytics
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T05:59:38.725-0400
lochandoffdate: 2018-07-27T03 26 46.030-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Campaign dimensions and metrics in Analytics
publishexternaldate: 2018-07-23T05 59 38.725-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/integrating/using/campaign-dimensions-and-metrics-in-analytics.html
sha1: e3e37e86ab87eb0518e3e199af4c55aa9c2f785d
topicBrowsingSortDate: 2018-07-23T05:59:38.725-0400
index: y
internal: n
snippet: y
---

# Campaign dimensions and metrics in Analytics

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

