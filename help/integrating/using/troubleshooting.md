---
title: Troubleshooting
seo-title: Troubleshooting
description: Troubleshooting
seo-description: 
uuid: 854b8396-6946-45c7-8f89-62557858fc7b
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/integrating/using/troubleshooting
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-10T02 18 58.705-0400
cq-lastreplicated: 2018-09-07T15 07 27.320-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-audience-manager-or-people-core-service
cq-template: /apps/help/templates/article-3
discoiquuid: 45527058-a3d0-4f50-bdd6-e77d5b3475e1
firstPublishExternalDate: 2018-09-07T15:07:26.740-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-06-15T07 29 58.798-0400
jcr-createdby: admin
jcr-description: Troubleshooting
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T15:07:26.740-0400
lochandoffdate: 2018-09-10T02 18 58.704-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Troubleshooting
publishexternaldate: 2018-09-07T15 07 26.740-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/integrating/using/troubleshooting.html
sha1: 60e1597f6c08b89d82200862d0a5d682aa3bcaa5
topicBrowsingSortDate: 2018-09-07T15:07:26.740-0400
index: y
internal: n
snippet: y
---

# Troubleshooting{#troubleshooting}

Troubleshooting

Errors may be encountered while using the integration with Audience Manager or People core service.

In this case, make sure that the following elements are correctly configured:

* **External accounts**

  In **Administration** > **Application settings** > **External accounts**, make sure that the following external S3 accounts are correctly configured. The mentioned S3 servers should have been configured during provisioning.

    * **importSharedAudience**: S3 account dedicated to importing audiences.
    * **exportSharedAudience**: S3 account dedicated to exporting audiences.

* **Shared Data Sources**

  In **Administration** > **Application settings** > **Shared Data Sources**, check that the shared data source is set properly.

  **Priority** is used when you have multiple data sources defined. Priority decides which data source will be used to match with alias received in the order defined. **Priority** is only needed for Triggers implementation.

  Check that the reconciliation key is correct. It is the hashed/encrypted value of this field that is used to export and import audiences.

  In case of hashing or encryption of the declared ID, check that the same parameters/encryption algorithms are used on your Website.

  Only one encryption algorithm is supported: AES in CBC mode with a key size of 128, 192 or 256 bits, with PKCS padding.

  If the AES encryption algorithm is selected, the following additional fields must be correctly set:

    * **Encryption Key** for AES
    * **Encryption IV** (Initialization Vector) for AES
    * **Channel** (Email/SMS/Other): This field allows to directly decrypt email addresses and SMS numbers. Make sure that the reconciliation key matches the setting of the **Channel** field. If you select "Other", this specific decryption will not happen and the reconciliation key will be used to reconcile the data.

  Experience Cloud audiences might not be shared because the technical workflow has stopped or paused. Access the **Import shared audience** workflow by clicking directly the **Show ImportShared Audience workflow** option in your Data source.

It can occur that some data are missing when sharing an audience via People core service or when importing an audience. Only records of which the ID ('Visitor ID' or 'Declared ID') was able to be reconciled with the profile dimension are transferred. IDs from the People core service segments that are not recognized by Adobe Campaign are not imported.
