---
title: Provisioning and configuring People core service integration
seo-title: Provisioning and configuring People core service integration
description: Provisioning and configuring People core service integration
seo-description: Learn how to configure the People core service integration to start sharing audiences or segments with the different Adobe Marketing Cloud solutions. 
page-status-flag: never-activated
uuid: 1cec882a-9bc3-4390-82b8-fa7bb85c547f
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/integrating/using/provisioning-and-configuring-people-core-service-integration
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-01-10T15 24 10.085-0500
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: people-core-service-integration
cq-template: /apps/help/templates/article-3
discoiquuid: 4fd5f62e-ede3-42e3-bd87-3b9e11be29a7
firstPublishExternalDate: 2018-01-10T15:24:10.078-0500
herogradient: light
jcr-created: 2018-01-11T19 02 43.950-0500
jcr-createdby: admin
jcr-description: Provisioning and configuring People core service integration
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-01-10T15:24:10.078-0500
lr-lastreplicatedby: sauviat@adobe.com
moreHelpPaths: /content/help/en/campaign/standard/integrating/morehelp/people-core-service-integration;/content/help/en/campaign/standard/integrating/morehelp/people-core-service-integration
navTitle: Provisioning and configuring People core service integration
publishexternaldate: 2018-01-10T15 24 10.078-0500
publishExternalURL: https://helpx.adobe.com/campaign/standard/integrating/using/provisioning-and-configuring-people-core-service-integration.html
sha1: bd386c35b2d55a45979fce80e8d731f609cdfb84
topicBrowsingSortDate: 2018-01-10T15:24:10.078-0500
index: y
internal: n
snippet: y
---

# Provisioning and configuring People core service integration

Provisioning and configuring People core service integration

People core service integration lets you import and export audiences or segments in Adobe Campaign.

This integration must first be configured. To request provisioning of this integration, write an email to [Digital-Request@adobe.com](mailto:Digital-Request@adobe.com) with the following information:

|  **Request Type:** | Configure AAM/People core service-Campaign Integration  |
|---|---|
|  **Organization Name:** | Your organization name  |
|  **IMS Org ID** | Your IMS Org ID&#42;  |
|  **Environment:** | Example: Production  |
|  **AAM or People Service** | Example: Adobe Audience Manager  |
|  **Declared ID or Visitor ID** | Example: Declared ID  |
|  **Additional Information** | Any useful information or comment that you may have  |

&#42; You can find your IMS Org ID on the Marketing Cloud, in the **Administration** menu. It is also provided when you first connect to the Adobe Marketing Cloud.

After submitting this request, Adobe will proceed to the provisioning of the integration for you and contact you to provide details and information that you have to finalize the configuration:

1. Configure or check the external accounts in Adobe Campaign as follows:

   Go to **Administration** > **Application settings** > **External accounts**. The mentioned SFTP accounts should have been configured by Adobe and the necessary information should have been communicated to you.

    * **importSharedAudience**: SFTP account dedicated to importing audiences.
    * **exportSharedAudience**: SFTP account dedicated to exporting audiences.

   Use the **ftp-out.demdex.com** domain for the import external account and the **ftp-in.demdex.com** domain for the export external account. Remember that an export from Campaign is an import for Audience Manager or People core service.

   Specify the user name and password provided by Adobe.

1. In **Administration** > **Application settings** > **AMC Data sources**, configure the AMC Data sources or check that they are set properly.

   Configure the **Recipient - Visitor ID** data source by entering the Data Source ID and AAM Destination ID provided by Adobe.

1. Make sure the Campaign Tracking Server is registered on the domain (CNAME). You can find more information about domain name delegation in [this article](https://docs.campaign.adobe.com/doc/AC6.1/en/Technotes/AdobeCampaign_Deliverability_Sub_Domain_Delegation.pdf).
1. Configure the Visitor ID Service on your web properties/sites by following [this document](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-setup-aam-analytics.html).

Your configuration and provisioning are finalized, the integration can now be used to import and export audiences or segments.

## Troubleshooting

Errors may be encountered while using the People core service integration.

In this case, make sure that the following elements are correctly configured:

* **External accounts**

  In **Administration** > **Application settings** > **External accounts**, make sure that the following external SFTP accounts are correctly configured. The mentioned SFTP servers should have been configured during provisioning.

    * **importSharedAudience**: SFTP account dedicated to importing audiences.
    * **exportSharedAudience**: SFTP account dedicated to exporting audiences.

* **AMC Data source**

  In **Administration** > **Application settings** > **AMC Data sources**, check that the AMC Data source is set properly.

  Check that the reconciliation key is correct. It is the hashed/encrypted value of this field that is used to export and import audiences.

  In case of hashing or encryption of the declared ID, check that the same parameters/encryption algorithms are used on your Website.

  Only one encryption algorithm is supported: AES in CBC mode with a key size of 128, 192 or 256 bits, with PKCS padding.

  If the AES encryption algorithm is selected, the following additional fields must be correctly set:

    * **Encryption Key** for AES
    * **Encryption IV** (Initialization Vector) for AES
    * **Channel** (Email/SMS/Other): This field allows to directly decrypt email addresses and SMS numbers. Make sure that the reconciliation key matches the setting of the **Channel** field. If you select "Other", this specific decryption will not happen and the reconciliation key will be used to reconcile the data.

It can occur that some data are missing when sharing an audience via People core service or when importing an audience. Only records of which the ID ('Visitor ID' or 'Declared ID') was able to be reconciled with the profile dimension are transferred. IDs from the People core service segments that are not recognized by Adobe Campaign are not imported.
