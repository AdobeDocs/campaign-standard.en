---
title: Triggering a signal activity
description: Learn how to trigger a signal activity with APIs.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
feature: API
role: Data Engineer
level: Experienced
exl-id: 9f94e98f-fe04-4369-8946-1380e02cdece
---
# Triggering a signal activity {#triggering-a-signal-activity}

In an Adobe Campaign Standard workflow, there can be one or more **External signal** activities. These activities are 'listeners' that wait to be triggered.

Campaign Standard APIs let you trigger an **External signal** activity to call a workflow. The API call can include parameters that will be ingested into the workflow's events variables (an audience name to target, a file name to import, a part of message content, etc.). This way, you can easily integrate your Campaign automations with your external system.

>[!NOTE]
>
>External signal activities cannot be triggered more often than every 10 minutes and that the destination workflow must be already running.

To trigger a workflow, follow the steps below:

1. Perform a **GET** request on the workflow to retrieve the External signal activity trigger URL.

    `GET https://mc.adobe.io/<ORGANIZATION>/campaign/workflow/execution/<workflowID>`

1. Perform a **POST** request on the returned URL to trigger the signal activity, with the **"source"** parameter in the payload. This attribute is mandatory, it lets you indicate the triggering request source.

If you want to call the workflow with parameters, add them into the payload with the **"parameters"** attribute. The syntax consists of the parameter's name followed by its value (the following  types are supported: **string**, **number**, **boolean** and **date/time**).

  ```

    -X POST <TRIGGER_URL>
    -H 'Authorization: Bearer <ACCESS_TOKEN>' \
    -H 'Cache-Control: no-cache' \
    -H 'X-Api-Key: <API_KEY>' \
    -H 'Content-Type: application/json;charset=utf-8' \
    -H 'Content-Length:79' \
    -i
    -d {
    -d    "source":"<SOURCE>",
    -d    "parameters":{
    -d      "<PARAMETER_NAME":"<PARAMETER_VALUE>",
    -d      "<PARAMETER_NAME":"<PARAMETER_VALUE>",
    -d      "<PARAMETER_NAME":"<PARAMETER_VALUE>",  
    -d      "<PARAMETER_NAME":"<PARAMETER_VALUE>"
    -d    }
    -d }

  ```

  >[!NOTE]
  >
  >When adding a parameter to the payload, make sure that its **name** and **type** values are consistent with the information declared in the External signal activity. Moreover, the payload size should not exceed 64Ko.

<br/>

***Sample request***

Perform a GET request on the workflow.

```

-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/workflow/execution/<workflowID> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'

```

It returns the workflow signal activity and the associated trigger url.

```

{
"PKey": "<PKEY>",
"activities": {
  "activity": {
    "signal1": {
      ...
      "trigger": {
        "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/workflow/execution/<PKEY>/activities/activity/<PKEY>/trigger/"
        },
        ...
      }
    }
  }
}

```

To trigger a signal activity, perform a POST request on the trigger url with the "source". Add the "parameters" attributes if you want to call the workflow with parameters.

```

-X POST https://mc.adobe.io/<ORGANIZATION>/campaign/workflow/execution/<PKEY>/activities/activity/<PKEY>/trigger \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>' \
-i
-d '{
-d "source":"API",
-d "parameters":{
-d    "audience":"audience",
-d    "email":"anna.varney@mail.com",
-d    "template":"05",
-d    "contentURL":"http://www.adobe.com",
-d    "test":"true",
-d    "segmentCode":"my segment",
-d    "attribute":"2019-04-03 08:17:19.100Z"}
-d  }'

```

<!-- + réponse -->

If one of the parameters is not declared in the External signal activity, the POST request returns the error below, indicating which parameter is missing.

```

RST-360011 An error has occurred - please contact your administrator.
'contentURL' parameter isn't defined in signal activity.
XTK-170006 Unable to parse expression 'HandleTrigger(@name, $(source), $({parameters}))'.
RST-360000 Error while assessing 'HandleTrigger(@name, $(source), $({parameters}))' expression ('xtk:workflow:execution/activities/signal/trigger' resource)

```
