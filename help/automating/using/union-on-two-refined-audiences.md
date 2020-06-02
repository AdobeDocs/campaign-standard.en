---
title: Union on two refined audiences
description: This use case shows the union of two Read audience activities.
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

# Union on two refined audiences {#example--union-on-two-refined-audiences}

The workflow defined in this example shows the union of two **[!UICONTROL Read audience]** activities. The goal of this workflow is to send an email to Gold or Silver members that are between 18 and 30 years old.

For more on how to use the **[!UICONTROL Read audience]** activity, refer to [this section](../../automating/using/read-audience.md).

Specific audiences are already created in the system to keep track of Gold and Silver members.

The workflow is designed as follows:

![](assets/readaudience_activity_example1.png)

* A first **[!UICONTROL Read audience]** activity that retrieves the Gold members audience and refines it by selecting only profiles that are between 18 and 30 years old.
* A second **[!UICONTROL Read audience]** activity that retrieves the Silver members audience and refines it by selecting only profiles that are between 18 and 30 years old.
* A **[!UICONTROL Union]** activity that unites populations from both **[!UICONTROL Read audiences]** activities into one final population.
* An **[!UICONTROL Email delivery]** activity that sends the email to the population coming from the **[!UICONTROL Union]** activity.
