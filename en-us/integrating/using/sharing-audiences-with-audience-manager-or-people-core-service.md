---
title: Sharing audiences with Audience Manager or People core service
seo-title: Sharing audiences with Audience Manager or People core service
description: Sharing audiences with Audience Manager or People core service
seo-description: Learn how to import or export your audience within the different Adobe Experience Cloud solutions.
uuid: 86e3604d-c545-4edd-adc6-da79e939749b
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/integrating/using/sharing-audiences-with-audience-manager-or-people-core-service
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-27T03 26 56.787-0400
cq-lastreplicated: 2018-07-23T05 59 42.797-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-audience-manager-or-people-core-service
cq-template: /apps/help/templates/article-3
discoiquuid: 524aadb6-93c4-4237-a2e2-50db5d3566bf
firstPublishExternalDate: 2018-07-23T05:59:42.748-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 21.971-0400
jcr-createdby: admin
jcr-description: Sharing audiences with Audience Manager or People core service
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T05:59:42.748-0400
lochandoffdate: 2018-07-27T03 26 56.786-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Sharing audiences with Audience Manager or People core service
publishexternaldate: 2018-07-23T05 59 42.748-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/integrating/using/sharing-audiences-with-audience-manager-or-people-core-service.html
sha1: a5141a55780b14ed89caa38d94c11131143dc7f5
topicBrowsingSortDate: 2018-07-23T05:59:42.748-0400
index: y
internal: n
snippet: y
---

# Sharing audiences with Audience Manager or People core service

Sharing audiences with Audience Manager or People core service

## <p>Importing an audience</p>

People core service integration allows to directly import an audience into Adobe Campaign via a technical workflow to enrich your database. For more information on audience sharing in People core service, refer to this [documentation](https://marketing.adobe.com/resources/help/en_US/mcloud/t_publish_audience_segment.html).

Importing audiences/segments from People core service in Adobe Campaign can be carried out from the **Audiences** menu only by users connected via IMS (authentication via Adobe ID).

1. Go to the **Audiences** menu.
1. In the action bar, select **Create** to be taken to the screen to create an audience.
1. Specify the label of the new audience.
1. Set the audience **Type** to **Experience Cloud** to indicate that the audience being created is an audience that was imported from People core service.
1. From the **Name of the shared audience** field, select the audience to import. Only segments can be imported. Granular data including key-value pairs, traits and rules are not supported.

   ![](assets/aam_import_audience.png)

1. Select the corresponding **Shared Data Source**.

   If the selected data source is configured to use an encryption algorithm, an additional option offers you the possibility to **Force reconciliation with a profile**. Check this option if the **Channel** field of the data source is set to Email or Mobile (SMS) and if you want to leverage profile data.

   If you do not select the **Force reconciliation with a profile** and if **Channel** is set in AMC Data source to Email or Mobile (SMS) then all the encrypted declared IDs are decrypted. An audience of type **File** with a list of all the email addresses/mobile phone numbers is created/updated. This way, no email address/mobile phone number is lost while importing a shared audience through this integration, even if that profile does not exist in Campaign. Note that this type of audiences cannot be used directly as they need to be reconciled manually using workflows.

1. Confirm to create the audience.

   The audience is then imported via a technical workflow. It is composed of records of which the ID ('Visitor ID' or 'Declared ID') was able to be reconciled with the profile dimension. IDs from the People core service segments that are not recognized by Adobe Campaign are not imported.

Your audience is now imported in your Adobe Campaign database. The import process takes 24-36 hours to synchronize, when segments are imported directly from People core service or Audience Manager. After this period, you will be able to find and use your new audience in Adobe Campaign.

>[!NOTE]
>
>If you are importing audiences from Adobe Analytics to Adobe Campaign, these audiences need to first be shared in People Core Service or Audience Manager. This process takes 12-24 hours, which must be added to the 24-36 hours synchronization with Campaign. In that specific case, audience sharing timeframe can be up to 60 hours. For more information on Adobe Analytics audience sharing in People Core service and Audience manager, refer to this [documentation](https://marketing.adobe.com/resources/help/en_US/mcloud/t_publish_audience_segment.html).

## <p>Exporting an audience</p>

An audience can be exported from Adobe Campaign to Audience Manager or People core service using a workflow and the **Save audience** activity.

It can be carried out in a new workflow and only by users connected via IMS (authentication via Adobe ID).

1. Create a new workflow from a program, a campaign, or the list of marketing activities.
1. Using the different activities available, target a set of profiles.
1. After the targeting, drag and drop a **Save audience** activity into the workflow, then open it.
1. Select **Share in Adobe Experience Cloud**.

   ![](assets/aam_save_audience_activity.png)

1. Specify the audience using the **Shared audience** field. In the window that opens, you have the choice of selecting an existing audience or creating a new audience:

    * If you select an existing audience, only the new records will be added to the audience.
    * To export your profile list into a new audience, complete the **Segment name** field then click **Create** before selecting the newly created audience.

   ![](assets/aam_save_audience_segment_picker.png)

   In order to be reconciled and exchanged, the records must have an Adobe Experience Cloud ID ('Visitor ID' or 'Declared ID'). Non-reconciled records are ignored when importing and exporting audiences.

1. To finish, click the check mark located at the top right of the screen.
1. Select the corresponding **Shared Data Source**.
1. If you like, check the **Generate an outbound transition** box to use the profiles that were exported. Only the profiles that can be reconciled are exported.
1. Confirm the activity's configuration and save your workflow.
1. Start your workflow to export your audience. Synchronization between Adobe Campaign and People core service can take several hours

Synchronization between Adobe Campaign and People core service takes 24-36 hours. After this period, you will be able to find your new audience in People core service and reuse it in other Adobe Experience Cloud solutions. For more information on using an Adobe Campaign shared audience in Adobe People core service, refer to this [documentation](https://marketing.adobe.com/resources/help/en_US/mcloud/t_audience_create.html).

**Related topics:**

* [Workflows](../../automating/using/about-data-and-processes.md)
* [Audiences](../../audiences/using/about-audiences.md)

