---
solution: Campaign Standard
product: campaign
title: Defining the subject line and the sender of an email
description: Discover how to define the subject line and the sender of an email in the Email Designer.
audience: designing
content-type: reference
topic-tags: editing-email-content

feature: Email Design
role: Business Practitioner
level: Beginner
---

# Defining the subject line and the sender of an email{#defining-the-subject-line-of-an-email}

## Defining the subject line of an email {#subject-line}

The message subject is mandatory to prepare and send the message.

>[!NOTE]
>
>If the subject line is empty, a warning is displayed in the message dashboard and in the Email Designer.

1. Create an email.
1. Go the **[!UICONTROL Properties]** tab of the Email Designer home page (accessible through the home icon).
1. Fill in the **[!UICONTROL Subject]** section.

    ![](assets/email_designer_subject.png)

1. You can also add personalization fields, content blocks and dynamic content to the subject line by clicking the corresponding icons. For more on this, see [Personalization](../../designing/using/personalization.md).

## Defining the email sender of an email {#email-sender}

To define the name of the sender which will appear in the header of messages sent, go the **[!UICONTROL Properties]** tab of the Email Designer home page (accessible through the home icon).

![](assets/delivery_content_edition16.png)

* The **[!UICONTROL From: name]** field allows you to enter the sender name. By default, the default **Sender name** block is automatically entered in the field. The default sender email address and sender name are  defined in **[!UICONTROL Brands]** accessible via the Adobe Campaign logo under the advanced menu **[!UICONTROL Administration > Instance settings > Brand configuration]** .

  You can change the sender name by clicking the **Sender name** block. The field then becomes editable and you can enter the name you would like to use.

  This field can be personalized. To do this, you can add personalization fields, content blocks and dynamic content by clicking the icons below the sender name. For more on this, see [Personalization](../../designing/using/personalization.md).

* The **[!UICONTROL From: email address]** field cannot be edited from this section. You can change it by editing the properties of the email from its dashboard. For more information, see [List of email advanced parameters](../../administration/using/configuring-email-channel.md#advanced-parameters).

>[!NOTE]
>
>The header parameters must not be empty. The sender's address is mandatory to allow an email to be sent (RFC standard). Adobe Campaign checks the syntax of email addresses entered.

**Related topics:**

* [Inserting a personalization field](../../designing/using/personalization.md#inserting-a-personalization-field)
* [Adding a content block](../../designing/using/personalization.md#adding-a-content-block)
* [Defining dynamic content in an email](../../designing/using/personalization.md#defining-dynamic-content-in-an-email)
