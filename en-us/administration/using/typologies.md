---
title: Typologies
seo-title: Typologies
description: Typologies
seo-description: Improve your deliveries using typology rules.
page-status-flag: never-activated
uuid: e598b7e2-50b7-406d-a4df-a886bbee2bea
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/administration/using/typologies
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2017-11-28T11 04 14.217-0500
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: configuring-channels
cq-template: /apps/help/templates/article-3
discoiquuid: 87df79ad-3b14-4c42-8032-c4200d50d6ec
firstPublishExternalDate: 2017-11-16T10:52:26.229-0500
herogradient: light
isreadyforlocalization: false
jcr-created: 2017-11-29T19 03 43.623-0500
jcr-createdby: admin
jcr-description: Typologies
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2017-11-16T10:52:26.229-0500
lochandoffdate: 2017-11-28T11 04 14.215-0500
lr-lastreplicatedby: wmyersta@adobe.com
moreHelpPaths: /content/help/en/campaign/standard/administration/morehelp/configuring-channels;/content/help/en/campaign/standard/administration/morehelp/configuring-channels
navTitle: Typologies
publishexternaldate: 2017-11-16T10 52 26.229-0500
publishExternalURL: https://helpx.adobe.com/campaign/standard/administration/using/typologies.html
sha1: 8057c7ecb9059e8bca20f31cc236256af8e2ce9e
topicBrowsingSortDate: 2017-11-16T10:52:26.229-0500
index: y
internal: n
snippet: y
---

# Typologies

Typologies

## <p>About typologies</p>

A typology is a set of rules, executed during the message analysis phase, which allow the target, the content, and the configuration of the following elements to be validated: the subject, URL, images, unsubscription link, proof size, etc.

In Adobe Campaign, each message contains a link to a typology. This link is defined in the advanced parameters of the delivery template's properties (for more on this, refer to the [Preparation](../../administration/using/typologies.md#preparation) section).

>[!NOTE]
>
>Each message can only be assigned a single typology.

For each typology, the **Typology rules** section lists the set of rules for this typology.

![](assets/typology_typo-rule-list.png) 

### <p>Managing typologies</p>

Several typologies are present by default in the application. Based on your needs, you can create your own typologies or modify existing ones.

1. Access the **List of typologies** from the **Administration** > **Channels** > **Typologies** menu.
1. Select a typology to modify its content and properties or create a new one.

   ![](assets/typology_list.png)

1. Define the type of the typology. Typologies can be either Standard or Filtering typologies.
1. Add the typology rules you need using the **Add an element** button or remove the ones you do not want to use.

   You can modify the order in which the rules are applied for a given typology. To do this, move the elements to modify the order in which they appear on the screen. The numbers corresponding to the execution order are then automatically recalculated. The rule application mode is presented in the [Typology rules execution order](../../administration/using/typologies.md#typology-rules-execution-order) section.

   The rules displayed on this screen can be accessed in read-only mode.

Your typology is ready to be used. You can select it in message properties or in message template properties.

>[!NOTE]
>
>The **IP affinity** field allows you to manage the affinities according to your configuration. These are defined in the instance's configuration file. If you want to use the affinities, contact your administrator.

### <p>Typology rules</p>

Typology rules are business rules that are applied during the message preparation. They are used to check whether a message is valid and meets your quality criteria. They also check if each each member of the target audience is eligible to receive the message.

Typology rules are available under the **Administration** > **Channels** > **Typologies** > **Typology rules** menu.

There are two types of rules:

* **Filtering** rules: allow you to exclude one part of the message target according to criteria defined in a query, such as quarantined recipients or recipients that have already been sent a certain number of emails. See [Filtering rules](../../administration/using/typologies.md#filtering-rules).
* **Fatigue** rules: allow you to define a maximum number of messages per profile to avoid over-soliciting them. See [Fatigue rules](../../administration/using/typologies.md#fatigue-rules).
* **Control** rules: allow the user to check the validity and quality of the messages before they are sent, such as character display, SMS message size, address format, etc. See [Control rules](../../administration/using/typologies.md#control-rules).

A typlogy rule can be applied to only one channel or to all channels.

![](assets/typology_channel.png)

In the **Properties** of a typology rule, you can set its execution order. When several rules have to be applied, the execution order of each rule determines the ones to process first. For more on this, refer to the [Typology rules execution order](../../administration/using/typologies.md#typology-rules-execution-order) section.

![](assets/typology_rule-order.png)

A typology rule can be deactivated through its **Properties** if you do not want the rule to be applied at the moment that the messages concerned by the rule are analyzed.

![](assets/typology_rule-active.png)

>[!NOTE]
>
>As the content of the control rules cannot be modified, they are essentially filtering rules that are used.

### <p>Typology rules execution order</p>

The typology rules are executed in an order specified during the targeting, analysis, and message personalization phases.

In standard operation mode, the rules are applied in the following sequence:

1. Control rules, if they are applied at the start of targeting.
1. Filtering rules:

    * Native application rules for address qualification: defined address / non-verified address / blacklisted address / quarantined address / address quality.
    * Filtering rules defined by the user.

1. Control rules, if they are applied at the end of targeting.
1. Control rules, if they are applied at the start of personalization.
1. Control rules, if they are applied at the end of personalization.

However, you can adapt the execution order of the same type of rules in each typology. Indeed, when multiple rules are executed during the same message processing phase, you can choose the order in which they are applied.

For example, a filtering rule whose execution order is positioned at number 20 will be executed before a filtering rule whose execution order is positioned at number 30.

## <p>Filtering rules</p>

Filtering rules allow you to exclude one part of the message target according to criteria defined in a query, such as quarantined recipients or recipients that have already been sent a certain number of emails.

For example, you can filter the newsletter subscribers so that the subscribers that are younger than 18 years old never receive communications.

### <p>Creating a filtering rule</p>

1. Create a **Filtering** typology rule, one that can be applied on all communication channels.

   ![](assets/typology_create-rule.png)

1. In the **Filtering criteria** tab, select the subscriptions in the **Subscription** category.

   ![](assets/typology_create-rule-subscription.png)

1. In the **Explorer** tab of the query editor, drag and drop the **Subscriber** node into the main part of the screen.

   ![](assets/typology_create-rule-subscriber.png)

1. Select the **Age** field and define the filtering conditions so that the age of the subscribers is 18 or above.

   ![](assets/typology_create-rule-age.png)

1. In the **Typologies** tab, link this rule to a typology.

   ![](assets/typology_create-rule-typology.png)

1. Make sure that the typology in question is selected in the delivery template that you want to use.

   ![](assets/typology_template.png)

   >[!NOTE]
   >
   >To access the delivery templates, select **Resources** > **Templates** in the navigation menu, which can be accessed via the Adobe Campaign logo.

Whenever this rule is used in a message, the subscribers who are considered minors will be automatically excluded.

### <p>Restricting the applicability of a filtering rule</p>

You can restrict the applicability of a filtering rule according to the message to send.

1. In the typology rule's **Application criteria** tab, uncheck the **Apply the rule on all deliveries** option, which is enabled by default.

   ![](assets/typology_limit.png)

1. Use the query editor to define a filter. For example, you can apply the rule only on messages whose label starts with a given word or whose ID contains certain letters.

   ![](assets/typology_limit-rule.png)

In this case, the rule is only applied to the messages that correspond to the defined criteria.

### <p>Default deliverability exclusion rules</p>

Two filtering rules are available by default: **Exclusion of addresses** (**addressExclusions**) and **Exclusion of domains** (**domainExclusions**). During the email analysis, these rules compare the recipient email addresses with the forbidden addresses or domain names contained in an encrypted global suppression list managed in the deliverability instance. If there is a match, the message is not sent to that recipient.

This is to avoid being blacklisted due to malicious activity, especially the use of a Spamtrap. For example, if a Spamtrap is used to subscribe via one of your web forms, a confirmation email is automatically sent to that Spamtrap, and this results in your address being automatically blacklisted.

>[!NOTE]
>
>The addresses and domain names contained in the global suppression list are hidden. Only the number of excluded recipients is indicated in the delivery analysis logs.

## <p>Fatigue rules</p>

### <p>About fatigue rules</p>

Fatigue rules allow marketers to set global cross-channel business rules that will automatically exclude oversollicited profiles from campaigns.

To implement fatigue rules, you define a maximum number of messages per profile and select a period on which the rule will apply. During delivery preparation, profiles are excluded from the delivery if applicable, depending on the number of deliveries already sent to them.

>[!NOTE]
>
>For fatigue rules to apply, you need to define a contact date for your delivery. If you choose to send messages immediately, the fatigue rule will not be applied.

Related topics:

* [Preparation](../../administration/using/typologies.md#preparation)
* [Managing typologies](../../administration/using/typologies.md#managing-typologies)
* [Typology rules](../../administration/using/typologies.md#typology-rules)

### <p>Creating a fatigue rule</p>

To create and configure a **Fatigue** typology rule, apply the following steps:

1. Click the Adobe Campaign logo, in the top left corner of the interface, then select **Administration** > **Channels** > **Typologies** > **Typology rules**.

   ![](assets/fatigue4.png)

1. From the list of typology rules, click **Create**.

   ![](assets/fatigue.png)

1. In the **Rule type** field, select **Fatigue**.

   ![](assets/fatigue3.png)

1. In the **Channel** field, select which channel your rule will apply to. You can either select a single channel (email, SMS, direct mail, mobile application) or select **All channels**. See [Choosing the channel](../../administration/using/typologies.md#choosing-the-channel).

   ![](assets/fatigue5.png)

1. In the **General** tab, define the method for calculating the maximum number of messages per profile. You can choose either a constant threshold or a variable. You can also refine the threshold on profiles and deliveries. For more on this, refer to [Defining the threshold](../../administration/using/typologies.md#defining-the-threshold).

   ![](assets/fatigue2.png)

1. Choose a **Sliding period** on which the typology rule will apply. For more on this, refer to [Setting the sliding period](../../administration/using/typologies.md#setting-the-sliding-period).

   ![](assets/fatigue6.png)

   In this example (see previous screenshots), we choose to send a maximum number of 4 messages over a sliding period of 15 days.

1. In the **Application criteria** tab, you can choose to apply this rule to all deliveries or restrict the applicability of the rule according to the message to send. The rule will only execute if the application condition is met. For example, you can apply the rule only on messages with a label starting with a given word or with an ID containing certain letters. See [Restricting the applicability of a filtering rule](../../administration/using/typologies.md#restricting-the-applicability-of-a-filtering-rule).

   ![](assets/fatigue20.png)

1. Select the **Typologies** tab and link your typology rule to the typology used for your deliveries. See [Managing typologies](../../administration/using/typologies.md#managing-typologies) and [Typology rules](../../administration/using/typologies.md#typology-rules).

   ![](assets/fatigue12.png)

   >[!NOTE]
   >
   >The typology can be defined in the delivery template, to be applied automatically to all deliveries created using this template.

During delivery preparation, profiles are excluded from the delivery if applicable, depending on the number of deliveries already sent to them. You can view the fatigue rule execution results in the delivery logs. See [Viewing the fatigue results](../../administration/using/typologies.md#viewing-the-fatigue-results).

![](assets/fatigue16.png)

>[!CAUTION]
>
>For fatigue rules to work, you need to define a contact date for your delivery. If you choose to send messages immediately, the fatigue rule will not be applied.

### <p>Choosing the channel</p>

Fatigue rules are available for various channels. The channel is defined in the **Channel** field of the typology rule settings. You can either select a single channel or select **All channels**.

![](assets/fatigue5.png)

**Available channels**

The following channels are available:

* Email
* Mobile (SMS)
* Direct mail
* Mobile application: this channel allows you to send push notifications to profiles or to app subscribers. If you choose to send notifications to profiles, they will be compatible with multi-channel fatigue rules. If you're sending messages to app subscribers, the fatigue rule will be limited to the mobile application channel only.
* All channels: this option allows you to apply the rule to all channels. For example, you can decide to send a maximum of 3 messages per month on any channel. If you sent 2 emails to a profile last week and you try sending a push notification today, the same profile will be excluded.

**Delivery types**

Fatigue rules are compatible with all delivery types: one-shot deliveries, recurring deliveries, workflow deliveries and transactional messages.

**Transactional messaging** can be used to send service messages targeting an event (rtEevent) as well as remarketing messages (targeting profiles), for example a remarketing message. Fatigue rules are compatible with marketing messages only (targeting profiles). Event transactional messages do not contain profile information, therefore they are not compatible with fatigue rules (even in the case of an enrichment with profiles). With the support of marketing messages in transactional messaging, you can **apply a fatigue rule to all channels including marketing transactional messages**.

### <p>Defining the threshold</p>

Each fatigue rule defines a threshold, that is to say the maximum number of messages that can be sent to one profile over a given period. Once this threshold has been reached, no more deliveries can take place until the end of the period considered. This process lets you automatically exclude a profile from a delivery if a message exceeds the set threshold, thus avoiding over-solicitation.

Threshold values can be either constant or variable. This means that for a given period, thresholds can vary from one profile to another, or even for the same profile.

**Using a fix threshold**

The threshold represents the highest number of messages that can be sent to a profile during the concerned period.

By default, the threshold is constant and you need to indicate a maximum number of messages authorized by the rule.

![](assets/fatigue2.png)

**Using a variable threshold**

To define a variable threshold, select the **Depends on the recipient** value in the **Threshold type** field. 

![](assets/fatigue15.png)

You then have two options:

* select a profile field: the threshold will vary for each profile according to the selected field. For example, if you have extended the profiles resource with a 'Communication frequency' field, click the button on the right of the **Threshold computation formula** field and select your field. For each profile, the threshold will take the value of the 'Communication frequency' field.

  ![](assets/fatigue21.png)

* define a formula: click the second button on the right of the **Threshold computation formula** field to define an advanced threshold calculation formula. For example, you can index the number of authorized messages according to the segment to which the profile belongs. This means that a profile belonging to the 'Web' segment may receive more messages than other profiles. An **Iif (@origin='Web', 5, 3)** type formula authorizes the delivery of 5 messages to profiles of the Web segment and 3 for other segments. 

  ![](assets/fatigue14.png)

**Refining the threshold on profiles and deliveries**

By default, all messages are taken into account for threshold calculation. Check the **Refine Threshold on profiles and deliveries** box to filter the profiles and deliveries to count when preparing the delivery.

In the following example, only male profiles are counted and only deliveries with a label starting with **Newsletters** are counted.

![](assets/fatigue13.png)

Refining the threshold on deliveries is different than restricting the applicability of the entire rule (**Application criteria** tab):

* **Application criteria**: you choose to execute the rule or not according to specific criteria. For example, if your application condition is 'Label starts with Newsletter', the rule will only apply to deliveries which respect this condition. If the delivery's label starts with 'Promotion', the rule will not execute at all.
* **Refine threshold on profiles and deliveries > Deliveries to count**: all deliveries using this typology rule will execute the rule, but you decide, among the past and scheduled deliveries, which ones you want to count. For example, if your restriction is 'Label starts with Newsletter', the rule will be executed even if the delivery label starts with 'Promo'. It will count, over the selected sliding period, the number of deliveries whose label starts with 'Newsletter'.

### <p>Setting the sliding period</p>

Fatigue rules are defined in n-day rolling periods. The period is configured in the **Sliding period** section, for example 2 weeks, 7 days or 5 hours. 

![](assets/fatigue6.png)

When the rule executes, both past deliveries and scheduled deliveries are taken into account. This guarantees that, on a given sliding period, the threshold is never exceeded.

For example, if you define a 48-hour period, the system will be looking 48 hours **before the contact date ** and 48 hours **after the contact date **. So, the selected period is doubled to enable the integration of future deliveries as well as previous ones.

To restrict the deliveries taken into account to a 2-week period, enter **Day** and **7** or 1 week in the **Sliding period** section. Deliveries sent up to 7 days before the delivery date and scheduled up to 7 days after the delivery date on which the rule is applied will be taken into account in the calculation.

### <p>Viewing the fatigue results</p>

During delivery preparation, profiles are excluded from the delivery if applicable, depending on the number of deliveries already sent to them. To view fatigue rule execution results, click the button in the bottom right corner of the **Deployment** block. 

![](assets/fatigue22.png)

Three tabs are available, showing you the details of the fatigue execution results including the name of the rule that applied:

* Delivery logs:

  ![](assets/fatigue17.png)

* Exclusion logs:

  ![](assets/fatigue18.png)

* Exclusion causes:

  ![](assets/fatigue19.png)

### <p>Examples</p>

There are many possibilities in terms of fatigue management implementation. Here are some examples of what you can do:

* Create a fatigue rule using a **constant threshold** that applies to **all channels**:

  Let's say you create a multi-channel rule, with a constant threshold of 3 over a sliding period of 7 days.

  Last week, your premium profiles received a promotion email and a transactional remarketing email. You also scheduled an SMS that will be sent next week. Today, you decide to send a push notification targeting all your profiles. The premium profiles will be excluded from today's push because their maximum number of messages over a 2-week period has already been reached.

  ![](assets/fatigue23.png)

* Create a fatigue rule using a **variable threshold** based on a **profile field**:

  You have extended the profiles resource with a 'Communication limit' field, to define a different threshold for each profile. In your fatigue rule, define a variable threshold based on this field and select a sliding period of 2 days. Let's take two examples of profiles: John has a communication limit of 1 and David has a threshold of 2. Both have already received a newsletter email yesterday. You decide to send them another email today. Only David will receive it, because John has been excluded from the target. 

  ![](assets/fatigue24.png)

* Create a fatigue rule using a **threshold computation formula**:

  You want to change the threshold according to the age of your profiles. If a profile is under 40, you want to define a limit of 4 and for older profiles, a limit of 2. Instead of defining this threshold for each profile with an extended field, you can create a formula directly in your fatigue rule to calculate the threshold according to the profiles' age. In our example, the formula would be **Iif (@age&lt;40, 4, 2)**. 

  ![](assets/fatigue25.png)

  >[!NOTE]
  >
  >This section also includes a step-by-step example of a fatigue rule using a threshold computation formula.

* Create a fatigue rule that **refines the threshold** on profiles and deliveries:

  You have extended the profiles resource with a 'Score' field and you also have extended the deliveries resource with a 'Type' field. You want to define a constant threshold of 3 but you want to exclude from the count all the deliveries of the type 'Alert' or 'Black Friday' and all the profiles with a score greater than 10. When the rule will execute, it will count, among the past and scheduled deliveries, all the deliveries that are not of the type 'Alert' or 'Black Friday' sent to profiles whose score is smaller than 10. 

  ![](assets/fatigue26.png)

Here is a step-by-step example of a fatigue rule using a threshold computation formula.

In this use case, we want to create a typology rule to prevent the delivery of more than 2 messages per week to premium profiles and 2 messages per week to standard profiles.

To identify customers and prospects, we extended the profiles resource with the **Status** field, which contains 0 for premium profiles and 1 for standard profiles.

To create the rule, apply the following steps:

1. Create a new **Fatigue** type typology rule.
1. In the **Threshold** section, we want to create a formula to calculate the threshold depending on each profile. Select the **Depends on the recipient** value in the **Threshold type** field, then click the icon the second button on the right of the **Threshold computation formula** field.

   ![](assets/fatigue7.png)

1. In the **List of functions** section, double-click the **Iif** function in the **Others** node.

   ![](assets/fatigue8.png)

1. Then select the profile' **Status** in the **Available fields** section.

   ![](assets/fatigue9.png)

1. Enter the desired values to create the following formula: **Iif(@status=0,2,4)**

   ![](assets/fatigue10.png)

   This formula lets you assign the value 2 if the status equals 0, and the value 4 for all other statuses.

1. Click **Confirm** to approve the formula. 
1. Indicate the **Sliding period** on which the rule will apply: 7 days in this case, to restrict the deliveries taken into account to a 2-week period.

   ![](assets/fatigue11.png)

1. Now link the rule which you have just created to a typology in order to apply it to your deliveries. To do this, select the **Typologies** tab, click **Create element** and select the typology used for your deliveries.

   ![](assets/fatigue12.png)

1. Save the rule to approve creation.

The rule will be applied to all deliveries based on the typology.

## <p>Control rules</p>

Control rules allow the user to check the validity and quality of the messages before they are sent, such as character display, SMS message size, address format, etc.

A set of default rules available in Adobe Campaign ensures the standard controls:

* **Check subject** (email): checks that the subject and sender address do not contain special characters which may cause problems on certain mail transfer agents, and checks that the message subject has been completed.
* **Check URL labels** (email): checks that each tracking URL has a label.
* **Check URLs** (email): checks the tracking URLs (presence of the "&" character).
* **Check proof size** (all channels): generates an error message if the proof target population exceeds 100 recipients.
* **Check unsubscription link** (email): checks for the presence of at least one unsubscription (opt-out) URL in each content (HTML and Text).
* **Check delivery size** (all channels): checks the size of the messages.
* **Check social network sharing link** (email): checks the presence of a link to a mirror page when including a social network sharing link (ViralLinks) in the content.
* **A/B Test**: extracts the test population for a delivery with an A/B test.

You can choose the moment at which the rule will be applied from one of the phases of the delivery's life cycle. Select the value to apply in the drop-down list from the **Phase** field of the typology rule.

![](assets/typology_phase.png)

Possible values are:

* **At the start of targeting**

  The control rule can be applied at this phase so that the personalization step is not executed in the event of an error.

* **After targeting**

  If you need to know the volume of the target in order to apply the control rule, select this phase.

  For example, the **Check proof size** control rule applies after the targeting stage: this rule prevents the preparation of message personalization if there are too many proof recipients.

* **At the start of personalization**

  This phase must be selected if the check concerns approving message personalization. Message personalization is carried out during the analysis phase.

* **At the end of the analysis**

  When a check requires message personalization to be complete, select this phase.

