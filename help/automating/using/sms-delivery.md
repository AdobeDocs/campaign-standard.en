---
title: SMS delivery
seo-title: SMS delivery
description: SMS delivery
seo-description: The SMS delivery activity allows you to configure sending a single send SMS or a recurring SMS in a workflow.
page-status-flag: never-activated
uuid: dd49f15c-f0c2-4f8f-9c8f-cb845e96c30a
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: channel-activities
discoiquuid: a613e359-30f4-4346-8c72-12bd7d61fd89
isreadyforlocalization: true
index: y
internal: n
snippet: y
---

# SMS delivery{#sms-delivery}

SMS delivery

## Description {#description}

![](assets/sms.png)  ![](assets/recurrentSMS.png)

The **SMS delivery** activity allows you to configure sending an SMS in a workflow. This can be a **single send** SMS and sent just once, or it can be a **recurring** SMS.

Single send SMS messages are standard SMS, sent once.

Recurring SMS messages allow you to send the same SMS multiple times to different targets over a defined period. You can aggregate the deliveries per period in order to get reports that correspond to your needs.

## Context of use {#context-of-use}

The **SMS delivery** activity is generally used to automate sending an SMS to a target calculated in the same workflow.

When linked to a scheduler, you can define recurring SMS messages.

SMS recipients are defined upstream of the activity in the same workflow, via targeting activities such as queries, intersections, etc.

The message preparation is triggered according to the workflow execution parameters. From the message dashboard, you can select whether to request or not a manual confirmation to send the message (required by default). You can start the workflow manually or place a scheduler activity in the workflow to automate execution.

## Configuration {#configuration}

1. Drag and drop an **SMS delivery** activity into your workflow.
1. Select the activity, then open it using the  ![](assets/edit_darkgrey-24px.png)

   button from the quick actions that appear.

   >[!NOTE]
   >
   >You can access the general properties and advanced options of the activity (and not of the delivery itself) via the  ![](assets/dlv_activity_params-24px.png) button in the workflow's action bar. This button is specific to the **SMS delivery** activity. The SMS properties can be accessed via the action bar in the SMS dashboard.

1. Select the SMS send mode:

    * **SMS**: the SMS is sent a single time. You can specify here whether or not you would like to add an outbound transition to the activity. The different transition types are detailed in step 7 of this procedure.
    * **Recurring SMS**: the SMS is sent several times, according to the frequency defined in a **Scheduler** activity. Select the aggregation period of the sends. This allows you to regroup all the sends that occur during the defined period into one single view that is also called **Recurring execution** and can be accessed from the application's marketing activity list.

      For example, for a recurring birthday SMS, that is sent daily, you can choose to aggregate the sends per month. This allows you to receive reports on your delivery on a monthly basis although the SMS is sent every day.

1. Select an SMS type. The SMS types come from SMS templates defined in the **Resources** &gt; **Templates** &gt; **Delivery templates** menu.
1. Enter the general properties of the SMS. You can also attach it to an existing campaign. The label of the workflow's delivery activity is updated with the SMS label.
1. Define the SMS content. Refer to the section concerning [Creating an SMS message](../../channels/using/creating-an-sms-message.md).
1. By default, the **SMS delivery** activity does not include any outbound transitions. If you would like to add an outbound transition to your **SMS delivery** activity, go to the **General** tab of the advanced activity options (  ![](assets/dlv_activity_params-24px.png)

   button in the activity's quick actions) then check one of the following options:

    * **Add outbound transition without the population**: this lets you generate an outbound transition that contains the exact same population as the inbound transition.
    * **Add outbound transition with the population**: this lets you generate an outbound transition containing the population to whom the SMS was sent. The members of the target excluded during the delivery preparation (quarantine, invalid number, etc.) are excluded from this transition.

1. Confirm the configuration of your activity and save your workflow.

When you reopen the activity, you are taken directly to the SMS dashboard. Only its content can be edited.

By default, starting a delivery workflow only triggers the message preparation. The sending of messages created from a workflow still needs to be confirmed after the workflow has been started. But from the message dashboard, and only if the message was created from a workflow, you can disable the **Request confirmation before sending messages** option. By unchecking this option, messages are sent without further notice once the preparation is done.

## Remarks {#remarks}

The deliveries created within a workflow can be accessed in the application's marketing activity list. You can view the workflow's execution status using the dashboard. Links in the SMS summary pane allow you to directly access linked elements (workflow, campaign, parent delivery in case of a recurring SMS).

The executions of recurring deliveries are masked by default, though. To view them, check the **Show recurring executions** option in the marketing activities' search panel.

In the parent deliveries, which can be accessed from the marketing activity list or directly via the associated recurring executions, you can view the total number of sends that have been processed (according to the aggregation period specified when the **SMS delivery** activity was configured). To do this, open the detail view of the parent delivery's **Deployment** block by selecting  ![](assets/wkf_dlv_detail_button.png)

.

## Example {#example}

![](assets/wkf_SMS_example_1.png)

This example is a birthday workflow. Every day an SMS is sent to profiles whose birthday is on that day. To do this:

* The **Scheduler** allows you to start the workflow every day at 8am.

  ![](assets/wkf_delivery_example_2.png)

* The **Query** activity allows you to calculate the profiles who have provided a mobile phone number and whose birthday is on the current day, every time the workflow is executed. The birthday calculation is carried out using a predefined filter available in the palette in the query editing tool.

  ![](assets/wkf_delivery_example_3.png)

* The **SMS** is recurring. The sends are aggregated by month. So, all SMS messages sent in a month are aggregated into a single view. In one year, 365 deliveries are therefore executed but they are regrouped into 12 views (also called **recurring executions**) in the Adobe Campaign interface. History and report details are displayed every month and not for every send.

  ![](assets/wkf_sms_example_4.png)

