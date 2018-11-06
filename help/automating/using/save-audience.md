---
title: Save audience
seo-title: Save audience
description: Save audience
seo-description: The Save audience activity allows you to update an existing audience or create a new audience from the population computed upstream in a workflow.
uuid: dd8d793d-9708-4cf0-a2b9-25a54157f383
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/automating/using/save-audience
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-25T09 29 29.572-0400
cq-lastreplicated: 2018-07-23T05 57 07.044-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: targeting-activities
cq-template: /apps/help/templates/article-3
discoiquuid: e1f5f227-51b3-4f13-930f-81c8d853e43f
firstPublishExternalDate: 2018-07-23T05:57:06.975-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 41.058-0400
jcr-createdby: admin
jcr-description: Save audience
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T05:57:06.975-0400
lochandoffdate: 2018-07-25T09 29 29.572-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Save audience
publishexternaldate: 2018-07-23T05 57 06.975-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/automating/using/save-audience.html
sha1: 4e2e82d197c42a3923ec25b00be5a9db3fe0d3fe
topicBrowsingSortDate: 2018-07-23T05:57:06.975-0400
index: y
internal: n
snippet: y
---

# Save audience

Save audience

## Description

![](assets/save_audience.png)

The **Save audience** activity allows you to update an existing audience or create a new audience from the population computed upstream in a workflow. The audiences created or updated from this activity are **List** or **File** audiences. They are added to the list of application audiences, and are made available via the **Audiences** menu.

This activity also allows you to export profiles as Adobe Experience Cloud audiences/segments. This then allows you to exploit these audiences in other Adobe Experience Cloud solutions. For more information about shared audiences, refer to [Working with Campaign and People Core Service](../../integrating/using/about-campaign-audience-manager-or-people-core-service-integration.md).

## Context of use

The **Save audience** activity is essentially used to keep population groups computed in the same workflow, by converting them into reusable audiences.

## Configuration

1. Drop a **Save audience** activity into your workflow.
1. Connect it after the other targeting activities such as a query, an intersection, a union, or an exclusion.
1. Select the activity, then open it using the  ![](assets/edit_darkgrey-24px.png)

   button from the quick actions that appear.
1. Select the action that you would like to carry out:

    * **Update an existing audience**: Select an existing audience and choose the type of update:

        * **Replace audience content with new data**: The whole of the audience content is replaced. The old data is lost. Only the data from the inbound transition of the save audience activity is kept.
        * **Complete audience with new data**: The old audience data is kept and the data from the save audience activity's inbound transition is added to it.

    * **Create then update an audience**: Enter the name of the audience and select the update type. If the audience does not already exist, then it is created. If it already exists, it is updated according the mode selected:

        * **Replace audience content with new data**: The whole of the audience content is replaced. The old data is lost. Only the data from the inbound transition of the save audience activity is kept.

          Warning, this option erases the audience type and the targeting dimension of the updated audience.
        
        * **Complete audience with new data**: The old audience data is kept and the data from the save audience activity's inbound transition is added to it.

          Warning, this option causes an error if the audience type or the targeting dimension of the audience updated are not compatible with the current configuration of the workflow. For example, you cannot complete a file type audience with profiles that come from a query.

    * **Create a new audience**: Enter the name of the audience to create. The time and date the audience is created will automatically be added to the audience name. This makes the audience unique every time the workflow is executed.
    * **Share in Adobe Experience Cloud**: If you have targeted profiles and you would like to export your audience to Adobe Experience Cloud, select this option, then select an existing shared audience or create a new audience.

      Also select a **Shared Data source** that corresponds to the resource of the data contained in the audience so that the data is correctly reconciled in Adobe Experience Cloud.

      Using this option, the shared audience is not added to the list of Adobe Campaign audiences available via the **Audiences** menu.

      >[!NOTE]
      >
      >This option is only available if the shared audiences functionality with Adobe Experience Cloud has been configured by your administrator. For more information, refer to [Working with Campaign and People Core Service](../../integrating/using/about-campaign-audience-manager-or-people-core-service-integration.md).

   The type of audiences saved or available during an update depends on the activities placed upstream in the workflow.

   If the targeting dimension of the audience is unknown when it is saved (for example if it is from an imported file), the audience is created or updated as a **File** type audience.

   If the targeting dimension of the saved audience is already defined when it is saved (for example, if it comes from a targeting, after a query, etc.), then the audience is saved or updated as a **List** type audience.

   The content of the saved audience is then available in the detail view of the audience, which can be accessed from the **Audiences** menu. The columns available from this view correspond to the columns of the inbound transition of the workflow's save audience activity. For example: the columns of the imported file, the additional data added from a query.

1. Confirm the configuration of your activity and save your workflow.

## Example

The workflow defined in this example shows a regular audience update from targeting:

* It is automatically executed once a month using a **Scheduler**.
* You can use a **Query** to recover all the profiles subscribed to the different application services available.
* The **Save audience** activity updates the audience by deleting profiles that have unsubscribed from the service since the last workflow execution and by adding the newly subscribed profiles.

![](assets/save_audience_example_1.png)

The **Save audience** activity is configured as follows:

![](assets/save_audience_example_2.png)

