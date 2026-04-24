---
title: Identifying duplicates before a delivery
description: The following example illustrates a deduplication that lets you exclude the duplicates of a target before sending an email. This means you avoid sending a communication several times to the same profile.
audience: automating
content-type: reference
topic-tags: targeting-activities
context-tags: dedup,main
feature: Workflows
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: a09b101b-f76f-4377-9854-1fcffaad4f9a
TQID: https://experienceleague.adobe.com/4t0TujgM3kHTT36-Gy2lmiVQIRMy3OeChAw-Xx5MnWY
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
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
---
# Identifying duplicates before a delivery {#identifying-duplicates-before-a-delivery}

The following example illustrates a deduplication that lets you exclude the duplicates of a target before sending an email. This means you avoid sending a communication several times to the same profile.

The workflow is made up of:

![](assets/deduplication_example_workflow.png)

* A [Query](../../automating/using/query.md) which allows you to define the target of the email. Here, the workflow targets all profiles aged between 18 and 25 that have been in the client database for more than a year.

  ![](assets/deduplication_example_query.png)

* A [Deduplication](../../automating/using/deduplication.md) activity, which allows you to identify the duplicates that come from the preceding query. In this example, only one record is saved for each duplicate. The duplicates are identified using the email address. This means that the email delivery can only be sent once for each email address to be present in the targeting.

  The deduplication method selected is **[!UICONTROL Non-empty value]**. This allows you to ensure that amongst the records kept in case of duplicates, priority is given to those in which the **First name** has been provided. This will make it more coherent if the first name is used in the personalization fields of the email content.

  In addition, an extra transition is added to keep the duplicates and to be able to list them.

  ![](assets/deduplication_example_dedup.png)

* An [Email delivery](../../automating/using/email-delivery.md) placed after the main outbound transition of the deduplication.
* A [Save audience](../../automating/using/save-audience.md) activity placed after the additional transition of the deduplication to save the duplicates in a **Duplicates** audience. This audience can be reused to directly exclude its members from every email delivery.
