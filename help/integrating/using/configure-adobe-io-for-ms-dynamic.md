---
title: Configure Adobe IO for Microsoft Dynamics 365 integration
description: Learn how to configure Adobe IO for Microsoft Dynamics 365 integration.
page-status-flag: never-activated
uuid: effa1028-66b2-4bef-b5e4-7319dbb23d5d
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-ms-dynamics
discoiquuid: eb3639f5-7246-46c4-8ddb-da9413b40c32

internal: n
snippet: y
---

# Configure Adobe IO for Microsoft Dynamics 365 integration

Activate your CRM data on cross-channel communication: learn steps required during pre-integration setup to create a new Adobe IO project and configure it for the Microsoft Dynamics 365 integration.

## Overview

Adobe Campaign Standard - Microsoft Dynamics 365 integration is described in [this page](../../integrating/using/working-with-campaign-standard-and-microsoft-dynamics-365.md).

Before performing the pre-integration setup in this article, it is assumed that you have already been provisioned and have admin access to your organization’s Campaign Standard instance.  If this has not happened, then you will need to get in contact with Adobe Customer Care to complete Campaign provisioning.

>[!CAUTION]
>
>Steps described below need to be performed by an administrator.

## Configuration

You will need to create a new Adobe IO project and configure it for the integration. 

### Create a new project

To achieve this, follow the procedure below:

1. Navigate to [Adobe IO Console](https://console.adobe.io/home#) and select your Adobe IMS Organization ID from the drop-down menu at the top right of the screen.

1. Then click on **[!UICONTROL Create new project]** under **[!UICONTROL Quick Start]**.

![](assets/adobeIO1.png)

1. Under **[!UICONTROL Get started with your new project]**, click on **[!UICONTROL Add API]**.

![](assets/adobeIO2.png)

1. Select the Adobe Campaign API (you may need to scroll towards the bottom) and click on "Next".

![](assets/adobeIO3.png)

1. On the next screen you will have the option to upload your own public key or let Adobe IO generate the key pair for you. These instructions will follow the latter option. If you decide to let Adobe IO generate the key pair, click on option 1; then click on "Generate keypair" button.

![](assets/adobeIO4.png)

1. On the next screen you will be prompted to name and select the download location of the key pair zip file.

Once downloaded, you can unzip the file to reveal the public and private keys. Adobe IO has already applied the public key to your Adobe IO project. You will need to retain your private key for later; the private key will be used during the pre-integration setup of the integration tool.

1. Click on "Next" to continue

![](assets/adobeIO5.png)

1. On the next screen you will select product profiles to associate with this project.

1. Select the product profile that contains in the title: The tenant ID of your Campaign instance - [!UICONTROL Administrators] - Example: Campaign Standard - your-campaign-tenantID - Administrators

1. Click on [!UICONTROL Save configured API].

![](assets/adobeIO6.png)

1. On the next screen you will see the details of your new Adobe IO project.

1. Click on "Add to Project" at the top left of the screen and select "API" from the drop down.

![](assets/adobeIO7.png)

1. On the next screen you will need to select the I/O Events API, then click "Next".

1. On the next screen click "Save configured API".  You will be brought back to the project details screen.

1. Now click on "Add to Project" at the top left of the screen and select "API" from the drop down, as you did previously.

1. On the next screen you will need to select the I/O Management API and click "Next".

1. On the next screen click "Save configured API".

Pre-integration setup in Campaign is now complete.  Proceed to complete [pre-integration setup for Microsoft Dynamics 365](../../integrating/using/configure-microsoft-dynamics-365-for-campaign-integration.md).

**Related Topics** 

* [Adobe IO - Service Account Integration](https://www.adobe.io/authentication/auth-methods.html#!AdobeDocs/adobeio-auth/master/AuthenticationOverview/ServiceAccountIntegration.md)
* [Campaign Standard - API Access Setup](https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#setting-up-api-access)
* [Campaign Standard - Dynamics 365 integration](../../integrating/using/configure-microsoft-dynamics-365-for-campaign-integration.md)