---
solution: Campaign Standard
product: campaign
title: Build personalized content
audience: delivery
content-type: reference
topic-tags: deliveries-best-practices
index: y
description: Learn how to design your message content and try to avoid common issues that could prevent you from executing your delivery. 
feature: Deliverability
role: Business Practitioner
level: Intermediate
exl-id: 938989c9-ef19-4297-9b8b-c38eb1cec1f0
---
# Build personalized content {#build-personalized-content}

When designing your message content, try to avoid common issues that could prevent you from executing your delivery. Most of the time, possible errors are related to [personalization](../../designing/using/personalization.md), formatting when [using an existing content](../../designing/using/using-existing-content.md) - and [converting an HTML content](../../designing/using/using-existing-content.md#converting-an-html-content) - and [images](../../designing/using/images.md).

## Optimize personalization {#optimize-personalization}

To avoid common issues that could prevent you from executing your delivery and to improve your recipients' experience, Adobe Campaign enables you to personalize your messages.

You can use recipients' data stored in the Adobe Campaign database, or collected through tracking, landing pages, subscriptions, etc.
Personalization basics are presented in [this section](../../designing/using/personalization.md).

Make sure your message content is properly designed to avoid any errors, which are generally related to personalization.

Dynamic content can be manually added to display different content to your recipients according to conditions defined in the expression editor. When adding dynamic content, you must always leave a default variant for recipients who do not meet the selected conditions.
For more on dynamic content, refer to the [this section](../../designing/using/personalization.md#defining-dynamic-content-in-an-email).

**Tips** - Preview your email with different test profiles to make sure that your dynamic content has been correctly configured.

## Build optimized content {#optimize-content}

When building your emails, keep the general best practices below in mind.

* Keep design simple

* Keep mobile users in mind

* Avoid entirely image-based emails

* Use email-safe fonts

* Encode special characters

### Subject line

Work on the [subject line](../../designing/using/subject-line.md) to improve open rates:

* Avoid subjects that are too long. Use 50 characters maximum

* Avoid using repetitively words like "free" or "offer", that could be considered as spam

* Avoid capital letters, and special characters like "!", "£", "€", "$"

### Mirror page

Always include a mirror page link. Preferred position is a the top of the email. [Learn more](../../designing/using/personalization.md#adding-a-content-block) 

### Unsubscription link

The unsubscription link is essential. It must be visible and valid, and the form must be functional. Learn unsubscription link guidelines [in this section](../../designing/using/personalization.md#about-targeting-dimension).

By default, when the message is analyzed, a control [typology rule](../../sending/using/control-rules.md) checks whether an opt-out link has been included and generates a warning if it is missing.

**Tip**: Because human error is always possible, check that the opt-out link works correctly before each time you send. For example, when sending the proof, make sure the link is valid, that the form is on-line and that the No longer contact this recipient field is changed to Yes.

Learn how to insert an opt-out link [in this section](../../designing/using/personalization.md#adding-a-content-block).

### Email size {#email-size}

To avoid performance or deliverability issues, the recommended maximum size of an email is about **35KB**.

To keep your email under the limit, consider the following:

* Remove redundant or unused styles

* Move some of the email content to a [landing page](../../channels/using/getting-started-with-landing-pages.md)

* Minify your code

Make sure to test any changes before the final sending.

In Adobe Campaign, the default maximum size of an email is set to **100MB**. <!--This limit enables to prevent any error that could indefinitely increase the size of an email, which can lead to a system crash.-->

If the limit is reached, the message that exceeds the limit will fail and an error message will be displayed in the delivery logs. The other messages of the same delivery will not be impacted. In that case, you must adapt the dynamic part of the email template or the content fragments used by the delivery. <!--If you need assistance, or if you have any question or request about the **[!UICONTROL Maximum message size]** option, reach out to your Adobe contact.-->

Adobe recommmends keeping the maximum message size default value. However, this value can be changed in the **[!UICONTROL Maximum message size]** option, through the **[!UICONTROL Administration]** > **[!UICONTROL Application settings]** > **[!UICONTROL Options]** menu, by [functional administrators](../../administration/using/users-management.md#functional-administrators) only.

>[!CAUTION]
>
>If you set this value to zero, no limit will be applied.

### SMS length

By default, the number of characters in an SMS meets the GSM (Global System for Mobile Communications) standards. SMS messages using GSM encoding are limited to 160 characters, or 153 characters per SMS for messages sent in multiple parts.

Transliteration consists of replacing one character of an SMS by another when that character is not taken into account by the GSM standard. Note that inserting personalization fields into the content of your SMS message may introduce characters that are not taken into account by the GSM encoding. You can authorize character transliteration by checking the corresponding box in the SMPP channel settings tab of the corresponding **[!UICONTROL External account]**. 
Learn more [in this section](../../administration/using/configuring-sms-channel.md#sms-encoding--length-and-transliteration).

**Tips**:

* To keep all of the characters in your SMS messages as they are, to not alter proper names for example, do not enable transliteration.

* However, if your SMS messages contain a lot of characters that are not taken into account by the GSM standard, enable transliteration to limit the costs of sending your messages.

Learn more [in this section](../../administration/using/configuring-sms-channel.md#sms-encoding--length-and-transliteration).

### Responsive email design

Responsive design ensures that an email renders optimally for the device on which it is opened. 

* Use responsive email HTML rather than web HTML

* Use the preview mode and send proofs to test the rendering on as much devices as possible. Learn how to [preview message](../../sending/using/previewing-messages.md) before sending.

* Campaign Email Designer comes with responsive design formatted templates for mobile. Learn more [in this page](../../designing/using/using-reusable-content.md#content-templates).

## Manage images {#manage-images}

Follow the guidelines below when it comes to using images.

### Prevent images blocking

Some email clients block images by default, and some users change their settings to block images for saving on data usage. Therefore, if images are not downloaded, the whole message can be lost. To avoid this:

* Balance your content with image and text. Avoid entirely image-based emails.

* If text must be contained in an image, use alt and title text to make sure your message gets across. Style your alt/title text to improve its appearance.

* Avoid the use of background images as they are not supported by some email clients.

### Make images responsive

Try to make images responsive and resizable. Note that this can have a cost impact as it takes longer to build.

### Use absolute image references

To be accessible from the outside, the images used in emails and public resources linked to campaigns must be present on an externally accessible server.

## Preview your message {#preview-msg}

Adobe recommends previewing your message to check its personalization and how your recipients will see your delivery. 

In the Email designer, the **[!UICONTROL Preview]** button lets you view the rendering of each content for a recipient. The personalization fields and the conditional elements of content are replaced with the corresponding information for the selected profile. [Learn more](../../sending/using/previewing-messages.md)
