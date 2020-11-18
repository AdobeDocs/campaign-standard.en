# Opt in/out Workflow


  
This workflow allows you to identify the flow of the opt in/out information between Dynamics 365 and Adobe Campaign.
This assumes that the data is associated with the Microsoft Dynamics 365 entity "contact" and the Adobe Campaign
resource "profile".

Remember that you need to click "Save" to save your selections.   Also remember that you must stop the "Campaign to 
Dynamics 365"  workflow and then click play for the integration to incorporate your changes.

![](assets/d365-to-acs-ui-page-workflows-optinout-disabled.png)

## Opt in/out synchronization direction

* <u>Disabled</u>: When this is selected, no opt in/out information will move from Adobe Campaign and Dynamics 365.

* <u>Unidirectional (Dynamics 365 to Campaign)</u>: This selection is used when you want Opt in/out data to flow from
  Adobe Campaign to Dynamics 365.   The integration app will not let you define anything when this has been selected
  since you already have a workflow available to you that allow you to define how the data will flow in this direction.
  In this case, click the "Save" button, then on the Workflows page, and click to edit the "Dynamics 365 to Adobe 
  Campaign" workflow.   In this workflow, you can edit the contacts/profile table mapping to identify how you want the
  data to map.

* <u>Unidirectional (Campaign to Dynamics 365)</u>: This selection will make visable the "Mappings" section.   These
  inputs will allow you define which Adobe Campaign fields will map data to what fields in Dyhamics 365.   This means
  that if you happen to manually update a value in Dynamics 365 then its value would be overwritten by the Adobe
  Campaign value if it happens to change. 

* <u>Bidirectional</u>:  This selection will make visible a section named "Mappings".   These pairs will identify 
  which fields in Dynamics 365 and Adobe Campaign will map to each other.   Visit the page 
  [Manage data between Campaign and Dynamics 365](integrating/using/notices-and-recommendations-for-acs-and-ms-dynamics.md)
  for more information about how Bidirectional Opt in/out works.
  

## Mappings

This section only applies when the "Opt in/out synchronization direction" input has the selection "Unidirectional 
(Campaign to Dynamics 365)" or "Bidirectional".   You can define which fields in Dynamics 365 map to what inputs in
Adobe Campaign.

The Microsoft Dynamics 365 field names include all of those that are of type "boolean".

The Adobe Campaign field names are a fixed set of values specific to Opt in/out.   Note: the set of values in this list
cannot be changed.