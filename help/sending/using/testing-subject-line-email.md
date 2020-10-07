---
title: Testing the subject line of an email
description: Discover how to define the subject line of an email in the Email Designer.
page-status-flag: never-activated
uuid: 571ffc01-6e41-4501-9094-2f812b041a10
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: editing-email-content
discoiquuid: 39b86fda-7766-4e5f-ab48-bcc536ab66b3

---
# Testing the subject line of an email {#testing-a-subject}


## About predictive subject line {#about-predictive-subject-line}

When editing an email, you can try out different subject lines and get an estimation of its open rate before you send it.

This feature is disabled by default. It is enabled when the first model is imported. A model is the result of training data sets specific to a given industry. Models allow the system to predict the open rate of the email when a new subject line is submitted.

>[!NOTE]
>
>This feature is available for email messages and for databases that contain English contents only. The trained model will be inconsistent and will lead to erroneous results if your instance contains emails in other languages. The option that allows you to test a subject is only visible if a model is already available on your instance.

For more on importing models, see this [section](#importing-models).

## Testing the subject line {#testing-subject-line}

To test your subject line, follow the steps below:

1. Create or open your email.
1. Open the content and enter the subject of the email in the corresponding input field.
1. Click the **[!UICONTROL Test subject]** button to access the **[!UICONTROL Test your subject line]** window. You can still edit the subject from this window.
1. Select the correct model to be taken into account for the open rate prediction. Several models are available, each corresponding to a specific industry. For more on using models, see this [section](#importing-models).
1. Click **[!UICONTROL Test]**.

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

## Importing models {#importing-models}

By default, there is no model running on your Adobe Campaign server. There are two ways to get a model and activate the feature:

* You can train a local model from the data of your previous email messages.
* You can import pre-trained models that are specific to certain industries (medical, etc.) using the [package import](../../automating/using/managing-packages.md) feature.

### Training a local model {#training-local-model}

* If you are already using Adobe Campaign, the local model will be automatically trained on the messages that you have already sent.
* If you are new to Adobe Campaign, you can extract a CSV file from your previous system/ESP that contains 4 columns: date, subject, opens, sent. To do this, go to **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Email]** > **[!UICONTROL Subject Line Import]** and follow the instructions provided on the successive screens. When the subject upload is complete, import a local model as described below. The local model is automatically trained with the data you uploaded.
* If you are new to Adobe Campaign and cannot get a CSV file as described above, you can use a [pre-trained model](#pre-trained-models) or wait until you have enough delivery data in your system to train a local model. The system will automatically determine whether your current data set contains enough data to recognize patterns and to train the model.

>[!NOTE]
>
>There is no defined number of subject lines needed to train your own model. For more on this, see [Troubleshooting](#troubleshooting).
>
>You can only have one trained model on your instance.

To train a local model:
1. Download the subjectLineTraining.xml from [here](https://experience.adobe.com/#/downloads/content/software-distribution/en/campaign.html) and use the [package import](../../automating/using/managing-packages.md) feature to upload it to your Adobe Campaign instance. A technical workflow will automatically do the training for you.
1. The first time you want to train a model, an administrator can force the **[!UICONTROL SubjectLine Training workflow]** to start from the **[!UICONTROL Administration]** > **[!UICONTROL Application settings]** > **[!UICONTROL Workflows]** menu.
1. Once a model has been uploaded and trained, the feature is automatically activated and a new option appears next to the subject line field of your messages.
1. Then, the technical workflow will automatically continue to train your model every week.

### Importing pre-trained models {#pre-trained-models}

To access these models, click [here](https://experience.adobe.com/#/downloads/content/software-distribution/en/campaign.html). Use the [package import](../../automating/using/managing-packages.md) feature to upload a model to your Adobe Campaign instance.

The models that are available for use are:

* Cosmetic industry: subjectInsightCosmetic.xml
* Supermarket industry: subjectInsightSupermarket.xml
* Medical industry: subjectInsightMedical.xml
* Model to train: subjectlineTraining.xml.

These models cannot be trained.

Once a model has been uploaded, the feature is automatically activated and a new option appears next to the subject line field of your messages.

>[!NOTE]
>
>Importing and generating trained models can only be performed by an administrator.

## Troubleshooting {#troubleshooting}

Predictive subject line is a machine-learning process that takes into account all the subject lines that you have uploaded with their open rates. This allows the system to predict the open rate of an email when a new subject line is submitted.

To be able to train your own model, the subject lines need to be varied and must not have duplicates, no matter the number of subject lines that are used to train your model.

The quality of the subject lines is essential. If there is not enough quality data to process, or if all the previous subject lines are too similar, the system will not be able to train the model and you may get an error message. It means that your existing set of records does not allow to provide a reliable predictive suggestion.

In this case, you should review the data you are uploading and make sure the subject lines are varied enough to efficiently train your model.

<!--Some clients have reported this issue: I have had the subject line training workflow running for about a year now.  It has trained on 883 records and I am still seeing the message "The existing dataset is not enough to generate a model."  I do get an error in the workflow every time it runs "XML-110009 Unable to find the element 'runwf' of path '/' (document with schema 'serverConf')".

For this, campaign takes the subject line as training data and tries to come up with significant enough model to predict open rate with 95% confidence.

The 400 subject line number is mention with at least and is only indicative, model generation will also depend on quality of these lines.

It may happen that even 10k subject lines don't lead to model generation if they are too similar.

It means that it can be case that you don't have enough subject lines to generate the model and it is giving this error.

If you are getting an error/warning message, it means that your existing set of records is not enough for the predictive subject module to give a high confidence suggestion.

Adobe recommends reviewing the data you are uploading as the similarity of the subject lines might be the issue.-->
