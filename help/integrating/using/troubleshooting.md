---
solution: Campaign Standard
product: campaign
title: Troubleshooting
description: Learn how to troubleshoot issues when sharing resources.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-audience-manager-or-people-core-service

feature: Triggers
role: Data Architect
level: Intermediate
---

# Troubleshooting{#troubleshooting}

Errors may be encountered while using the integration with Audience Manager or People core service.

In this case, make sure that the following elements are correctly configured:

* **External accounts**

  In **[!UICONTROL Administration]** > **[!UICONTROL Application settings]** > **[!UICONTROL External accounts]**, make sure that the following external S3 accounts are correctly configured. The mentioned S3 servers should have been configured during provisioning.

    * **[!UICONTROL importSharedAudience]**: S3 account dedicated to importing audiences.
    * **[!UICONTROL exportSharedAudience]**: S3 account dedicated to exporting audiences.

* **Shared Data Sources**

  In **[!UICONTROL Administration]** > **[!UICONTROL Application settings]** > **[!UICONTROL Shared Data Sources]**, check that the shared data source is set properly.

  **[!UICONTROL Priority]** is used when you have multiple data sources defined. Priority decides which data source will be used to match with alias received in the order defined. **[!UICONTROL Priority]** is only needed for Triggers implementation.

  Check that the reconciliation key is correct. It is the hashed/encrypted value of this field that is used to export and import audiences.

  In case of hashing or encryption of the declared ID, check that the same parameters/encryption algorithms are used on your Website.

  Only one encryption algorithm is supported: AES in CBC mode with a key size of 128, 192 or 256 bits, with PKCS padding.

  If the AES encryption algorithm is selected, the following additional fields must be correctly set:

    * **Encryption Key** for AES
    * **Encryption IV** (Initialization Vector) for AES
    * **Channel** (Email/SMS/Other): This field allows to directly decrypt email addresses and SMS numbers. Make sure that the reconciliation key matches the setting of the **Channel** field. If you select "Other", this specific decryption will not happen and the reconciliation key will be used to reconcile the data.

  Experience Cloud audiences might not be shared because the technical workflow has stopped or paused. Access the **[!UICONTROL Import shared audience]** workflow by clicking directly the **[!UICONTROL Show ImportShared Audience workflow]** option in your Data source.

It can occur that some data are missing when sharing an audience via People core service or when importing an audience. Only records of which the ID ('Visitor ID' or 'Declared ID') was able to be reconciled with the profile dimension are transferred. IDs from the People core service segments that are not recognized by Adobe Campaign are not imported.
