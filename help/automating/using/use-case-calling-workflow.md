---
title: Calling a workflow with external parameters
description: This section details how to call a workflow with external parameters.
audience: automating
content-type: reference
topic-tags: workflow-general-operation

feature: Workflows
role: Data Architect
level: Intermediate
exl-id: 7a21f4f6-316f-4f3d-9d53-37d406a46aae
---
# Use case {#use-case}

The use case below shows how to call workflow with parameters within your workflows.

The objective is to trigger a workflow from an API call with external parameters. This workflow will load data into your database from a file and create an associated audience. Once the audience has been created, a second workflow will be triggered to send a message personalized with the external parameters defined in the API call.

To perform this use case, you need to perform the actions below:

1. **Make an API call** to trigger Workflow 1 with external parameters. See [Step 1: Configuring the API call](../../automating/using/use-case-calling-workflow.md#step-1--configuring-the-api-call).
1. **Build Workflow 1**: the workflow will transfer a file and load it into the database. It will then test if the data is empty or not, and eventually save the profiles into an audience. Finally, it will trigger Workflow 2. See [Step 2: Configuring Workflow 1](../../automating/using/use-case-calling-workflow.md#step-2--configuring-workflow-1).
1. **Build Workflow 2**: the workflow will read the audience that has been created in Workflow 1, then send a personalized message to the profiles, with a segment code customized with the parameters. See [Step 3: Configuring Workflow 2](../../automating/using/use-case-calling-workflow.md#step-3--configuring-workflow-2).

![](assets/extsignal_uc_process.png)

## Prerequisites {#prerequisites}

Before configuring the workflows, you need to create Workflow 1 and 2 with an **[!UICONTROL External signal]** activity in each of them. This way, you will be able to target these signal activities when calling the workflows.

## Step 1: Configuring the API call {#step-1--configuring-the-api-call}

Make an API call to trigger Workflow 1 with parameters. For more on the API call syntax, refer to the [Campaign Standard REST APIs documentation](../../api/using/triggering-a-signal-activity.md).

In our case, we want to call the workflow with the parameters below:

* **fileToTarget**: the name of the file that we want to import into the database.
* **discountDesc**: the description that we want to display into the delivery for the discount.

```
-X POST https://mc.adobe.io/<ORGANIZATION>/campaign/<TRIGGER_URL>
-H 'Authorization: Bearer <ACCESS_TOKEN>' 
-H 'Cache-Control: no-cache' 
-H 'X-Api-Key: <API_KEY>' 
-H 'Content-Type: application/json;charset=utf-8' 
-H 'Content-Length:79' 
-i
-d {
-d "source:":"API",
-d "parameters":{
-d "fileToTarget":"profile.txt",
-d "discountDesc":"Running shoes"
-d } 
```

## Step 2: Configuring Workflow 1 {#step-2--configuring-workflow-1}

Workflow 1 will be built as below:

* **[!UICONTROL External signal]** activity: where the external parameters must be declared in order to be used within the workflow.
* **[!UICONTROL Transfer file]** activity: imports the file with the name defined in the parameters.
* **[!UICONTROL Load file]** activity: loads data from the imported file into the database.
* **[!UICONTROL Update data]** activity: insert or update the database with data from the imported file.
* **[!UICONTROL Test]** activity: checks if there is data imported.
* **[!UICONTROL Save audience]** activity: if the file contains data, saves the profiles into an audience.
* **[!UICONTROL End activity]** activity: calls Workflow 2 with the parameters that you want to use within it.

![](assets/extsignal_uc_wkf1.png)

Follow the steps below to configure the workflow:

1. Declare the parameters that have been defined in the API call. To do this, open the **[!UICONTROL External signal]** activity, then add the parameters' names and types.

   ![](assets/extsignal_uc1.png)

1. Add a **[!UICONTROL Transfer file]** activity to import data into the database.To do this, drag and drop the activity, open it, then select the **[!UICONTROL Protocol]** tab.
1. Select the **[!UICONTROL Use a dynamic file path]** option, then use the **fileToTarget** parameter as the file to transfer:

   ```
   $(vars/@fileToTarget)
   ```

   ![](assets/extsignal_uc2.png)

1. Load the data from the file into the database.

   To do this, drag and drop a **[!UICONTROL Load file]** activity into the workflow, then configure it according to your needs.

1. Insert and update the database with data from the imported file.

   To do this, drag and drop an **[!UICONTROL Update data]** activity, then select the **[!UICONTROL Identification]** tab to add a reconciliation criteria (in our case the **email** field).

   ![](assets/extsignal_uc3.png)

1. Select the **[!UICONTROL Fields to update]** tab, then specify the fields to update in the database (in our case the **firstname** and **email** fields).

   ![](assets/extsignal_uc4.png)

1. Check if data is retrieved from the file. To do this, drag and drop a **[!UICONTROL Test]** activity into the workflow, then click the **[!UICONTROL Add an element]** button to add a condition.
1. Name and define the condition. In our case, we want to test if the outbound transition contains data with the syntax below:

   ```
   $long(vars/@recCount)>0
   ```

   ![](assets/extsignal_uc5.png)

1. If data is retrieved save it into an audience. To do this, add a **[!UICONTROL Save audience]** activity to the **Target not empty** transition, then open it.
1. Select the **[!UICONTROL Use a dynamic label]** option, then use the **fileToTarget** parameter as the label of the audience:

   ```
   $(vars/@fileToTarget)
   ```

   ![](assets/extsignal_uc6.png)

1. Drag and drop an **[!UICONTROL End]** activity that will call Workflow 2 with parameters, then open it.
1. Select the **[!UICONTROL External signal]** tab, then specify the workflow to trigger and its associated signal activity.
1. Define the parameters that you want use within Workflow 2 and their associated values.

   In our case, we want to pass the parameters originally defined in the API call (**fileToTarget** and **discountDesc**), and an additional **segmentCode** parameter with a constant value ("20% discount").

   ![](assets/extsignal_uc7.png)

Workflow 1 is configured, you can now build Workflow 2. For more on this, refer to [this section](../../automating/using/use-case-calling-workflow.md#step-3--configuring-workflow-2).

## Step 3: Configuring Workflow 2 {#step-3--configuring-workflow-2}

Workflow 2 will be built as below:

* **[!UICONTROL External signal]** activity: where the parameters must be declared in order to be used within the workflow.
* **[!UICONTROL Read audience]** activity: reads the audience saved in Workflow 1.
* **[!UICONTROL Email delivery]** activity: sends a recurring message to the targeted audience, personalized with parameters.

![](assets/extsignal_uc_wkf2.png)

Follow the steps below to configure the workflow:

1. Declare the parameters that have been defined in Workflow 1.

   To do this, open the **[!UICONTROL External signal]** activity, then add the name and type of each parameter defined in the **[!UICONTROL End]** activity of Workflow 1.

   ![](assets/extsignal_uc8.png)

1. Use the audience that has been saved in Workflow 1. To do this, drag and drop a **[!UICONTROL Read audience]** activity into the workflow, then open it.
1. Select the **[!UICONTROL Use a dynamic audience]** option, then use the **fileToTarget** parameter as the name of the audience to read:

   ```
   $(vars/@fileToTarget)
   ```

   ![](assets/extsignal_uc9.png)

1. Name the outbound transition according to the **segmentCode** parameter.

   To do this, select the **[!UICONTROL Transition]** tab, then the **[!UICONTROL Use a dynamic segment code]** option.

1. Use the **segmentCode** parameter as the name of the outbound transition:

   ```
   $(vars/@segmentCode)
   ```

   ![](assets/extsignal_uc10.png)

1. Drag and drop an **[!UICONTROL Email delivery]** activity to send a message to the audience.
1. Identify the parameters to use in the message to personalize it with the **discountDesc** parameter. To do this, open the activity's advanced options, then add the parameter name and value.

   ![](assets/extsignal_uc10b.png)

1. You can now configure the message. Open the activity, then select **[!UICONTROL Recurring email]**.

   ![](assets/extsignal_uc11.png)

1. Select the template to use, then define the email properties according to your needs.
1. Use the **discountDesc** parameter as a personalization field. To do this, select it from the personalization fields list. 

   ![](assets/extsignal_uc13.png)

1. You can now finish configuring the message, then send it as usual.

   ![](assets/extsignal_uc14.png)

## Executing the workflows {#executing-the-workflows}

Once the workflows has been built, you can execute them. Make sure the two workflows are started before performing the API call.
