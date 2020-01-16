---
title: Managing audiences
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

# Managing audiences {#about-audiences}

An audience is a list of profiles from your database that meet specific conditions defined in segments.

You can access the Unified Segment builder directly in your Campaign instance to build an audience using data from the Adobe Experience Platform. You can also manage these type (i.e., ‘Data Services Query’) of audiences directly in the ‘Audiences’ list view, where you can duplicate, delete or edit them directly from the Campaign interface.

For more on global concepts for managing audiences in Campaign, refer to the Campaign Standard documentation.

## Accessing audiences

Adobe Experience Platform audiences are available in the list of audiences, which is accessible from the Audiences card on the Adobe Campaign home page or from the Audiences link.

They can be identified by the Data Services Query label in the Type column.

![](assets/audiences_list.png)

## Creating audiences

Audiences are created directly from the list of audiences. To do this, follow the steps below:

1. Go to the list of audiences, then click the Create button.

    ![](assets/audiences_creation_create_button.png)

1. Choose the Adobe Experience Platform segment builder environment.

    ![](assets/audiences_creation_type_selection.png)

2. The Unified Segment Builder should now be displayed in your workspace. It allows you to build a segment using data from the Adobe Experience Platform that will eventually be used to create your audience.

    In order to successfully create a segment, you must specify the desired merge policy (see Real-time Customer Profile overview) and name the segment in the right pane. (Optional): Enter a description.

    ![](assets/audienceS_creation_edit_name.png)

1. Define the rules that will identify the profiles to be retrieved in your audience. To do this, drag the desired attributes from the left pane into the workspace, define the corresponding rules then click the Create Segment button to save the segment. For more details on this, refer to Using the Unified Segment Builder.

    ![](assets/audiences_creation_query.png)

The audience is now ready to be activated, you can use it as a target for your campaigns.

## Deleting and duplicating audiences

To delete or duplicate an audience, hover over it then click the Delete element or Duplicate element button.

![](assets/audiences_delete_duplicate.png)

Once duplicated, a copy of the audience is created.

![](assets/audiences_duplicate.png)

The copy of the audience has the same segment definition as the duplicated audience. The Segment name field is therefore identical for both audiences. If you intend to modify the segment's rules, thereby essentially creating a new segment, we strongly recommend changing its name.

![](assets/audiences_duplicate_rename.png)

## Editing audiences

To edit an audience, open it and modify the rules as needed within the Unified Segment Builder interface (see Using the Unified Segment Builder for more details on rule building).

Once the changes have been completed, click the Save Segment button to update your audience.

![](assets/audiences_editing.png)
