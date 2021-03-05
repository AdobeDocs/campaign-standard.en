---
solution: Campaign Standard
product: campaign
title: Triggering data ingestion through APIs
description: Learn how to trigger data ingestion through APIs.
audience: administration
content-type: reference
topic-tags: configuring-channels

---

# Triggering data ingestion through APIs {#triggering-data-ingestion-apis}

>[!IMPORTANT]
>
>Adobe Experience Platform Data Connector is currently in beta, which may be subject to frequent updates without notice. Customers are required to be hosted on Azure (currently in beta for North America only) to access these capabilities. Please reach out to Adobe Customer Care if you would like access.

Adobe Campaign Standard allows you to trigger the immediate ingestion of data mappings via APIs, and retrieve the status of your ingestion requests.

This page describes how to trigger and retrieve the ingestion status of your data mappings. For global information on Campaign Standard APIs, refer to [this section](../../api/using/get-started-apis.md).

## Prerequisites {#prerequisites}

Before using the APIs, the data mapping must first have been configured and published within Campaign Standard interface. For more on thisn refer to these sections:

* [Mapping definition](../../integrating/using/aep-mapping-definition.md)
* [Mapping activation](../../integrating/using/aep-mapping-activation.md)

Once the data mapping is created, you must stop it from running so that you can trigger it from the APIs whenever you want. To do this, follow these steps:

1. In Campaign Standard, go to the **[!UICONTROL Administration]** > **[!UICONTROL Development]** > **[!UICONTROL Platform]** > **[!UICONTROL Status of data export to platform]** menu.

1. Double-click the data mapping to open it, then click the **[!UICONTROL Stop]** button.

    ![](assets/aep_datamapping_stop.png)

1. Save your changes

The data mapping execution is now stopped. You can use Campaign Standard APIs to trigger it manually.

## Starting the immediate ingestion of data mapping {#starting-immediate-ingestion}

Immediate ingestion of a XDM mapping into Adobe Experience Platform is triggered with a POST operation:

`POST https://mc.adobe.io/<ORGANIZATION>/campaign/dataIngestion/xdmIngestion/<XDM Mapping ID>/ingest`

>[!NOTE]
>
>In order to execute ingest POST API call, user must have an **SQL function execution** role, which can be provided by a Campaign Standard administrator by executing below JS Script:
>
>```
>var sqlRoleObj = REST.head.roleBase.sql.get();
>REST.head.securityGroup.Administrators.roles.post(sqlRoleObj);
>```
>

The POST operation returns information regarding the created request status:

* Request successfully submitted for the XDM Mapping:

```
{
"requestId": <value>,
"info": "Ingestion request submitted successfully for the Mapping ID: <value>",
"status":"Success"
}
```

* Request already in progress for the XDM Mapping:

```
{
"requestId": <value>,
"info": "Ingestion request already in progress for the Mapping ID: <value>",
"status":"In Progress"
}
```

* Request failed because the XDM mapping is not published or is stopped:

```
{
"info": "Unable to submit data ingestion request, XDM Mapping ID: <value> is not stopped",
"status": "Failed"
}
{
"info": "Unable to submit data ingestion request, XDM Mapping ID: <value> is not published",
"status": "Failed"
}
```

## Retrieving the status of an ingestion request {#retrieving-status}

The status of an ingestion request can be retrieved with a GET operation and the desired request ID in the parameters:

```
GET https://mc.adobe.io/<ORGANIZATION>/campaign/dataIngestion/xdmIngestion/<XDM Mapping ID>/ingest
{"requestId"="<value>"}
```

>[!NOTE]
>
>Detailed information about the XDM mapping request status and its related jobs is available in Campaign Standard interface, in the **[!UICONTROL Status of data export to platform]** menu (see [Mapping activation](../../integrating/using/aep-mapping-activation.md)).

The GET operation returns the information below:

* **batchId**: this field is populated only if failure occurred after batch prepare and upload,
* **info**: the XDM mapping ID,
* **numRecords**: the number of records that have been ingested (success status only),
* **status**: the ingest request status (success/failed/in progress)

Possible responses to the GET operation are:

* Ingest request successful:

    ```
    {
    "batchId": "",
    "info": "Mapping Id: <value>. ",
    "numRecords": 15,
    "requestId": 3520,
    "status": "Success"
    }
    ```

* Ingest request failed with 0 record ingested:

    ```
    {
    "batchId": "",
    "info": "Mapping Id: <value>. ACP-880056 Failed to fetch the record from the database.",
    "numRecords": 0,
    "requestId": 3520,
    "status": "Failed"
    }
    ```

* Ingest request failed, with some record uploaded under a batch:

    ```
    {
    "batchId": "<value>",
    "info": "Mapping Id: <value>. ACP-880096 Sync Job failed to upload. Please check the error in the Platform UI.",
    "numRecords": 0,
    "requestId": <value>,
    "status": "Failed"
    }
    ```

* Ingest request aborted after ingesting some records (this may happen in crash scenarios):

    ```
    {
    "batchId": "",
    "info": "Mapping Id: <value>. Ingestion request aborted due to some issue with data ingestion service. Please submit a new request",
    "numRecords": 0,
    "requestId": <value>,
    "status": "Aborted"
    }
    ```

* Ingest request in progress (when request uploaded the data in a batch or when batch is getting prepared for the request):
    ```
    {
    "batchId": "",
    "info": "Mapping Id: <value>.",
    "numRecords": 0,
    "requestId": <value>,
    "status": "In Progress"
    }
    ```
