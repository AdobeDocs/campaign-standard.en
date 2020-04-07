---
title: Working with Campaign Standard and Microsoft Dynamics 365
description: Learn how to Work with Campaign Standard and Microsoft Dynamics 365
page-status-flag: never-activated
uuid: ed6c1b76-87f7-4d23-b5e2-0765297a905c
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-experience-manager
discoiquuid: 6c0c3c5b-b596-459e-87dd-a06bb7d633d2

internal: n
snippet: y
---

# Working with Campaign Standard and Microsoft Dynamics 365

Activate your CRM data on cross-channel communication: learn how to pass on contacts from Microsoft Dynamics 365 to Adobe Campaign, and share campaign performance data (sends, opens, clicks, and bounces) back from Adobe Campaign to Microsoft Dynamics 365.

>[!NOTE]
>
>The Microsoft Dynamics 365 / Adobe Campaign Standard integration supports the **Microsoft Dynamics 365 Sales app** only.

## Benefits and use cases

### Principles

The Adobe Campaign and Microsoft Dynamics 365 integration enables synchronization of all available Contact data in the CRM system, making all relevant Contact data available for campaign activities.

Conversely, as profiles within Adobe Campaign interact with messages, those data (e.g.: sends, opens, clicks, and bounces) automatically flow into Microsoft Dynamics 365 to keep Contact records complete with marketing activity as well.  

The latest release of the integration also adds support for custom entities, enabling custom entities in Dynamics 365 to be synchronized to corresponding custom entities in Campaign.

This integration is designed to support three main use cases: 

1. Synchronizing Contacts from Dynamics 365 to Campaign so they can be targeted in marketing campaigns
1. Sending email marketing events (sends, opens, clicks, bounces) from Campaign to Dynamics 365 to display to the sales repository in the Dynamics 365 interface
1. Synchronizing custom entities from Dynamics 365 to Campaign so they can be used for segmentation and personalization

Watch Dynamics 365-Campaign Standard integration feature video [here](https://helpx.adobe.com/campaign/kt/acs/using/acs-ms-dynamics-crm-connector-tutorial.html).

### Key benefits

* Consistent messaging between sales & marketing

The Adobe Campaign and Microsoft Dynamics 365 integration gives both systems access to customer insight and email marketing history allowing all messages to the customer to share the same consistent messaging.

* Holistic view of all prospect and customer data

By integrating Adobe Campaign with Dynamics 365, it is possible to share and access email marketing history on each Contact from within the CRM system.

* Activate Dynamics 365 data on any channel

With contact data synchronized to Adobe Campaign, communications can be sent on any online or offline channel with Campaign including mobile push, in-app, email, or direct mail. Regardless of each Contacts’ preferred channel, Campaign has you covered.

>[!CAUTION]
>
>For Contacts synchronization, this integration considers Dynamics 365 as the source of truth.  Any changes to synchronized contact attributes should be done in Dynamics 365, not in Campaign.  If changes are made in Campaign, they can eventually get overwritten during synchronization.
