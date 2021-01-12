---
solution: Campaign Standard
product: campaign
title: Creating a multilingual email with the Adobe Experience Manager integration.
description: With the Adobe Experience Manager integration, you can create content directly in AEM and use it later on in Adobe Campaign.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-experience-manager

---

# Creating a multilingual email with the Adobe Experience Manager integration {#creating-multilingual-email-aem}

Using this document, you will learn how to create a multilingual email using Adobe Experience Manager content and language copies.

The prerequisites are:

* Access to an AEM instance configured for the integration.
* Access to an Adobe Campaign instance configured for the integration.
* An Adobe Campaign multilingual email template configured to receive AEM content.

## Creating new email content in Adobe Experience Manager {#creating-email-content-aem}

1. From Adobe Experience Manager homepage, select **[!UICONTROL Site]**.

   ![](assets/aem_acs_1.png)

1. Select in which folder you want to create your page and click **[!UICONTROL Create]** then **[!UICONTROL Page]**. Here, we create our page in the en_us folder which will be our default language.

   ![](assets/aem_acs_2.png)

1. Select the **[!UICONTROL Adobe Campaign Email (ACS)]** template.

1. Fill in the properties of your email and click **[!UICONTROL Create]**.

   ![](assets/aem_acs_3.png)

1. Open your new email content and personalize it as needed. For more on this, refer to this [page](../../integrating/using/creating-email-experience-manager.md#editing-email-aem).

   ![](assets/aem_acs_4.png)

1. From the **[!UICONTROL Workflow]** tab, select the **[!UICONTROL Approve for Adobe Campaign]** validation workflow. You will not be able to send an email in Adobe Campaign if it uses a content that has not been approved.

   ![](assets/aem_acs_7.png)

1. Click **[!UICONTROL Complete]** then **[!UICONTROL Newsletter review]** from the **[!UICONTROL Complete work item]** window.

1. Click **[!UICONTROL Complete]** then **[!UICONTROL Newsletter approval]**. Once the content and sending parameters are defined, you can proceed to approving, preparing, and sending the email in Adobe Campaign Standard.

   ![](assets/aem_acs_8.png)

## Creating language copies {#creating-language-copies}

After designing your email content, you now need to create your language copies which will be sync with Adobe Campaign Standard as variants.

1. Select your previously created page, click **[!UICONTROL Create]** then **[!UICONTROL Language Copy]**.

   ![](assets/aem_acs_5.png)

1. Select your previously created email content which will be translated in the chosen languages then click **[!UICONTROL Next]**.

   ![](assets/aem_acs_6.png)

1. In the **[!UICONTROL Target language(s)]** drop-down, select in which language your content will be translated then click **[!UICONTROL Next]**.

   ![](assets/aem_acs_9.png)

1. Click **[!UICONTROL Create]**.

Your language copies are now created, you can now edit your content depending on the chosen language.

>[!CAUTION]
>
>Every language copy need to be approved via the **[!UICONTROL Approve for Adobe Campaign]** validation workflow. You will not be able to send an email in Adobe Campaign if it uses a content that has not been approved.

![](assets/aem_acs_11.png)

## Creating your multilingual content in Adobe Campaign Standard {#multilingual-acs}

1. From Adobe Campaign Standard homepage, click **[!UICONTROL Create an email]**.

    ![](assets/aem_acs_12.png)

1. Select your Adobe Campaign multilingual email template configured to receive Adobe Experience Manager content. To learn more on how to create a template linked to your Adobe Experience Manager instance and a multilingual email, refer to this [page](../../integrating/using/configure-experience-manager.md#config-acs).

    ![](assets/aem_acs_13.png)

1. Fill in the **[!UICONTROL Properties]** and **[!UICONTROL Audience]** of your email.

1. Click **[!UICONTROL Create]**.

1. In the **[!UICONTROL Edit properties]**, make sure your Adobe Experience Manager account is correctly set in the **[!UICONTROL Content]** drop-down.

    ![](assets/aem_acs_20.png)

1. Access the email designer and click **[!UICONTROL Link with AEM content]**.

    ![](assets/aem_acs_14.png)

1. Select your previously created Adobe Experience Manager email content.

    ![](assets/aem_acs_15.png)

1. Click **[!UICONTROL Save & Close]**.

1. Click **[!UICONTROL Language copy creation]**.

    ![](assets/aem_acs_16.png)

1. Select one of your previously created language copy of your Adobe Experience Manager content and click **[!UICONTROL Confirm]**.

    ![](assets/aem_acs_17.png)

1. Adobe Campaign Standard will automatically link the other language copies to this content. Select the variant you want to add to Adobe Campaign Standard and click **[!UICONTROL Create variants]**.

    ![](assets/aem_acs_18.png)

1. Click the **[!UICONTROL Content variant]** block to change your default variant if needed and click **[!UICONTROL Confirm]**.

    ![](assets/aem_acs_19.png)

1. Your email is ready to be send. For more information on this, refer to this [page](../../sending/using/get-started-sending-messages.md).

Your audience will receive your email depending on the **[!UICONTROL Preferred languages]** set in their **[!UICONTROL Profiles]**. To learn more on how to edit profiles and preferred languages, refer to this [page](../../audiences/using/editing-profiles.md).