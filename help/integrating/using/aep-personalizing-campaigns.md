---
solution: Campaign Standard
product: campaign
title: Personalizing campaigns using Adobe Experience Platform attributes
description: Learn how to personalize your campaigns using Adobe Eperience Platform attributes.
audience: automating
content-type: reference
topic-tags: channel-activities

---

# Personalizing campaigns using Adobe Experience Platform attributes {#personalizing-campaigns-using-aep-attributes}

>[!IMPORTANT]
>
>Audience Destinations service is currently in beta, which may be subject to frequent updates without notice. Customers are required to be hosted on Azure (currently in beta for North America only) to access these capabilities. Please reach out to Adobe Customer Care if you would like access.
>
>**Push** and **In-App** channels are not available yet for personalization using contextual data from Adobe Experience Platform.

Once your workflow is configured with an [Adobe Experience Platform audience](../../integrating/using/aep-about-audience-destinations-service.md), you can personalize messages with profile attributes that exist exclusively in the Experience Data Model (XDM).

To do this, you must add these attributes into the **[!UICONTROL Read audience]** activity:

1. Open the **[!UICONTROL Read audience]** activity. In the **[!UICONTROL Additional data]** tab, click the **[!UICONTROL Create element]** button.

    Note that the **[!UICONTROL Additional data]** tab is only available after an Adobe Experience Platform audience has been selected.

    ![](assets/aep_wkf_readaudience_attributes.png)

    >[!NOTE]
    >
    >Array and map data types are not supported in this feature. Also, only data from the union schema will be displayed in the picker.

1. Select the desired XDM field from the list, then click **[!UICONTROL Confirm]**.

    ![](assets/aep_wkf_readaudience_perso1.png)

1. Click the **[!UICONTROL Add]** button to add it to the list of additional data.

    ![](assets/aep_wkf_readaudience_perso3.png)

1. Repeat these steps for every XDM field that you want to add into your workflow.

    >[!NOTE]
    >
    >You can add a maximum of 20 XDM fields in a **[!UICONTROL Read audience]** activity.

1. Once all the fields have been added, click the **[!UICONTROL Confirm]** button to save your changes. They will now be available to personalize your deliveries.

For more information on how to create and personalize deliveries, refer to the Campaign Standard documentation:

* [Discovering communication channels](../../channels/using/get-started-communication-channels.md)
* [About channel activities](../../automating/using/about-channel-activities.md)
* [Personalizing deliveries](../../designing/using/personalization.md)
