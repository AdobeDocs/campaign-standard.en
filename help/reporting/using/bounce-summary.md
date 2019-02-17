---
title: Bounce summary
seo-title: Bounce summary
description: Bounce summary
seo-description: With the Bounce summary out-of-the-box report, learn about the status of your sent campaigns and errors they may have encountered.
uuid: 0c222879-a2d7-4daa-b8da-50ab69af7c14
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: reporting
content-type: reference
topic-tags: list-of-reports
discoiquuid: b0aff9c2-fdc8-48b0-b0c5-604f1f35d838
index: y
internal: n
snippet: y
---

# Bounce summary{#bounce-summary}

Bounce summary

This report details the overall hard and soft errors encountered during deliveries as well as the automatic processing of bounces.

![](assets/campaign_reports_bounces.png)

Each table is represented by summary numbers and charts. You can change how the details are shown in their respective visualization settings.

**Flop 5 repartition** lists the five deliveries with the highest number of quarantines:

The **Bounce reasons** table contains the available data for the types of errors that caused bounces for each delivery:

* **[!UICONTROL User unknown]** : The type of error generated when a delivery is sent to an invalid email address.
* **[!UICONTROL Invalid domain]** : The type of error generated when a delivery is sent to an email address whose domain is wrong or no longer exists.
* **[!UICONTROL Unreachable]** : The type of error encountered in the message delivery string. For example, SMTP relay incident, domain temporarily unreachable, etc. 
* **[!UICONTROL Account disabled]** : The type of error generated when a delivery is sent to an email address that no longer exists.
* **[!UICONTROL Mailbox full]** : The type of error generated when the recipient's inbox is full. There are five attempts to deliver the message before this error is generated.
* **[!UICONTROL Not connected]** : The type of error generated when the recipient's mobile phone is off or it is not connected to a network at the time the message is sent.

  >[!NOTE]
  >
  >This type of error only concerns deliveries on mobile channels.

* **[!UICONTROL Refused]** : The type of error generated when an address is refused by the Internet service provider (ISP). For example, when a security rule has been applied by anti-Spam software.

The **Domain repartition** table displays the overall problems encountered during the deliveries according to the recipient domain.
