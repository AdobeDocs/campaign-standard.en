---
title: Creating a custom profile dimension
seo-title: Creating a custom profile dimension
description: Creating a custom profile dimension
seo-description: Learn how to create a custom profile dimension based on custom profile data.
uuid: df4224a1-e777-4c86-b7a4-f0ddad87ec88
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: reporting
content-type: reference
topic-tags: customizing-reports
discoiquuid: 129f9399-6baa-4c60-9dad-3d311ac92105
index: y
internal: n
snippet: y
---

# Creating a custom profile dimension{#creating-a-custom-profile-dimension}

Creating a custom profile dimension

Reports can also be created and managed based on custom profile data created during the profile custom resource extension.

In this example, we want to create the custom profile field **Loyalty programs** which will be divided into three levels: gold, silver and bronze. This custom profile will then be extended to be able to use it as a custom profile dimension in dynamic reports.

* [Step 1: Create a new profile field](../../reporting/using/creating-a-custom-profile-dimension.md#step-1--create-a-new-profile-field)
* [Step 2: Extend the sending logs with the profile field](../../reporting/using/creating-a-custom-profile-dimension.md#step-2--extend-the-sending-logs-with-the-profile-field)
* [Step 3: Create a delivery targeting recipients enrolled in the loyalty program](../../reporting/using/creating-a-custom-profile-dimension.md#step-3--create-a-delivery-targeting-recipients-enrolled-in-the-loyalty-program)
* [Step 4: Create a dynamic report to filter recipients with the custom profile dimension](../../reporting/using/creating-a-custom-profile-dimension.md#step-4--create-a-dynamic-report-to-filter-recipients-with-the-custom-profile-dimension)

## Step 1: Create a new profile field {#step-1--create-a-new-profile-field}

We first need to create the new profile field **Loyalty program** that will assign loyalty level to our recipients: gold, silver or bronze.

>[!NOTE]
>
>Custom resources can only be managed by an administrator.

To do so:

1. From the advanced menu, select **[!UICONTROL Administration]** > **[!UICONTROL Development]** > **[!UICONTROL Custom resources]** then the **[!UICONTROL Profile (profile)]** custom resource.

   ![](assets/custom_profile_1.png)

1. From the **[!UICONTROL Data structure]** tab, in the **[!UICONTROL Fields]** category, click the **[!UICONTROL Add field]** button.

   ![](assets/custom_profile_2.png)

1. Enter the **[!UICONTROL Label]** , **[!UICONTROL ID]** and select the custom resource **[!UICONTROL Type]** . Here, we selected **[!UICONTROL Text]** since recipients will have the choice between gold, silver and bronze.

   ![](assets/custom_profile_3.png)

1. Click the ![](assets/custom_profile_22.png) icon to define your field. 

   ![](assets/custom_profile_12.png)

1. Here, we need to specify the authorized values by checking **[!UICONTROL Specify a list of authorized valued]** and create each value by clicking **[!UICONTROL Create element]** .

   ![](assets/custom_profile_13.png)

1. Enter the **[!UICONTROL Label]** and **[!UICONTROL Value]** then click **[!UICONTROL Add]** . For this example, we need to create the value gold, silver and bronze. Click **[!UICONTROL Confirm]** when done.

   ![](assets/custom_profile_14.png)

1. Select the **[!UICONTROL Screen definition]** tab. In the **[!UICONTROL Detail screen configuration]** drop-down, check **[!UICONTROL Add personalized fields]** section to create a new section in our profile.

   ![](assets/custom_profile_4.png)

1. Click the **[!UICONTROL Add an element]** button to create your new section. Select the **[!UICONTROL Type]** : **[!UICONTROL Input field]** , **[!UICONTROL Value]** or **[!UICONTROL List]** , then the field to add in this new section.

   ![](assets/custom_profile_5.png)

1. You can also add a title to your section in the field **[!UICONTROL Customize the title of the section where the fields will be displayed]** .

   Click **[!UICONTROL Save]** when the configuration is done.

   ![](assets/custom_profile_6.png)

1. From the advanced menu, select **[!UICONTROL Administration]** > **[!UICONTROL Development]** > **[!UICONTROL Publication]** to start publishing your custom resource.
1. Click **[!UICONTROL Prepare publication]** then when the preparation is done, click the **[!UICONTROL Publish]** button.

   ![](assets/custom_profile_7.png)

Your new profile field is now ready to be used and selected by your recipients.

![](assets/custom_profile_8.png)

## Step 2: Extend the sending logs with the profile field {#step-2--extend-the-sending-logs-with-the-profile-field}

Now that your profile field is created, we need to extend the sending logs with our profile field to create the associated custom profile dimension in dynamic reports.

Before extending the log with our profile field, make sure that the PII window was accepted to have access to the **[!UICONTROL Sending logs extension]** tab. For more on this, refer to this [page](../../reporting/using/about-dynamic-reports.md#dynamic-reporting-usage-agreement).

>[!NOTE]
>
>Logs can only be extended with profile fields by administrator.

1. From the advanced menu, select **[!UICONTROL Administration]** > **[!UICONTROL Development]** > **[!UICONTROL Custom resources]** then the **[!UICONTROL Profile (profile)]** custom resource.
1. Open the **[!UICONTROL Sending logs extension]** drop-down.

   Check **[!UICONTROL Add segment code]** to store the segment code from the targeting workflow. Please note that segments can not be used in Dynamic reports. For more information on segmentation, refer to this [page](../../automating/using/segmentation.md).

1. Click the **[!UICONTROL Create element]** button.

   ![](assets/custom_profile_9.png)

1. Select your previously created field and click **[!UICONTROL Confirm]** .
1. Check **[!UICONTROL Add this field in Dynamic reporting as a new dimension]** to create your custom profile dimension.

   ![](assets/custom_profile_10.png)

   This option is only available if the PII window was accepted. For more on this, refer to this [page](../../reporting/using/about-dynamic-reports.md#dynamic-reporting-usage-agreement).

1. Click **[!UICONTROL Add]** then save your custom resource.
1. Since the custom resource was modified, we need to publish it to implement the new changes.

   From the advanced menu, select **[!UICONTROL Administration]** > **[!UICONTROL Development]** > **[!UICONTROL Publication]** to start publishing your custom resource.

1. Click **[!UICONTROL Prepare publication]** then when the preparation is done, click the **[!UICONTROL Publish]** button.

   ![](assets/custom_profile_7.png)

Your custom profile is now available as a custom profile dimension in your reports.

Now that your field has been created and that sending logs have been extended with this profile field, you can start targeting recipients in deliveries.

## Step 3: Create a delivery targeting recipients enrolled in the loyalty program {#step-3--create-a-delivery-targeting-recipients-enrolled-in-the-loyalty-program}

Once your profile field is published, you can start your delivery. In this example, we want to target every recipient enrolled in the loyalty program.

1. From the **[!UICONTROL Marketing activities]** tab, click **[!UICONTROL Create]** then select **[!UICONTROL Email]** .
1. Choose an **[!UICONTROL Email type]** then enter your email's properties.
1. To target recipient enrolled in the loyalty program, drag and drop the **[!UICONTROL Profiles (attributes)]** activity.
1. Select your previously created field from the **[!UICONTROL Field]** drop-down.

   ![](assets/custom_profile_16.png)

1. Select your **[!UICONTROL Filter conditions]** . Here, we want to target recipients who are part of one of the three loyalty program's levels.

   ![](assets/custom_profile_17.png)

1. Click **[!UICONTROL Confirm]** then when done filtering, click **[!UICONTROL Next]** .
1. Define and personalize the message content, sender name and subject. For more information on email creation refer to this [page](../../designing/using/about-email-content-design.md#about-the-email-designer).

   Then, click **[!UICONTROL Create]** .

1. When ready, you can preview and send your message. For more information on how to prepare and send your message, refer to this [page](../../sending/using/preparing-the-send.md).

Once your email is correctly sent to your selected recipients, you can start filtering your data and track the success of your delivery with reports.

## Step 4: Create a dynamic report to filter recipients with the custom profile dimension {#step-4--create-a-dynamic-report-to-filter-recipients-with-the-custom-profile-dimension}

After sending your delivery, you can breakdown reports using your custom profile dimension from the **[!UICONTROL Profile]** table.

1. From the **[!UICONTROL Reports]** tab, select an out-of-the-box report or click the **[!UICONTROL Create]** button to start one from scratch.

   ![](assets/custom_profile_18.png)

1. In the **[!UICONTROL Dimensions]** category, click **[!UICONTROL Profile]** then drag and drop your custom **Loyalty program** profile dimension to your freeform table.

   ![](assets/custom_profile_19.png)

1. Drag and drop the **[!UICONTROL Processed/Sent]** and **[!UICONTROL Open]** metrics to start filtering your data.

   ![](assets/custom_profile_20.png)

1. Drag and drop a visualization in your workspace if needed.

   ![](assets/custom_profile_21.png)

