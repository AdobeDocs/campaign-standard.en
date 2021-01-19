---
solution: Campaign Standard
product: campaign
title: About templates
description: "Adobe Campaign templates allow you to pre-configure parameters depending on your needs: templates may contain a full or partial configuration of the marketing activity, to simplify Adobe Campaign usage for non-technical end users."
audience: start
content-type: reference
topic-tags: managing-templates

---

# Marketing activity templates {#marketing-activity-templates}

## About templates {#about-templates}

When you create a new marketing activity, the first screen in the wizard asks you to select a type, or template. Templates allow you to pre-configure certain parameters according to your needs. The template may contain a full or partial configuration of the marketing activity. The template management is performed by the functional administrator.

The end user has a simplified interface. When creating a new marketing activity, you just need to select the template you would like to use. There is no need to worry about any technical configurations. This has already been pre-configured by the functional administrator in the template.

For example, in the case of an email template, you can pre-fill the HTML content, the audience, and any other parameter of your delivery: schedule, test profiles, your delivery's general properties, the advanced parameters, etc. This allows you to save time when creating a new activity.

![](assets/template_1.png)

For each type of marketing activity, one or several out-of-the-box templates are available with minimal configuration. These out-of-the-box templates cannot be modified or deleted.

Templates are available for the following marketing activities:

* Programs
* Campaigns
* Email deliveries
* SMS deliveries
* Push notifications
* Landing pages
* Workflows
* Services
* Import
* Transactional messages

## Creating a new template {#creating-a-new-template}

Message templates can be managed by the functional administrator of the platform, under the **[!UICONTROL Resources > Templates]** menu. Out-of-the-box templates cannot be modified or deleted. To create a new template, you must duplicate an existing one.

1. Select an existing template. In our example, we have chosen a **[!UICONTROL Delivery template]**.

   ![](assets/template_2.png)

1. Hover over it with the mouse, then select the **[!UICONTROL Duplicate element]** option.

   ![](assets/template_3.png)

1. Configure any settings you want, just like you would do when [creating a new marketing activity](../../start/using/marketing-activities.md#creating-a-marketing-activity) from scratch.

   ![](assets/template_4.png)

Created templates can then be selected by standard user in the first screen of the wizard while creating a marketing activity.

## Using a template {#using-a-template}

We are now going to look into how to use a template created in the earlier section.

>[!NOTE]
>
>Creating a marketing activity based on a template is generally carried out by a standard user type profile.

1. Create a new marketing activity.

   ![](assets/template_5.png)

1. In the first screen in the wizard, select the template that you would like to use.

   ![](assets/template_6.png)

   The marketing activity is pre-configured with the parameters defined in the template.

   ![](assets/template_7.png)
