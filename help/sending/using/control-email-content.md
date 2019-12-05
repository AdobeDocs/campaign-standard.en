---
title: About deliverability in Adobe Campaign Standard
description: Learn about the concepts and best practices related to deliverability as well as the tools offered by Adobe Campaign Standard to optimize sending your deliveries.
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

# Control email content{#control-email-content}

To improve your email deliverability rate and make sure that your emails reach your recipients, the email must respect a certain number of rules:

* **Sender name and address**: The address has to explicitly identify the sender. The domain has to be owned by and registered to the sender. The domain registry must not be privatized.
* **Subject**: Avoid excessive capitalization and punctuation, and words that are frequently used by spammers ("Win", "Free", etc.).
* **Personalize your email**: Personalizing the email increases the chances of your message being opened.
* **Images and text**: Respect a decent text/image ratio (for example 60% text and 40% images).
* **Unsubscription link and landing page**: The unsubscription link is essential. It must be visible and valid, and the form must be functional.
* **Use tools** offered by Adobe Campaign to optimize the content of your email (delivery analysis, anti-spam analysis).

## Editing email content
Here is some additional information on editing email content. Don't forget to read the Message design best practices.

## Sender address
Certain ISPs check the validity of the sender address (From) before accepting messages. A badly formed address may result in it being rejected by the receiving server. You must make sure a correct address is given at the instance level or in the most frequently-used scenarios. Contact your administrator. See Personalizing the sender name and address.

![](assets/yyy.png)
  
## Predictive subject line
When editing an email, you can try out different subject lines and get an estimation of its open rate before you send it. Consult the documentation for more details.

![](assets/yyy.png)
  
## Send time optimization
To improve the success rate of your messages, you can manually define a sending time per recipient. Each profile will receive the message at the specified date and time, whenever possible.
Refer to the documentation for more information.

## Opt-out link and form
By default, when the message is analyzed, a typology rule checks whether an opt-out link has been included and generates a warning if it is missing.

You must check that the opt-out link works correctly before each time you send. For example, when sending the proof, make sure the link is valid, that the form is on-line and that validating this changes the value of the No longer contact boxes are checked. You should make this check systematically because human error is always possible when entering the link or when changing the form.

If a problem is detected concerning unsubscription after the delivery is started, it is still possible to perform an unsubscription manually (using the mass-update function, for example) for those recipients who click the opt-out link even if they were not able to confirm their choice.

As a general rule, do not try to get in the way of recipients who want to opt-out by requiring them to fill out fields such as their email address or name, for example. The unsubscription landing page should have one validation button only. Requesting additional confirmation is not reliable: a user may have two email addresses redirected to the same box (for example: firstname.lastname@club.com and firstname.lastname@internet-club.com). If the profile is able to remember the first address only and wishes to unsubscribe via a message sent to the other one, the form will refuse this because the encrypted identifier and the email address entered will not match.

## Anti-spam analysis
Adobe Campaign's message editor integrates an which allows you to score emails to determine whether a message runs the risk of being considered as spam by the anti-spam tools used upon receipt. Refer to the documentation for more information.
In the message content editor, click Preview. A message warns you if the anti-spam checking has detected a high risk for this message. Click Anti-spam analysis to view details.

![](assets/yyy.png)
  
## Checking the message responsiveness
You can check what your message is going to look like on different devices. Refer to the documentation for more information.
In the message content editor, click Preview and select a type of device in the top action bar.

![](assets/yyy.png)
  

>[!CAUTION]
>
>xxxxx.

the **[!UICONTROL zzzz]** 

![](assets/yyy.png)
