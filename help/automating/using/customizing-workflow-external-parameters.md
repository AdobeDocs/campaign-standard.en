---
title: Customizing a workflow with external parameters
description: This section details how to call a workflow with external parameters.
audience: automating
content-type: reference
topic-tags: workflow-general-operation

feature: Workflows
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: 8c1a47ed-3467-4fcd-8747-86f0e8f15cec
---
# Customizing a workflow with external parameters {#customizing-a-workflow-with-external-parameters}

Once the workflow has been triggered, the parameters are ingested into the events variables and can be used to customize the workflow's activities.

They can, for example, be used to define which audience to read in the **[!UICONTROL Read audience]** activity, the name of the file to transfer in the **[!UICONTROL Transfer file]** activity, etc. (see [this page](../../automating/using/customizing-workflow-external-parameters.md)).

## Using events variables {#using-events-variables}

Events variables are used within an expression that must respect the [Standard syntax](../../automating/using/advanced-expression-editing.md#standard-syntax).

The syntax to use events variables must follow the format below, and use the parameter's name that has been defined in the **[!UICONTROL External signal]** activity (see [Declaring the parameters in the External signal activity](../../automating/using/declaring-parameters-external-signal.md)):

```
$(vars/@parameterName)
```

In this syntax, the **$** function returns **string** data type. If you want to specify another type of data, use the following functions:

* **$long**: integer number.
* **$float**: decimal number.
* **$boolean**: true/false.
* **$datetime**: timestamp.

When using a variable in an activity, the interface provides help to call it.

![](assets/extsignal_callparameter.png)

* ![](assets/extsignal_picker.png): select the events variable among all variables that are available in the workflow.

  ![](assets/wkf_test_activity_variables.png)

* ![](assets/extsignal_expression_editor.png): edit expressions combining variables and functions (see [this page](../../automating/using/advanced-expression-editing.md)).

  ![](assets/wkf_test_activity_variables_expression.png)

  This list provides functions that allow you to carry out complex filtering. These functions are detailed in [this section](../../automating/using/list-of-functions.md).
  
  Additionally, you can use the functions below, which are available in all the activities that allow you to use events variables after calling a workflow with external parameters (see [this section](../../automating/using/customizing-workflow-external-parameters.md#customizing-activities-with-events-variables)):

  | Name | Description | Syntax|
  | ---------|----------|---------|
  | EndWith | Indicates if a string (1st parameter) ends with a specific string (2nd parameter). | EndWith(&lt;String&gt;,&lt;String&gt;)|
  | startWith | Indicates if a string (1st parameter) starts with a specific string (2nd parameter). | startWith(&lt;String&gt;,&lt;String>)|
  | Extract | Returns the first characters of a string using a separator. | Extract(&lt;String&gt;,&lt;Separator&gt;)|
  | ExtractRight | Returns the last characters of a string using a separator. | ExtractRight(&lt;String&gt;,&lt;Separator&gt;)|
  | DateFormat | Formats a date using the format specified in the 2nd parameter (example:  '%4Y%2M%2D') | DateFormat(&lt;Date&gt;,&lt;Format&gt;)|
  | FileName | Returns the name of a file path. | FileName(&lt;String&gt;)|
  | FileExt | Returns the extension of a file path. | FileExt(&lt;String&gt;)|
  | GetOption | Returns the value of the specified function. | GetOption(&lt;optionName&gt;)|
  | IsNull | Indicates if a string or a date is null. | IsNull(&lt;String/date&gt;)|
  | UrlUtf8Encode | Encodes an URL in UTF8. | UrlUtf8Encode(&lt;String&gt;)|

## Customizing activities with events variables {#customizing-activities-with-events-variables}

Events variables can be used to customize several activities, listed in the section below. For more on how to call a variable from an activity, refer to [this section](../../automating/using/customizing-workflow-external-parameters.md#using-events-variables).

**[!UICONTROL Read audience]** activity: define the audience to target based on events variables. For more on how to use the activity, refer to [this section](../../automating/using/read-audience.md).

![](assets/extsignal_activities_audience.png)

**[!UICONTROL Test]** activity: build conditions based on events variables. For more on how to use the activity, refer to [this section](../../automating/using/test.md).

![](assets/extsignal_activities_test.png)

**[!UICONTROL Transfer file]** activity: customize the file to transfer based on events variables. For more on how to use the activity, refer to [this section](../../automating/using/transfer-file.md).

![](assets/extsignal_activities_transfer.png)

**[!UICONTROL Query]** activity: parameters can be referenced in a query, by using expressions combining events variables and functions. To do this, add a rule then click the **[!UICONTROL Advanced mode]** link to access the expression editing window (see [Advanced expression editing](../../automating/using/advanced-expression-editing.md)).

For more on how to use the activity, refer to [this section](../../automating/using/query.md).

![](assets/extsignal_activities_query.png)

**[!UICONTROL Channels]** activities: personalize deliveries based on events variables.

  >[!NOTE]
  >
  >The delivery parameters' values are retrieved each time the delivery is prepared.
  >
  >Recurring deliveries preparation is based on the delivery **aggregation period**. For example, if the aggregation period is "by day", then the delivery will be re-prepared only once a day. If a delivery parameter's value is modified during the day, then it will not be updated in the delivery, as it has already been prepared once.
  >
  >If you plan on calling the workflow multiple times a day, use the [!UICONTROL No aggregation] option, so that the delivery parameters are updated each time. For more on recurring deliveries configuration, refer to [this section](/help/automating/using/email-delivery.md#configuration).

To personalize a delivery based on events variables, you must first declare into the delivery activity the variables that you want to use:

1. Select the activity, then click the ![](assets/dlv_activity_params-24px.png) button to access the settings.
1. Select the **[!UICONTROL General]** tab, then add the events variables that will be available as personalization fields in the delivery.

   ![](assets/extsignal_activities_delivery.png)

1. Click the **[!UICONTROL Confirm]** button.

Declared events variables are now available from the list of personalization fields. You can use them in the delivery to perform the actions below:

* Define the name of the template to use for the delivery.

  >[!NOTE]
  >
  >This action is available for **recurring** deliveries only.

  ![](assets/extsignal_activities_template.png)

* Personalize the delivery: when selecting a personalization field to configure a delivery, events variables are available in the **[!UICONTROL Workflow parameters]** element. You can use them as any personalization field, for example to define the delivery subject, the sender etc.

  Delivery personalization is detailed in [this section](../../designing/using/personalization.md).

  ![](assets/extsignal_activities_perso.png)

**Segment codes**: define the segment code based on events variables.

>[!NOTE]
>
>This action can be performed from any activity that lets you define a segment code like, for example, **[!UICONTROL Query]** or **[!UICONTROL Segmentation]** activities.

![](assets/extsignal_activities_segment.png)

**Delivery label**: define the delivery label based on events variables.

![](assets/extsignal_activities_label.png)
