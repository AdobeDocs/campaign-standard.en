---
title: Technical workflows
description: Technical workflows are out-of-the-box workflows designed to handle background technical processes in Adobe Campaign, ensuring correct behaviour of the platform.
page-status-flag: never-activated
uuid: 6e763dc1-e1d3-4d94-bc0b-ef5b1703d8e5
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: application-settings
discoiquuid: e9f147bd-6a5b-4b82-b9bb-311e38e22c62

internal: n
snippet: y
---

# Technical workflows{#technical-workflows}

Technical workflows are delivered out-of-the-box with Adobe Campaign. Technical workflows are operations or jobs scheduled to be executed on a regular basis on the server.

They allow you to carry out maintenance operations on the database, leverage the tracking information in the deliveries, and update the provisional jobs on the deliveries.

Functional administrators can access technical workflows under the **[!UICONTROL Administration > Application settings > Workflows]** menu.

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
   <td> <span class="uicontrol">A/B Testing</span> <br /> </td> 
   <td> <span class="uicontrol">abTesting</span> <br /> </td> 
   <td> This workflow analyzes the tracking logs of each variant. At the end of the A/B testing period, it automatically calculates the winning variant. By default, it is started every day.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">Billing</span> <br /> </td> 
   <td> <span class="uicontrol">billing</span> <br /> </td> 
   <td> This workflow sends the system activity report to the 'billing' user by email. By default, it is automatically started every day at 1am.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">Database cleanup</span> <br /> </td> 
   <td> <span class="uicontrol">cleanup</span> <br /> </td> 
   <td> This workflow is the database maintenance workflow: it runs different statistics and processes, and deletes obsolete data from the database according to the configuration that has been defined. By default, it is automatically started every day 4am.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">Forecasting</span> <br /> </td> 
   <td> <span class="uicontrol">forecasting</span> <br /> </td> 
   <td> This workflow executes the analysis of the deliveries stored in the provisional forecasting (creation of the provisional logs). By default, it is started every day at 1am. <br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">Import a shared audience</span> <br /> </td> 
   <td> <span class="uicontrol">importSharedAudience</span> <br /> </td> 
   <td> This workflow synchronizes the Adobe Experience Cloud audience data imported in Adobe Campaign. By default, it is started every hour.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">Instant Report Sharing</span> <br /> </td> 
   <td> <span class="uicontrol">reportSendingNow</span> <br /> </td> 
   <td> This workflow is started as soon as a report is scheduled to be sent. It converts your report into a pdf file then sends it in an email to the targeted recipients.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">KPIs reconciliation with Adobe Analytics</span> <br /> </td> 
   <td> <span class="uicontrol">kpiReconciliation</span> <br /> </td> 
   <td> This workflow fetches the KPIs from Reporting service once a day and reconciles them with the data from Adobe Analytics. It then pushes the difference if needed. By default, it is started every day at 4.20am.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">Managing NMAC opt-outs</span> <br /> </td> 
   <td> <span class="uicontrol">mobileAppOptOutMgt</span> <br /> </td> 
   <td> This workflow updates unsubscriptions to notifications on mobile devices. By default, it is started every 6 hours between 1am and midnight.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">Message Center local archiving</span> <br /> </td> 
   <td> <span class="uicontrol">mcSynch_local</span> <br /> </td> 
   <td> This workflow archives real-time events into a historical table. By default, it is started every hour.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">Reporting aggregates</span> <br /> </td> 
   <td> <span class="uicontrol">reportingAggregates</span> <br /> </td> 
   <td> This workflow updates the aggregates used in the reports. By default, it is automatically started at 2am.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">Share KPIs with Adobe Analytics</span> <br /> </td> 
   <td> <span class="uicontrol">kpiSharing</span> <br /> </td> 
   <td> This workflow pushes KPI data every 15 minutes from Adobe Campaign Standard to Adobe Analytics.<br /> </td> 
  </tr> 
    </tr> 
   <tr> 
   <td> <span class="uicontrol">Sync with Launch</span> <br /> </td> 
   <td> <span class="uicontrol">SyncWithLaunch</span> <br /> </td> 
   <td> This workflow synchronizes the Adobe Launch mobile properties imported in Adobe Campaign Standard. It is started every 15 minutes.<br /> </td> 
  </tr>
  <tr> 
   <td> <span class="uicontrol">Update delivery execution</span> <br /> </td> 
   <td> <span class="uicontrol">updateDeliveryExecInfo</span> <br /> </td> 
   <td> This workflow updates the delivery's tracking. By default, it is started every 10 minutes.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">Update delivery indicators</span> <br /> </td> 
   <td> <span class="uicontrol">updateDeliveryIndicators</span> <br /> </td> 
   <td> This workflow updates the delivery's KPIs (Key Performance Indicator). By default, it is started every hour.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">Update event status</span> <br /> </td> 
   <td> <span class="uicontrol">updateEventsStatus</span> <br /> </td> 
   <td> This workflow allows you to attribute a status to an event. The following event statuses are available:<br /> <strong>Pending</strong>: The event is in a queue. No message template has been assigned to it yet.<br /> <span class="uicontrol">Pending delivery</span> : The event is in the queue, a message template has been assigned to it and it is being processed by the delivery.<br /> <strong>Sent</strong>: This status is copied from the delivery logs. It means that the delivery was sent.<br /> <strong>Ignored by the delivery</strong>: This status is copied from the delivery logs. It means that the delivery was ignored.<br /> <strong>Delivery failed</strong>: This status is copied from the delivery logs. It means that the delivery failed.<br /> <span class="uicontrol">Event not taken into account</span> : The event could not be linked to a message template. The event will not be processed.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">Update for deliverability</span> <br /> </td> 
   <td> <span class="uicontrol">deliverabilityUpdate</span> <br /> </td> 
   <td> This workflow allows you to create the list of bounce rule qualification rules, as well as the list of domains and MX in the platform. This workflow only functions if the HTTPS is open. By default, it is automatically started at 2am.<br /> </td> 
  </tr> 
 </tbody> 
</table>

