---
title: Targeting Adobe Experience Platform audiences
description: Learn how to target Adobe Experience PLatform audiences within workflows.
page-status-flag: never-activated
uuid: 528d9472-e447-47af-a6b2-3181aa5fb5ad
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: channel-activities
discoiquuid: 19796aca-6e9e-4d3a-8917-ba660ec7993c

internal: n
snippet: y
---

# Targeting Adobe Experience Platform audiences {#targeting-aep-audiences}

To activate an Adobe Experience Platform audience into your workflows, you must configure a Read audience activity. To do this, follow the steps below:

1. Add a Read audience activity into the workflow, then open it to configure it with an Experience Platform audience.

1. Select the Adobe Experience Platform option under Type of audience, then add the desired audience.

    >[!NOTE]
    >
    >Only Adobe Experience Platform audiences created in Audiences within Campaign are available for use in the activity.

    ![](assets/aep_wf_readaudience.png)

1. (Optional) Once the audience is selected, you can click the eye button to review and/or edit the segment definition (make sure to save your changes again). Clicking the eye button will simply direct you to the Unified Segment Builder (in another tab) associated with the selected audience within Campaign.

1. You must select a Platform data mapping element to specify the desired targeting dimension for the selected Adobe Experience Platform audience.

    By default, the primary key (e.g., iRecipientID for Profile table, iAppSubscriptionID for AppSubscription table) used for reconciliation will automatically be available from the dropdown list. To target outside of the primary key, you must create a custom Namespace

    >[!NOTE]
    >
    >For targets outside of the primary key, you must also create a custom Target Mapping that corresponds to the custom Namespace. For more information on Target Mapping, refer to this dedicated document.

    ![](assets/aep_wkf_readaudience_namespace.png)

    This list contains all the Experience Data Model (XDM) mappings that have been configured on your instance. For more on Data Mapping, refer to this dedicated document.

    ![](assets/aep_wkf_readaudience_namespace2.png)

1. Once the audience and targeting dimensions are configured properly, click the Confirm button to save your changes.

You can now configure your workflow with other activities. You can, for example, link an Email delivery activity to send an email to the audience that has been selected.

![](assets/wkf_email.png)

>[!NOTE]
>
>Campaign Standard lets you target Adobe Experience Platform audiences within all delivery channels: Emails, SMS messages, Direct mail messages, Push notifications, and In-app messages.

For more on how to use workflows and deliveries, refer to the Campaign Standard documentation:

* Discovering workflows
* Building a workflow
* Discovering communication channels
* About channel activities
