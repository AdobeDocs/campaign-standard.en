---
title: About the Creative Designer
seo-title: About the Creative Designer
description: About the Creative Designer
seo-description: Learn about the main principles of the Creative Designer.
uuid: 56547bea-eb53-444f-9ee6-74e711432729
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/designing/using/about-the-creative-designer
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-06-25T08 45 16.031-0400
cq-lastreplicated: 2018-06-14T08 43 47.973-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: designing-email-content
cq-template: /apps/help/templates/article-3
discoiquuid: 5ef81b0d-ee34-4dc9-8708-9ab7ed3afa12
firstPublishExternalDate: 2018-06-14T08:43:47.942-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-27T07 29 04.617-0400
jcr-createdby: admin
jcr-description: About the Creative Designer
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-06-14T08:43:47.942-0400
lochandoffdate: 2018-06-25T08 45 16.031-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: About the Creative Designer
publishexternaldate: 2018-06-14T08 43 47.942-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/designing/using/about-the-creative-designer.html
sha1: b4a68b3ef025eeadd8a85d40f27f840f9f65788e
topicBrowsingSortDate: 2018-06-14T08:43:47.942-0400
index: y
internal: n
snippet: y
---

# About the Creative Designer

About the Creative Designer

>[!NOTE]
>
>The Creative Designer is currently in Beta mode. To use it, you have to agree with the Terms and Conditions displayed when selecting this editor in the interface.

The Creative Designer allows you to create email content and email content templates. It is compatible with simple emails, transactional emails, A/B test emails, multilingual emails, and recurring emails.

Check out this [introduction video](https://www.youtube.com/watch?time_continue=1&v=5S_6A4fsfms).

## Creative Designer interface

The Creative Designer offers many options that allow you to create, edit and customize every aspect of your content. Through a responsive layout, you can notice several areas containing different options:

![](assets/email_designer_overview.png)

From the elements available in the **Palette** (3), drag and drop structure components and content fragments in the main **Workspace** (1). Select a component or element in the **Workspace** (1) and customize its main styling and display characteristics from the **Settings** pane (2).

Access more general options and settings from the main **Toolbar** (4).

>[!NOTE]
>
>The different parts displayed in the above example can move according to your screen resolution and display.

## General recommendations

To make proper use of the Creative Designer and create the best emails as simply as possible, we recommend to apply the following principles:

* Use inline styling rather than a separate CSS and CSS at the beginning of the HTML. By using inline styling, you will be able to optimize content fragment save and reuse.
* Settle your branding easily by creating and reusing content fragments to keep consistency across your marketing campaigns.

Also check the [general best practices for email design](../../designing/using/design-best-practices.md).

## About compatibility mode

When you upload a content, it must contain specific tagging to be fully compliant and editable with the WYSIWYG editor of the Creative Designer. If all or part of the uploaded HTML is not compliant with the expected tagging, the content is then loaded in 'compatibility mode', which limits the edition possibilities through the UI.

When a content is loaded in compatibility mode, you can still perform the following modifications through the UI (unavailable actions are hidden):

* Changing the text or changing an image
* Inserting links and personalization fields
* Editing some styling parameters of a content fragment
* Defining conditional content.

>[!NOTE]
>
>Default content templates are not fully compatible with the Creative Designer. You can still use them in compatibility mode or create your own content templates from the Creative Designer.

Other modifications such as adding new sections to your email or advanced styling must be done directly in the source code of the email via the HTML mode.

![](assets/email_designer_compatibility.png)

