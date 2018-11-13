---
title: External accounts
seo-title: External accounts
description: External accounts
seo-description: Configure external accounts to set up connections with external systems such as SFTP servers.
uuid: 412f0d02-265f-453d-8d03-afc2bde52cc9
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/administration/using/external-accounts
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-10T07 26 24.990-0400
cq-lastreplicated: 2018-09-07T15 02 20.601-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: application-settings
cq-template: /apps/help/templates/article-3
discoiquuid: 4c55d97d-a4cb-4daa-adb4-473eac345758
firstPublishExternalDate: 2018-09-07T15:02:17.551-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-02-16T08 04 23.760-0500
jcr-createdby: admin
jcr-description: External accounts
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T15:02:17.551-0400
lochandoffdate: 2018-09-10T07 26 24.989-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: External accounts
publishexternaldate: 2018-09-07T15 02 17.551-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/administration/using/external-accounts.html
sha1: 8b3b1458c03ac8b8e04a339b23642bf2c2f17fa8
topicBrowsingSortDate: 2018-09-07T15:02:17.551-0400
index: y
internal: n
snippet: y
---

# External accounts{#external-accounts}

External accounts

An external account is a configuration that allows you to configure and test the access to a server that is external to Adobe Campaign.

The following external account types are available: SFTP, HTTP and Amazon Storage Service (S3).

>[!NOTE]
>
>More types of external accounts are available. They are used during provisioning operations performed by Adobe. From build 17.9, FTP external accounts can still be defined but are no longer usable in new workflow activities. If you already had a connection set up, it is still enabled.

External accounts can be configured by administrators under the **Administration > Application settings > External accounts** menu.

## Creating an external account {#creating-an-external-account}

Adobe Campaign comes with a set of pre-defined external accounts. In order to set up connections with external systems such as FTP servers used for file transfers, you can create your own external accounts.

External accounts are used by technical processes such as technical workflows or campaign workflows. When setting up a file transfer in a workflow or a data exchange with any other application (Adobe Target, Experience Manager, etc.), you need to select an external account.

1. Click the **Create** button.
1. Enter a label. The label and the ID will be used when selecting external accounts in workflows.
1. Select the type of account you want to create.
1. Configure the access to the account by specifying credentials, server address, port number, and or keys when relevant.

   The necessary information is usually provided by the provider of the server you are connecting to.

1. Save your account.

The external account is created and added to the account list. It is now available for your data/file transfers or routing configurations in workflow activities and delivery properties.

## How to define an SFTP external account {#how-to-define-an-sftp-external-account}

Different external account types require different information to be specified.

For an SFTP external account, provide the following details:

* Server address. For example, **ftp.domain.com**.
* Port number. For example, **22**.
* SFTP server credentials: account name and password used to connect to the server.

### Best practices for Adobe hosted SFTP servers {#best-practices-for-adobe-hosted-sftp-servers}

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

## How to define an Amazon S3 external account {#how-to-define-an-amazon-s-external-account}

The S3 server field should be filled as follows:

```
<S3 bucket name>.s3.amazonaws.com/<s3 object path>
```

To store your file in S3 encrypted mode, check the **Keep files in S3 encrypted** box.

![](assets/external_accounts_2.png)

The necessary information is usually provided by the provider of the server you are connecting to.

Specify the **AWS Region** associated to your endpoint. You can check the supported regions and signature versions in the official [Amazon S3 documentation](https://docs.aws.amazon.com/general/latest/gr/rande.html#s3_region) .

### S3 account recommendations {#s-account-recommendations}

To help you set up your S3 account, we advise you to follow these recommendations:

* Create strict bucket policy to restrict access to S3 buckets. Bucket policy can be configured while creating a bucket. For more information, refer to the [Amazon S3 documentation](http://docs.aws.amazon.com/AmazonS3/latest/dev//example-bucket-policies.html). 
* While creating an external account, enable the encryption to store sensitive data in the S3 bucket by checking the **Keep files in S3 encrypted** box.
* Grant bucket permissions to specify who can access the object in a bucket. For more information on bucket permission, refer to the [Amazon S3 documentation](http://docs.aws.amazon.com/AmazonS3/latest/dev//access-control-overview.html)

## How to define an Adobe Experience Manager external account {#how-to-define-an-adobe-experience-manager-external-account}

AEM external accounts are used when integrating Campaign with AEM.

The list of compatible versions of AEM and more details about this integration are available in [this document](../../integrating/using/about-campaign-integrations.md).

Provide the following details:

* Server: AEM server URL. For example, **http://aem.domain.com:4502**.
* AEM account credentials: use the account that will access the AEM instance. It should be an account part of the campaign-remote group in AEM.

