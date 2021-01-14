---
title: Get Access to the Adobe Campaign Standard Integration with Dynamics 365 Self-Service App
description: Adobe Campaign Standard Integration with Dynamics 365 Self-Service App
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-microsoft-dynamics-365
---

# Access the Adobe Campaign Standard Integration with Dynamics 365 Self-Service App

This configuration will require you to work with an Experience Cloud (EC) Administrator for you organization. These are the initial steps required to give you access to the self-service integration application interface. Once you have access to the tool, you will set up connections to your data and configure the flow of data between Adobe Campaign and Microsoft Dynamics 365.

>[!NOTE]
>
>You need to reach out to your Adobe Representative and provide the Adobe Campaign Standard org and instance names. A ticket will be logged to request that the integration app be enabled for your organization.

## Add a product profile

In this section you will learn how to grant access to the Adobe Campaign Standard integration with Dynamics 365 self-service app. Users who have access to your organization in Adobe Experience Cloud will not have access to the integration self-service app, unless you follow the steps below to grant them access.

>[!IMPORTANT]
>
> These steps require **Administrator** role in the Experience Cloud for your organization.
>

1. Browse to https://experience.adobe.com/ and log into the Adobe Experience Cloud.
1. Access the **Admin Console**.

   ![](assets/d365-to-acs-access-3.png)

1. Click on **[!UICONTROL Products]** to access your Experience Cloud solutions.

   ![](assets/d365-to-acs-access-6.png)


   >[!IMPORTANT]
   >
   >The remaining steps in this section will be performed for each of your Campaign instances (dev, text, production).
   >

1. Click on the first instance to configure.

    ![](assets/d365-to-acs-access-6.png)

   The instance page should look something like this:

   ![](assets/d365-to-acs-access-8.png)

1. Click the **[!UICONTROL New Profile]** button and add a new entry named: **Campaign Standard - your-prod-instance-name - D365/ACS Integration**

   * If you see this entry in the list then you do not need to proceed. Click on **Adobe Campaign Standard** in the left menu and check the other Campaign instances.

   * Make sure to replace "your-prod-instance-name" with the actual name for your instance.

1. You can leave the **[!UICONTROL Permission Group]** dropdown with the default value.

1. If your entries look similar to the following, then click the **[!UICONTROL Done]** button.

   ![](assets/d365-to-acs-access-14.png)

   The new product profile has been added.

   ![](assets/d365-to-acs-access-15.png)

## Grant access to users {#add-users-to-profile}

From the **[!UICONTROL Products]**  page, select your Campaign instance and follow the steps below:

1. Click on the new profile that you've created earlier:  **Campaign Standard - your-prod-instance-name - D365/ACS Integration**

   ![](assets/d365-to-acs-access-15.png)

1. Click on the **[!UICONTROL Developers]** tab.

   ![](assets/d365-to-acs-access-18.png)

1. Click on the **[!UICONTROL Add Developer]** button

1. Enter the name or email address of the user you want to add.  Select the result that matches the user.
   
   If this is the first time the user is getting added to the Org, enter details.

1. Click **[!UICONTROL Save]** to confirm.
