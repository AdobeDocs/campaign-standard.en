---
title: Request and configure the Microsoft Dynamics 365 integration
description: Learn how to Request and configure the Microsoft Dynamics 365 with Campaign Standard integration
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

# Request and configure the Microsoft Dynamics 365 integration

In order to provision this integration, you will need to follow the steps below.

Please follow the flowchart and flowchart details below to request and configure the integration.

![](assets/provisioning-wf.png)

Flowchart Details (maps to steps above):

* **Step 1** - It is assumed that you already have, or are in the process of procuring, a license for Microsoft Dynamics 365 for Sales and for Adobe Campaign Standard.

* **Step 2** - The standard integration offering is free* to all customers.

    * You will need to sign a zero-dollar contract to take advantage of the integration

    * Additional costs may apply depending on your requirements (see “Guardrails and Product Boundaries” section)

* **Step 3** - Complete pre-integration steps for Dynamics 365 and Campaign (see section below).

* **Steps 4-7** - The Adobe onboarding team will work closely with you through the onboarding process.

## Configuring this integration

Three systems need to be provisioned and configured for this integration: Adobe Campaign Standard, Microsoft Dynamics 365 for Sales and the integration tool. Configuration articles are linked below.

>[!CAUTION]
>
>For each system, these steps need to be performed by an administrator.
>
>Steps in the articles below will guide you through creating integrations/registrations that involve assigning permissions and/or admin access.  It is your responsibility to ensure these steps comply with your company policies before performing, and to perform them carefully.

In ADOBE CAMPAIGN, you need to set up API access and configure a new integration for the integration tool. To achieve this, refer to [this article](../../integrating/using/configure-adobe-io-for-ms-dynamic.md).

In MICROSOFT DYNAMICS 365, you need to create a new app registration and enable an application user to use the integration.  To configure Microsoft Dynamics 365 for this integration, refer to [this article](../../integrating/using/configure-microsoft-dynamics-365-for-campaign-integration.md).

In the integration tool, you need to set up the configuration for ingress, egress, and opt-out data flows. To configure the integration tool, refer to [this article](../../integrating/using/configure-integration-tool-for-microsoft-dynamics-365-integration.md).

>[!NOTE]
>
>Until the UI for the self-service tool is available later this year, the onboarding team will assist you in configuring the integration. 

## Requesting support 

Support tickets can be logged with Adobe Custom Care, as usual; Customer Care will bring in support personnel, as needed.

For any issues with integration data flows, make sure to include the report suite as part of the issue description as well as the following information:

* Process Owner: Engineering Architects

* ES Process ID: 

* Process Title: 

Issue Description: [Description of the issue]


Integration support is currently 24/5 (24-hours, Monday through Friday, excluding holidays), unless there is as a system-wide issue, which will be covered 24/7.
