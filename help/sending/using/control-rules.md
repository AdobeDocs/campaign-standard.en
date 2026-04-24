---
title: Control rules
description: Learn how to reinforce the quality check of your messages with control rules.
audience: administration
content-type: reference
topic-tags: working-with-typology-rules
feature: Typology Rules
role: User
level: Intermediate
exl-id: 6461c128-1e42-4685-88f8-507244147e6f
TQID: https://experienceleague.adobe.com/lpPFofV3IPl7zmbaR4TOuyCcVqgjwI3maxr-jKzkd0Q
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Control rules {#control-rules}

Control rules allow you to check the validity and quality of the messages before they are sent, such as character display, SMS message size, address format, etc.

>[!NOTE]
>
>For security reasons, control rules are read-only and cannot be modified.

## Default control rules {#default-control-rules}

A set of default rules ensures the standard controls. The table below provides information about these rules, as well as their related channel and [execution phases](#control-rules-execution-phases).

| Label | Channel | Execution phase | Description|
|---------|----------|---------|---------|
| **[!UICONTROL A/B Test]** | Email | At the start of personalization | Extracts the test population for a delivery with an A/B test.|
| **[!UICONTROL Check delivery size]** | All | After targeting | Checks the size of the messages.|
| **[!UICONTROL Check email content is not empty]** | Email | After targeting | Generates an error if the content of the message is empty.|
| **[!UICONTROL Check In-App content for broadcast template]** | In-App | At the start personalization | Checks that In-App content / triggers are not empty for broadcast template.|
| **[!UICONTROL Check In-App content for profile template]** | In-App | At the start of personalization | Checks that In-App content / triggers are not empty for profile template.|
| **[!UICONTROL Check In-App content for subscriber template]** | In-App | At the start of personalization | Checks that In-App content / triggers are not empty for subscriber template.|
| **[!UICONTROL Check proof size]**| All | After targeting | Generates an error message if the proof target population exceeds 100 recipients.|
| **[!UICONTROL Check social network sharing link]** | Email | At the start of personalization | Checks the presence of a link to a mirror page when including a social network sharing link (ViralLinks) in the content.|
| **[!UICONTROL Check subject]** | Email | At the start of personalization | Checks that the subject and sender address do not contain special characters which may cause problems on certain mail transfer agents, and checks that the message subject has been completed.|
| **[!UICONTROL Check unsubscription link]** | Email | At the start of personalization | Checks for the presence of at least one unsubscription (opt-out) URL in each content (HTML and Text).|
| **[!UICONTROL Check URL labels]** | Email | At the start of personalization | Checks that each tracking URL has a label.|
| **[!UICONTROL Check URLs]** | Email | At the start of personalization | Checks the tracking URLs (presence of the "&" character).|

## Control rules execution phases {#control-rules-execution-phases}

Control rules can be applied at different phases of the delivery's life cycle:

* **At the start of targeting**: The control rule can be applied at this phase so that the personalization step is not executed in the event of an error.

* **After targeting**: Executing after targeting allows you to know the volume of the target in order to apply the control rule.

  For example, the **Check proof size** control rule applies after the targeting stage: this rule prevents the preparation of message personalization if there are too many proof recipients.

* **At the start of personalization**: Applies when the check relates to message personalization approval. Message personalization is carried out during the analysis phase.

* **At the end of the analysis**: When a check requires message personalization to be complete.
