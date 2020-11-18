---
title: Editing plain text, HTML and mobile email formats
description: Discover the Plain text and HTML modes
page-status-flag: never-activated
uuid: 571ffc01-6e41-4501-9094-2f812b041a10
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: editing-email-content
discoiquuid: 39b86fda-7766-4e5f-ab48-bcc536ab66b3

---

# Editing plain text, HTML and mobile email formats {#plain-text-and-html-modes}

The Email Designer enables you to edit several rendering of your emails. You can generate a text version of your email, edit the HTML source of an email and design emails for mobile view.

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

## Designing emails for mobile rendering {#switching-to-mobile-view}

You can fine-tune the responsive design of an email by separately editing all style options for mobile display. For example, you can adapt margins and padding, use smaller or bigger font sizes, change buttons, or apply different background colors that will be specific to the mobile version of your email.

All style options are available in mobile view. The Email Designer style settings are presented previously on this page.

1. Create an email and start editing the content. For more on this, see [Designing an email content from scratch](../../designing/using/designing-from-scratch.md#designing-an-email-content-from-scratch).
1. To access the dedicated mobile view, select the **[!UICONTROL Switch to mobile view]** button.

   ![](assets/email_designer_mobile_view_switch.png)

   The mobile version of the email is displayed. It contains all the components and styles that were defined in desktop view.

1. Edit independently all style settings such as background color, alignment, padding, margin, font family, text color, and so on.

   ![](assets/email_designer_mobile_view.png)

1. When editing any style setting in mobile view, the modifications are only applied to the mobile display.

   For example, reduce the size of an image, add a green background and change the padding in mobile view.

   ![](assets/email_designer_mobile_view_change.png)

1. You can hide a component when displayed on a mobile device. To do this, select **[!UICONTROL Show only on desktop devices]** from the **[!UICONTROL Display options]**.

   You can also choose to hide this component on desktop devices, which means that it will be displayed on mobile devices only. To do this, select **[!UICONTROL Show only on mobile devices]**.

   For example, this option enables you to display a specific image on mobile devices and another image on desktop devices.

   You can either set this option from the mobile or desktop view.

   ![](assets/email_designer_mobile_hide.png)

1. Click again the **[!UICONTROL Switch to mobile view]** button to go back to the standard desktop view. The style changes you just made are not reflected.

   ![](assets/email_designer_mobile_view_desktop_no-change.png)

   >[!NOTE]
   >
   >The only exception is the **[!UICONTROL Style inline]** settings. Any style inline setting change is also applied to the standard desktop view.

1. Any other change to the structure or the content of the email such as text edits, uploading a new image, adding a new component, etc. is also applied to the standard view.

   For example, switch back to mobile view, edit some text and replace an image.

   ![](assets/email_designer_mobile_view_change_content.png)

1. Click again the **[!UICONTROL Switch to mobile view]** button to go back to the standard desktop view. The changes are reflected.

   ![](assets/email_designer_mobile_view_desktop_content-change.png)

1. Removing a style in mobile view takes you back to the style that was applied in desktop mode.

   For example, in mobile view, apply a green background color to a button.

   ![](assets/email_designer_mobile_view_background_mobile.png)

1. Switch to desktop view and apply a grey background to the same button.

   ![](assets/email_designer_mobile_view_background_desktop.png)

1. Switch again to mobile view, and now disable the **[!UICONTROL Background color]** setting.

   ![](assets/email_designer_mobile_view_background_mobile_disabled.png)

   The background color defined in desktop view is now applied: it turns grey (not blank).

   The only exception is the **[!UICONTROL Border color]** setting. When disabled in mobile view, no border is applied anymore, even if a border color is defined in desktop view.

>[!NOTE]
>
>The mobile view is not available in [fragments](../../designing/using/using-reusable-content.md#about-fragments).
