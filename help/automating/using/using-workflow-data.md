---
title: Using workflow data
seo-title: Using workflow data
description: Using workflow data
seo-description: Learn the different possibilities to consume the data you imported or targeted.
uuid: 756e0695-a0cd-4619-a312-a1ae67cdfc80
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/automating/using/using-workflow-data
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-25T09 29 15.533-0400
cq-lastreplicated: 2018-07-23T05 56 53.191-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: workflow-general-operation
cq-template: /apps/help/templates/article-3
discoiquuid: 09bbe7aa-471e-4c2d-af47-9499ce0503b8
firstPublishExternalDate: 2018-07-23T05:56:53.155-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 17.780-0400
jcr-createdby: admin
jcr-description: Using workflow data
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T05:56:53.155-0400
lochandoffdate: 2018-07-25T09 29 15.533-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Using workflow data
publishexternaldate: 2018-07-23T05 56 53.155-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/automating/using/using-workflow-data.html
sha1: 42eb31aa7b04624e929276ffca08607a514e9ba6
topicBrowsingSortDate: 2018-07-23T05:56:53.155-0400
index: y
internal: n
snippet: y
---

# Using workflow data

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

