---
title: List of components 
seo-title: List of components 
description: List of components 
seo-description: Find here the list of every components available in     Dynamic reports as well as their definitions.
page-status-flag: never-activated
uuid: a2403806-8df4-4bb1-bac2-2689dc584ae0
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: reporting
content-type: reference
topic-tags: about-reporting
discoiquuid: 17cf126a-7ce1-4e11-bb5e-2bdce01cfded

internal: n
snippet: y
---

# List of components {#list-of-components}

To learn more on compatibility between dimensions and metrics, refer to this [table](https://docs.campaign.adobe.com/doc/standard/en/Technotes/dynamic_report_compatibility.pdf). If two components are not compatible, the cell will display the value **None**.

![](assets/dynamic_report_compatibility.png)

## Dimensions {#dimensions}

The table below gives you the list of dimensions used in reports and their definitions.

<table> 
 <thead> 
  <tr> 
   <th> Dimension<br /> </th> 
   <th> Definition<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Browser<br /> </td> 
   <td> Browser from which the message was opened or clicked on.<br /> </td> 
  </tr> 
  <tr> 
   <td> Campaign<br /> </td> 
   <td> Label and ID of your campaign.<br /> </td> 
  </tr> 
  <tr> 
   <td> City<br /> </td> 
   <td> City registered in the recipient's profile.<br /> </td> 
  </tr> 
  <tr> 
   <td> Country<br /> </td> 
   <td> Country registered in the recipient's profile.<br /> </td> 
  </tr> 
  <tr> 
   <td> Delivery<br /> </td> 
   <td> Label and ID of the delivery.<br /> </td> 
  </tr> 
  <tr> 
   <td> Device<br /> </td> 
   <td> Device from which the email/SMS/push notification was opened/viewed/clicked on.<br /> </td> 
  </tr> 
  <tr> 
   <td> Failure reason<br /> </td> 
   <td> Types of errors that caused bounces for each delivery e.g. user unknown, invalid domain or mailbox full.<br /> </td> 
  </tr> 
  <tr> 
   <td> Gender<br /> </td> 
   <td> Recipient's gender such as male or female. If the gender field is empty in the recipient's profile, the value will be none.<br /> </td> 
  </tr> 
  <tr> 
   <td> In-App message actions<br /> </td> 
   <td> Actions on the In-App message delivered, e.g. actions on button 1 or 2 or dismissals.<br /> </td> 
  </tr> 
  <tr> 
   <td> Message type<br /> </td> 
   <td> Channel used for the delivery, such as email, SMS, push notification or In-App.<br /> </td> 
  </tr> 
  <tr> 
   <td> Mobile App name<br /> </td> 
   <td> Name of the mobile application<br /> </td> 
  </tr> 
  <tr> 
   <td> Platform<br /> </td> 
   <td> Platform of the device from which the message was opened/viewed/clicked on.<br /> </td> 
  </tr> 
  <tr> 
   <td> Profiles<br /> </td> 
   <td> Regroups out-of-the-box and custom profile fields created during the profile resource extension, for more on this refer to this <a href="../../developing/using/key-steps-to-add-a-resource.md">page</a> or this <a href="../../reporting/using/creating-a-custom-profile-dimension.md">example</a>.<br /> Note that data for this dimension is retrieved as soon as the custom resource linked to the profile field is published.<br /> </td> 
  </tr> 
  <tr> 
   <td> Push platform<br /> </td> 
   <td> Platform of the device from which the push notification was opened, such as iOS or Android.<br /> </td> 
  </tr> 
  <tr> 
   <td> Recipient domain<br /> </td> 
   <td> Domain used to open the email.<br /> </td> 
  </tr> 
  <tr> 
   <td> Recurring delivery<br /> </td> 
   <td> Label and ID of the recurring delivery.<br /> </td> 
  </tr> 
  <tr> 
   <td> Sender domain<br /> </td> 
   <td> Domain used to send the email.<br /> </td> 
  </tr> 
  <tr> 
   <td> Sender IP<br /> </td> 
   <td> IP used to send the email.<br /> </td> 
  </tr> 
  <tr> 
   <td> State<br /> </td> 
   <td> State registered in the recipient's profile.<br /> </td> 
  </tr> 
  <tr> 
   <td> Tracking URL<br /> </td> 
   <td> URL that was clicked on by the user from the message.<br /> </td> 
  </tr> 
  <tr> 
   <td> Tracking URL category<br /> </td> 
   <td> Category assigned to the tracking URL.<br /> </td> 
  </tr> 
  <tr> 
   <td> Tracking URL label<br /> </td> 
   <td> Label given to the URL, such as mirror page, contact us or open.<br /> </td> 
  </tr> 
  <tr> 
   <td> Transactional delivery<br /> </td> 
   <td> Label and ID of the transactional delivery.<br /> </td> 
  </tr> 
  <tr> 
   <td> Variant<br /> </td> 
   <td> Variant of the email in case of A/B testing.<br /> </td> 
  </tr> 
 </tbody> 
</table>

## Metrics {#metrics}

The tables below give you the list of metrics used in reports and their definitions depending on the delivery type.

### Email and SMS metrics {#email-and-sms-metrics}

<table> 
 <thead> 
  <tr> 
   <th> Metric<br /> </th> 
   <th> Definition<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Blacklisted<br /> </td> 
   <td> Number of recipients who have declared an email as spam or junk.<br /> </td> 
  </tr> 
  <tr> 
   <td> Blacklisted rate<br /> </td> 
   <td> Percentage of deliveries marked as blacklisted.<br /> </td> 
  </tr> 
  <tr> 
   <td> Bounces + Errors<br /> </td> 
   <td> Total of errors cumulated during delivery and automatic return processing in relation to the total number of sent messages.<br /> </td> 
  </tr> 
  <tr> 
   <td> Bounce + Error rate<br /> </td> 
   <td> Percentage of emails that bounced compared to email sent.<br /> </td> 
  </tr> 
  <tr> 
   <td> Click<br /> </td> 
   <td> Number of times a content was clicked in a delivery.<br /> </td> 
  </tr> 
  <tr> 
   <td> Click through rate<br /> </td> 
   <td> Percentage of clicks in a delivery.<br /> </td> 
  </tr> 
  <tr> 
   <td> Delivered<br /> </td> 
   <td> Number of messages successfully sent, in relation to the total number of sent messages.<br /> </td> 
  </tr> 
  <tr> 
   <td> Delivered rate<br /> </td> 
   <td> Percentage of messages successfully sent.<br /> </td> 
  </tr> 
  <tr> 
   <td> Hard bounce<br /> </td> 
   <td> Total number of permanent errors, such as a wrong email address.<br /> </td> 
  </tr> 
  <tr> 
   <td> Hard bounce rate<br /> </td> 
   <td> Percentage of deliveries that failed due to permanent errors.<br /> </td> 
  </tr> 
  <tr> 
   <td> Mirror page<br /> </td> 
   <td> Number of recipients who clicked on the mirror page link.<br /> </td> 
  </tr> 
  <tr> 
   <td> Mirror page rate<br /> </td> 
   <td> Percentage of clicks on the mirror page link compared to the total delivery messages.<br /> </td> 
  </tr> 
  <tr> 
   <td> Offer clicks<br /> </td> 
   <td> Number of time an offer was clicked on in a delivery.<br /> </td> 
  </tr> 
  <tr> 
   <td> Offer click rate<br /> </td> 
   <td> Percentage of clicks on an offer.<br /> </td> 
  </tr> 
  <tr> 
   <td> Open<br /> </td> 
   <td> Number of times a message was opened in a delivery.<br /> </td> 
  </tr> 
  <tr> 
   <td> Open rate<br /> </td> 
   <td> Percentage of opened messages.<br /> </td> 
  </tr> 
  <tr> 
   <td> Processed/sent<br /> </td> 
   <td> Total number of sends for the delivery.<br /> </td> 
  </tr> 
  <tr> 
   <td> Quarantine<br /> </td> 
   <td> Number of messages that bounced and resulted in the quarantine of the address.<br /> </td> 
  </tr> 
  <tr> 
   <td> Quarantine rate<br /> </td> 
   <td> Percentage of quarantines compared to sent messages.<br /> </td> 
  </tr> 
  <tr> 
   <td> Rejected<br /> </td> 
   <td> Number of messages classified as spam by the SMTP servers.<br /> </td> 
  </tr> 
  <tr> 
   <td> Rejected rate<br /> </td> 
   <td> Percentage of messages marked as rejected.<br /> </td> 
  </tr> 
  <tr> 
   <td> Soft bounce<br /> </td> 
   <td> Total number of temporary errors, such as a full inbox.<br /> </td> 
  </tr> 
  <tr> 
   <td> Soft bounce rate<br /> </td> 
   <td> Percentage of deliveries that failed due to temporary reason.<br /> </td> 
  </tr> 
  <tr> 
   <td> Unique clicks<br /> </td> 
   <td> Number of recipients who clicked on a content in a delivery.<br /> </td> 
  </tr> 
  <tr> 
   <td> Unique opens<br /> </td> 
   <td> Number of recipients who opened the delivery.<br /> </td> 
  </tr> 
  <tr> 
   <td> Unsubscribe rate<br /> </td> 
   <td> Percentage of unsubscriptions by recipient compared to the delivered messages.<br /> </td> 
  </tr> 
  <tr> 
   <td> Unsubscribed<br /> </td> 
   <td> Number of clicks on the unsubscription link.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Push notification metrics {#push-notification-metrics}

<table> 
 <thead> 
  <tr> 
   <th> Metric<br /> </th> 
   <th> Definition<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Bounces + Errors<br /> </td> 
   <td> Total of errors cumulated during delivery in relation to the total number of sent messages, e.g. errors from MCPNS or provider.<br /> </td> 
  </tr> 
  <tr> 
   <td> Bounce + Error rate<br /> </td> 
   <td> Percentage of push notifications that bounced compared to push notifications sent.<br /> </td> 
  </tr> 
  <tr> 
   <td> Click<br /> </td> 
   <td> Number of times a push notification has been delivered to the device and clicked on by the user. The user either wanted to view the notification, which will then be moved to Push Open tracking, or dismiss it.<br /> </td> 
  </tr> 
  <tr> 
   <td> Click through rate<br /> </td> 
   <td> Percentage of users who interacted with the push notification.<br /> </td> 
  </tr> 
  <tr> 
   <td> Delivered<br /> </td> 
   <td> Number of push notifications successfully sent, in relation to the total number of sent push notifications.<br /> </td> 
  </tr> 
  <tr> 
   <td> Delivered rate<br /> </td> 
   <td> Percentage of push notifications successfully sent.<br /> </td> 
  </tr> 
  <tr> 
   <td> Impressions<br /> </td> 
   <td> Number of times a push notification has been delivered to the device and left untouched in the notification center. In most cases, impressions number should be similar to the delivered number. This ensures that the device got the message and relayed that information back to the server.<br /> </td> 
  </tr> 
  <tr> 
   <td> Processed/sent<br /> </td> 
   <td> Total number of push notifications sent.<br /> </td> 
  </tr> 
  <tr> 
   <td> Open<br /> </td> 
   <td> Total number of push notifications delivered to the device and clicked on by users thus opening the app. This is similar to the Push Click except a Push Open will not be triggered if the notification was dismissed.<br /> </td> 
  </tr> 
  <tr> 
   <td> Open rate<br /> </td> 
   <td> Percentage of opened push notifications.<br /> </td> 
  </tr> 
  <tr> 
   <td> Unique click<br /> </td> 
   <td> Number of times a unique user interacts with the push notification, e.g. clicks on the notification or button.<br /> </td> 
  </tr> 
  <tr> 
   <td> Unique impressions<br /> </td> 
   <td> Number of impressions by recipient.<br /> </td> 
  </tr> 
  <tr> 
   <td> Unique Opens<br /> </td> 
   <td> Number of recipients who opened the delivery.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### In-App metrics {#in-app-metrics}

<table> 
 <thead> 
  <tr> 
   <th> Metric<br /> </th> 
   <th> Definition<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Delivered<br /> </td> 
   <td> Total number of In-App messages delivered to the device by the service provider.<br /> </td> 
  </tr> 
  <tr> 
   <td> Impressions<br /> </td> 
   <td> Total of In-App messages seen by recipients depending on whether trigger criterion was met.<br /> </td> 
  </tr> 
  <tr> 
   <td> In-App clicks <br /> </td> 
   <td> Total number of recipients who clicked on Button 1 or Button 2.<br /> </td> 
  </tr> 
  <tr> 
   <td> In-App click through rate<br /> </td> 
   <td> Percentage of users who clicked on Button 1 or Button 2 compared to users who saw the message.<br /> </td> 
  </tr> 
  <tr> 
   <td> In-App dismissal<br /> </td> 
   <td> Total number of messages that recipients dismissed either by clicking the close button or auto-dismiss.<br /> </td> 
  </tr> 
  <tr> 
   <td> In-App dismissal rate<br /> </td> 
   <td> Percentage of In-App messages that recipients dismissed.<br /> </td> 
  </tr> 
  <tr> 
   <td> Processed/sent<br /> </td> 
   <td> Total number of In-App messages sent from Adobe Campaign as part of the delivery sent process.<br /> </td> 
  </tr> 
  <tr> 
   <td> Unique impressions<br /> </td> 
   <td> Number of impressions by a unique recipient.<br /> </td> 
  </tr> 
  <tr> 
   <td> Unique In-App clicks<br /> </td> 
   <td> Number of times recipients clicked on Button 1 or Button 2.<br /> </td> 
  </tr> 
  <tr> 
   <td> Unique In-App dismissals<br /> </td> 
   <td> Number of time recipients dismissed an In-App message.<br /> </td> 
  </tr> 
 </tbody> 
</table>

## Segments {#segments}

>[!NOTE]
>
>By default, the **[!UICONTROL Exclude proof]** segment is alredy selected to filter your reports but can be changed if needed.

The table below gives you the list of segments used in reports and their definitions.

<table> 
 <thead> 
  <tr> 
   <th> Segment<br /> </th> 
   <th> Definition<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Age: Boomers 1<br /> </td> 
   <td> Recipients born from 1946 to 1954.<br /> </td> 
  </tr> 
  <tr> 
   <td> Age: Boomers 2<br /> </td> 
   <td> Recipients born from 1955 to 1965.<br /> </td> 
  </tr> 
  <tr> 
   <td> Age: From 18 to 25<br /> </td> 
   <td> Recipients from 18 to 25 years old.<br /> </td> 
  </tr> 
  <tr> 
   <td> Age: From 26 to 30<br /> </td> 
   <td> Recipients from 26 to 30 years old.<br /> </td> 
  </tr> 
  <tr> 
   <td> Age: From 31 to 40<br /> </td> 
   <td> Recipients from 31 to 40 years old.<br /> </td> 
  </tr> 
  <tr> 
   <td> Age: From 41 to 50<br /> </td> 
   <td> Recipients from 41 to 50 years old.<br /> </td> 
  </tr> 
  <tr> 
   <td> Age: Generation X<br /> </td> 
   <td> Recipients born from 1966 to 1976.<br /> </td> 
  </tr> 
  <tr> 
   <td> Age: Generation Y (Millennials)<br /> </td> 
   <td> Recipients born from 1977 to 1994.<br /> </td> 
  </tr> 
  <tr> 
   <td> Age: Generation Z<br /> </td> 
   <td> Recipients born from 1995 to today.<br /> </td> 
  </tr> 
  <tr> 
   <td> Age: Greater than 50<br /> </td> 
   <td> Recipients whose age is greater than 50.<br /> </td> 
  </tr> 
  <tr> 
   <td> Age: Less than 25<br /> </td> 
   <td> Recipients whose age is less than 25.<br /> </td> 
  </tr> 
  <tr> 
   <td> Age: Less than 30<br /> </td> 
   <td> Recipients whose age is less than 30.<br /> </td> 
  </tr> 
  <tr> 
   <td> Age: Less than 40<br /> </td> 
   <td> Recipients whose age is less than 40.<br /> </td> 
  </tr> 
  <tr> 
   <td> Age: Less than 50<br /> </td> 
   <td> Recipients whose age is less than 50.<br /> </td> 
  </tr> 
  <tr> 
   <td> Age: Silent Generation<br /> </td> 
   <td> Recipients born in 1945 or before.<br /> </td> 
  </tr> 
  <tr> 
   <td> All visits<br /> </td> 
   <td> Every recipient<br /> </td> 
  </tr> 
    <tr> 
   <td> Exclude proof<br /> </td> 
   <td> Exclude proofs from your reports (starting Campaign 19.4 release only)<br /> </td> 
  </tr> 
 </tbody> 
</table>

