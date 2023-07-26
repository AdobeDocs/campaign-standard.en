---
title: Configure Microsoft Dynamics 365 for Campaign integration
description: Learn how to configure Microsoft Dynamics 365 for Campaign integration.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-ms-dynamics

feature: Microsoft CRM Integration
role: Data Architect
level: Experienced
exl-id: 57e85f8e-65b4-44ea-98e6-0c555acf6dee
---
# Configure Microsoft Dynamics 365 for the integration with Adobe Campaign Standard

Learn how to configure Microsoft Dynamics 365 integration and activate your CRM data on cross-channel communication with Adobe Campaign Standard.

## Overview

The general description of the Adobe Campaign Standard integration with Microsoft Dynamics 365 is described in [this page](../../integrating/using/d365-acs-get-started.md).

Multiple applications will need to be configured to enable the integration, however, this article will focus on steps required within Dynamics 365.  

## Prerequisites

Before performing the pre-integration setup in this document, it is assumed that you have already provisioned and have admin access to your organization's Microsoft Dynamics 365 instance.  If this has not happened, then you will need to get in contact with Microsoft customer support to complete Dynamics 365 provisioning.

If you are configuring the integration for both staging and production environments, you will need to perform the steps below for both your staging and production Dynamics 365 instances. A few instructions below vary slightly depending if you are configuring a stage or production Dynamics 365 instance (e.g., for production instance, select "prod" for `<stage or prod>`)

## Setting up application and permissions

An OAuth access token allows the integration tool to authenticate with your Microsoft Dynamics 365 instance via web APIs in order to post Campaign Standard experience events to the timeline view of the Microsoft Dynamics 365 interface.

Main steps are outlined in the following video:

>[!VIDEO](https://video.tv.adobe.com/v/27637)

To generate the OAuth access token, follow the steps outlined below.

### Register a new application {#register-a-new-app}

1. Under your administrator login, login to [portal.azure.com](https://portal.azure.com){target="_blank"}.  

1. Click on **[!UICONTROL Azure Active Directory]** in the left side menu; then click **[!UICONTROL App registrations]** on the sub menu that appears. 

1. Click **[!UICONTROL New registration]** at the top of screen.

1. Fill out the app registration screen:

    * Name: adobe campaign `<stage or prod>` 
    * Supported account type: **[!UICONTROL Accounts in this organizational directory only]** (default value)

 For more information about creating a new application, refer to [this section](https://docs.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app){target="_blank"}.

>[!NOTE]
>
>Microsoft Azure Directory assigns a unique application (client) ID to your app. You will need this ID later on in configuring Dynamics 365, as well as when you perform the integration tool setup.

### Generate client secret {#generate-a-client-secret}

1. From the app overview screen, on the sub menu on the left, click **[!UICONTROL Certificates and Secrets > New client secret]**

1. Enter a description, set duration and click **[!UICONTROL OK]**.

Your client secret is now created. Retain the value temporarily for the completion of the pre-integration setup of the integration tool.

>[!CAUTION]
>
>Keep this value as you will need it to complete the integration tool pre-integration setup. It cannot be retrieved afterwards.


### Setup permissions

1. From this screen or the app overview screen, click on **[!UICONTROL API permissions]** in the sub menu on the left.  After clicking **[!UICONTROL Add a permission]**,  you need to select **[!UICONTROL Dynamics CRM]** in the menu.

1. Then check the box for **[!UICONTROL user_impersonation]**, and click the **[!UICONTROL Add permissions]** button.

For more information about permission set up, refer to [this section](https://docs.microsoft.com/en-us/azure/active-directory/develop/quickstart-configure-app-access-web-apis#add-permissions-to-access-web-apis){target="_blank"}.

### Create the app user

This new user is a generic user. It will be used by the application: any change to Microsoft Dynamics 365 using the API will be done by this user. To create it, follow the steps below:

1. Navigate to your Dynamics 365 instance and log in as Admin.

1. Click on the gear icon in the upper right corner and click on **[!UICONTROL Advanced Settings]**. In the top banner, click on the drop down next to **[!UICONTROL Settings]**, click on **[!UICONTROL Security > Users]**.

1. Click on the drop-down menu go to **[!UICONTROL Application Users]**. Click **[!UICONTROL New]**.

1. Ensure drop down next to user icon says **[!UICONTROL USER:APPLICATION USER]**.

    Fill out the screen for the new user.  Parameters suggestions:

    * **[!UICONTROL User Name]** (email): adobe_api_`<stage-or-prod>`@`<your-d365-hostname>`" (e.g., adobe_api_stage@some-company.crm.dynamics.com)
    * **[!UICONTROL Application ID]**: ID of the application you registered in Azure AD (this is required)
    * You can leave blank **[!UICONTROL Application ID URI]** and **[!UICONTROL Azure AD Object ID]**
    * **[!UICONTROL Full Name]**: Adobe API `<stage or prod>` 
    * **[!UICONTROL Email]**: same as **[!UICONTROL User Name]** (or admin's email if you wish)

    For more information about app user creation, refer to [this section](https://docs.microsoft.com/en-gb/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user){target="_blank"}.

1. Click on the user icon and upload an Adobe Campaign icon; this is the icon that will be displayed in the Timeline view when new Adobe events appear in Dynamics 365.

1. Open the user roles list by clicking **[!UICONTROL MANAGE ROLES]** in the top ribbon.

1. Scroll down and select **[!UICONTROL System administrator]** access for this user.

1. Click **[!UICONTROL OK]**.

### Get the tenant ID {#get-the-tenant-id}

Follow the instructions [in this page](https://docs.microsoft.com/en-us/onedrive/find-your-office-365-tenant-id) to find your tenant ID.  You'll need this ID during pre-integration setup in the integration tool.

## Install Campaign Standard for Microsoft Dynamics 365 {#install-appsource-app}

To integrate the Dynamics 365 App to your Campaign Standard environment, follow the steps below:

1. Browse to [Microsoft Business Apps](https://appsource.microsoft.com/en-us/marketplace/apps){target="_blank"} and search for_Adobe Campaign Standard_ in the search bar.
    Alternatively, you can navigate to this [link](https://appsource.microsoft.com/en-us/product/dynamics-365/adobe.adobe_campaign_d365?tab=Overview){target="_blank"}.
1. Follow the instructions to install the app for your Dynamics 365 instance.
1. Once installed, navigate to your Dynamics 365 instance and sign in as administrator.
1. Click on the gear icon in the upper right corner and click on **[!UICONTROL Advanced Settings]**. In the top banner, click on the drop down next to **[!UICONTROL Settings]**, click on **[!UICONTROL Processes]** under **[!UICONTROL Process Center]**.
1. Search for **[!UICONTROL Adobe Campaign Email Bounce]** task and click it.
1. On the **[!UICONTROL Administration]** tab, change the owner to the Adobe API application user created earlier by clicking **[!UICONTROL Actions]** from the top ribbon, then select **[!UICONTROL Assign to another User]** option, select **[!UICONTROL Adobe API application user]** from the dropdown to assign.
1. Reactivate the process.
1. Do the same for the **[!UICONTROL Adobe Campaign Email Click]** task. 

>[!NOTE]
>
>If at any time you wish to deactivate these processes, you can do so in this **[!UICONTROL Processes]** screen.

**Related topics** 

* [Configure Adobe Developer for Microsoft Dynamics 365 integration](../../integrating/using/d365-acs-configure-adobe-io.md) is the next step in setting up the integration
* [Get started with the self-service integration app](../../integrating/using/d365-acs-self-service-app-quick-start-guide.md) contains the full list of steps to get the integration up-and-running.
