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

The Unified Segment Builder allows you to define rules based on data coming from the Unified Profile Service.

For detailed information on the Unified Segment Builder, refer to this dedicated document.

The Unified Segment Builder interface is composed as follows:

* The left pane provides all fields (e.g., attributes, events and segments) available to build the segment by dragging and dropping desired fields into the segment builder workspace.
* The center area provides a workspace to build the segment by defining and combining rules from the available fields.
* The header and right pane displays the segment's properties (i.e., name, description, and estimated qualified profiles for the segment).

![](assets/aep_audiences_interface.png)

## Building a segment

To build a segment, follow these steps:

1. Name the segment and enter a description (optional). Specify the desired merge policy (this can be done after the rules have been built).

    ![](assets/aep_audiences_editdetails.png)

1. Look for the desired fields in the left pane, and then drag them into the center workspace.

    ![](assets/aep_audiences_dragfield.png)

1. Configure the rules corresponding to the dragged fields.

    ![](assets/aep_audiences_configure_rules.png)

1. Click the Create segment button.

## Finding the right fields for a segment

The left pane lists fields (i.e., attributes, events and segments) that are available for use to construct rules.

The fields listed are attributes captured by your company and can be made available through Data Services model in the Experience Data Model (XDM) schemas.

For detailed information on the left pane, refer to the dedicated section from the Unified Segment Builder documentation.

Fields are organized into tabs:

* Attributes: Existing profiles attributes that can originate from your Adobe Campaign database and/or Adobe Experience Platform. They refer to static information attached to a profile (e.g., email address, country of residence, loyalty program status, etc.).

    ![](assets/aep_audiences_attributestab.png)

* Events: Events are activities that identify consumers who have had some interaction with your company's customer touchpoints, such as “anyone who has ordered twice in two weeks”. This can be streamed from Adobe Analytics, or ingested directly into the Adobe Experience Platform using third-party ETL tools.

    ![](assets/aep_audiences_eventstab.png)

By default, the Unified Segment builder displays fields for which data is present. To display the full schema, including fields for which data is not present, deselect the option from the settings tab.

![](assets/aep_audiences_populatedfields.png)

The symbol at the end of each field provides additional information about the attribute and how to use it.

![](assets/aep_audiences_isymbol.png)

## Defining rules for a segment

To build a rule, follow the steps below:

>[!NOTE]
>
>Detailed information on rule definition is presented in the "Building a segment" section from the Unified Segment Builder documentation.

1. Find the field from the left pane that reflects the attributes or events to which the rule will be based on.

1. Drag the field onto the center workspace, then configure it according to the desired segment definition. To do this, several string and date/time functions are available (for more on this, refer to the Unified Segment Builder documentation).

    In the example below, the rule will target all profiles with gender that equals to "Male".

    ![](assets/aep_audiences_malegender.png)

    The estimated population corresponding to the segment is automatically recalculated in the Segment Properties section. For more on this, refer to the "Building a segment" section from the Unified Segment Builder documentation.

1. The View Profiles button gives you a preview of the first 20 records corresponding to the rule, enabling you to quickly validate the segment.

    ![](assets/aep_audiences_samplepreview.png)

    You can add as many additional rules as desired, in order to target the right profiles.

    When adding a rule to a container, it will be appended to any existing rules with the AND operator. Click the operator to access the option to change it to OR.

    ![](assets/aep_audiences_andoperator.png)

Once linked together, the two rules form a container.

## Comparing fields

The Unified Segment Builder lets you compare two fields to define a rule. For example, females whose home address is in a different ZIP code from their work address.

To do this, follow the steps below:

1. Drag the first field that you want to compare (e.g., the home address postal code) onto the center workspace.

    ![](assets/aep_audiences_comparing_1.png)

1. Select the second field (e.g., the work address postal code) that will be compared with the first field.

    Drag it onto the center workspace, in the same container as the first field, in the Drop here to compare operands box.

    ![](assets/aep_audiences_comparing_2.png)

1. Configure the operator between the two fields as desired. In this example, our segment requires that the home address postal code does not equal the work address one.

    ![](assets/aep_audiences_comparing_3.png)

The rule is now configured and ready to be activated as an audience.
