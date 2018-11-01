---
title: Optional: Deleting a resource
seo-title: Optional: Deleting a resource
description: Optional: Deleting a resource
seo-description: 
uuid: 75406e46-1c76-4274-bcff-2058fee3797e
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/developing/using/optional--deleting-a-resource
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-26T02 53 34.828-0400
cq-lastreplicated: 2018-07-23T05 59 13.663-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: adding-or-extending-a-resource
cq-template: /apps/help/templates/article-3
discoiquuid: 7add1708-6e4e-4438-9a3d-75be9fff1c06
firstPublishExternalDate: 2018-07-23T05:59:13.617-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 01 54.573-0400
jcr-createdby: admin
jcr-description: Optional  Deleting a resource
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T05:59:13.617-0400
lochandoffdate: 2018-07-26T02 53 34.827-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Optional: Deleting a resource
publishexternaldate: 2018-07-23T05 59 13.617-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/developing/using/optional--deleting-a-resource.html
sha1: dcee49f363833cc56b4163b731d3d98b0f265db7
topicBrowsingSortDate: 2018-07-23T05:59:13.617-0400
index: y
internal: n
snippet: y
---

# Optional: Deleting a resource

Optional: Deleting a resource

To delete a resource, the resource in question must be a **Draft**. The resource is in **Draft** status if:

* It has just been created and has not yet been published.
* If it has already been published, the resource has to be re-drafted.

To re-draft a published resource:

1. Select the resource.
1. Click the **Re-draft** button in the action bar.
1. Click **Ok**.

   >[!CAUTION]
   >
   >This action is definitive: the resource's data will be deleted when the modification is published.

1. Publish the resource.

   The resource then goes into **Draft** mode and its activation status is **Inactive**.

1. In **List** mode, check the resource to delete then click the  ![](assets/delete_darkgrey-24px.png)

   icon.

Your resource is deleted from the data model.

>[!NOTE]
>
>If a field of a custom resource used on an event is modified or deleted, the corresponding event will automatically be unpublished. See [Configuring Transactional messaging](../../administration/using/configuring-transactional-messaging.md).

