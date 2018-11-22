---
title: Using workflow data
seo-title: Using workflow data
description: Using workflow data
seo-description: Learn the different possibilities to consume the data you imported or targeted.
page-status-flag: never-activated
uuid: 3d3237d5-ef7e-4f33-8141-fc6c98e2c828
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/automating/using/using-workflow-data
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: workflow-general-operation
discoiquuid: ce7dfae9-8bb4-4c54-bdf8-0af757164886
isreadyforlocalization: false
navTitle: Using workflow data
publishexternaldate: 2018-11-20
sha1: 341489964153e3d08763fefe1b349130c21a7872
index: y
internal: n
snippet: y
---

# Using workflow data{#using-workflow-data}

Using workflow data

Once the data has been identified and prepared, it can be used in the following contexts:

* The **Update data** activity allows you to perform a mass update on fields in the database.
* The **Save audience** activity allows you to update an existing audience or create a new audience from the population computed upstream in a workflow. The audiences created or updated from this activity are **List** or **File** audiences. This activity also allows you to export profiles as Adobe Experience Cloud audiences/segments.
* The **Subscription Services** activity allows you to take profiles in mass and subscribe them to a service or unsubscribe them from a service.
* The **Extract file** activity allows you to export data from Adobe Campaign in the form of an external file.

After defining a profile target, you can use several activities to create and send deliveries:

* The **Email delivery** activity allows you to configure sending an email in a workflow. This can be a **single send** email and sent just once, or it can be a **recurring** email.
* The **SMS delivery** activity allows you to configure sending an SMS in a workflow. This can be a **single send** SMS and sent just once, or it can be a **recurring** SMS.
* The **Mobile app delivery** activity allows you to configure sending a push notification in a workflow. This can be a **single send** notification and sent just once, or it can be a **recurring** notification.

