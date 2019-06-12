---
title: External accounts
seo-title: External accounts
description: External accounts
seo-description: Configure external accounts to set up connections with external systems such as SFTP servers.
page-status-flag: never-activated
uuid: 5d2e2e3d-5d1f-4466-97e5-842c50390146
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: application-settings
discoiquuid: d5c6a3d4-f767-46c1-a8c0-3b9dc52dcea8
internal: n
snippet: y
context-tags: extAccount,main;extAccount,overview
---

# External accounts{#external-accounts}

An external account is a configuration that allows you to configure and test the access to a server that is external to Adobe Campaign.

These external accounts can be used in Campaign workflows to access and manage data.

You can set up the following types of external accounts:

* SFTP. For more on this, refer to [this section](../../administration/using/external-accounts.md#sftp-external-account).
* Amazon Storage Service (S3). For more on this, refer to [this section](../../administration/using/external-accounts.md#amazon-s3-external-account).
* Adobe Experience Manager. For more on this, refer to [this section](../../administration/using/external-accounts.md#adobe-experience-manager-external-account).
* Adobe Analytics. For more on this, refer to [this section](../../integrating/using/configure-campaign-analytics-integration.md).
* Google reCAPTCHA. For more on this, refer to [this section](../../administration/using/external-accounts.md#google-recaptcha-external-account).

>[!NOTE]
>
>Other types of external accounts are used by Adobe during product provisioning process. From Campaign Standard 17.9 release, FTP external accounts can still be defined but are no longer usable in new workflow activities. If you already had a connection set up, it is still enabled.

External accounts can be configured by administrators under the **[!UICONTROL Administration > Application settings > External accounts]** menu.

## Creating an external account {#creating-an-external-account}

Adobe Campaign comes with a set of pre-defined external accounts. In order to set up connections with external systems such as FTP servers used for file transfers, you can create your own external accounts.

External accounts are used by technical processes such as technical workflows or campaign workflows. When setting up a file transfer in a workflow or a data exchange with any other application (Adobe Target, Experience Manager, etc.), you need to select an external account.

1. Click the **[!UICONTROL Create]** button.
1. Enter a label. The label and the ID will be used when selecting external accounts in workflows.
1. Select the type of account you want to create.
1. Configure the access to the account by specifying credentials, server address, port number, and or keys when relevant.

   The necessary information is usually provided by the provider of the server you are connecting to.

1. Save your account.

The external account is created and added to the account list. It is now available for your data/file transfers or routing configurations in workflow activities and delivery properties.

## SFTP external account {#sftp-external-account}

Different external account types require different information to be specified.

For an SFTP external account, provide the following details:

* Server address. For example, **ftp.domain.com**.
* Port number. For example, **22**.
* SFTP server credentials: account name and password used to connect to the server.

### Adobe hosted SFTP server recommendations {#adobe-hosted-sftp-server-recommendations}

When managing files and data for ETL purposes, these files are stored on a hosted SFTP server provided by Adobe. This SFTP is designed to be a temporary storage space on which you can control retention and deletion of files.

When not correctly used or monitored, this space can quickly fill the physical space available on the server and cause severe problems. It can result in data loss or corruption on your platform.

To avoid such problems, Adobe recommends to follow the best practices below:

* Keep the minimum data possible.
* Use key based authentication to avoid password expiry. Supported formats are **OpenSSH** and **SSH2** only. You will have to provide the public key to Adobe support team to have it uploaded on the Campaign server.
* Keep data for only as long as required. 15 days is the maximum time limit.
* Use workflows to properly delete the data (manage the retention from workflows consuming the data).
* Use batching in SFTP uploads as well as in workflows.
* Handle errors/exceptions.
* Occasionally, log-in to SFTP to directly check what is lying there.
* Remember that SFTP disk management is primarily your responsibility.

Also, note that the public IPs from which you are trying to initiate the SFTP connection must be whitelisted on the Campaign instance. Whitelisting of IP addresses can be requested via a [support ticket](https://support.neolane.net), along with providing the public key to use for authentication.

## Amazon S3 external account {#amazon-s3-external-account}

The Amazon S3 server field should be filled as follows:

```
<S3 bucket name>.s3.amazonaws.com/<s3 object path>
```

To store your file in S3 encrypted mode, check the **[!UICONTROL Keep files in S3 encrypted]** box.

![](assets/external_accounts_2.png)

The necessary information is usually provided by the provider of the server you are connecting to.

Specify the **[!UICONTROL AWS Region]** associated to your endpoint. You can check the supported regions and signature versions in the official [Amazon S3 documentation](https://docs.aws.amazon.com/general/latest/gr/rande.html#s3_region) .

### Amazon S3 account recommendations {#amazon-s3-account-recommendations}

To help you set up your Amazon S3 account, we advise you to follow these recommendations:

* Create strict bucket policy to restrict access to S3 buckets. Bucket policy can be configured while creating a bucket. For more information, refer to the [Amazon S3 documentation](http://docs.aws.amazon.com/AmazonS3/latest/dev//example-bucket-policies.html). 
* While creating an external account, enable the encryption to store sensitive data in the S3 bucket by checking the **[!UICONTROL Keep files in S3 encrypted]** box.
* Grant bucket permissions to specify who can access the object in a bucket. For more information on bucket permission, refer to the [Amazon S3 documentation](http://docs.aws.amazon.com/AmazonS3/latest/dev//access-control-overview.html)

## Adobe Experience Manager external account {#adobe-experience-manager-external-account}

Adobe Experience Manager external accounts are used when integrating Campaign with Experience Manager.

Process and requirements related to this integration are available in [this document](../../integrating/using/about-campaign-integrations.md).

As you are setting up this new external account, you need to provide the following details:

* Server: enter the URL of the Adobe Experience Manager server. For example, **http://aem.domain.com:4502**.
* AEM account credentials: use the account that will access the Adobe Experience Manager instance. It should be an account part of the campaign-remote group in Experience Manager.

## Google reCAPTCHA external account {#google-recaptcha-external-account}

>[!NOTE]
>
>Google reCAPTCHA configuration requires a Google account.

The Google reCAPTCHA mechanism allows you to protect your landing page from spam and abuse caused by bots. This is non-intrusive for your customers since it does not require any interaction from them and is based on interactions with your site. To register your site, refer to this [page](https://www.google.com/recaptcha/admin/create). You need to choose the V3 reCAPTCHA type.

To add the Google reCAPTCHA V3 to you landing page, you first need to configure it in your external account. For more information on how to add it to your landing page, refer to this [section](../../channels/using/designing-a-landing-page.md#setting-google-recaptcha).

For a Google reCAPTCHA V3 external account, provide the following details:

* A **[!UICONTROL Label]** and **[!UICONTROL ID]** of your external account
* **[!UICONTROL Type]** : Google reCAPTCHA
* Your **[!UICONTROL Site key]** and **[!UICONTROL Site secret]** 
* A **[!UICONTROL Threshold]** between 0 and 1

  The 0.0 **[!UICONTROL Threshold]** value means that it is likely a bot and 1.0 likely a good interaction. By default, you can use a threshold of 0.5.

![](assets/external_accounts_3.png)

