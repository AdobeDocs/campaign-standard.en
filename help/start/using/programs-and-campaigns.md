---
title: Programs and campaigns
seo-title: Programs and campaigns
description: Programs and campaigns
seo-description: In Adobe Campaign, programs and campaigns allow you to group and orchestrate the different marketing activities that are linked to them. Reports on programs and campaigns allow you to analyze their impact.
uuid: 5aa64b88-18de-4f3f-a68a-70851cc22de3
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/start/using/programs-and-campaigns
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-08T08 23 07.233-0400
cq-lastreplicated: 2018-09-07T15 08 20.356-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: start
content-type: reference
topic-tags: marketing-plans
cq-template: /apps/help/templates/article-3
discoiquuid: c1fb1401-6b08-4697-a11d-b0a81705e09f
firstPublishExternalDate: 2018-09-07T15:08:19.981-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 08.267-0400
jcr-createdby: admin
jcr-description: Programs and campaigns
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T15:08:19.981-0400
lochandoffdate: 2018-09-08T08 23 07.233-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
moreHelpPaths: /content/help/en/campaign/standard/start/morehelp/marketing-plans;/content/help/en/campaign/standard/start/morehelp/marketing-plans
navTitle: Programs and campaigns
publishexternaldate: 2018-09-07T15 08 19.981-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/start/using/programs-and-campaigns.html
sha1: 83a5d66d7c5c6f801c19cbfa00def9569fb6c0b6
topicBrowsingSortDate: 2018-09-07T15:08:19.981-0400
index: y
internal: n
snippet: y
---

# Programs and campaigns{#programs-and-campaigns}

Programs and campaigns

## About plans, programs and campaigns {#about-plans-programs-and-campaigns}

Adobe Campaign allows you to plan marketing campaigns in which you can create and manage different types of activities: emails, SMS messages, push notifications, workflows, landing pages. These campaigns and their contents can be gathered into programs.

The programs and campaigns allow you to regroup and view the different marketing activities that are linked to them.

* A **program** may contain other programs as well as campaigns, workflows, and landing pages. It appears in the timeline and help you organize your marketing activities: you can separate them by country, by brand, by unit, etc.
* A **campaign** enables you to gather all the marketing activities of your choice under a single entity. A campaign may contain emails, SMS, push notifications, direct mails, workflows, and landing pages.

To better organize your marketing plans, Adobe recommends the following hierarchy: Program > Sub-programs > Campaigns > Workflows > Deliveries.

Reports on programs and campaigns allow you to analyze their impact. For example, you can build reports at the campaign level to aggregate data on all deliveries contained in that campaign.

**Related topics:**

* [Timeline](../../start/using/timeline.md)
* [About dynamic reports](../../reporting/using/about-dynamic-reports.md)

## Creating a program {#creating-a-program}

The program is the first level of organization. It can contain sub-programs, campaigns, workflows or landing pages.

1. From the Adobe Campaign home page, select the **Programs & Campaigns** card.
1. Click on the **Create** button. 
1. In the **Creation mode** screen, select a program type.

   ![](assets/programs_and_campaigns_2.png)

   The program types available are based on templates defined in the **Resources** > **Templates** > **Program templates** section. For more on this, refer to the [Managing templates](../../start/using/about-templates.md) section.

1. In the **Properties** screen, enter the name and ID of the program.

   ![](assets/programs_and_campaigns_3.png)

1. Select a start and end date to your program. These dates only apply to the program itself.

   You can create your program within a parent program. To do this, select the parent program from the existing programs.

1. Click on **Create** to confirm the creation of the program.

The program is created and displayed. Use the **Create** button to add sub-programs, campaigns, workflows or landing pages.

>[!NOTE]
>
>You can also create a program from the list of marketing activities.

## Creating a campaign {#creating-a-campaign}

In programs and sub-programs, you can add campaigns. Campaigns can contain marketing activities such as emails, SMS, push notifications, workflows, and landing pages.

1. From the Adobe Campaign home page, select the **Programs & Campaigns** card and access a program or sub-program. 
1. Click on the **Create** button and select **Campaign**.
1. In the **Creation mode** screen, select a campaign type.

   ![](assets/programs_and_campaigns_7.png)

   The campaign types available are based on templates defined in **Resources** > **Templates** > **Campaign templates**. For more on this, refer to the [Managing templates](../../start/using/about-templates.md) section.

1. In the **Properties** screen, enter the name and ID of the campaign.
1. Select a start and end date to your campaign. These dates only apply to the campaign itself.

   ![](assets/programs_and_campaigns_8.png)

1. Click on **Create** to confirm the creation of the campaign.

The campaign is created and displayed. Use the **Create** button to add marketing activities to your campaign.

>[!NOTE]
>
>Depending on your license agreement, you may access only some of these activities.

You can also create a campaign from the marketing activity list. You can choose to link the marketing activity to a parent program or sub-program via the properties window of the campaign.

## Programs and campaigns icons and statuses {#programs-and-campaigns-icons-and-statuses}

Each program and each campaign in the list has a visual symbol and an icon whose color indicates the execution status. This status depends on the validity period of the program or the campaign.

* Gray: the program/campaign has not yet started - **Editing** status.
* Blue: the program/campaign is in progress - **In progress** status.
* Green: the program/campaign has finished - **Finished** status. By default, the current date is automatically shown as the validity start date and the end date is calculated according to the start date (**D+186 days**). You can change these dates in the program or campaign properties.

![](assets/programs_and_campaigns.png)

