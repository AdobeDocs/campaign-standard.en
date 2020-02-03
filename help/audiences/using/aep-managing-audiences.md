---
title: Managing Adobe Experience Platform audiences
description: Learn how to manage Adobe Experience Platform within Campaign Standard.
page-status-flag: never-activated
uuid: b3996642-96ec-489e-b146-c8c2cb52aa32
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: audiences
content-type: reference
topic-tags: managing-audiences
discoiquuid: 750ecd8d-67a5-4180-bfec-2a8e3098c812
context-tags: audience,wizard;audience,overview;delivery,audience,back
internal: n
snippet: y
---

# Managing Adobe Experience Platform audiences {#about-audiences}

>[!IMPORTANT]
>
>Audience Destinations Service is currently in beta, which may be subject to frequent updates without notice. Customers are required to be hosted on Azure (currently in beta for North America only) to access these capabilities. Please reach out to Adobe Customer Care if you would like access.

## Accessing Adobe Experience Platform audiences

To access the Adobe Experience Platform segment builder, navigate to the **[!UICONTROL Audiences]** card on Campaign Standard home page (or the **[!UICONTROL Audiences]** link in the header), and then select the **[!UICONTROL Adobe Experience Platform]** option.

![](assets/aep_audiences_access.png)

You will first be directed to the Adobe Experience Platform segment list page, where already existing Adobe Experience Platform segments can be accessed for further editing, if desired.

A search bar and filter are available to help you find the desired Adobe Experience Platform segment.

![](assets/aep_audiences_list.png)

## Creating Adobe Experience Platform audiences

To create an Adobe Experience Platform audience directly in Campaign Standard, follow these steps:

1. From the Adobe Experience Platform segment list page, click the **[!UICONTROL New audience]** button located in the right-hand corner.

    ![](assets/aep_audiences_creation_create.png)

1. The Unified Segment Builder should now be displayed in your workspace. It allows you to build a segment using data from Adobe Experience Platform that will eventually be used to create your audience.

1. Name the segment in the right pane and enter a description (optional).

    ![](assets/aep_audiences_creation_edit_name.png)

1. In order to successfully create a segment, you must select a **merge policy** that matches your marketing purpose for this segment.

    In the settings pane, a Platform default merge policy is selected. For more information on merge policies, refer to the dedicated section from the [Segment Builder user guide](https://www.adobe.io/apis/experienceplatform/home/profile-identity-segmentation/profile-identity-segmentation-services.html#!api-specification/markdown/narrative/technical_overview/segmentation/segment-builder-guide.md)

    ![](assets/aep_audiences_mergepolicy.png)

1. Define the rules that will identify the profiles to be retrieved in your audience.

    To do this, drag the desired attributes and/or events from the left pane into the workspace, define the corresponding rules then click the **[!UICONTROL Create segment]** button to save the segment (see [Using the Unified Segment Builder](../../audiences/using/aep-using-segment-builder.md)).

    ![](assets/aep_audiences_creation_query.png)

The audience is now ready to be activated, you can use it as a target for your campaigns (see [Targeting Adobe Experience Platform audiences](../../automating/using/aep-targeting-audiences.md)).

## Editing audiences

To edit an audience, open it and modify the rules as needed within the Unified Segment Builder interface (see [Using the Unified Segment Builder](../../audiences/using/aep-using-segment-builder.md)).

Once the changes have been completed, click the **[!UICONTROL Save segment]** button to update your audience.

![](assets/aep_audiences_editing.png)
