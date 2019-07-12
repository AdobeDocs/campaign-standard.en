---
title: Calling a resource through an identification key made of two fields
seo-title: Calling a resource through an identification key made of two fields
description: Calling a resource through an identification key made of two fields
seo-description: Learn how to call a resource through an identification key made of two fields
---

In some cases, you may need to define an dentification key for a resource that is made up of two fields. For example, the identification of your profiles can be the "Last name" and "Internal reference" fields.

Once the identification key is configured, you will need to configure a filter definition in order to be able to call the resource, either from the interface or the APIs.

In this use case, the Profile resource has been extended with custom "CRM ID" and "category" field. We will configure an identification key for the Profile resource, that will be made up of these two fields. We will then configure a filter definition so that we can access the resource through the identification key, from the interface and from the APIs.

This main steps are:

1. Configure the identification key for the resource, based on two fields.
1. Configure the filter definition, to be able to call the resource based on its identification key.
1. Call the resource from the interface or from the APis.

# Step 1: Configure the identification key

   >[!NOTE]
   >Before configuring the identification key, check that the two fields that will be used exist in the data structure.
   >If you plan on using a custom field, make sure that the resource has been extended with this field and that it has been published. For more on this, refer to this section.

1. Go to the **[!UICONTROL Administration]** / **[!UICONTROL Developement]** / **[!UICONTROL Custom resources]** menu, then open the **[!UICONTROL Profile]** resource.

   ![](assets/uc_idkey1.png)

1. Open the **[UICONTROL Identification keys]** section, then click the **[!UICONTROL Create element]** button.

   ![](assets/uc_idkey2.png)

1. Add the two custom "CRM ID" and "Category" fields, then click **[UICONTROL Confirm]**.

   ![](assets/uc_idkey3.png)

1. note: select the screen definition tab if you want to display the field in the profile's interface

   >[!NOTE]
   > If you want to display the two custom fields in the profile's interface, configure the **[UICONTROL Screen definition]** tab. For more on this, refer to this section.

1. You can now configure the filter definition to be able to call the resource through its identification key.

# Step 2: Configure the filter definition

1. In the **[UICONTROL Filter definition]** tab, click **[UICONTROL Add an element]**, then enter the filter definition's Label and ID.

1. Edit the filter definition's properties to configure it associated rules.

   ![](assets/uc_idkey4.png)

1. Drag and drop into the workspace the table that contains the fields used in the identification key.

   ![](assets/uc_idkey5.png)

1. Select the first field used in the identification key ("CRM ID"), then activate the **[UICONTROL Switch to parameters]**.

   ![](assets/uc_idkey6.png)

1. In the **[UICONTROL Filter conditions]**, keep the **[UICONTROL Equal]** operator, then define the parameter's name and click the plus sign to create it.

   ![](assets/uc_idkey7.png)

   >[!NOTE]
   > Once you have clicked the plus button, the parameter's name is automatically generated. Note this information: you will need it when using the filter from the REST APIs.

1. Repeat the steps above with all the fields that compose the identification key ("category"), then save your changes.

   ![](assets/uc_idkey8.png)

1. The filter definition is now configured. You can publish the resource so that the filter is available.

# Step 3: Call the resource based on its identification key

Once the identification key and its filter definition are configured, you can use to call the resource, either from Campaign standard interface or REST APIs.

To use the filter definition from the interface, use a **[UICONTROL Query]** activity in a workflow. The filter is then available in the left pane.

   ![](assets/uc_idkey9.png)

To use the filter definition from Campaign Standard REST APIs, use the syntax below:

\``` GET /profileAndServicesExt/&lt;resourceName&gt;&lt;filterName&gt;?&lt;param1_parameter&gt;=&lt;value&gt;&&lt;param2_parameter&gt;=&lt;value&gt;\```

In our case, the syntax to retrieve a profile from the "spring" category and with the "123456" CRM ID would be:

\``` GET https://mc.adobe.io/&lt;ORGANIZATION&gt;/campaign/profileAndServicesExt/profile/identification_key?category_parameter=spring&crm_id_parameter=123456\```