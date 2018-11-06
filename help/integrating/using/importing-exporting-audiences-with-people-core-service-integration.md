---
title: Importing/Exporting audiences with People core service integration
seo-title: Importing/Exporting audiences with People core service integration
description: Importing/Exporting audiences with People core service integration
seo-description: Learn how to import or export your audience within the different Adobe Marketing Cloud solutions.
page-status-flag: never-activated
uuid: 7c48d14d-8427-46c9-ac89-076af49d588e
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/integrating/using/importing-exporting-audiences-with-people-core-service-integration
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-01-10T15 24 11.241-0500
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: people-core-service-integration
cq-template: /apps/help/templates/article-3
discoiquuid: aa759768-e41f-4a39-b05d-d0d858e46e1e
firstPublishExternalDate: 2018-01-10T15:24:11.233-0500
herogradient: light
jcr-created: 2018-01-11T19 02 13.270-0500
jcr-createdby: admin
jcr-description: Importing/Exporting audiences with People core service integration
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-01-10T15:24:11.233-0500
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Importing/Exporting audiences with People core service integration
publishexternaldate: 2018-01-10T15 24 11.233-0500
publishExternalURL: https://helpx.adobe.com/campaign/standard/integrating/using/importing-exporting-audiences-with-people-core-service-integration.html
sha1: 1242cad9b96f603a561afbb7f2d320ddcece34e0
topicBrowsingSortDate: 2018-01-10T15:24:11.233-0500
index: y
internal: n
snippet: y
---

# Importing/Exporting audiences with People core service integration

Importing/Exporting audiences with People core service integration

## Importing an audience

People core service integration allows to directly import an audience into Adobe Campaign via a technical workflow to enrich your database.

Importing audiences/segments from People core service in Adobe Campaign can be carried out from the **Audiences** menu only by users connected via IMS (authentication via Adobe ID).

1. Go to the **Audiences** menu.
1. In the action bar, select **Create** to be taken to the screen to create an audience.
1. Specify the label of the new audience.
1. Set the audience **Type** to **Marketing Cloud** to indicate that the audience being created is an audience that was imported from People core service.
1. From the **Name of the shared audience** field, select the audience to import. Only segments can be imported. Granular data including key-value pairs, traits and rules are not supported.

   ![](assets/aam_import_audience.png)

1. Select the corresponding **AMC Data source**.

   If the selected data source is configured to use an encryption algorithm, an additional option offers you the possibility to **Force reconciliation with a profile**. Check this option if the **Channel** field of the data source is set to Email or Mobile (SMS) and if you want to leverage profile data.

   If you do not select the **Force reconciliation with a profile** and if **Channel** is set in AMC Data source to Email or Mobile (SMS) then all the encrypted declared IDs are decrypted. An audience of type **File** with a list of all the email addresses/mobile phone numbers is created/updated. This way, no email address/mobile phone number is lost while importing a shared audience through this integration, even if that profile does not exist in Campaign. Note that this type of audiences cannot be used directly as they need to be reconciled manually using workflows.

1. Confirm to create the audience.

   The audience is then imported via a technical workflow. It is composed of records of which the ID ('Visitor ID' or 'Declared ID') was able to be reconciled with the profile dimension. IDs from the People core service segments that are not recognized by Adobe Campaign are not imported.

Your audience is now imported in your Adobe Campaign database and are automatically synchronized over time. This synchronization can take up to 24 hours and will replace your audience data.

## Exporting an audience

An audience can be exported from Adobe Campaign to People core service using a workflow and the **Save audience** activity.

Exporting audience from Adobe Campaign to People core service can be carried out in a new workflow and only by users connected via IMS (authentication via Adobe ID).

1. Create a new workflow from a program, a campaign, or the list of marketing activities.
1. Using the different activities available, target a set of profiles.
1. After the targeting, drag and drop a **Save audience** activity into the workflow, then open it.
1. Check the **Share in Adobe Marketing Cloud** box.

   ![](assets/aam_save_audience_activity.png)

1. Specify the audience using the **Shared audience** field. In the window that opens, you have the choice of selecting an existing audience or creating a new audience:

    * If you select an existing audience, only the new records will be added to the audience.
    * To export your profile list into a new audience, complete the **Segment name** field then click **Create** before selecting the newly created audience.

   In order to be reconciled and exchanged, the records must have an Adobe Marketing Cloud ID ('Visitor ID' or 'Declared ID'). Non-reconciled records are ignored when importing and exporting audiences.

1. To finish, click the check mark located at the top right of the screen.
1. Select the corresponding **AMC Data source**.
1. If you like, check the **Generate an outbound transition** box to use the profiles that were exported. Only the profiles that can be reconciled are exported.
1. Confirm the activity's configuration and save your workflow.
1. Start your workflow to export your audience. Synchronization between Adobe Campaign and People core service can take several hours

Your audience is now available in your various Adobe Marketing Cloud solutions.

**Related topics:**

* [Workflows](../../automating/using/about-data-and-processes.md)
* [Audiences](../../audiences/using/about-audiences.md)

