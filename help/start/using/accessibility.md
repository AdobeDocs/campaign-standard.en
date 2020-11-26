---
solution: Campaign Standard
product: campaign
title: Accessibility in Email Designer
description: Learn about accessibility in Email Designer.
audience: designing
content-type: reference
topic-tags: editing-email-content

---

# Accessibility in Email Designer {#accessibility-email-designer}

A high level summary of the accessibility available in the product - typical topics include keyboard accessibility, headings, alt text for images, contrast, etc. No need to go into details (Release Notes will do that, most likely), but it's helpful to understand in layman's terms what the product provides for support
Any specific custom solutions (ex. shortcut keys) or "accessibility mode" type features that Campaign has implemented
Basic tasks and their respective accessibility support
Read on to know more about the various accessibility features in XD.


Overview

· Adobe’s commitment to accessibility and inclusivity

· Standards with reference to latest ACR

· Work done on [product] to date

· Supported user needs, assistive technologies, and OS/browser/AT combinations

Accessibility refers to making products usable for people with visual, auditory, motor, and other disabilities.

Examples of accessibility features for software products include contextual help, content assistant, support for screen readers and so on.

## Accessibility features · Keyboard accessibility

· Contrast

· Text equivalents

· Forms

· Discoverability

## Custom accessibility solutions for [product] · Navigation

· Keyboard shortcuts

· Datepickers

· Trees

· Carousels

· Cards

· Data visualizations

## Navigate Workspace using the keyboard

However, the email designer does not fully support keyboard accessibility

### Email designer

| Shortcut  |  Action |
|:-:|:-:|
| CTRL + Z  | Undo  |
| CTRL + Y  |  Redo |

### Homepage

| Shortcut  |  Action |
|:-:|:-:|
| Tab | Navigate through cards |
| Enter |  Select your card |

### Dynamic reports

| Shortcut  |  Action |
|:-:|:-:|
| CTRL + O | Open project |
| CTRL + S  |  Save |
| Shift + CTRL + S | Save as |
| Alt + R  | Refresh project |
| Shift + CTRL + V | Download CSV |
| Alt + P | Print |
| CTRL + Z | Undo |
|  CTRL + Shift + Z | Redo |
| Alt + B | New blank panel |
| Alt + A | New freeform |
| Alt + 1 | New freeform table |
| Alt + 2 | New line |
| Alt + 3 | New bar |
| Alt + S | Send report now |
| Shift + Alt + S | Send report on schedule |
| Shift = Alt + L | Scheduled reports |

## Create responsive resize for multiple devices

When designing for multiple devices and platforms, it's important to create a seamless experience for screen sizes across mobile and desktop resolutions. 

Work in your preferred language

## Contextual help

Description of the feature + doc link

## Content Assistant

When building a component, required fields are validated when you save. If a required field does not pass validation, it will be outlined in red with an error icon. A written description appears of the issue that needs to be fixed.

Once a component is fully validated, pressing Save closes the builder.

## Support for screen magnifiers

A screen reader reads text that appears on the computer screen. It also reads non-textual information, such as button labels or image descriptions in the application, provided in accessibility tags or attributes.

## Alternative texts for image buttons

The Alt text attribute lets you create alternate text that can be read in lieu of viewing an illustration.

## Work in your preferred language

It is available in English, French and German.

Please note that language is set up at the installation, and cannot be changed afterwards.

## Further Reading

Adobe Campaign Standard strives to provide an ever increasing degree of accessibility, making the product easy to use for everyone.

We encourage you to use the [Adobe Accessibility Feedback Form](https://www.adobe.com/accessibility/feedback.html) to send us improvement suggestions and accessibility issues that you run into. 

· [Product] user guide and general help documentation

· [Product] release roadmap (if available publicly)

· [Product] release notes (link to)

· Feedback (e.g. email address, form submission)



Contrast ratio
•	Workflow icons when focused
•	Ensure text and images of text provide sufficient contrast
•	Provide a valid label form field
•	Ensure parts of graphical objects essential for understanding content have sufficient contrast
•	Ensure active user interface components have sufficient contrast

Properties
•	Ensure the language of a document is set
•	Breadcrumb and missing headings
•	Ensure that instructive text is placed at the beginning of a form
•	Ensure data table headers cells are not blank
•	Provide text equivalent for object elements

UI
•	Ensure color is not the sole means of communicating information
•	Ensure shape and location are not the sole methods used to communicate information or hierarchy
•	Ensure custom controls provide proper textual name, role, and state information
•	Ensure that content and functionality is available when the user overrides text spacing properties
•	Provide alternative text for images
•	Ensure text can be resized
•	Ensure that content that appears on hover or focus may be dismissed by the user
•	Ensure containing elements allow text resize without loss of functionality.

UI controls
•	Update the "search" button's aria-label to reflect state
•	Improve the so-w-button widget's accessibility
•	Improve input widgets error state


Some examples of things you may want to include within your documentation would be: