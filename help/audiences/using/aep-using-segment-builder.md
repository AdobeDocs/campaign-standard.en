---
title: Using the Unified Segment Builder
description: Learn how to use the Unified Segment Builder to create audiences.
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

# Using the Unified Segment Builder {#using-the-unified-segment-builder}

>[!IMPORTANT]
>
>Audience Destinations service is currently in beta, which may be subject to frequent updates without notice. Customers are required to be hosted on Azure (currently in beta for North America only) to access these capabilities. Please reach out to Adobe Customer Care if you would like access.

The Unified Segment Builder allows you to build audiences by defining rules based on data coming from the [Unified Profile Service](https://docs.adobe.com/content/help/en/experience-platform/profile/home.html).

This section presents global concepts when building a segment. For detailed information on the Unified Segment Builder itself, refer to the [Segment Builder user guide](https://docs.adobe.com/content/help/en/experience-platform/segmentation/ui/overview.html).

The Unified Segment Builder interface is composed as follows:

* The left pane provides all attributes, events and audiences available to build the segment by dragging and dropping desired fields into the segment builder workspace.
* The center area provides a workspace to build the segment by defining and combining rules from the available fields.
* The header and right pane display the segment's properties (i.e., name, description, and estimated qualified profiles for the segment).

![](assets/aep_audiences_interface.png)

## Building a segment

To build a segment, follow these steps:

 The Unified Segment Builder should now be displayed in your workspace. It allows you to build a segment using data from Adobe Experience Platform that will eventually be used to create your audience.

1. Name the segment, then enter a description (optional).

    ![](assets/aep_audiences_creation_edit_name.png)

1. Make sure that the desired merge policy is selected in the settings pane.

    For more information on merge policies, refer to the dedicated section from the [Segment Builder user guide](https://docs.adobe.com/content/help/en/experience-platform/segmentation/ui/overview.html).

    ![](assets/aep_audiences_mergepolicy.png)

1. Look for the desired fields in the left pane, and drag them into the center workspace.

    ![](assets/aep_audiences_dragfield.png)

1. Configure the rules corresponding to the dragged fields.

    ![](assets/aep_audiences_configure_rules.png)

1. Click the **[!UICONTROL Create segment]** button.

## Finding the right fields for a segment

The left pane lists all attributes, events and audiences that are available for use to construct rules.

The fields listed are attributes captured by your company and have been made available through the [Experience Data Model (XDM) System](https://docs.adobe.com/content/help/en/experience-platform/xdm/home.html).

Fields are organized into tabs:

* **[!UICONTROL Attributes]**: Existing profiles attributes that can originate from your Adobe Campaign database and/or Adobe Experience Platform. They refer to static information attached to a profile (e.g., email address, country of residence, loyalty program status, etc.).

    ![](assets/aep_audiences_attributestab.png)

* **[!UICONTROL Events]**: Activities that identify consumers who have had some interaction with your company's customer touchpoints, such as “anyone who has ordered twice in two weeks”. This can be streamed from Adobe Analytics, or ingested directly into the Adobe Experience Platform using third-party ETL tools.

    ![](assets/aep_audiences_eventstab.png)

>[!NOTE]
>
>**Multi-entity segmentation** allows you to extend Profile data with additional data based on products, stores, or other non-profile classes. Once connected, data from additional classes becomes available as if they were native to the Profile schema.
>
>For more on this, refer to the [dedicated documentation](https://docs.adobe.com/content/help/en/experience-platform/segmentation/multi-entity-segmentation.html).

By default, the Unified Segment builder displays fields in which data is already present. To display the full schema, including fields for which data is not present, enable the **[!UICONTROL Show full XDM schema]** option from the settings.

![](assets/aep_audiences_populatedfields.png)

The symbol at the end of each field provides additional information about the attribute and how to use it.

![](assets/aep_audiences_isymbol.png)

## Defining rules for a segment

>[!NOTE]
>
>The section below provides global information on rules definition. For more on this, refer to the [Segment Builder user guide](https://docs.adobe.com/content/help/en/experience-platform/segmentation/ui/overview.html).

To build a rule, follow these steps:

1. Find the field from the left pane that reflects the attributes or events to which the rule will be based on.

1. Drag the field onto the center workspace, then configure it according to the desired segment definition. To do this, several string and date/time functions are available.

    In the example below, the rule will target all profiles with gender that equals to "Male".

    ![](assets/aep_audiences_malegender.png)

    The estimated population corresponding to the segment is automatically recalculated in the **[!UICONTROL Segment Properties]** section. 

1. The **[!UICONTROL View Profiles]** button gives you a preview of the first 20 records corresponding to the rule, enabling you to quickly validate the segment.

    ![](assets/aep_audiences_samplepreview.png)

    You can add as many additional rules as desired, in order to target the right profiles.

    When adding a rule to a container, it will be appended to any existing rules with the AND logical operator. If needed, click on the logical operator to modify it.

    ![](assets/aep_audiences_andoperator.png)

Once linked together, the two rules form a container.

## Comparing fields

The Unified Segment Builder lets you compare two fields to define a rule. For example, females whose home address is in a different ZIP code from their work address.

To do this, follow these steps:

1. Drag the first field that you want to compare (e.g., the home address postal code) onto the center workspace.

    ![](assets/aep_audiences_comparing_1.png)

1. Select the second field (e.g., the work address postal code) that will be compared with the first field.

    Drag it onto the center workspace, in the same container as the first field, in the **[!UICONTROL Drop here to compare operands]** box.

    ![](assets/aep_audiences_comparing_2.png)

1. Configure the operator between the two fields as desired. In this example, we want our segment to target profiles with the home address different from the work address.

    ![](assets/aep_audiences_comparing_3.png)

The rule is now configured and ready to be activated as an audience.
