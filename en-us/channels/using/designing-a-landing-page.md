---
title: Designing a landing page
seo-title: Designing a landing page
description: Designing a landing page
seo-description: Follow these steps to design the content of a landing page and link it to a service.
uuid: 246a0606-78a9-481c-ae19-56a0f0ca5880
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/channels/using/designing-a-landing-page
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-30T04 54 12.259-0400
cq-lastreplicated: 2018-07-23T06 03 15.970-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: landing-pages
cq-template: /apps/help/templates/article-3
discoiquuid: 4b225cc1-99e7-465f-a6f0-00f97b3ab3f9
firstPublishExternalDate: 2018-07-23T06:03:15.928-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 28.480-0400
jcr-createdby: admin
jcr-description: Designing a landing page
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T06:03:15.928-0400
lochandoffdate: 2018-07-30T04 54 12.259-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Designing a landing page
publishexternaldate: 2018-07-23T06 03 15.928-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/channels/using/designing-a-landing-page.html
sha1: 932c0391ba4f0584f79ad9123108a322d9551f52
topicBrowsingSortDate: 2018-07-23T06:03:15.928-0400
index: y
internal: n
snippet: y
---

# Designing a landing page

Designing a landing page

## <p>About content design</p>

Landing pages are created as any other [marketing activity](../../start/using/marketing-activities.md#about-marketing-activities).

When designing a landing page, you need to define the content of:

* the page itself,
* the confirmation page,
* the error page.

Use the switcher under the action bar to display and configure each of these pages.

The content of these pages is designed through Campaign content editor. Refer to [Design content](../../designing/using/about-landing-page-content-design.md).

## <p>Mapping form fields</p>

Input fields are used to store or update data in Campaign database. For this, you need to link database fields with input zone, radio button, or checkbox type blocks. To do this:

1. Select a block in the landing page.
1. Complete the **Form data** part in the palette.

   ![](assets/editing_lp_content_4.png)

1. Choose a database field to link with the form field in the **Field** selection zone.

   When the **Mandatory** option is checked, the page can only be submitted if the user has completed this field. If a mandatory field is not completed, an error message will appear when the user validates the page.

   By default, landing pages are mapped with **Profiles**. You can modify the target mapping and select a different one via the **Edit properties** button in the action bar. This modification can be performed at the template level.

1. Define the field type by choosing, for example **Text**, **Number**, or **Date** in the **HTML type of the field** selection area.

>[!NOTE]
>
>The default fields of the out-of-box landing pages are preconfigured. You can modify them as needed.

## <p>Submitting the form</p>

You can select the action to perform when the visitor clicks the submit button. To do this:

1. Select the submit button of the landing page.
1. Select the action in the drop-down list in the left panel. Possible actions are: **Refresh** (to refresh the page) and **Next page** (to display the confirmation page).

   ![](assets/editing_lp_content_5.png)

In addition, you can change the label of the button or configure a specific link. To do this:

1. Select the submit button.
1. Click on the  ![](assets/lp_link_properties.png)

   button in the left panel.
1. Enter the label of the button, select the type of link, its properties, and the target.

   ![](assets/lp_link_custom.png)

## <p>Linking a form to a service</p>

You can link a form to a service so that profiles can subscribe to a specific service when validating the landing pages.

The parameters for linking a landing page allow you to specify the performed action type and whether the landing page is specifically linked to a single service or whether it is generic.

In order to select the service to link, you need to:

1. Edit the landing page properties accessed via the  ![](assets/edit_darkgrey-24px.png) icon in the landing page dashboard, and display the **Job** parameters.

   ![](assets/lp_edit_properties_button.png)

1. Choose **Subscription** in the **Specific actions** drop-down list.

   ![](assets/lp_parameters_5.png)

1. Select **Specific service** to link the landing page to a single service. Do not select this option if you would like to use several services with the landing page.

   Use the **Specified service in the URL** option to allow the landing page to be used for several services. You therefore must reference the landing page when configuring the service.

### <p>Confirm a landing page submission</p>

When a landing page is submitted by a visitor, you can configure the actions triggered. To do this:

1. Edit the landing page properties accessed via the  ![](assets/edit_darkgrey-24px.png) icon in the landing page dashboard, and display the **Job** parameters.

   ![](assets/lp_edit_properties_button.png)

1. Under the **Specific actions** section, select **Start sending message** to determine the sending of an automatic message, for example to confirm subscription to a service. You need then to select an email delivery template.

   Note that if a confirmation message is already configured at the service level, you should not select one in this screen to avoid sending multiple confirmation messages. Refer to [Configure a service](../../audiences/using/creating-a-service.md). 

1. Create **Additional data** to enable storing additional data when the landing page is being submitted. This data is not visible to people who visit the page. Only constant values are taken into account.

   ![](assets/lp_parameters_6.png)

## <p>Setting permissions and pre-loading data</p>

Access to a landing page can be restricted to identified visitors, who come from a link in a message sent by Campaign for example. In this case, you can preload their data in the landing page. To do this:

1. Edit the landing page properties accessed via the  ![](assets/edit_darkgrey-24px.png) icon in the landing page dashboard, and display the **Access & loading** parameters. 

   ![](assets/lp_edit_properties_button.png)

1. Select **Preload visitor data**.

   If a visitor to the page corresponds to a profile in the database, their data is displayed in the form's fields that are mapped with the database data and the landing page's personalization elements are taken into account.

   ![](assets/lp_parameters_3.png)

You can also:

* Use the URL parameters to identify the visitors, using the **Authorize visitor identification via URL parameters** option: then you must choose the loading key and map the filter parameters with the parameters of the corresponding URL.
* Authorize any visitor to access the landing page, using the **Authorize unidentified visitors** option.

