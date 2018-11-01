---
title: Importing data with import templates
seo-title: Importing data with import templates
description: Importing data with import templates
seo-description: 
uuid: e1e2e4fa-93b0-4f12-8c7f-93cad276f874
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/automating/using/importing-data-with-import-templates
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-25T09 29 58.480-0400
cq-lastreplicated: 2018-07-23T05 57 52.393-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: importing-and-exporting-data
cq-template: /apps/help/templates/article-3
discoiquuid: 081b87a9-fe77-40e1-93d1-dbb589882a2d
firstPublishExternalDate: 2018-07-23T05:57:52.301-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-04-05T07 29 31.766-0400
jcr-createdby: admin
jcr-description: Importing data with import templates
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T05:57:52.301-0400
lochandoffdate: 2018-07-25T09 29 58.480-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Importing data with import templates
publishexternaldate: 2018-07-23T05 57 52.301-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/automating/using/importing-data-with-import-templates.html
sha1: 10bc4938c7c8df43abfd473f2a872f5a4c125252
topicBrowsingSortDate: 2018-07-23T05:57:52.301-0400
index: y
internal: n
snippet: y
---

# Importing data with import templates

Importing data with import templates

Importing data allows you to collect data to feed your Campaign's database.

Alternatively to [Workflows](../../automating/using/discovering-workflows.md), Adobe Campaign offers a simplified import function that allows the user to manage certain types of import that were defined by an administrator.

The operating principle is as follows: an **administrator** defines and manages import templates (see [Defining import templates](../../automating/using/defining-import-templates.md)). These import templates are then made available to users with simplified views under the **Profiles & audiences** &gt; **Imports** menu.

These users therefore just have to select the type of import they want to carry out and upload the file with the data to import. The workflow defined by the administrator is executed transparently for the user, who can access the details of the result of the import once it has finished.

>[!NOTE]
>
>Import data function can be managed by users with **GENERIC IMPORT (import)** and **WORKFLOW (workflow)** roles. For more on roles, refer to [this section](../../administration/using/list-of-roles.md).

Imports can be filtered according to the template from which they were executed, their execution date, and their execution status.

1. From the imports overview, click the **Create** button. The wizard opens.
1. Select the type of import that you would like to carry out. The import types correspond to the available import templates.
1. If necessary, download the sample file linked to the template to your computer to view the data types expected in the file to be imported.
1. Download the file containing the data to import in the wizard.
1. Start the import. The wizard closes and takes you back to the list of imports carried out with the template used.
1. Refresh your page and select the import that you have just carried out to view the execution detail.

   ![](assets/simplified_import1.png)

The details of the import execution are now available. Both the file that was imported, as well as the file containing the rejected data (data that was not imported), can be downloaded to your computer.
