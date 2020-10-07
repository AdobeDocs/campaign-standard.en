---
title: Track and monitor messages
seo-title: Track and monitor messages
page-status-flag: never-activated
uuid: a540efc7-105d-4c7f-a2ee-ade4d22b3445
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: delivery
content-type: reference
topic-tags: deliveries-best-practices
discoiquuid: 0cbc4e92-482f-4dac-a1fb-b738e7127938
index: y
---

# Track and monitor {#track-and-monitor}

You clicked the Send button? Let's see what happens. Once the delivery is sent, Adobe Campaign enables you to keep track of the sent messages and discover how your recipients react to your delivery. This will help you improve future sending and optimize your next campaigns.

## Monitoring deliveries {#monitoring-deliveries}

To control your campaigns, you must ensure that the message has indeed been delivered to your recipients.

**Tips**

* You can control the status of the messages in the delivery logs.

* To keep track of delivery successes or failures, Adobe Campaign provides an email alerting system that sends notifications to inform users of important system activities.

* From the message dashboard, you can access several reports for this specific message.

For more this, see [Monitoring a delivery](../../sending/using/monitoring-a-delivery.md).

## Tracking {#tracking-deliveries}

To better know the behavior of your targeted profiles, you can track how they react to a delivery: reception, opening, clicks on links, unsubscriptions, etc. Refer to the **Tracking logs** tab of the delivery.

**Tip**: Message tracking is enabled by default. To configure URLs, select the Display URLs option in the lower section of the delivery wizard. For each URL of the message, you can choose whether to activate tracking.

For more on this, refer to the [Tracking messages](../../sending/using/tracking-messages.md) section and the [Tracking indicators](../../reporting/using/tracking-indicators.md) description. 

## Dynamic reports {#dyn-reports}

Dynamic reports allow you to create fully customizable and real-time reports to monitor your campaigns. Dimensions, metrics and visualizations let you measure the impact and success of your campaigns on recipients.

**Tip** - Built-in reports are available for you to monitor your campaigns but these reports can also be customized by drag and dropping any metrics or dimensions to your report.

For more on this, refer to the [Reporting guide](../../reporting/using/about-dynamic-reports.md).

## Hot clicks

The Hot clicks report presents the message content (HTML and/or text) with the percentage of clicks on each link. By displaying the percentage of clicks on each dynamic content, you can measure which content most appeals to the recipients.

For more on this, refer to the [Hot click report](../../reporting/using/hot-clicks.md).

## Delivery performance tips {#performance-tips}

* Do not keep deliveries in failed state on the instance, as this maintains temporary tables and impacts the performance.

* Remove deliveries which are no longer needed and inactive recipients from the database to maintain address quality.

* Do no try to schedule large deliveries together. Please note that it can take 5 to 10 minutes to spread the load uniformly over the system.

**Related topics:**

* [Receiving alerts when failures happen](../../sending/using/receiving-alerts-when-failures-happen.md)
* [Reports](../../reporting/using/about-dynamic-reports.md)
