---
title: Scheduler
seo-title: Scheduler
description: Scheduler
seo-description: The Scheduler activity allows you to schedule when a workflow or an activity is started.
uuid: ea1c25c7-4144-4ca4-b6ba-1db60a4a2897
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/automating/using/scheduler
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-25T09 29 37.380-0400
cq-lastreplicated: 2018-07-23T05 57 15.400-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: execution-activities
cq-template: /apps/help/templates/article-3
discoiquuid: 4521f353-d72b-4dcf-83fe-ec1fe833295c
firstPublishExternalDate: 2018-07-23T05:57:15.363-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 24.895-0400
jcr-createdby: admin
jcr-description: Scheduler
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T05:57:15.363-0400
lochandoffdate: 2018-07-25T09 29 37.380-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Scheduler
publishexternaldate: 2018-07-23T05 57 15.363-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/automating/using/scheduler.html
sha1: ebdf6fee661bae9a916cd27c7d18ee17f515cf9e
topicBrowsingSortDate: 2018-07-23T05:57:15.363-0400
index: y
internal: n
snippet: y
---

# Scheduler

Scheduler

## <p>Description</p>

![](assets/scheduler.png)

The **Scheduler** activity allows you to schedule when a workflow or an activity is started.

## <p>Context of use</p>

The **Scheduler** activity should be considered as a scheduled start. The activity positioning rules within the chart are the same as for the **Start** activity. This activity must not have an inbound transition.

When building your workflow, only use one **Scheduler** activity per branch and remember to set a time zone. It will be set otherwise to run at the server time zone.

>[!CAUTION]
>
>The **Repetition frequency** of the activity cannot be less than 10 minutes. It means that a workflow cannot be automatically executed more than once every 10 minutes.

## <p>Configuration</p>

1. Drag and drop a **Scheduler** activity into your workflow.
1. Select the activity, then open it using the  ![](assets/edit_darkgrey-24px.png)

   button from the quick actions that appear.
1. Specify the **Execution frequency**:

    * **Once**: the workflow is executed a single time.
    * **Several times a day**: the workflow is regularly executed several times a day.
    * **Daily**: the workflow is executed at a specific time, once a day.
    * **Weekly**: the workflow is executed at a specified moment, once or several times a week.
    * **Monthly**: the workflow is executed at a specified moment, once or several times a month.
    * **Yearly**: the workflow is executed at a specified moment, once or several times a year.

1. Define the execution details according to the frequency selected. The detail fields may vary depending on the frequency used (time, repetition frequency, specified days, etc.).

   >[!NOTE]
   >
   >The **Repetition frequency** field allows you to space out the times when the workflow is triggered. For example, if you select a daily execution period and the repetition frequency is set at **2** (days), the workflow will be triggered every two days. It cannot be less than 10 minutes. If the repetition frequency is set at **0** (also the default value), this option is not taken into account and the workflow will run according to the execution frequency specified.

1. Specify when the execution will expire:

    * **Never**: the workflow will be executed, according to the frequency specified, without any limits to the time frame or number of iterations.
    * **After a certain number of iterations**: the workflow will be executed according to the frequency specified, up until the limit of **X** is reached. The **Number of iterations** will therefore need to be specified.
    * **On a specific date**: the workflow will be executed according to the frequency specified, up until a specific date. The execution deadline will therefore need to be specified.

1. In the **Execution options** tab, set up the time zone for your scheduler in the **Time zone** field. This allows you to start your workflow at a specific time zone, otherwise the workflow will run in server time zone by default.

   For more information on sending delivery depending on the recipient's time zone, refer to this [section](../../sending/using/sending-messages-at-the-recipient-s-time-zone.md) or this [example](../../automating/using/mobile-app-delivery.md#sending-a-recurring-push-notification-with-a-workflow) of a recurring workflow.

1. Confirm the configuration of your activity and save your workflow.

## <p>Example</p>

In the following example, the activity is configured so that it will start the workflow on a weekly basis, every other Monday at 7am, for an undetermined duration.

![](assets/wkf_scheduler_example.png)

