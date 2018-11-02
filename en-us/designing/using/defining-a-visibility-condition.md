---
title: Defining a visibility condition
seo-title: Defining a visibility condition
description: Defining a visibility condition
seo-description: Make a web page element visible only if a certain condition is respected.
uuid: 6d058a32-094e-4943-a5a4-53bdaa509ba1
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/designing/using/defining-a-visibility-condition
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-26T02 53 58.463-0400
cq-lastreplicated: 2018-07-23T08 13 55.646-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: defining-conditional-content
cq-template: /apps/help/templates/article-3
discoiquuid: 4795b338-0be4-4fb1-86fb-35bca4f93453
firstPublishExternalDate: 2018-07-23T05:58:43.265-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 01 47.878-0400
jcr-createdby: admin
jcr-description: Defining a visibility condition
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T08:13:55.610-0400
lochandoffdate: 2018-07-26T02 53 58.463-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Defining a visibility condition
publishexternaldate: 2018-07-23T08 13 55.610-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/designing/using/defining-a-visibility-condition.html
sha1: c174b39248b3242acb7b9c45422d4d9de3867343
topicBrowsingSortDate: 2018-07-23T08:13:55.610-0400
index: y
internal: n
snippet: y
---

# Defining a visibility condition

Defining a visibility condition

You can specify a visibility condition on any element. It will only be visible if the condition is respected.

To add a visibility condition, select a block and enter the condition to be respected in the **Visibility condition** field of its settings.

This option is only available for the following elements: ADDRESS, BLOCKQUOTE, CENTER, DIR, DIV, DL, FIELDSET, FORM, H1, H2, H3, H4, H5, H6, NOSCRIPT, OL, P, PRE, UL, TR, TD.

Non-visible dynamic blocks like drop-down lists cannot be edited.

The expression editor is presented in the [Advanced expression editing](../../automating/using/editing-queries.md#about-query-editor) section.

![](assets/delivery_content_5.png)

These conditions adopt the XTK expression syntax (e.g. **context.profile.email !=''** or **context.profile.status='0'**). By default, all fields are visible.

>[!NOTE]
>
>A condition cannot be defined for a block that already contains a sub-element with a dynamic content or a block that already makes up a dynamic content.

