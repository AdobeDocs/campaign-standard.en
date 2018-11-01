---
title: Use cases
seo-title: Use cases
description: Use cases
seo-description: Learn how to use the Marketing Cloud Triggers integration with these different use cases.
page-status-flag: never-activated
uuid: 8996780b-4cec-4b52-b389-bab45ab802b2
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/integrating/using/use-cases
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-01-10T15 24 20.521-0500
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: marketing-cloud-triggers
cq-template: /apps/help/templates/article-3
discoiquuid: 506be235-5ddb-40e4-b97d-72cb6b0dfbc9
firstPublishExternalDate: 2018-01-10T15:24:20.514-0500
herogradient: light
jcr-created: 2018-01-11T19 02 37.084-0500
jcr-createdby: admin
jcr-description: Use cases
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-01-10T15:24:20.514-0500
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Use cases
publishexternaldate: 2018-01-10T15 24 20.514-0500
publishExternalURL: https://helpx.adobe.com/campaign/standard/integrating/using/use-cases.html
sha1: 5b0214e35162ec7f1c80306fb252053c12e904fc
topicBrowsingSortDate: 2018-01-10T15:24:20.514-0500
index: y
internal: n
snippet: y
---

# Use cases

Use cases

This section presents different use cases that can be implemented using the integration between Adobe Campaign and Marketing Cloud Triggers. You will find two examples of use cases:

* [Browse abandonment Trigger](../../integrating/using/use-cases.md#browse-abandonment-trigger): send a communication to customers who abandoned their visit on your website.
* [Search abandonment Trigger](../../integrating/using/use-cases.md#search-abandonment-trigger): reengage with visitors who made a search on your website, but didn't make a purchase.

>[!NOTE]
>
>The use cases described in this section rely on Marketing Cloud Visitor ID. It is also possible to implement them with Marketing Cloud Declared ID. Hashed and encrypted declared IDs are also supported. You can send emails/SMS to a profile which does not exist in Campaign by directly decrypting the encrypted email address/mobile number. But in this case, personalization using profile data can not be used.

## <p>Prerequisites</p>

In order for these use cases to be implemented, you need to have access to the following solutions/core services:

* Adobe Campaign
* Adobe Analytics
* Marketing Cloud Triggers Core Service

  ![](assets/trigger_uc_prereq_1.png)

* Marketing Cloud DTM Core Service

  ![](assets/trigger_uc_prereq_2.png)

* Marketing Cloud Visitor ID and Marketing Cloud People Core Service

  ![](assets/trigger_uc_prereq_3.png)

You also need to have a working website.

![](assets/trigger_uc_prereq_4.png)

>[!CAUTION]
>
>Sub-domain delegation is a deliverability key element. Make sure that the Adobe Campaign emails are sent from the same domain as the one used by the website.

## <p>Configuration</p>

**Marketing Cloud DTM Core Service**

1. In Marketing Cloud DTM Core Service (Dynamic Tag Management), activate Marketing Cloud ID and Adobe Analytics for your website pages.

   ![](assets/trigger_uc_conf_1.png)

1. ID reconciliation between the website, Adobe Analytics and Adobe Campaign requires to use aliasing. Create an alias, "visitorid" for example.

   ![](assets/trigger_uc_conf_2.png)

**Marketing Cloud People Core Service**

The alias previously referenced in DTM needs to be created in the Marketing Cloud People Core Service through a Customer Attribute. Make sure you create a new one and reference the same DTM alias in the integration code (for example "visitorid").

![](assets/trigger_uc_conf_3.png)

>[!NOTE]
>
>We are going to use this Customer Attribute in the Data source in Adobe Campaign (next step).

**Adobe Campaign**

1. Make sure you have **Event triggers** visible on your Adobe Campaign Standard instance. If you don't, contact the Adobe Campaign administrators.

   ![](assets/trigger_uc_conf_4.png)

1. You need to configure the aliases resolution in Adobe Campaign via a Data source (**Administration** > **Application Settings** > **Data Sources**). Make sure you choose the correct data source in the **AMC Data source** drop-down menu, which is mapped with the same Customer Attribute data source created in previous step.

   ![](assets/trigger_uc_conf_5.png)

## <p>Browse abandonment Trigger</p>

In this use case, we are going to create a simple trigger that will fire every time a client abandons a visit on the website. This example assumes you already have DTM collecting and pushing data to Adobe Analytics and have all your events created.

### <p>Creating a Marketing Cloud Trigger</p>

1. Select **Triggers** from the Marketing Cloud Activation Core Service menu. 

   ![](assets/trigger_uc_browse_1.png)

1. Choose a trigger type (**Abandonment** in our use case). 

   ![](assets/trigger_uc_browse_2.png)

1. For this use case, we need a simple abandonment trigger. The business purpose is to identify visitors who browse our trip booking website, look at the "Deals" page but don't book any trip. Once we identify this audience, we want to reach back to them within a short period of time. In this example, we choose to send the trigger after a period of 10 minutes.

   ![](assets/trigger_uc_browse_3.png)

### <p>Using the trigger in Adobe Campaign</p>

Now that we've created a Marketing Cloud Trigger, let's use it in Adobe Campaign.

In Adobe Campaign, you need to create a Trigger linked to the one you created in the Marketing Cloud.

1. To create the Trigger in Adobe Campaign, click the **Adobe Campaign** logo, in the top left corner, then select **Marketing plans** > **Transactional messages** > **Marketing Cloud Triggers**.

   ![](assets/trigger_uc_conf_4.png)

1. Click **Select an Analytics Trigger**. 

   ![](assets/trigger_uc_browse_4.png)

1. Select the Trigger you created earlier.

   ![](assets/trigger_uc_browse_5.png)

1. Publish the Trigger in Adobe Campaign. This process will automatically create a transactional message template.

   ![](assets/trigger_uc_browse_6.png)

1. Click the **Adobe Campaign** logo, in the top left corner, then select **Marketing plans** > **Transactional messages** > **Transactional messages**. 

   ![](assets/trigger_uc_conf_4.png)

1. Identify and select the newly created transactional message template.

   ![](assets/trigger_uc_browse_7.png)

1. Personalize its content and sender details.

   ![](assets/trigger_uc_browse_8.png)

1. Publish the message template. The trigger is now live and functional. 

   ![](assets/trigger_uc_browse_0.png)

### <p>Running the scenario</p>

1. This use case starts with an initial email sent to your audience with Adobe Campaign. 

   ![](assets/trigger_uc_browse_9.png)

1. The recipient opens the email.

   ![](assets/trigger_uc_browse_10.png)

1. He clicks on a link that brings him to your website. In this example, the banner brings the recipient to the home page of the trip booking website.

   ![](assets/trigger_uc_browse_11.png)

1. The recipient goes to the "Deals" page but suddenly stops his visit. After a 10 minute period, Adobe Campaign triggers the sending of the transactional message.

   ![](assets/trigger_uc_browse_12.png)

1. At any time, you can check the Marketing Cloud logs to see how many times the trigger fired.

   ![](assets/trigger_uc_browse_13.png)

1. You can also display the Adobe Campaign trigger report.

   ![](assets/trigger_uc_browse_14.png)

## <p>Search abandonment Trigger</p>

In this use case, we are going to create a trigger to reengage with visitors who went on our trip booking website, searched for a destination, found no successful results, and didn't book anything after that. The general process is the same as in the previous use case (see [Browse abandonment Trigger](../../integrating/using/use-cases.md#browse-abandonment-trigger)). We will focus here on how to personalize the remarketing email message.

### <p>Creating a Marketing Cloud Trigger</p>

Follow the steps described in the previous use case to create the Marketing Cloud Trigger. See [Creating a Marketing Cloud Trigger](../../integrating/using/use-cases.md#creating-a-marketing-cloud-trigger). The main difference is the trigger definition.

![](assets/trigger_uc_search_1.png)

The **Include Meta Data** section allows you to pass any data collected from Analytics to the Trigger payload. In this example, we create a custom eVar (for example, eVar 3) to collect the search term the visitor enters. This term will then be used in the transactional email message sent to the same visitor.

### <p>Using the trigger in Adobe Campaign</p>

1. Follow the steps described in the previous use case to create the trigger in Adobe Campaign. See [Using the trigger in Adobe Campaign](../../integrating/using/use-cases.md#using-the-trigger-in-adobe-campaign). The main difference is how we access and use, in Adobe Campaign, the meta data pushed in the Trigger payload. 
1. In the Search Abandonment trigger you created in Adobe Campaign, click on the **Event content and enrichment** icon to view the payload pushed to Adobe Campaign.

   ![](assets/trigger_uc_search_2.png)

1. As you can see, the custom eVar is passed in the Trigger payload and mapped to the **Event Context** table (ctx). We can now access it to personalize the transactional message.

   ![](assets/trigger_uc_search_3.png)

1. In this example, we choose to include the destination search term in the subject line as well as in the email body.

   ![](assets/trigger_uc_search_4.png)

1. When selecting a personalized field, look for your payload meta data in the **Transactional event** (rtEvent) table then in the **Event context** (ctx) sub table.

   ![](assets/trigger_uc_search_5.png)

### <p>Running the scenario</p>

1. The visitor goes on the trip booking website and searches for a destination. In this example, the visitor is looking for a trip to Japan but finds no result. This is an opportunity for us to reach back to this visitor and recommend an alternative travel plan.

   ![](assets/trigger_uc_search_6.png)

   >[!NOTE]
   >
   >In this use case, we assume the visitor/recipient has already opened and clicked on an email originating from the same website. This allows us to use and collect the VisitorID and map it to the recipient. We only need to do this once.

1. A few moments later, the same visitor/recipient receives a remarketing message. The message includes the recently searched destination.

   ![](assets/trigger_uc_search_7.png)

