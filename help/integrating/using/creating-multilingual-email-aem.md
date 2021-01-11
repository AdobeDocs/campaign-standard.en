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

Using this document, you will learn how to create and manage email contents in Adobe Experience Manager, then use them for your marketing campaigns by importing them in your emails into Adobe Campaign Standard.

The prerequisites are:

* Access to an AEM instance configured for the integration.
* Access to an Adobe Campaign instance configured for the integration.
* An Adobe Campaign email template configured to receive AEM content.

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

1. Create email Campaign

    ![](assets/aem_acs_12.png)

1. Select template AEM multilingual email click next

    ![](assets/aem_acs_13.png)

1. Fill in the Properties
1. Select audience
1. Click Create

1. In the Edit properties, from the Content drop-down, select which Adobe Experience Manager account you want to use for this email.

1. Access the email designer.

1. Click Use Adobe Experience Manager content.

    ![](assets/aem_acs_14.png)

1. Select your previously created email content.

    ![](assets/aem_acs_15.png)

1. Edit your email as needed. For more information, refer to this page.

1. Click Save & Close.

1. Click Language copy creation.

1. Select your previously created Adobe Experience Manager content and click Confirm. Be careful with your content path. Content needs to be approved for this to work.
1. 
