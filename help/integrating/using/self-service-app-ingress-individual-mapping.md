# Editing Table Mapping

The "Dynamics 365 to Campaign" workflow (a.k.a Ingress) is a list of mappings of Dynamics 365 tales to Campaign tables.
This page will explain how to configure a ***single*** one of these mapping for one Dyanmics 365 table to one Campaign
table.   If you want to better understand the page that lists ***all*** of the table mappings that have been configured
then click [here](self-service-app-ingress-list.md) to get more information about this other page.

The "Edit Table Mapping" page is split up into five sections:
* [Tables](#tables)
* [Mappings](#mappings)
* [Field Replacements](#field-replacements)
* [Filters](#filters)
* [Advanced Settings](#advanced-settings)

## Tables {#tables}

This section lists the name of the Dynamics 365 table and the Campaign table to which it will be mapped.   

### Editing Existing Mapping

If you edit an existing mapping then you will see that the table selections are not editable (see below).   

![](assets/d365-to-acs-ui-page-ingress-table-read-only.png)

This is by design 
because the inputs further down in the page are based on the fields associated with these tables.   Changing the tables 
would make all the fields associated with these tables invalid.    If you want to change the table you want to map to, 
then you will need to return to the previous page, delete the mapping you want to change, and add a new mappings.

### Adding a New Mapping

If you chose to "Add a new Mapping" on the "Dynamics 365 to Campaign" page then you will be shown a page that will 
allow you choose which tables you want to map.    Click [here](self-service-app-ingress-list.md) to see more information
about the "Dynamics 365 to Campaign" page and how you can add a new mapping.

The first thing you should see when adding a new mapping is something similar to the following:

![](assets/d365-to-acs-ui-page-ingress-choose-tables.png)

This modal window will require you to choose the Dynamics 365 and Campaign tables before you can proceed.   The reason
why you have to pick a table is due to the fact that most of the other inputs on the page will be dependant on which
tables you choose.   If you click the "Cancel" button in the modal then you will be returned to the previous page 
because you cannot proceed without making a selection.  

Once you have chosen a Dynamics 365 Table and Campaign Table then click the "OK" button to proceed.  The app will need
to read in field information associated with the tables you've selected, so you will be asked to wait for a short time
until this has completed.

    >[!NOTE]
    >
    > IMPORTANT: You can only choose the tables in this page when you're first adding the mapping.   Once you click 
    > the "Save" button and then the Edit button to return to this page then the tables selected will be read only.
    > You will not have the option to edit them.   Therefore, make sure that you are sure that you have selected the 
    > the correct tables before you click the "Save" button.   


    >[!NOTE]
    >
    > The integration will only allow you to map FROM a Dynamics 365 table once, and you can only map TO a Campaign 
    > once.    Therefore, you will notice that the dropdown selections will not include tables that you've already
    > mapped.

## Field Mappings {#mappings}

### Primary Keys

If you're adding a new Dynamics 365 to Campaign table mapping, then you will be asked to identify the ID field (similar
to below).    The Dynamics 365 field is read only because the integration will recognize which field is the primary key.
You will have an opportunity to select which field will serve as the unique key in Campaign.   It is important that you
choose a field that cannot have any duplicates and that field is configured properly in Campaign.    A link to the page 
["Configuring the resource's data structure"](https://experienceleague.adobe.com/docs/campaign-standard/using/developing/adding-or-extending-a-resource/configuring-the-resource-s-data-structure.html?lang=en#developing) is 
provided to give you more information on how to configure this field in Campaign.

![](assets/d365-to-acs-ui-page-ingress-mappings-first-key.png)

    >[!NOTE]
    >
    > You will only be able to choose the ID field on the table when you've selected "Add a New Mapping" in the 
    > "Dynanics 365 to Campaign" page.    If you click the edit button to edit an existing table mapping then the ID
    > field will be read only.

The primary keys will always be the first field names listed in the "Field Mappings" section.   As a reminder, the
following icon is listed to the right to remind you that these are the primary keys.

![](assets/d365-to-acs-icon-primary-key.png)

### Add New Field Mapping

The Field Mappings sections allows you to add other field mappings other than the Primary Keys addressed in the section
directly above this one.    To add a new mapping of a field from Dynamics 365 to Adobe Campaign, click the "Add New
Field Mapping" button (shown below).

![](assets/d365-to-acs-icon-add-new-field-mapping.png)

Once you click this, then a new set of inputs will be added that look like this:

![](assets/d365-to-acs-ui-page-ingress-new-field-mapping.png)

The Dynamics 365 inputs will contain a list of field names that are associated with the Dynamics 365 table you have 
selected at the top of the page.   Similarly, the Campaign input will contain a list of field names associated with the
Campaign table selected above.   

The switch in the "Apply Updates" column allows you to control whether updates
to this field will be propagated from Dynamics 365 to Campaign.   If it is switched on 
(![](assets/d365-to-acs-icon-switch-on.png)) then updates to the value(s) in Dynamics 365 will be propagated to 
Adobe Campaign as the updates occur.   If you 
deselect the button (![](assets/d365-to-acs-icon-switch-off.png)) then it means that the value will be propagated when
data is intially loaded (or replayed), but incremental updates to the field in Dynamics 365 will not be propagated.

    >[!NOTE]
    > If you click on the "Apply Updates" column heading then it will show you a dialog that will give you the ability
    > to update ***all*** of the switches to on or off.
    
The button ![](assets/d365-to-acs-icon-delete.png) allows you to delete a single field mapping.

When you select values you should the data type show up below the drop downs (see below).   This is something to keep
in mind when mapping values from one field to the other.

![](assets/d365-to-acs-ui-page-ingress-mappings-fields-selected.png)    

    >[!NOTE]
    > You cannot map more than one Dynamics 365 fields to a single Campaign field.

## Field Replacements {#field-replacements}

## Filters {#filters}

## Advanced Settings {#advanced-settings}


* Overview 
  - Discuss the differences between adding and editing
  - Reiterate that the changes do not take effect *until* you save it
* Mappings
* Replacements
* Filters
* Advanced Settings
