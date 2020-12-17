---
title: Request and configure the Microsoft Dynamics 365 integration
description: Learn how to Request and configure the Microsoft Dynamics 365 with Campaign Standard integration
page-status-flag: never-activated
uuid: ed6c1b76-87f7-4d23-b5e2-0765297a905c
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-ms-dynamics
discoiquuid: 6c0c3c5b-b596-459e-87dd-a06bb7d633d2

---

# Request and configure the Microsoft Dynamics 365 integration

In order to provision this integration, you will need to follow the steps below.

Please follow the flowchart and flowchart details below to request and configure the integration.

![](assets/provisioning-wf.png)

Flowchart Details (maps to steps above):

* **Step 1** - It is assumed that you already have, or are in the process of procuring, a license for Microsoft Dynamics 365 for Sales and for Adobe Campaign Standard.

* **Step 2** - The standard integration offering is free to all customers; however, additional costs may apply depending on your requirements (see [Integration guardrails and boundaries](../../integrating/using/d365-acs-guardrails.md)). A new sales order (SO) will need to be signed in order to take advantage of the integration if it was not included in the original SO.

* **Step 3** - Complete pre-integration steps for Dynamics 365 and Campaign. See [Configure this integration](#configure-this-integration).

* **Step 4** - The Adobe onboarding team will provide you access to the integration application user interface (UI).

* **Step 5** - You will be able to configure your data mappings, replacements, filters, etc. and test your integration from within the integration application UI.

## Configure this integration {#configure-this-integration}

Three systems need to be provisioned and configured for this integration:

* Adobe Campaign Standard, 
* Microsoft Dynamics 365 for Sales, and 
* Adobe Campaign Standard integration with Dynamics 365 integration self-service application.

Configuration articles are linked below.

>[!CAUTION]
>
>For each system, these steps need to be performed by an administrator.
>
>Steps in the articles below will guide you through creating integrations/registrations that involve assigning permissions and/or admin access.  It is your responsibility to ensure these steps comply with your company policies before performing, and to perform them carefully.

In **Adobe Campaign Standard**, you need to set up API access and configure a new integration for the integration tool. To achieve this, refer to [this article](../../integrating/using/d365-acs-configure-adobe-io.md).

In **Microsoft Dynamics 365**, you need to create a new app registration and enable an application user to use the integration.  To configure Microsoft Dynamics 365 for this integration, refer to [this article](../../integrating/using/d365-acs-configure-d365.md).

To get access to the **Adobe Campaign Standard integration with Dynamics 365 Self-Service App**, you will need to follow the steps in [this article](../../integrating/using/d365-acs-self-service-app-control-access.md).

## Request support

Support tickets can be logged with Adobe Custom Care, as usual; Customer Care will bring in support personnel, as needed.

For any issues with integration data flows, make sure to include the report suite as part of the issue description as well as the following information:

* **Process Owner**: Engineering Architects

* **ES Process ID**: Provided during onboarding process

* **Process Title**: Dynamics 365 / Adobe Campaign Standard Integration

* **Issue Description**: Description of the issue

Integration support coverage is currently 24x5 (available Monday through Friday, excluding Adobe holidays and break periods).