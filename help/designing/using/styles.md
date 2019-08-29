---
title: Managing Styles
seo-title: Managing Styles
description: Managing Styles
seo-description: Discover how to manage email styles in the Email Designer.
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

# Managing Styles {#managing-styles}

## Editing email styles{#editing-email-styles}

## Editing an element {#editing-an-element}

In the Email Designer, when selecting an element, several options specific to the type of content selected are displayed in the **[!UICONTROL Settings]** pane. You can use these options to easily change the style of your email.

### Selecting an element {#selecting-an-element}

To select an element in the Email Designer interface, you can either:

* click directly in the email,
* or browse the structure tree available from the options located in the left **Palette**.

![](assets/des_tree_structure.png)

Browsing the structure tree enables you to make a more accurate selection. You can select either:

* the whole structure component,
* one of the columns that compose the structure component,
* or only a component that is located inside a column.

![](assets/des_tree_structure_selection.png)

To select a column, you can also do the following:

1. Select a structure component (directly in the email or using the structure tree available from the left **Palette**).
1. From the **contextual toolbar**, click **[!UICONTROL Select a column]** to choose the desired column.

See an example in [this section](../../designing/using/editing-email-styles.md#example--adjusting-vertical-alignment-and-padding).

### Adjusting style settings {#adjusting-style-settings}

1. Select an element in your email. For more on this, see [Selecting an element](../../designing/using/editing-email-styles.md#selecting-an-element).
1. Adjust the settings according to your needs. Each selected element offers a different set of settings.

   You can insert backgrounds, change sizes, modify horizontal or vertical alignment, manage colors, add [padding or margin](../../designing/using/editing-email-styles.md#about-padding-and-margin), and so on.

   To do this, use the options displayed in the **[!UICONTROL Settings]** pane or [add inline styling attributes](../../designing/using/editing-email-styles.md#adding-inline-styling-attributes).

   ![](assets/des_settings_pane.png)

1. Save your content.

### About padding and margin {#about-padding-and-margin}

The Email Designer interface allows you to quickly adjust padding and margin settings.

**[!UICONTROL Padding]**: this setting enables you to manage the space that is located inside an element's border.

![](assets/des_padding.png)

For example:

* Use padding to set margins on the left and right sides of an image.
* Use top and bottom padding to add more spacing to a **[!UICONTROL Text]** or a **[!UICONTROL Divider]** component.
* To set borders between columns inside a structure element, define padding for each column.

**[!UICONTROL Margin]**: this setting enables you to manage the space between the element's border and the next element.

![](assets/des_margin.png)

>[!NOTE]
>
>Depending on your selection (structure component, column or content component), the result will not be the same. Adobe recommends setting the **[!UICONTROL Padding]** and **[!UICONTROL Margin]** parameters at the column level.

For both **[!UICONTROL Padding]** and **[!UICONTROL Margin]**, click the lock icon to break synchronization between top and bottom or right and left parameters. This enables you to adjust each parameter separately.

![](assets/des_padding_lock_icon.png)

### About alignment {#about-alignment}

* **Text alignment**: place the cursor of your mouse on some text and use the contextual toolbar to align it.

  ![](assets/des_text_alignment.png)

* **Horizontal alignment** can be applied to text, images and buttons - currently not to the **[!UICONTROL Divider]** and **[!UICONTROL Social]** components.

  ![](assets/des_horizontal_alignment.png)

* To set **vertical alignment**, select a column inside a structure component and choose an option from the Settings pane.

  ![](assets/des_set_vertical_alignment.png)

### About backgrounds {#about-backgrounds}

When it comes to setting backgrounds with the Email Designer, Adobe recommends the following:

1. Apply a background color to the body of your email if required by your design.
1. In most cases, set background colors at the column level.
1. Try not to use background colors on image or text components as they are difficult to manage.

Below are the available background settings that you can use.

* Set a **[!UICONTROL Background color]** for the whole email. Make sure you select the body settings in the navigation tree accessible from the left Palette.

  ![](assets/des_background_body.png)

* Set the same background color for all structure components by selecting **[!UICONTROL Viewport background color]**. This option enables you to select a different setting from the background color.

  ![](assets/des_background_viewport.png)

* Set a different background color for each structure component. Select a structure in the navigation tree accessible from the left Palette to apply a specific background color only to that structure.

  ![](assets/des_background_structure.png)

  Make sure you do not set a viewport background color as it may hide the structure background colors.

* Set a **[!UICONTROL Background image]** for the content of a structure component.

  ![](assets/des_background_image.png)

  >[!NOTE]
  >
  >Some email programs do not support background images. Make sure you select an appropriate fallback background color in case the image cannot be displayed.

* Set a background color at the column level.

  ![](assets/des_background_column.png)

  >[!NOTE]
  >
  >This is the most common use case. Adobe recommends setting background colors at the column level as this allows for more flexibility when editing the whole email content.

  You can also set a background image at the column level, but this is rarely used.

#### Example: adjusting vertical alignment and padding {#example--adjusting-vertical-alignment-and-padding}

You want to adjust padding and vertical alignment inside a structure component composed of three columns. To do this, follow the steps below:

1. Select the structure component directly in the email or using the structure tree available from the left **Palette**.
1. From the **contextual toolbar**, click **[!UICONTROL Select a column]** and choose the one that you want to edit. You can also select it from the structure tree.

   ![](assets/des_selecting_column.png)

   The editable parameters for that column are displayed in the **[!UICONTROL Settings]** pane on the right.

1. Under **[!UICONTROL Vertical alignment]**, select **[!UICONTROL Up]**.

   ![](assets/des_vertical_alignment.png)

   The content component displays on top of the column.

1. Under **[!UICONTROL Padding]**, define the top padding inside the column. Click the lock icon to break synchronization with the bottom padding.

   Define the left and right padding for that column.

   ![](assets/des_adjusting_padding.png)

1. Proceed similarly to adjust the other columns' alignment and padding.

   ![](assets/des_adjusting_columns.png)

1. Save your changes.

### Adding inline styling attributes {#adding-inline-styling-attributes}

In the Email Designer interface, when you select an element and display its settings on the side panel, you can customize the inline attributes and their value for that specific element.

1. Select an element in your content.
1. On the side panel, look for the **[!UICONTROL Styles Inline]** settings.

   ![](assets/email_designer_inlineattributes.png)

1. Modify the values of the existing attributes, or add new ones using the **+** button. You can add any attribute and value that is CSS-compliant.

The styling is then applied to the selected element. If the child elements do not have specific styling attributes defined, the styling of the parent element is inherited.

## Switching to mobile view {#switching-to-mobile-view}

You can fine-tune the responsive design of an email by separately editing all style options for mobile display. For example, you can adapt margins and padding, use smaller or bigger font sizes, change buttons, or apply different background colors that will be specific to the mobile version of your email.

All style options are available in mobile view. The Email Designer style settings are presented in the [Editing email styles](../../designing/using/editing-email-styles.md) section.

1. Create an email and start editing the content. For more on this, see [Designing an email content from scratch](../../designing/using/about-email-content-design.md#designing-an-email-content-from-scratch).
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

   Click again the **[!UICONTROL Switch to mobile view]** button to go back to the standard desktop view. The changes are reflected.

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
