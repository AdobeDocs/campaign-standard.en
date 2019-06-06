---
title: Setting up image properties
seo-title: Setting up image properties
description: Setting up image properties
seo-description: See how to manage the properties of the images included in your content.
page-status-flag: never-activated
uuid: 1a439105-d9aa-4b30-a00d-bcf731a04e08
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: using-images
discoiquuid: 80c9c1a5-6050-443d-810a-6bb755d39dca

internal: n
snippet: y
---

# Setting up image properties{#setting-up-image-properties}

When you select a block that contains an image, the following properties are offered in the palette:

* **Enable personalization** allows you to customize the image source. See [Personalizing an image source](../../designing/using/personalizing-an-image-source.md).
* **Image Title** lets you define a title for the image.
* **Alt text** (email) or **Caption** (landing page) lets you define the caption linked to the image (corresponds to the **alt** HTML attribute).
* When editing an email, **Style** lets you specify the image size, background, and border.
* When editing a landing page, **Dimensions** lets you specify the image size in pixels.

The editor allows you to work with **all image types** whose formats are compatible with browsers. To be compatible with the editor, the **"Flash" type animations** have to be inserted in an HTML page as follows:

```

<object type="application/x-shockwave-flash" data="http://www.mydomain.com/flash/your_animation.swf" width="200" height="400">
 <param name="movie" value="http://www.mydomain.com/flash/your_animation.swf" />
 <param name="quality" value="high" />
 <param name="play" value="true"/>
 <param name="loop" value="true"/> 
</object>

```

