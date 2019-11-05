---
title: Plain text and HTML modes
description: Discover the Plain text and HTML modes
page-status-flag: never-activated
uuid: 571ffc01-6e41-4501-9094-2f812b041a10
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: editing-email-content
discoiquuid: 39b86fda-7766-4e5f-ab48-bcc536ab66b3

internal: n
snippet: y
---

# Plain text and HTML modes {#plain-text-and-html-modes}

## Generating a text version of the email {#generating-a-text-version-of-the-email}

By default, the **[!UICONTROL Plain text]** version of your email is automatically generated and synchronized with the **[!UICONTROL Edit]** version.

Personalization fields and content blocks added to the HTML version are also synchronized with the plain text version.

>[!NOTE]
>
>To use content blocks in plain text version, make sure they do not contain HTML code.

To have a plain text version different from the HTML version, you can disable this synchronization by clicking the **[!UICONTROL Sync with HTML]** switch from the **[!UICONTROL Plain text]** view of your email.

![](assets/email_designer_textversion.png)

You can then edit the plain text version as desired.

>[!NOTE]
>
>If you edit the **[!UICONTROL Plain text]** version while synchronization is disabled, the next time you enable the **[!UICONTROL Sync with HTML]** option, all the changes you made in the plain text version will be replaced with the HTML version. The changes made in **[!UICONTROL Plain text]** view cannot be reflected in **[!UICONTROL HTML]** view.

## Editing an email content source in HTML {#editing-an-email-content-source-in-html}

For the most advanced users and debugging, you can view and edit the email content directly in HTML.

You have two ways to edit the HTML version of the email:

* Select **[!UICONTROL Edit]** > **[!UICONTROL HTML]** to open the HTML version of the entire email.

  ![](assets/email_designer_html1.png)

* From the WYSIWYG interface, select an element and click the **[!UICONTROL Source code]** icon.

  Only the source of the selected element is displayed. You can edit the source code if the selected element is a **[!UICONTROL HTML]** content component. Other components are in read-only mode, but can still be edited in the full HTML version of the email.

  ![](assets/email_designer_html2.png)

If you modify the HTML the code, the responsiveness of the email could be broken. Make sure to test it using the **[!UICONTROL Preview]** button. See [Previewing messages](../../sending/using/previewing-messages.md).
