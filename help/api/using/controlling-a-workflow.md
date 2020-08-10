---
title: Controlling a workflow
description: Learn how to control a workflow with APIs.
page-status-flag: never-activated
uuid: c7b9c171-0409-4707-9d45-3fa72aee8008
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
discoiquuid: 304e7779-42d2-430a-9704-8c599a4eb1da

internal: n
snippet: y
---

# Controlling a workflow {#controlling-a-workflow}

You can control a workflow directly from the REST API, through a POST request containing the workflow ID and the required execution command:

`POST https://mc.adobe.io/<ORGANIZATION>/campaign/workflow/execution/<workflowID>/commands`

>[!CAUTION]
>
>If the worfklow ID is changed in Adobe Campaign, the API request will not work anymore.

Four execution commands are available to control a workflow:

* Start
* Pause
* Resume
* Stop

For more information on the execution commands, refer to the [Campaign documentation](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/executing-a-workflow/about-workflow-execution.html).

<br/>

***Sample requests***

* Start a workflow.

  ```

  -X POST https://mc.adobe.io/<ORGANIZATION>/campaign/workflow/execution/<workflowID>/commands \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer <ACCESS_TOKEN>' \
  -H 'Cache-Control: no-cache' \
  -H 'X-Api-Key: <API_KEY>' \
  -i
  -d '{"method":"start"}'

  ```

  <!-- + réponse -->

* Stop a workflow.

    ```

    -X POST https://mc.adobe.io/<ORGANIZATION>/campaign/workflow/execution/<workflowID>/commands \
    -H 'Content-Type: application/json' \
    -H 'Authorization: Bearer <ACCESS_TOKEN>' \
    -H 'Cache-Control: no-cache' \
    -H 'X-Api-Key: <API_KEY>' \
    -i
    -d '{"method":"stop"}'

    ```

    <!-- + réponse -->
