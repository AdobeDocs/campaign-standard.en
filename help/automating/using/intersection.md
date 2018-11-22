---
title: Intersection
seo-title: Intersection
description: Intersection
seo-description: The Intersection activity allows you to keep only the elements common to the different inbound populations in the activity.
page-status-flag: never-activated
uuid: 9924f945-ab09-4a27-90ba-8e3607ff88e8
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/automating/using/intersection
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: targeting-activities
discoiquuid: 5d0554b4-0fa9-45f9-92f2-58dd19c3f030
isreadyforlocalization: false
navTitle: Intersection
publishexternaldate: 2018-11-20
sha1: c848c91916b3512da8a0e04824c323af46e72590
index: y
internal: n
snippet: y
---

# Intersection{#intersection}

Intersection

## Description {#description}

![](assets/intersection.png)

The **Intersection** activity allows you to keep only the elements common to the different inbound populations in the activity.

## Context of use {#context-of-use}

The **Intersection** activity is generally used to carry out additional filtering on populations from inbound transitions.

## Configuration {#configuration}

1. Drag and drop an **Intersection** activity into your workflow.
1. Connect it to the other activities that come before it, such as queries.
1. Select the activity, then open it using the  ![](assets/edit_darkgrey-24px.png)

   button from the quick actions that appear.
1. Select the **Reconciliation type**:

    * **Keys only**: Default mode. The activity only keeps one element when elements from the different inbound transitions have the same key.
    * **All shared columns**: The data is reconciled on the basis of columns in common with the inbound transitions. Therefore, you have to select the primary set that will serve as a basis for comparison. This option can be used if the inbound population targeting dimensions are different.
    * **A selection of columns**: Select this option to define the list of columns on which the data reconciliation will be applied. You must first select the primary set (the one which contains the source data), then specify the fields to use for the join.

1. Check the **Use common additional data only** box if you would like to keep only the additional data that is in all inbound transitions.
1. If needed, manage the activity's [Transitions](../../automating/using/executing-a-workflow.md#managing-an-activity-s-outbound-transitions) to access the advanced options for the outbound population.
1. Confirm the configuration of your activity and save your workflow.

## Example {#example}

The following example shows the intersection between two query activities. It is being used here to look into the Adobe Campaign database and retrieve profiles who are between 18 to 27 years old and profiles whose email address has been provided respectively.

![](assets/wkf_intersection_example.png)

