---
title: Check before sending
audience: delivery
content-type: reference
topic-tags: deliveries-best-practices
index: y
description: "Once your message is ready, learn how to perform all checks before sending"
feature: Deliverability
role: User
level: Intermediate
exl-id: dfc5fc00-87aa-4d22-ad7c-cc0ba1ee21be
---
# Perform all checks before sending {#perform-all-checks}

Once your message is ready, make sure its content is displayed correctly, on all devices, and does not contain any errors such as wrong personalization or broken links.

Before sending your message, also ensure that the parameters and configuration are consistent with the delivery.

## Why validation is key {#validation-is-key}

Before sending a delivery, you need to ensure that your recipients will receive the message that you really want to send them. To do this, you need to validate the message content and delivery parameters.

This step enables you to detect possible errors and fix them before delivering to your main target.

The steps for validating a delivery are presented [in this section](../../sending/using/get-started-sending-messages.md#prepare-test-send).

## Email rendering {#email-rendering}

Before hitting the **[!UICONTROL Send]** button, make sure that your message will be displayed in an optimal way on a variety of web clients, web mails and devices.

To allow this, Adobe Campaign captures the rendering and makes it available in a dedicated report. This enables you to preview the sent message in the different contexts in which it may be received.

**Tips**:

* You can view the sent message in the different contexts in which it may be received: webmail, message service, mobile, etc.

* Email rendering capabilities are crucial to identifying whether your email campaigns successfully make it past the filters of major ISPs (Internet Service Providers) and webmail services. Such tools send a pre-flight copy of an email to a network of test inboxes, so you can see how the message will display, or render, across these services. They may also include reports and code correction options that help you quickly identify and make fixes that improve deliverability.

Learn more [in this section](../../sending/using/email-rendering.md).

## Proof messages {#proof-messages}

Sending proofs enables you to check the opt-out link, mirror page and any other links, validate the message, verify that images are displayed, detect possible errors, etc. You may also want to check your design and rendering on different devices.

Learn more [in this section](../../sending/using/sending-proofs.md).

## Set up A/B testing deliveries {#a-b-testing-deliveries}

If you have several contents for an email delivery, you can use A/B testing to find out which version will have the biggest impact on the targeted population.

**Tips**:

* Send the different versions to some of your recipients

* Select the one with the highest success rate and send it to the rest of your target

Learn more [in this section](../../channels/using/designing-an-a-b-test-email.md).
