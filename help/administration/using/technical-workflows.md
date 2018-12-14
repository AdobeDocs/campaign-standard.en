---
title: Technical workflows
seo-title: Technical workflows
description: Technical workflows
seo-description: Technical workflows are out-of-the-box workflows designed to handle background technical processes in Adobe Campaign, ensuring correct behaviour of the platform.
page-status-flag: never-activated
uuid: 603e1001-6e89-4158-bef6-33f107a11a21
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: application-settings
discoiquuid: de3c1615-e077-4843-bae1-bc3f66693876
isreadyforlocalization: true
index: y
internal: n
snippet: y
---

# Technical workflows{#technical-workflows}

Technical workflows

Technical workflows are delivered out-of-the-box with Adobe Campaign. Technical workflows are operations or jobs scheduled to be executed on a regular basis on the server.

They allow you to carry out maintenance operations on the database, leverage the tracking information in the deliveries, and update the provisional jobs on the deliveries.

Functional administrators can access technical workflows under the **Administration > Application settings > Workflows** menu.

>[!NOTE]
>
>As a functional administrator, you can restart or pause technical workflows, and modify their properties and structure.

![](assets/technical_workflows.png)

## List of technical workflows {#list-of-technical-workflows}

Technical workflows are used to handle self-triggered background and technical processes in Adobe Campaign.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Label</strong><br /> </td> 
   <td> <strong>ID</strong><br /> </td> 
   <td> <strong>Description</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>A/B Testing</strong><br /> </td> 
   <td> <strong>abTesting</strong><br /> </td> 
   <td> This workflow analyzes the tracking logs of each variant. At the end of the A/B testing period, it automatically calculates the winning variant. By default, it is started every day.<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Billing</strong><br /> </td> 
   <td> <strong>billing</strong><br /> </td> 
   <td> This workflow sends the system activity report to the 'billing' user by email. By default, it is automatically started every day at 1am.<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Database cleanup</strong><br /> </td> 
   <td> <strong>cleanup</strong><br /> </td> 
   <td> This workflow is the database maintenance workflow: it runs different statistics and processes, and deletes obsolete data from the database according to the configuration that has been defined. By default, it is automatically started every day 4am.<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Forecasting</strong><br /> </td> 
   <td> <strong>forecasting</strong><br /> </td> 
   <td> This workflow executes the analysis of the deliveries stored in the provisional forecasting (creation of the provisional logs). By default, it is started every day at 1am. <br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Import a shared audience</strong><br /> </td> 
   <td> <strong>importSharedAudience</strong><br /> </td> 
   <td> This workflow synchronizes the Adobe Experience Cloud audience data imported in Adobe Campaign. By default, it is started every hour.<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Instant Report Sharing</strong><br /> </td> 
   <td> <strong>reportSendingNow</strong><br /> </td> 
   <td> This workflow is started as soon as a report is scheduled to be sent. It converts your report into a pdf file then sends it in an email to the targeted recipients.<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>KPIs reconciliation with Adobe Analytics</strong><br /> </td> 
   <td> <strong>kpiReconciliation</strong><br /> </td> 
   <td> This workflow fetches the KPIs from Reporting service once a day and reconciles them with the data from Adobe Analytics. It then pushes the difference if needed. By default, it is started every day at 4.20am.<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Managing NMAC opt-outs</strong><br /> </td> 
   <td> <strong>mobileAppOptOutMgt</strong><br /> </td> 
   <td> This workflow updates unsubscriptions to notifications on mobile devices. By default, it is started every 6 hours between 1am and midnight.<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Message Center local archiving</strong><br /> </td> 
   <td> <strong>mcSynch_local</strong><br /> </td> 
   <td> This workflow archives real-time events into a historical table. By default, it is started every hour.<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Reporting aggregates</strong><br /> </td> 
   <td> <strong>reportingAggregates</strong><br /> </td> 
   <td> This workflow updates the aggregates used in the reports. By default, it is automatically started at 2am.<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Share KPIs with Adobe Analytics</strong><br /> </td> 
   <td> <strong>kpiSharing</strong><br /> </td> 
   <td> This workflow pushes KPI data every 15 minutes from Adobe Campaign Standard to Adobe Analytics.<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Update delivery execution</strong><br /> </td> 
   <td> <strong>updateDeliveryExecInfo</strong><br /> </td> 
   <td> This workflow updates the delivery's tracking. By default, it is started every 10 minutes.<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Update delivery indicators</strong><br /> </td> 
   <td> <strong>updateDeliveryIndicators</strong><br /> </td> 
   <td> This workflow updates the delivery's KPIs (Key Performance Indicator). By default, it is started every hour.<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Update event status</strong><br /> </td> 
   <td> <strong>updateEventsStatus</strong><br /> </td> 
   <td> This workflow allows you to attribute a status to an event. The following event statuses are available:<br /> <strong>Pending</strong>: The event is in a queue. No message template has been assigned to it yet.<br /> <strong>Pending delivery</strong>: The event is in the queue, a message template has been assigned to it and it is being processed by the delivery.<br /> <strong>Sent</strong>: This status is copied from the delivery logs. It means that the delivery was sent.<br /> <strong>Ignored by the delivery</strong>: This status is copied from the delivery logs. It means that the delivery was ignored.<br /> <strong>Delivery failed</strong>: This status is copied from the delivery logs. It means that the delivery failed.<br /> <strong>Event not taken into account</strong>: The event could not be linked to a message template. The event will not be processed.<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Update for deliverability</strong><br /> </td> 
   <td> <strong>deliverabilityUpdate</strong><br /> </td> 
   <td> This workflow allows you to create the list of bounce rule qualification rules, as well as the list of domains and MX in the platform. This workflow only functions if the HTTPS is open. By default, it is automatically started at 2am.<br /> </td> 
  </tr> 
 </tbody> 
</table>

