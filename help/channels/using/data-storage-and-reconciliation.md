---
title: Data storage and reconciliation
seo-title: Data storage and reconciliation
description: Data storage and reconciliation
seo-description: Adobe Campaign allows you to define how the data entered in the landing page is managed once submitted by a user.
uuid: 6d3b359e-5fc8-449b-9d1b-4f130a9d2f14
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: landing-pages
discoiquuid: 058d6e8d-9e79-4b11-a003-08617826eb46
isreadyforlocalization: false
index: y
internal: n
snippet: y
---

# Data storage and reconciliation{#data-storage-and-reconciliation}

Data storage and reconciliation

Data reconciliation parameters allow you to define how the data entered in the landing page is managed once it has been submitted by a user.

To do this:

1. Edit the landing page properties accessed via the  ![](assets/edit_darkgrey-24px.png) icon in the landing page dashboard, and display the **[!UICONTROL Job]** parameters.

   ![](assets/lp_parameters_4.png)

1. Select the **[!UICONTROL Reconciliation key]** : these database fields (for example: email, first name, last name) are used to determine whether the visitor has a profile that is already known in the Adobe Campaign database. This allows you to update or create a profile, according to the update strategy parameters defined.
1. Define the **[!UICONTROL Form parameter mapping]** : this section allows you to map the landing page field parameters and those used in the reconciliation key.
1. Select the **[!UICONTROL Update strategy]** : if the reconciliation key recovers an existing database profile, you can choose for this profile to be updated with the data entered in the form or instead prevent this update.

