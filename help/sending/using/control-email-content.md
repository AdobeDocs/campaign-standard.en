---
title: Controlling the email content in Adobe Campaign Standard
description: Learn how to improve deliverability in Adobe Campaign Standard when editing your email content.
page-status-flag: never-activated
uuid: 286fceee-65a9-4cb9-b205-9ce5d024675c
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: sheduling-messages
discoiquuid: 9c7fd670-bba9-4f3c-8cb1-87397a1acd27
context-tags: delivery,schedule,back
internal: n
snippet: y
---

# Controlling email content{#control-email-content}

To improve your email deliverability rate and make sure that your emails reach your recipients, the email must respect a certain number of rules.

* **Sender name and address**: The address has to explicitly identify the sender. The domain has to be owned by and registered to the sender. The domain registry must not be privatized.
* **Subject**: Avoid excessive capitalization and punctuation, and words that are frequently used by spammers ("Win", "Free", etc.).
* **Personalize your email**: Personalizing the email increases the chances of your message being opened.
* **Images and text**: Respect a decent text/image ratio (for example 60% text and 40% images).
* **Unsubscription link and landing page**: The unsubscription link is essential. It must be visible and valid, and the form must be functional.
* **Use tools** offered by Adobe Campaign to optimize the content of your email (delivery analysis, anti-spam analysis).

For additional information on editing email content, consult the [Email Designer overview](../../designing/using/designing-content-in-adobe-campaign.md) and the [Message design best practices](../../designing/using/overview.md#content-design-best-practices).

## Sender name and address {#sender-name}

Certain ISPs check the validity of the sender address (From) before accepting messages. A badly formed address may result in it being rejected by the receiving server. You must make sure a correct address is given at the instance level or in the most frequently-used scenarios. Contact your administrator.

![](assets/delivery_content_edition16.png)

For more on this, see [Personalizing the sender name](../../designing/using/personalization.md#personalizing-the-sender).
  
## Subject line {#subject-line}

When editing an email, you can try out different subject lines and get an estimation of its open rate before you send it. For more on this, see [Testing the subject line of an email](../../sending/using/testing-subject-line-email.md).

![](assets/predictive_subject_line_example.png)

For more on defining the subject line of an email, see [this section](../../designing/using/subject-line.md).
  
## Send time optimization {#send-time-optimization}

To improve the success rate of your messages, you can manually define a sending time per recipient. Each profile will receive the message at the specified date and time, whenever possible.

For more on this, see [Optimizing the sending time](../../sending/using/optimizing-the-sending-time.md).

## Opt-out link and form {#opt-out}
By default, when the message is analyzed, a typology rule checks whether an opt-out link has been included and generates a warning if it is missing.

You must check that the opt-out link works correctly before each time you send. For example, when sending the proof, make sure the link is valid, that the form is on-line and that validating this changes the value of the No longer contact boxes are checked. You should make this check systematically because human error is always possible when entering the link or when changing the form.

If a problem is detected concerning unsubscription after the delivery is started, it is still possible to perform an unsubscription manually (using the mass-update function, for example) for those recipients who click the opt-out link even if they were not able to confirm their choice.

As a general rule, do not try to get in the way of recipients who want to opt-out by requiring them to fill out fields such as their email address or name, for example. The unsubscription landing page should have one validation button only. Requesting additional confirmation is not reliable: a user may have two email addresses redirected to the same box (for example: firstname.lastname@club.com and firstname.lastname@internet-club.com). If the profile is able to remember the first address only and wishes to unsubscribe via a message sent to the other one, the form will refuse this because the encrypted identifier and the email address entered will not match.

## Anti-spam analysis {#anti-spam-analysis}

Adobe Campaign's message editor integrates an **Anti-spam analysis** which allows you to score emails to determine whether a message runs the risk of being considered as spam by the anti-spam tools used upon receipt. For more on this, see [Previewing messages](../../sending/using/previewing-messages.md).

In the message content editor, click **[!UICONTROL Preview]**. A message warns you if the anti-spam checking has detected a high risk for this message. Click **[!UICONTROL Anti-spam analysis]** to view details.

![](assets/sending_anti-spam_analysis.png)
  
## Checking the message responsiveness {#message-responsiveness}

You can check what your message is going to look like on different devices. To allow this, Adobe Campaign captures the rendering and makes it available in a dedicated report. This enables you to preview the sent message in the different contexts in which it may be received. For more on this, see [Email rendering](../../sending/using/email-rendering.md).

![](assets/inbox_rendering_report_3.png)
