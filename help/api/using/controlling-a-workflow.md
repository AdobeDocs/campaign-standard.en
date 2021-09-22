---
title: Controlling a workflow
description: Learn how to control a workflow with APIs.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis

feature: API
role: Data Engineer
level: Experienced
exl-id: 79eacc31-d5a2-4e13-aa0b-744d7ab7004f
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

For more information on the execution commands, refer to the [Campaign documentation](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/executing-a-workflow/about-workflow-execution.html).

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
