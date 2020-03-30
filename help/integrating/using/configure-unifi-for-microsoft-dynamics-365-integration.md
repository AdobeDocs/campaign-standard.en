---
title: Configure Unifi for Microsoft Dynamics 365 integration
description: Learn how to configure Unifi for Microsoft Dynamics 365 integration
page-status-flag: never-activated
uuid: effa1028-66b2-4bef-b5e4-7319dbb23d5d
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-analytics
discoiquuid: eb3639f5-7246-46c4-8ddb-da9413b40c32

internal: n
snippet: y
---


# Configure Unifi for Microsoft Dynamics 365 integration

Configure Unifi to setup and activate Microsoft Dynamics 365 - Adobe Campaign integration.

## Prerequisites

Before performing the post-provisioning steps in this article, it is assumed that you have already successfully completed the [post-provisioning steps for Campaign](../../integrating/using/configure-adobe-io-for-ms-dynamic.md) and [for Dynamics 365](../../integrating/using/configure-microsoft-dynamics-365-for-campaign-integration.md).  If this has not happened, then you will need to follow those steps to complete Campaign Standard and Dynamics 365 post-provisioning.

It is also assumed that you have contacted Unifi, have had a Unifi account created for you, and have been able to successfully log in.  If this has not happened, then follow the steps outlined in [this article](../../integrating/using/working-with-campaign-standard-and-microsoft-dynamics-365.md).

>[!CAUTION]
>
>It is strongly recommended that you work with Unifi and/or Adobe consulting (contact your Adobe CSM) when configuring Unifi.

## Configure Campaign integration

At your first connection, click **[!UICONTROL Adobe Campaign Standard]** to enter your Campaign credentials.

Most of these credentials will come from the integration you created in Adobe I/O Console during [Campaign Standard configuration steps](../../integrating/using/configure-adobe-io-for-ms-dynamic.md). 

>[!NOTE]
>
>To ensure security and privacy, sensitive credentials fields appear blank when revisiting these configuration screens.

1. For Adobe Authentication URL, enter `https://ims-na1.adobelogin.com/ims/exchange/jwt`

1. Enter your **[!UICONTROL Adobe IO Organization ID]** and your **[!UICONTROL Adobe IO Integration ID]**.

To get your Adobe IO Organization and Integration IDs, navigate to your Adobe I/O Console Integration Over screen and note the web URL. 

It should look something like this: `https://console.adobe.io/integrations/<Org ID>/<Int ID>/overview`, where Org ID and Int ID are numbers. 

1. Enter your **[!UICONTROL Tenant ID]**

To get your Tenant ID, follow the steps below:

 1. Navigate to the [Adobe Admin Console](https://adminconsole.adobe.com/) and select your IMS Org from the top right drop down menu.
 1. Select your Adobe Campaign Standard product then select your Campaign  Standard instance (if you have more than one).  This will bring up a list of product profiles.

    The product profile descriptions typically appear in one of the following formats, where `<tenantID>` is the tenant ID of your instance.

`Campaign Standard – https://<tenantID> - <ROLE>`

`Campaign Standard – <tenantID> - <ROLE>`

>[!NOTE]
>
>If you experience trouble identifying your Tenant ID, please contact you > Adobe technical contact or Adobe Customer Care.
>
>Partner sandbox instance tenant IDs typically follow the pattern `https://<tenantId>`, where `tenantId` is  `tbd.campaign-sandbox.adobe.com`.

1. Enter your **[!UICONTROL Campaign Instance ID]**.

To get your Instance ID, follow the steps below: 

    1. Enter `https://<acs-instance-url>/r/test` into a web browser, replacing `<acs-instance-url>` with the URL of your Campaign Standard instance.
    1. The response will contain `instance=`, followed by the instance ID.

1. Select the region of your Campaign instance.

1. You can leave **[!UICONTROL Base Directory]** blank.

1. Select the **[!UICONTROL Allow as Output Destination]** option.

Once parameters have been set, click **[!UICONTROL CONNECT]** and check connection is successful. 

If not, click **[!UICONTROL CLOSE]** and check parameters.

>[!NOTE]
>
>If you are unable to complete this step, contact [Unifi customer service](mailto:support@unifisoftware.atlassian.net).

## Configure Dynamics 365 integration

Click Microsoft Dynamics CRM to configure Dynamics 365 credentials. Most of these credentials will come from the integration you created in Micosoft Dynamics 365 during Microsoft Dynamics 365 configuration steps.

>[!NOTE]
>
>To ensure security and privacy, sensitive credentials fields appear blank when revisiting these configuration screens.

1. For **[!UICONTROL URL]**, enter the URL of your Dynamics 365 instance, taking care to insert “.api” before “.crm” (e.g., `https://mydynamicsinstance.api.crm.dynamics.com`)

1. For **[!UICONTROL clientid]**, you will use the application ID that was generated when you created the app registration as [configuring Dynamics 365](../../integrating/using/configure-microsoft-dynamics-365-for-campaign-integration.md).

1. For **[!UICONTROL clientsecret]**, you will use the client secret that was generated when you added a client secret to the app registration as [configuring Dynamics 365](../../integrating/using/configure-microsoft-dynamics-365-for-campaign-integration.md).

1. For **[!UICONTROL callbackurl]**, add `http://localhost:33333`.

1. For **[!UICONTROL refresh token]**, leave blank.

1. For **[!UICONTROLtenant ID]**, use the tenant ID that you got from portal.azure.com as [configuring Dynamics 365](../../integrating/using/configure-microsoft-dynamics-365-for-campaign-integration.md).

1. Lastly, check the box for **[!UICONTROL Allow as Output Destination]**.

Once parameters have been entered, click **[!UICONTROL CONNECT]** and check connection is successful. 

If not, click **[!UICONTROL CLOSE]** and check parameters.

>[!NOTE]
>
>If you are unable to complete this step, contact [Unifi customer service](mailto:support@unifisoftware.atlassian.net).

## Unifi setup completion

Once your credentials are set up, you need to notify Unifi as some additional steps need to be performed before you can finish integration setup.  Reach out to the Unifi contact information provided to you to indicate you have set up your credentials.  

You need to select an opt-out option, and notify Unifi when completed (indicating to Unifi which opt-out option is being selected).  An explanation of opt-out options can be found in the [Unifi User Guide](https://drive.google.com/drive/folders/16seHF45e6bFxHX15zWLqFLEXymCuA_wn). 

Once Unifi completes their work, they will notify you and provide further information to help you configure your Unifi instance, run data ingress once and then, once sucessful completion, you can enable schedules.

Following frequency is recommended for various use cases:

* Ingress: Every 15 minutes
* Egress: Every 15 minutes
* Deletes: Every day
* Opt-Outs: Every day

>[!NOTE]
>
>By default, SEND marketing events are filtered out of the egress job.  If you wish to see SEND marketing events in Dynamics 365, you need to modify the filter (step 5) of the egress job in Unifi.

There are two separate roles in Unifi, an owner user and a read-only analyst user. An owner user has the ability to modify jobs and schedules, while the read-only analyst does not.  There can be only one owner user for a given customer instance.  If the customer needs to change the individual assigned as the owner user, they can send an email to [adobe-support@unifisoftware.com](mailto: adobe-support@unifisoftware.com) with the requested change.

Unifi configuration, job details, setup and monitoring are presented in the videos below.

## Unifi Jobs

### Overview of the Unifi jobs

>[!VIDEO](https://video.tv.adobe.com/v/27392)

This video explains the different Unifi jobs that required for the Adobe Campaign Standard integration with Microsoft Dynamics 365 (02:10 min)

### Unifi Job Details: Ingress & Egress

>[!VIDEO](https://video.tv.adobe.com/v/27396)

This video explains the ingress and egress jobs in Unifi (04:27 min)

### Operationalization & Monitoring

>[!VIDEO](https://video.tv.adobe.com/v/27391)

This video explains the workflows and schedules (03:03 min)

More like this
* [Working with Adobe Campaign Standard - Microsoft Dynamics 365](../../integrating/using/working-with-campaign-standard-and-microsoft-dynamics-365.md)
* [Configure Microsoft Dynamics 365 for Campaign integration](../../integrating/using/configure-microsoft-dynamics-365-for-campaign-integration.md)
* [Configure Adobe IO for Microsoft Dynamics 365 - Campaign Standard integration](../../integrating/using/configure-adobe-io-for-ms-dynamic.md)
* [Microsoft Dynamics 365 integration feature page](https://helpx.adobe.com/campaign/kt/acs/using/acs-ms-dynamics-crm-connector-tutorial.html)