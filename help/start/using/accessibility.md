---
title: Accessibility in Adobe Campaign Standard
description: Learn about accessibility support in Adobe Campaign Standard Workspace.
audience: designing
content-type: reference
topic-tags: accessibility

feature: Campaigns
role: User
level: Intermediate
exl-id: 958f7beb-ab41-4492-bc0a-e9e342e3c12e
---
# Accessibility in Adobe Campaign Standard {#accessibility-acs}

Learn about accessibility support in Adobe Campaign Standard Workspace.

Accessibility refers to making products usable for people with visual, auditory, cognitive, motor, and other disabilities. Examples of accessibility features for software products include semantically structured content, screen reader support, text equivalents for graphics, keyboard shortcuts, and so on.

Adobe Campaign Standard provides features that make it more accessible to use such as contrast, labels, structured content, keyboard navigation and contextual help.

## Accessibility features {#accessibility-features}

### Contrast and color {#contrast}

The Adobe Campaign Standard user interface strives to provide enough contrast in the application to ensure an accessible viewing experience for users with low vision or color deficiencies.

* Large text and headings have been enhanced to meet a 3:1 contrast ratio.

    ![](assets/accessibility_2.png)

* Help content and body text in the application have been updated to meet a 4.5:1 contrast ratio.

* Workflows' pause and cancel icons have been updated to improve the contrast between background and foreground colors.

    ![](assets/accessibility_1.png)

* Color, shape and location are not the sole methods used to communicate information or hierarchy in the application.

### User interface {#user-interface}

The Adobe Campaign Standard user interface makes it easier for all users to interact with content by adding alternative texts to visual elements and by using semantic structure to convey information both visually and programmatically.

* When the user leaves a required ID field blank, a graphic indicates visually which field is in error with error message text and that same information is conveyed programmatically to users with assistive technologies like screen readers.

    ![](assets/accessibility_3.png)

* Content that appears on hover or focus can be dismissed by the user and does not obscure other content.

    ![](assets/accessibility_4.png)

* Alternative texts for image and accessible names for buttons have been added and can be read aloud with assistive technology instead of relying solely on visual cues for identifying elements.

<!--
### Create responsive resize for multiple devices {#resize-devices}

When designing for multiple devices and platforms, it's important to create a seamless experience for screen sizes across mobile and desktop resolutions.

Adobe Campaign Standard allows you to design and test emails and push notifications on different devices such as: iPhone, Android devices, iPad, Android tablet and desktop.

![](assets/accessibility_6.png)
-->

## Contextual help {#contextual-help}

Contextual help can help you better understand the different requested fields and features available. It also guides you through product documentation to learn more information on the selected feature.

When designing an email, you can access a tooltip which will provide features descriptions and links to the product documentation.

![](assets/accessibility_7.png)

## Support for assistive technology {#screen-magnifiers}

We strive to make the Adobe Campaign Standard application as usable as possible by various assistive technologies, including but not limited to modified keyboards, screen magnifying software, screen readers, voice recognition software, and other assistive devices.

## Work in your preferred language {#languages}

Adobe Campaign Standard is available in different languages: English, French and German.

Please note that language is set up at installation, and cannot be changed afterwards.

## Keyboard shortcuts {#shortcuts}

### Homepage {#homepage-shortcuts}

|  Action | Shortcut |
| --- | --- |
| Navigate through individual elements of the user interface| Tab |
| Activate the selected item | Enter or Spacebar |

### Email designer {#email-designer-shortcuts}

|  Action | Windows shortcut | macOS shortcut |
| --- | --- | --- |
| Undo  | Ctrl + Z | Command + Z |
| Redo | Ctrl + Y  | Shift + Command + Z |

### Dynamic reports {#report-shortcuts}

|  Action | Windows shortcut | macOS shortcut |
| --- | --- | --- |
| Open a project | Ctrl + O | Command + O |
| Save | Ctrl + S  | Command + S |
| Save as | Shift + Ctrl + S | Shift + Command + S |
| Refresh project | Alt + R  | Command + R |
| Download CSV file | Shift + Ctrl + V | Shift + Command + V |
| Print | Alt + P | Command + P |
| Undo  | Ctrl + Z | Command + Z |
| Redo | Ctrl + Y  | Shift + Command + Z |
| New blank panel | Alt + B | Option + B |
| New freeform | Alt + A | Option + A |
| New freeform table | Alt + 1 | Option + 1 |
| New line | Alt + 2 | Option + 2 |
| New bar | Alt + 3 | Option + 3 |
| Send report now | Alt + S | Option + S |
| Send report on schedule | Shift + Alt + S | Shift + Option + S |
| Scheduled reports | Shift + Alt + L |<!-- Should be 'Shift + Option + L ' but does not work on Mac -->|

## Further Reading {#further-reading}

Adobe Campaign Standard strives to provide an ever-increasing degree of accessibility, making the product easy to use for everyone.

We encourage you to use the [Adobe Accessibility Feedback Form](https://www.adobe.com/accessibility/feedback.html) to send us improvement suggestions and accessibility issues that you run into.

You can also refer to [Adobe Campaign Standard release notes](https://experienceleague.adobe.com/docs/campaign-standard/using/release-notes/release-notes.html?lang=en#release-notes) to follow the latest improvements and features.
