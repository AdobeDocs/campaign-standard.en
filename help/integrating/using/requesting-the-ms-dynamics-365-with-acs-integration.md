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

Please note that this integration uses a third-party provider, Unifi.  In connection with your requests for support assistance, Adobe may be required to share your Adobe Campaign instance information with Unifi.

Please follow the flowchart and flowchart details below to request and configure the integration.

![](assets/provisioning-wf.png)

Flowchart Details (maps to steps above):

1. You must already have Campaign Standard and Microsoft Dynamics 365 provisioned, with admin access to start implementing this integration.

1. Read this article, check notices and configuration steps.

1. Send an account request to adobe-support@unifisoftware.com; Unifi will require the following information when you request an account:
    * User First Name
    * User Last Name
    * User Email
    * Company Name
    * Region (North America, EMEA or APAC)
    * Usage Type:  Customer Type (customer users that will be using their production data in this integration), or Partner Type (partner consultants that are testing out the integration to get a better understanding so that they can help their Campaign customers) or Internal Type (Adobe internal users that are testing out the integration to get a better understanding of the solution)
    * Campaign Standard data status (starting with clean database or bringing existing data to integration)
    * Campaign Tenant ID (see Configure Campaign integration section step 3 to get your Tenant ID)
    * Campaign Instance URL

    Unifi expected response time: 1 hour during regular U.S. business hours (9am to 5pm Pacific Time, Mon - Fri, excluding holidays).

1. Complete post-provisoning steps for Microsoft Dynamics 365 and for Campaign Standard. 
    Additionally, submit a ticket to Adobe Customer Care (either directly or through your Adobe contact) to have the single-sign-on feature flag enabled in your Campaign instance. Partners should reach out to their Adobe partner sandbox rep, instead contacting Adobe Customer Care, to enable the feature flag.
    If you have existing data in Campaign that you plan to incorporate into the integration, then follow the guidance in "Existing Campaign Data" and consult closely with your Adobe technical contact before proceeding.

1. Complete initial onboarding steps in Unifi by navigating to Unifi, clicking through onboarding screens, filling in Dynamics 365 and Campaign Standard account credentials, and notifying Unifi when completed.

1. Unifi will ask the customer for their desired opt-out configuration and opt-out attribute mapping.

1. The customer will indicate the selected opt-out configuration and opt-out attribute mapping.
Unifi expected response time: 1 business day (Mon - Fri, excluding holidays)

1. Configuring Unifi involves reviewing OOTB mappings, filters, jobs, etc. and making modifications, if necessary.  See the Unifi User Guide for details.
This step involves setting the run frequency of the Unifi schedules
* Set the run frequency of the schedules in the schedules screen in Unifi; however, for “ingress” and "egress" schedules, run these manually once before setting the schedule frequency
* The following schedule frequencies are recommended: Ingress (15 minutes), Egress (15 minutes), Deletes (Once a day), Opt-Outs (Once a day)

**It is recommended that you work with Unifi and/or Adobe consulting (contact your Adobe account team) when configuring Unifi.**

To enable the integration between Adobe Campaign Standard and Microsoft Dynamics 365, customers must create a user account with Unifi, a third party provider, as described in this document.   As an end user of the Unifi system, for any inquiries related to data requests initiated by customer within the Unifi system, customer should contact Unifi.

## Configuring this integration

Three systems need to be provisioned and configured for this integration: Adobe Campaign Standard, Microsoft Dynamics 365 for Sales and Unifi. Configuration articles are linked below.

>[!CAUTION]
>
>For each system, these steps need to be performed by an administrator.
>
>Steps in the articles below will guide you through creating integrations/registrations that involve assigning permissions and/or admin access.  It is your responsibility to ensure these steps comply with your company policies before performing, and to perform them carefully.

In ADOBE CAMPAIGN, you need to set up API access and configure a new integration for Unifi. To achieve this, refer to [this article](../../integrating/using/configure-adobe-io-for-ms-dynamic.md).

In MICROSOFT DYNAMICS 365, you need to create a new app registration and enable an application user to use the integration.  To configure Microsoft Dynamics 365 for this integration, refer to [this article](../../integrating/using/configure-microsoft-dynamics-365-for-campaign-integration.md).

In UNIFI, you need to setup integration and configure mapping or add custom attributes. To configure Unifi for this integration, refer to [this article](../../integrating/using/configure-unifi-for-microsoft-dynamics-365-integration.md).

## Requesting support 

If you run into issues, please reach out to Unifi customer support: [support@unifisoftware.atlassian.net](mailto:support@unifisoftware.atlassian.net). 

Unifi expected response time: 4 hours during regular U.S. business hours (9am to 5pm Pacific Time, Mon - Fri, excluding holidays).

>[!CAUTION]
>
>In connection with your request for support assistance, Adobe may be required to share your Adobe Campaign instance information with Unifi.