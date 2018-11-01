---
title: Adding fragments and content components
seo-title: Adding fragments and content components
description: Adding fragments and content components
seo-description: Populate your email with customizable and reusable sets of content.
uuid: 6369a4bb-91de-449f-a606-4ee29fcc7e7c
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/designing/using/adding-fragments-and-content-components
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-06-25T08 45 19.863-0400
cq-lastreplicated: 2018-06-14T08 43 50.151-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: designing-email-content
cq-template: /apps/help/templates/article-3
discoiquuid: f9d1ae19-9955-4b21-9456-56156488c735
firstPublishExternalDate: 2018-06-14T08:43:50.129-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-27T07 29 04.860-0400
jcr-createdby: admin
jcr-description: Adding fragments and content components
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-06-14T08:43:50.129-0400
lochandoffdate: 2018-06-25T08 45 19.863-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Adding fragments and content components
publishexternaldate: 2018-06-14T08 43 50.129-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/designing/using/adding-fragments-and-content-components.html
sha1: 17d5138103f3bcddcddf7c39772dde7adb573f43
topicBrowsingSortDate: 2018-06-14T08:43:50.129-0400
index: y
internal: n
snippet: y
---

# Adding fragments and content components

Adding fragments and content components

After adding structure components to your email, you can define their content. To do that, you need to add content components or fragments inside each structure component.

There are two categories of content elements that you can use:

* **Fragments**: Reusable components with content already defined from a fragment template. By default, several fragments are already defined. You can save your own fragments by [creating your own templates](../../designing/using/adding-fragments-and-content-components.md#saving-a-content-fragment-for-reuse) and reuse them later in new emails.

  >[!NOTE]
  >
  >Fragments are locked by default when added to an email since they are based on a fragment template. You can break the synchronization with the template if you want to modify the fragment for a specific email, or you can perform your modification directly in the fragment template.

* **Content components**: raw, empty components that you can edit once placed in the email. It can be a simple text, an image, raw HTML, and so on.

## <p>Inserting elements into an email</p>

To define the content of your email, you can add default or customized content elements in the structure components you have placed beforehand.

1. Access the content elements by selecting the **+** icon on the left.
1. If you already know the label or part of the label of the element you want to add, you can search for it.

   ![](assets/email_designer_fragmentsearch.png)

1. Drag and drop a fragment or content component from the palette to a structure component of the email.

   ![](assets/email_designer_addfragment.png)

   Once an element is added to the email, it can be moved to other places in the email.

   ![](assets/email_designer_movefragment.png)

1. Edit the element to match the exact needs of this email. You can add text, links, images, and so on.

   Fragments are locked by default when added to an email since they are based on a fragment template. You can break the synchronization with the template if you want to modify the fragment for a specific email, or you can perform your modification directly in the fragment template.

1. Customize the style of the element. Refer to [Customizing the display and style of an element](../../designing/using/customizing-the-display-and-style-of-an-element.md).
1. Repeat this procedure for all elements you need to add to your email.

If a fragment template is modified, the change is automatically synchronized in the emails where it is used.

## <p>Saving a content fragment for reuse</p>

You can create your own content fragments to reuse later in other emails

1. Go to **Resources** > **Content templates & fragments** and click **Create**.
1. If you are offered a choice, choose to use the new email editor.
1. Click on the template title to access its properties.
1. Specify a recognizable label and select the following parameter to be able to find the fragment later in new emails:

    * **Content type**: 'Delivery'. Content fragments are only compatible with emails.
    * **HTML type**: 'Fragment'. Selecting 'Fragment' here indicates that the content created in this template is a fragment and will be utilized as such in future email contents.

   ![](assets/email_designer_createfragment.png)

1. If needed, define a thumbnail for the fragment. This thumbnail will be displayed next to the fragment's name when editing an email.

   Select the **Thumbnail** tab of the template properties. From this tab, you can select an image that will be used as thumbnail for the fragment.

   ![](assets/email_designer_createfragment_thumbnail.png)

1. Save the properties to return to the main editing area.
1. Define one fragment by adding a structural component and a default fragment that you can customize.
1. Once edited, save your fragment.

The fragment template can now be used in emails. It appears under the **Fragments** section of the editor's palette.

>[!NOTE]
>
>You cannot add personalization in the fragment template. You have to add personalization by editing the fragment directly in each email where it is used.

