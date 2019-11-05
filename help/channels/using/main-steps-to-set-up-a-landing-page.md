---
title: Main steps to set up a landing page
description: Learn the main steps to set up a landing page
page-status-flag: never-activated
uuid: b316bf47-7d98-46fa-ab4f-67ff50de8095
contentOwner: lemaitre
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: landing-pages
discoiquuid: ca8d1698-6e8a-4f5a-b017-74a152e14286
context-tags: landingPage,wizard;landingPage,overview;landingPage,main
internal: n
snippet: y
---

# Main steps to set up a landing page {#main-steps-create-a-landing-page}

## About landing page creation

The main steps when setting up landing pages are as follows:

![](assets/lp_steps.png)

In this page, you will find information on each of these steps, as well as references to the dedicated documentations for more details.

## Configure the landing page template {#configure-the-landing-page-template}

Before setting up a landing page, the first step is to configure a landing page template that corresponds to your needs. Once the template ready, all the landing pages based on it will be pre-configured with the desired parameters.

1. From the advanced menu, via the Adobe Campaign logo, select **[!UICONTROL Resources]** / **[!UICONTROL Templates]** / **[!UICONTROL Landing page templates]**, then duplicate the template that you want to use.
1. In the template properties, specify all of the parameters that your landing pages must have in common. For example: the targeting dimension, the page access parameters for identified or non-identified visitors, actions that are specific to form validation by a visitor, the brand/logo to use in the content, etc.
1. Save your modifications.

For more on landing page templates, refer to [this section](../../channels/using/about-landing-pages.md).

![](assets/lp-steps1.png)

## Create and configure the landing page {#create-and-configure-the-landing-page}

From the template defined in the previous step, create a new landing page in a program or campaign.

1. Create the landing page based on the desired template.
1. Enter the general parameters of the landing page (label, description, etc.).
1. You will then access the landing page dashboard. Edit the landing page properties, if necessary. By default, the properties are those configured in the landing page template.
    For security reasons and platform performances, we highly recommend that you set an expiration date in the landing page properties. Once done, the landing page will be automatically unpublished on the selected date. For more on validity parameters, refer to [this section](../../channels/using/sharing-a-landing-page.md#setting-up-validity-parameters).

    ![](assets/lp-steps3.png)

    >[!NOTE]
    >
    >Your modifications are only effective for the landing page that is being edited. If you want to apply these modifications to other landing pages, you can carry them out in a dedicated template and then create other landing pages from that template.

## Design the landing page {#design-the-landing-page}

You can now define the content of the landing page. By default, the landing page contains three pages that can be accessed via scrolling arrows: the main content page, a confirmation page, and an error page.

![](assets/lp-steps4.png)

Several fields are configured by default on each page. If necessary, you can edit their properties and mapping.

You can also configure the way the confirmation button will behave once a profile clicks on it, and personalize the content according to your needs (image, personalization fields, etc.). For example, you can insert a profile's first name on the confirmation page of the landing page, to thank them for registering.

For more on landing page design, refer to [this section](../../channels/using/designing-a-landing-page.md).

## Test the landing page {#test-the-landing-page}

Once the landing page is defined, you can simulate the way it will execute and behave when it is available online.

![](assets/lp-steps5.png)

>[!CAUTION]
>
>The landing page tests can only be carried out with profiles, and not with test profiles. When the form is being submitted, the selected profile's data will be updated for real. To avoid modifying real profiles, use a fake customer profile.

If you are satisfied with the way the landing page behaves, you can publish it to make it available online.

For more on how to test a landing page, refer to [this section](../../channels/using/sharing-a-landing-page.md#testing-the-landing-page-).

## Publish the landing page {#publish-the-landing-page}

Once the tests are successfull, you can publish the landing page using the **[!UICONTROL Publish]** button from the action bar in the dashboard. A monitoring block shows the progression and status of the publication.

Publishing the landing page makes it accessible online. Once published, you can always update it: to do this, you have to republish it after each modification. You can also unpublish a landing page at any time so that it is no longer available.

![](assets/lp-steps6.png)

Once published, your landing page is ready to be used. You can then put different mechanisms in place that allow you to access it to acquire new profiles in your database or to obtain additional information on existing profiles.

For more on landing page publishing, refer to [this section](../../channels/using/sharing-a-landing-page.md#publishing-a-landing-page).
