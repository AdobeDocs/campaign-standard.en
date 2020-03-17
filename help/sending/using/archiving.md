---
title: Archiving messages in Adobe Campaign Standard
description: Learn how to archive emails with Adobe Campaign Standard using a BCC email address.
page-status-flag: never-activated
uuid: c3721647-0663-4614-a9c9-3b3a40af328a
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: sending-and-tracking-messages
discoiquuid: 6fa50f0d-3dcf-4a9e-bccc-1ecda2bfb449

internal: n
snippet: y
---

# Archiving emails{#archiving-emails}

You can configure Adobe Campaign to keep a copy of emails sent from your platform.

If your organization needs to archive all outbound email messages for compliance, you can enable BCC emails. This capability sends a hidden copy of each email message to an email address you specify. Once enabled, the user can activate BCC from the 'Email archiving' / Archive emails option in their email template.

However, Adobe Campaign itself does not manage archived files. It does enable you to send the messages of your choice to a dedicated address, from where they can be processed and archived using an external system.

When activated in the delivery template, this feature allows you to send an exact copy of the corresponding sent messages to a BCC email address (invisible to the delivery recipients) that you must specify.

## Recommendations and limitations {#recommendations-and-limitations}

* This feature is optional. Please check your license agreement and contact your account executive to activate it.
* The BCC address of your choice must be provided to the Adobe team who will configure it for you.
* You can only use one BCC email address.
* Only successfully sent emails are taken in account. Bounces are not.
* For privacy reasons, BCC emails must be processed by an archiving system capable of storing securely personally identifiable information (PII).
* When creating a new delivery template, Email BCC is not enabled by default, even if the option has been purchased. You must enable it manually in each delivery template where you want to use it.

>[!NOTE]
>
>Currently the archived emails cannot be sent with the [Adobe Campaign Enhanced MTA](https://helpx.adobe.com/campaign/kb/campaign-enhanced-mta.html), even if you are already upgraded to the Enhanced MTA.

## Activating email archiving {#activating-email-archiving}

Email BCC is activated in the [email template](../../start/using/marketing-activity-templates.md), through a dedicated option:

1. Go to **Resources** > **Templates** > **Delivery templates**.
1. Duplicate the out-of-the-box **[!UICONTROL Send via email]** template.
1. Select the duplicated template.
1. Click the **[!UICONTROL Edit properties]** button to edit the template's properties.
1. Expand the **[!UICONTROL Send]** section.
1. Check the **[!UICONTROL Archive emails]** box to keep a copy of all sent messages for each delivery based on this template.

   ![](assets/email_archiving.png)

>[!NOTE]
>
>If the emails sent to the BCC address are opened and clicked through, this will be taken into account in the **[!UICONTROL Total opens]** and **[!UICONTROL Clicks]** from the send analysis, which could cause some miscalculations.