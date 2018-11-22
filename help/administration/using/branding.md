---
title: Branding
seo-title: Branding
description: Branding
seo-description: Discover all the tools available to manage your branding identities.
page-status-flag: never-activated
uuid: 4edd4c70-73fb-4719-a218-c981e91c662b
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/administration/using/branding
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: application-settings
discoiquuid: 074214f9-8758-48ee-9fb1-726e94c2f111
isreadyforlocalization: false
navTitle: Branding
publishexternaldate: 2018-11-20
sha1: 06ad8d8c1f46af380dd2542ffeddcab3b0601dce
index: y
internal: n
snippet: y
---

# Branding{#branding}

Branding

Technical administrators can define one or several brands to centrally enter the parameters that affect a brand's identity. This can include the brand logo, technical parameters such as the domain of the landing pages' access URL, as well as managing message tracking. Thus, Adobe Campaign allows you to create these brands and link them to delivery or landing page templates.

The main principle of configuring and using brands is to:

1. Create and configure the brand - this operation is carried out by the Adobe Campaign technical administrator.
1. Create one or several delivery and landing page templates for this brand. Refer to the [Creating a template](../../start/using/about-templates.md) section.
1. Create deliveries and landing pages based on this template. Refer to the [Creating an email](../../channels/using/creating-an-email.md) and [Creating a landing page](../../channels/using/designing-a-landing-page.md) sections.

Brands can be found in the **Administration > Instance settings > Brand configuration** menu.

By default, a newly created brand is visible only to users assigned with the corresponding rights by the administrator.

A **Brand** is defined by the following characteristics:

* An **Identity**, which defines and personalizes your brand. This section contains the following fields:

  ![](assets/branding_01.png)

    * **Label** visible in the interface
    * **Brand name**
    * **Website URL** and **Website label** of the brand
    * **Brand logo**

* **Header parameters of sent emails** which personalizes what the recipients of your campaigns will see. This section contains the following fields:

  ![](assets/branding_04_header.png)

    * **Sender (email address)** with the brand's email address.
    * **Sender (name)** with the brand's name.
    * **Reply to (email address)** with the email address the customer can reply to.
    * **Reply to (name)** with the brand's name.
    * **Error (email address)** with the email address to use in case of an error.

  >[!CAUTION]
  >
  >If, after having updated the header parameters of the emails, the name and email address of the sender have not changed in the email created from the template, check the template's advanced settings.

* **Server(s) exposed on the internet** defines the servers used for tracking but also for landing page access. This section contains the following fields:

  ![](assets/configure_branding_04.png)

    * **External URL of the application server** used for hosting and accessing the different landing pages you create.
    * **External URL of the tracking server** used as the tracked URL during the deliveries.
    * **External URL of the mirror page server** used as the default mirror page in your deliveries.

* **Tracking URL configuration (Web Analytics)**, which defines the configuration of the URLs tracking for your brand.

  The additional parameters that allow the links to be tracked on external systems such as Web Analytics tools like Adobe Analytics or Google Analytics are defined here.

  ![](assets/branding_05.png)

## Assigning a brand to an email {#assigning-a-brand-to-an-email}

Brands are created and configured by the Adobe Campaign technical administrator.

### Linking a brand to a template {#linking-a-brand-to-a-template}

To use the parameters defined for a brand, it must be linked to a delivery or landing page template. To do this, you have to create or edit a template.

>[!NOTE]
>
>For more information about creating a template, refer to the [Creating a template](../../start/using/about-templates.md) section.

Once your template has been created, you can link it to a brand. To do this:

1. Click the **Edit properties** button to access the template properties.

   ![](assets/branding_04.png)

1. Use the drop-down list to select the brand that you want to link to the template.

   >[!NOTE]
   >
   >By default, the **Default brand (branding)** is selected.

   ![](assets/branding_05.png)

   To view how the brand selected is configured, click the **Navigate to the detail of the element selected** icon.

   ![](assets/branding_06.png)

1. Confirm your selection and save your template.

Your template is linked to the brand. In the content editor, the elements such as the **Email address of default sender**, the **Default sender name**, or the **Logo** will use the configured brand data.

### Example of a brand linked to an email template {#example-of-a-brand-linked-to-an-email-template}

In this example, we are going to create a new travel-related brand, and use it in an email.

The Adobe Campaign administrator creates the brand in **Administration > Instance settings > Brand configuration**. He adds the **Vacations in the Tropics** element from the advanced menu and configures the **ID** and the **Header parameters of sent emails** of the brand.

![](assets/branding_07.png)

The administrator then configures the URL of the **Server(s) exposed on the Internet** so that landing pages can be used, then the tracking URLs.

In this example, the **Web Analytics** tool used is **Google Analytics**. The administrator configures the tracking URL as follows:

![](assets/branding_12.png)

The brand is correctly created and configured. It can now be used by the marketing teams.

A delivery manager who is part of the aforementioned units, is in charge of creating the delivery templates that use the brand. In the advanced menu **Resources > Templates > Delivery templates**, the delivery manager duplicates an out-of-the-box template to configure a new delivery template.

![](assets/branding_08.png)

To link this template to the **Vacations in the Tropics** brand, he edits the template properties and selects the brand from the drop-down list. 

![](assets/branding_09.png)

The delivery manager configures his email template according to his needs.

Once the template is completed, he can save it.

![](assets/branding_10.png)

The delivery template can now be used to create emails that will be sent to an audience.

To create an email linked to a brand, select the **Create** button from the **Marketing activities** menu.

![](assets/branding_14.png)

Select the **Email** activity, then choose the template linked to the brand.

![](assets/branding_15.png)

Your email is already configured. You can check the information before testing it using the test profiles, then sending it to your audience.

![](assets/branding_16.png)

