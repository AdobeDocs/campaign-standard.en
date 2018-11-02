---
title: Creating an A/B test
seo-title: Creating an A/B test
description: Creating an A/B test
seo-description: Discover the A/B test functionality and follow these steps to create an email from an A/B test template in Adobe Campaign.
page-status-flag: never-activated
uuid: afaf9e2e-3031-40d7-9e58-a1d71f817d9d
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/channels/using/creating-an-a-b-test
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2017-11-28T11 29 53.507-0500
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: email-messages
cq-template: /apps/help/templates/article-3
discoiquuid: 88b7f044-32a8-4878-aca6-f1d20659f9f8
firstPublishExternalDate: 2017-11-16T10:51:05.033-0500
herogradient: light
isreadyforlocalization: false
jcr-created: 2017-11-29T19 02 25.584-0500
jcr-createdby: admin
jcr-description: Creating an A/B test
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2017-11-16T10:51:05.033-0500
lochandoffdate: 2017-11-28T11 29 53.505-0500
lr-lastreplicatedby: wmyersta@adobe.com
navTitle: Creating an A/B test
publishexternaldate: 2017-11-16T10 51 05.033-0500
publishExternalURL: https://helpx.adobe.com/campaign/standard/channels/using/creating-an-a-b-test.html
sha1: 92bb769621b0328534e4b3540ec69151bf8c5109
topicBrowsingSortDate: 2017-11-16T10:51:05.033-0500
index: y
internal: n
snippet: y
---

# Creating an A/B test

Creating an A/B test

The A/B test functionality in Adobe Campaign allows you to define two to three email variants. Each variant is sent to population samples in order to determine which has the best result. Once determined, the winning variant is then sent to the remaining population.

You can choose to vary the email's content, subject, or sender.

>[!NOTE]
>
>You cannot perform an A/B test on content imported from Adobe Experience Manager.

An A/B test can be created using the standard email creation wizard, to which an A/B test configuration step is added. Creating a standard email is detailed in the [Creating an email](../../channels/using/creating-an-email.md) section.

In the specific context of an A/B test:

1. Create a new email from one of the three A/B testing specific templates, according to the element that you want to vary:

    * A/B test on sender
    * A/B test on content
    * A/B test on subject

   ![](assets/create_ab_testing.png)

   >[!NOTE]
   >
   >Follow-up and A/B test templates are hidden by default. Check the A/B test boxe on the left side (**Filter** lateral panel) to display them.

1. Define the general properties and the target audience of the email, just as for a standard email. Refer to the [Creating audiences](../../audiences/using/creating-audiences.md) section.
1. At the fourth step in the creation wizard, define the A/B test parameters:

    * **Number of variants**: You can choose to use two or three variants. If you choose three variants, this choice cannot be modified after this step has been confirmed in the wizard.
    * **Winning strategy**: Select the criterion to be used to determine the winning variant.
    * **Target breakdown**: Choose which percentage of the target will receive each variant. The remaining percentage will receive the winning variant once it has been determined. The targeted profiles are selected randomly.
    * **Winner sending method**: Choose whether you would like the winning variant to be automatically sent once it has been determined or whether you would like to manually confirm sending to the remaining population.
    * **Test duration**: Specify the duration of the test. The winning variant is determined automatically after this duration. You can manually choose the winning variant before the end of the test from the email dashboard.

      The test must be at least one hour in order for all of the tracking data to be collected and correctly taken into account to select the winning variant.

   ![](assets/ab_parameters.png)

1. Once the A/B test parameters have been defined, pass to the next step in the wizard and define the email content. Depending on the template that you have chosen, you can define several subjects, several sender names, or several different contents. Use the carousel to navigate between the different variants of the element. For more information, consult the [content editor](../../designing/using/example--email-personalization.md) section.

   ![](assets/create_ab_testing2.png)

1. Confirm creating the email. The email dashboard will then be displayed.
1. Schedule the send. The date defined indicates the start of the A/B test.
1. Check the A/B test parameters displayed in the **A/B test parameters** block. You can modify them up until you confirm sending the test (step 9) by selecting the block.

   ![](assets/create_ab_testing3.png)

1. Prepare the email send to analyze the target and the number of messages to send. Consult the [Preparing the send](../../sending/using/preparing-the-send.md) section.
1. Before sending the A/B test, check your email by sending proofs.
1. Once preparation has finished, confirm sending the test. Once confirmed, the A/B test parameters cannot be modified.

   The A/B test starts on the date defined in the **Schedule**. You can track its progress using the **A/B test** and **Deployment** blocks.

   You can manually select the winning variant at any time if you would like to cut the test duration short.

   Once testing has finished, a summary table is displayed in the **A/B Test** block and this allows you to view the various indicators for the different variants that were tested.

1. If you have selected **Send after confirmation** as the sending method, you have to manually select the winning variant to start sending it to the remaining population. If you have selected **Automatic**, the winning variant is automatically sent to the remaining population as soon as it has been determined by the system.

   >[!NOTE]
   >
   >If there is a tie, the winning variant must be manually selected. You can notify the email creator and modifier(s) that a variant has been chosen or needs to be selected. See [Adobe Campaign notifications](../../administration/using/adobe-campaign-notifications.md).

Your email is now defined and sent. You can access its logs and reports to measure the success of your campaign.

**Related topic**:

[Creating an email](https://docs.campaign.adobe.com/doc/standard/en/Videos/email_creation.mp4) video
