---
title: Editing email styles
seo-title: Editing email styles
description: Editing email styles
seo-description: Quickly edit the style of your email through the UI with easily accessible settings.
uuid: 08119d23-8c6a-4ec8-a44d-ef0661e7eeaa
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/designing/using/editing-email-styles
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-10T07 23 27.313-0400
cq-lastreplicated: 2018-09-07T14 48 45.013-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: editing-email-content
cq-template: /apps/help/templates/article-3
discoiquuid: 075afdc5-13d0-4667-bc3b-412c6a0cc9d2
firstPublishExternalDate: 2018-09-07T14:48:43.279-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-07-23T07 30 12.807-0400
jcr-createdby: admin
jcr-description: Editing email styles
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T14:48:43.279-0400
lochandoffdate: 2018-09-10T07 23 27.312-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Editing email styles
publishexternaldate: 2018-09-07T14 48 43.279-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/designing/using/editing-email-styles.html
sha1: 88c1a2e19ae1ce1d1b5dc704af3ccf1aa5561498
topicBrowsingSortDate: 2018-09-07T14:48:43.279-0400
index: y
internal: n
snippet: y
---

# Editing email styles{#editing-email-styles}

Editing email styles

## Editing an element with the Creative Designer {#editing-an-element-with-the-creative-designer}

In the Creative Designer, when selecting an element, several options specific to the type of content selected are displayed in the **Settings** pane. You can use these options to easily change the style of your email.

### Selecting an element {#selecting-an-element}

To select an element in the Creative Designer interface, you can either:

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
1. From the **contextual toolbar**, click **Select a column** to choose the desired column.

See an example in [this section](../../designing/using/editing-email-styles.md#example--adjusting-vertical-alignment-and-padding).

### Adjusting style settings {#adjusting-style-settings}

1. Select an element in your email. For more on this, see [this section](../../designing/using/editing-email-styles.md#selecting-an-element).
1. Adjust the settings according to your needs. Each selected element offers a different set of settings.

   You can insert backgrounds, change sizes, modify horizontal or vertical alignment, manage colors, add [padding or margin](../../designing/using/editing-email-styles.md#about-padding-and-margin), and so on.

   To do this, use the options displayed in the **Settings** pane or [add inline styling attributes](../../designing/using/editing-email-styles.md#adding-inline-styling-attributes-in-the-creative-designer).

   ![](assets/des_settings_pane.png)

1. Save your content.

### About padding and margin {#about-padding-and-margin}

The Creative Designer interface allows you to quickly adjust padding and margin settings.

**Padding**: this setting enables you to manage the space that is located inside an element's border.

![](assets/des_padding.png)

**Margin**: this setting enables you to manage the space between the element's border and the next element.

![](assets/des_margin.png)

>[!NOTE]
>
>Before adjusting **Padding** and **Margin**, make sure that you select the relevant element (structure component, column or content component) that you want to act upon. Depending on your selection, the result will not be the same.

For both **Padding** and **Margin**, click the lock icon to break synchronization between top and bottom or right and left parameters. This enables you to adjust each parameter separately.

![](assets/des_padding_lock_icon.png)

### Example: adjusting vertical alignment and padding {#example-adjusting-vertical-alignment-and-padding}

You want to adjust padding and vertical alignment inside a structure component composed of three columns. To do this, follow the steps below:

1. Select the structure component directly in the email or using the structure tree available from the left **Palette**.
1. From the **contextual toolbar**, click **Select a column** and choose the one that you want to edit. You can also select it from the structure tree.

   ![](assets/des_selecting_column.png)

   The editable parameters for that column are displayed in the **Settings** pane on the right.

1. Under **Vertical alignment**, select **Up**.

   ![](assets/des_vertical_alignment.png)

   The content component displays on top of the column.

1. Under **Padding**, define the top padding inside the column. Click the lock icon to break synchronization with the bottom padding.

   Define the left and right padding for that column.

   ![](assets/des_adjusting_padding.png)

1. Proceed similarly to adjust the other columns' alignment and padding.

   ![](assets/des_adjusting_columns.png)

1. Save your changes.

## Adding inline styling attributes in the Creative Designer {#adding-inline-styling-attributes-in-the-creative-designer}

In the Creative Designer interface, when you select an element and display its settings on the side panel, you can customize the inline attributes and their value for that specific element.

1. Select an element in your content.
1. On the side panel, look for the **Styles Inline** settings.

   ![](assets/email_designer_inlineattributes.png)

1. Modify the values of the existing attributes, or add new ones using the **+** button. You can add any attribute and value that is CSS-compliant.

The styling is then applied to the selected element. If the child elements do not have specific styling attributes defined, the styling of the parent element is inherited.

## Managing email style with the content editor {#managing-email-style-with-the-content-editor}

Customizing the style of an email within the content editor is similar to editing this element in a landing page. See [Managing landing page structure and style](../../designing/using/managing-landing-page-structure-and-style.md).
