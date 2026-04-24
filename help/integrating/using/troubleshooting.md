---
title: Troubleshooting integration issues
description: Learn how to troubleshoot issues when sharing resources.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-audience-manager-or-people-core-service
feature: Triggers
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: 5882ada6-dff4-4fd1-a433-0eb31570f73c
TQID: https://experienceleague.adobe.com/Im9-z6yuesgiE6sMO-dM9WgPbty2C9d-PWCv5AE-kNY
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
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
