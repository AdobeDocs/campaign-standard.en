---
solution: Campaign Standard
product: campaign
title: Tracking messages
description: Learn how to track the behavior of your delivery recipients.
audience: sending
content-type: reference
topic-tags: sending-and-tracking-messages

feature: Performance Monitoring
role: Business Practitioner
level: Intermediate
exl-id: fac29bc2-57fa-40f9-a160-cd75f695b91e
---
# Tracking messages{#tracking-messages}

## About tracking {#about-tracking}

Thanks to its tracking functionalities, Adobe Campaign enables you to track the behavior of your delivery recipients. To do this, Adobe Campaign uses session cookies and permanent cookies.

You can inform users that your sites are equipped with web tracking tools via an authorization request (that comes up over the page, for example) with a checkbox to authorize the use of cookies, or add a banner at the top of the first page they land on, etc. Pop-up windows should be avoided as they are often blocked by browsers.

Tracking information are available for each contact of your database into **[!UICONTROL integrated customer profiles]**. For more on this, refer to [this section](../../audiences/using/integrated-customer-profile.md).

Adobe Campaign uses two types of cookies:

* A session cookie (nlid). This contains the identifier of the email sent to the contact (broadlogId) and the identifier of the message template (deliveryId). It is added when the contact clicks a URL included in an email sent by Adobe Campaign and enables you to track their behavior on the web. This session cookie is erased automatically when the browser is closed. The contact can configure their browser to refuse cookies.
* A cookie shared between Adobe Experience Cloud solutions. This enables you to identify the users who interact with the Experience Cloud solutions when they visit a website. The description of this cookie is available [here](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-mc.html).

Tracking with the Adobe Campaign Standard allows you to access to the following functionalities:

<table>
<tr>
    <td valign="top">
        <a href="../../administration/using/configuring-email-channel.md#tracking-parameters"><img width="60px" alt="conditions" src="assets/icon_email_parameters.png"/></a>
    </td>
    <td valign="top">
        <a href="https://helpx.adobe.com/campaign/kb/push-tracking.html"><img width="60px" alt="conditions" src="assets/icon_push_parameters.png"/></a>
    </td>
    <td valign="top">
        <a href="../../designing/using/links.md#about-tracked-urls"><img width="60px" alt="conditions" src="assets/icon_url.png"/></a>
    </td>
        <td valign="top">
          <a href="../../sending/using/tracking-messages.md#tracking-logs"><img width="60px" alt="conditions" src="assets/icon_log.png"/></a>
    </td>
    </td>
    <td valign="top">
          <a href="../../reporting/using/tracking-indicators.md"><img width="60px" alt="conditions" src="assets/icon_report.png"/></a>
</tr>
<tr>
<td>Email tracking</td>
<td>Push tracking</td>
<td>Tracked URLs</td>
<td>Tracking logs</td>
<td>Tracking report</td>
</tr>
</table>

## Tracking logs {#tracking-logs}

The **[!UICONTROL Tracking logs]** tab lists the tracking history for this delivery. This tab displays the tracking information for the sent messages, such as all the URLs which have been tracked by Adobe Campaign. Tracking information in this tab is updated every 10 minutes.

>[!NOTE]
>
>If tracking is not enabled for a delivery, this tab is not displayed. Tracking logs are available for the **email** and **push notification** channels only.

![](assets/tracking_logs.png)

In the example above, the recipient:

* Opened the message.
* Clicked on the mirror page link.
* Clicked on the "LEARN MORE" custom link.

In the **[!UICONTROL Type]** column, the possible values are:

* **[!UICONTROL Email click]**: the recipients clicked on a custom link.
* **[!UICONTROL Mirror page]**: the recipient clicked on a link to the mirror page.
* **[!UICONTROL Open]**: the recipient opened the email.
* **[!UICONTROL Opt-out]**: the recipient clicked on an unsubscription link.

>[!NOTE]
>
>For the **push notification** channel, only clicks on mobile notifications are tracked. In that case, the value will be **[!UICONTROL Click on mobile notification]**.

For more on how to insert tracking links, refer to [this page](../../designing/using/links.md#inserting-a-link).

The **[!UICONTROL Tracking indicators]** report contains the key indicators for tracking behavior after email messages are received. For more on this, refer to this [page](../../reporting/using/tracking-indicators.md).

## Tracked URLs {#tracked-urls}

The **[!UICONTROL Tracked URLs]** tab regroups the URLs contained in the sent message, including their URL type and their source URL.

![](assets/sending_delivery6.png)

For more on tracking links, refer to [this section](../../designing/using/links.md#about-tracked-urls).
