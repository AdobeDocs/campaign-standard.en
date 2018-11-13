---
title: Personalizing the subject line of an email
seo-title: Personalizing the subject line of an email
description: Personalizing the subject line of an email
seo-description: You can personalize the subject of an email, but also try out different subject lines and get an estimation of its open rate.
uuid: b9f4ba67-5d1e-47f5-836a-f4b6b691a67e
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/designing/using/personalizing-the-subject-line-of-an-email
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-10T07 25 23.844-0400
cq-lastreplicated: 2018-09-07T15 02 19.558-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: personalizing-content
cq-template: /apps/help/templates/article-3
discoiquuid: d366cb2e-cc51-4579-ad6e-9989087e018c
firstPublishExternalDate: 2018-09-07T15:02:16.550-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-07-23T07 30 13.819-0400
jcr-createdby: admin
jcr-description: Personalizing the subject line of an email
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T15:02:16.550-0400
lochandoffdate: 2018-09-10T07 25 23.842-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Personalizing the subject line of an email
publishexternaldate: 2018-09-07T15 02 16.550-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/designing/using/personalizing-the-subject-line-of-an-email.html
sha1: 026d7e797749aab50e8eaa4098f482eb8c7f9ca5
topicBrowsingSortDate: 2018-09-07T15:02:16.550-0400
index: y
internal: n
snippet: y
---

# Personalizing the subject line of an email{#personalizing-the-subject-line-of-an-email}

Personalizing the subject line of an email

## Personalizing an email subject {#personalizing-an-email-subject}

The message subject is mandatory to prepare and send the message. It can be configured by clicking on the email label.

![](assets/email_designer_subject.png)

By clicking the **Edit** button, you can also add personalization fields and dynamic content to the subject line.

## Predictive subject line {#predictive-subject-line}

When editing an email, you can try out different subject lines and get an estimation of its open rate before you send it.

This feature is disabled by default. It is enabled when the first model is imported. A model is the result of training data sets specific to a given industry. Models allow the system to predict the open rate of the email when a new subject line is submitted.

>[!NOTE]
>
>This feature is available for email messages and for databases that contain English contents only. The trained model will be inconsistent and will lead to erroneous results if your instance contains emails in other languages. The option that allows you to test a subject is only visible if a model is already available on your instance.

### Testing a subject {#testing-a-subject}

To test your subject line:

1. Create or open your email.
1. Open the content and enter the subject of the email in the corresponding input field.
1. Click the **Test subject** button to access the **Test your subject line** window. You can still edit the subject from this window.
1. Select the correct model to be taken into account for the open rate prediction. Several models are available, each corresponding to a specific industry.
1. Click **Test**.

Your subject is then analyzed.

>[!NOTE]
>
>If the subject line is too short, it cannot be analyzed and an error message is displayed.

Several indicators are calculated and a set of tools are displayed to help you:

* **Predicted open rate**: This chart gives you an idea of the open rate you can expect for the email with its current subject.
* **Subject length**: This indicator lets you see if the current length of the subject is correct or whether it would need to be longer or shorter.
* **Colored words**: When testing the subject, words highlighted in green are the words that contribute the most to increasing the open rate prediction. Words highlighted in red are the words that contribute the least to increasing the open rate prediction. If you add or remove words in the subject, highlighted words will change.
* **Categories and word suggestions**: Towards the lower part of the window, a number of relevant categories for the selected model are displayed. These categories are sorted by order of importance and they allow you to see whether your subject contains words that are associated with it via a check symbol. Each category contains a set of suggested words that could be used in your subject to make it more relevant and increase the open rate. These words are the words that are used the most often in a given category.

>[!NOTE]
>
>Personalization fields and punctuation marks are stripped from the subject analysis. In the case of dynamic/conditional text, all variants are considered as one subject line.

![](assets/predictive_subject_line_example.png)

### Importing models {#importing-models}

By default, there is no model running on your Adobe Campaign server. There are two ways to get a model and activate the feature:

* You can train a local model from the data of your previous email messages:

    * If you are already using Adobe Campaign, the local model will be automatically trained on the deliveries that you have already sent.
    * If you are new to Adobe Campaign, you can extract a CSV file from your previous system/ESP that contains 4 columns: date, subject, sent, opens. To do that, go to **Administration** > **Channels** > **Email** > **Subject Line Import** and follow the instructions provided on the successive screens. When the subject upload is complete, import a local model as described below. The local model is automatically trained with the data you uploaded.
    * If you are new to Adobe Campaign and cannot get a CSV file as described above, you can use a pre-trained model or wait until you have enough delivery data in your system to train a local model. The system will automatically determine whether your current data set contains enough data to recognize patterns and to train the model.

      >[!NOTE]
      >
      >You need at least 400 subject lines in order to be able to train your own model. If there is not enough data to process, the system will not be able to train the model. You can only have one trained model on your instance.

  To train a local model, download the subjectLineTraining.xml from [here](https://support.neolane.net/webApp/downloadCenter?__userConfig=psaDownloadCenter) and use the [package import](../../automating/using/managing-packages.md) feature to upload it to your Adobe Campaign instance. A technical workflow will automatically do the training for you.

  The first time you want to train a model, an administrator can force the **SubjectLine Training workflow** to start from the **Administration** > **Application settings** > **Workflows** menu.

  Once a model has been uploaded and trained, the feature is automatically activated and a new option appears next to the subject line field of your messages.

  Then, the technical workflow will automatically continue to train your model every week.

* You can import pre-trained models that are specific to certain industries (medical, etc.) using the [package import](../../automating/using/managing-packages.md) feature. These models are available [here](https://support.neolane.net/webApp/downloadCenter?__userConfig=psaDownloadCenter) and cannot be trained.

  Once a model has been uploaded, the feature is automatically activated and a new option appears next to the subject line field of your messages.

>[!NOTE]
>
>Importing and generating trained models can only be performed by an administrator.

The models that are available for use are:

* Cosmetic industry: subjectInsightCosmetic.xml
* Supermarket industry: subjectInsightSupermarket.xml
* Medical industry: subjectInsightMedical.xml
* Model to train: subjectlineTraining.xml.

