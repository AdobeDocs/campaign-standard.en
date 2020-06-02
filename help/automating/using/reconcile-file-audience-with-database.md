---
title: Reconcile a File audience with the database
description: This example shows how to use the Read audience activity to reconcile an audience directly created from a file import.
page-status-flag: never-activated
uuid: 58c54e71-f4a7-4ae9-80a3-33c379ab1db9
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: targeting-activities
discoiquuid: 674684e5-8830-4d2f-ba97-59ed4ba7422f
context-tags: readAudience,main
internal: n
snippet: y
---

# Reconcile a File audience with the database {#example--reconcile-a-file-audience-with-the-database}

This example shows how to use the **[!UICONTROL Read audience]** activity to reconcile an audience directly created from a file import.

For more on how to use the **[!UICONTROL Read audience]** activity, refer to [this section](../../automating/using/read-audience.md).

When performing a file import, you can directly save its content in an audience. This audience is a File audience and its data is not linked to any database resources.

The import workflow is designed as follows:

![](assets/readaudience_activity_example3.png)

* A [Load file](../../automating/using/load-file.md) activity uploads a file containing profiles data that were extracted from an external tool.

  For example:

  ```
  lastname;firstname;birthdate;email;crmID
  Smith;Hayden;23/05/1989;hayden.smith@example.com;124365
  Mars;Daniel;17/11/1987;dannymars@example.com;123545
  Smith;Clara;08/02/1989;hayden.smith@example.com;124567
  Durance;Allison;15/12/1978;allison.durance@example.com;120987
  Lucassen;Jody;28/03/1988;jody.lucassen@example.com;127634
  Binder;Tom;19/01/1982;tombinder@example.com;128653
  Binder;Tommy;19/01/1915;tombinder@example.com;134576
  Connor;Jade;10/10/1979;connor.jade@example.com;132452
  Mack;Clarke;02/03/1985;clarke.mack@example.com;149876
  Ross;Timothy;04/07/1986;timross@example.com;157643
  ```

* A [Save audience](../../automating/using/save-audience.md) activity saves the incoming data as an audience. As the data has not been reconciled yet, the audience is a File audience and its data is not recognized as profile data yet.

The reconciliation workflow is designed as follows:

![](assets/readaudience_activity_example2.png)

* A **[!UICONTROL Read audience]** activity uploads the File audience created in the import workflow. The audience data is not yet reconciled with the Adobe Campaign database.
* A [Reconciliation](../../automating/using/reconciliation.md) activity identifies the incoming data as profiles through its **[!UICONTROL Identification]** tab. For example by using the **email** field as reconciliation criteria.
* An [Update data](../../automating/using/update-data.md) activity inserts and updates the profiles resource of the database with the incoming data. As the data is already identified as profiles, you can select the **[!UICONTROL Directly using the targeting dimension]** option and select **[!UICONTROL Profiles]** in the **[!UICONTROL Identification]** tab of the activity. Then, you simply have to add the list of fields that need to be updated in the according tab.
