---
title: Use the Microsoft Dynamics 365 integration
description: Learn how to use the Microsoft Dynamics 365 with Campaign Standard integration
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-ms-dynamics
---

# Using the Microsoft Dynamics 365 integration

There are several data flows that the Adobe Campaign Standard Integration with Dynamics 365 performs:

* Dynamics 365 to Adobe Campaign

    * Send *contacts* from Dynamics 365 into Campaign
    * *Custom entities*: Bring in custom tables from Dynamics 365 to Campaign. Learn more [in this section](../../integrating/using/d365-acs-self-service-app-workflows.md).
    * This is also known as **"Ingress"** (referring to the ingress of data from Dynamics 365 to Adobe Campaign Standard)

* Adobe Campaign to Dynamics 365     
    * Email marketing events from Adobe Campaign Sandard are sent to Dynmics 365 (email send, open, click, bounce)
    * This is also known as **"Egress"** (referring to the egress of data from Adobe Campaign Standard to Dynamics 365)

* Opt-out
    * Opt-out statuses (e.g., denyList) can be synchronized from Dynamics 365 to Campaign or from Campaign to Dynamics 365. The data can also by synchronized bidirectionally (i.e. data flows in both directions).  You can read more about the basics of opt-out in the [Opt-Out Flow](#opt-out) section below.

More details on the data flows can be found further down in this document in the [Data Flows](#data-flows)  section.

## Adobe Campaign Standard User Experience

When a contact is created, modified, or deleted (if deleted is enabled) in Dynamics 365, it will be sent over to Campaign Standard. These contacts will be visible in the Profiles screen in Campaign and can be targeted in marketing campaigns. See the Profiles screen below.

![](assets/MSdynamicsACS-usage1.png)

When an opt-out attribute is modified in Campaign, it will be reflected in Dynamics 365 if you’ve selected the Campaign-to-Dynamics 365 or bi-directional opt-out configuration, and if you have that particular attribute mapped correctly.

## Microsoft Dynamics 365 User Experience

For egress, the following email marketing events are sent from Campaign to Dynamics 365 and displayed in the Dynamics 365 Timeline view as custom activities:

* Adobe Campaign Email Send

* Adobe Campaign Email Open

* Adobe Campaign Email URL Click

* Adobe Campaign Email Bounce

To view a contact’s Timeline, navigate to your contacts list by clicking on Sales Hub from the Dynamics 365 drop down menu. Then click on Contacts on the left hand menu bar and select a contact.

>[!NOTE]
>
>The "Adobe Campaign for Dynamics 365" app in AppSource will need to be installed in your Dynamics 365 instance in order to view these events. [This article](../../integrating/using/d365-acs-configure-d365.md#install-appsource-app) explains more about configuring Dynamics 365 and installing this app.

Below you can see a snapshot of the Contact screen for "Dynamics User". In the Timeline view, you you’ll notice that Dynamics User was sent an email associated with Campaign Name "2019LoyaltyCamp" and Delivery Name "DM190". Dynamics User opened the email and also clicked a URL in the email; both of these actions created events which also show below. If you look to the right corner, you’ll see the Relationship Assistant (RA) card; currently, it contains a task to follow up on the clicked URL.

![](assets/do-not-localize/MSdynamicsACS-usage4.png)

See below for a close up of the Timeline view for Dynamics User.

![](assets/do-not-localize/MSdynamicsACS-usage5.png)

Below is a close up of the Relationship Assistant (RA) card. The AppSource app contains a workflow that watches for an Adobe Email URL Click event. When this event occurs, it creates a task and sets a due date. This allows the task to show up in the RA card, giving it additional visibility. There is a similar workflow for Adobe Email Bounce events, adding a task to reconcile the invalid email address. These workflows can be turned off in the solution.

![](assets/do-not-localize/MSdynamicsACS-usage6.png)

If you click on the subject of the send event, you’ll see a form similar to the one below. The forms for open and bounce events are similar.

![](assets/do-not-localize/mirror_page_url_send.png)

The form for email url click events adds an additional attribute for the URL that was clicked:

![](assets/do-not-localize/mirror_page_url_click.png)

The following is a list of the attributes and a description:

* Subject: Subject of the event; composed of the Campaign ID and Delivery ID of the email delivery

* Owner: The application user that is created in the post-provisioning steps

* Regarding: The name of the contact

* Campaign Name: The Campaign ID in Campaign Standard

* Delivery Name: The Delivery ID in Campaign Standard

* Date Sent/Opened/Clicked/Bounced: Date/time when the event was created

* Tracking URL: URL that was clicked

* Mirror Page URL: The URL to the mirror page of the email that was sent/opened/clicked/bounced

>[!NOTE]
>
>The expiry period of the email mirror page can be modified in the configuration screen of the corresponding Campaign email channel activity (see [Validity period parameters](../../administration/using/configuring-email-channel.md#validity-period-parameters)).

>[!NOTE]
>
>For opt-out, when an opt-out attribute is modified in Dynamics 365, it will be reflected in Campaign if you’ve selected the Dynamics 365-to-Campaign or bi-directional opt-out configuration, and if you have that particular attribute mapped correctly.

## Data Flows {#data-flows}

### Contact and custom entity Ingress

New, updated, and deleted records (Note: deleted must be enabled) are sent from the Dynamics 365 contact table to the Campaign profile table.

Table mappings can be configured in the integration application UI to map Dynamics 365 table attributes to Campaign table attributes. The table mappings can be modified to add/remove attributes, as needed.

The initial run of the data flow is designed to transfer all mapped records, including those marked as "inactive"; subsequently, the integration will only process incremental updates. The exception to this is if the data is replayed or if a filter is configured; basic, attribute-based, filtering rules can be configured to determine which records to sync to Campaign.

Basic replacement rules can be configured in the integration application UI to replace an attribute value with a different value (e.g., "green" for "#00FF00", "F" for 1, etc.).

Depending on the volume of records, your Campaign SFTP storage may need to be utilized for the initial data transfer.  See the section on [Initial Data Transfer](#initial-data-transfer) for more information.

The Campaign profile table attribute externalId must be populated with the Dynamics 365 contact attribute contactId in order for contact ingress to work. Campaign custom entities must also be populated with a Dynamics 365 unique ID attribute; however, this attribute can be stored in any Campaign custom entity attribute (i.e., doesn’t have to be externalId).

>[!NOTE]
>
>For custom entity ingress, change tracking must be enabled within Dynamics 365 for synchronized custom entities.

#### Custom Entities

The [Microsoft Dynamics 365-Adobe Campaign Standard integration](../../integrating/using/d365-acs-get-started.md) supports custom entities, enabling custom entities in Dynamics 365 to be synchronized to corresponding custom resources in Campaign.

The new data in the custom resources can be used for several purposes, including segmentation and personalization.

The integration supports both linked and non-linked tables. Linking is supported up to three levels (i.e., level1->level2->level3).

>[!CAUTION]
>
>If any Campaign custom resource record contains personal information, specific recommendations apply. Learn more [in this section](../../integrating/using/d365-acs-notices-and-recommendations.md#privacy-linked-resources).

When configuring custom entity data flows, it is important to be aware of the following:

* Creating and modifying Campaign custom resources are sensitive operations which must be performed by expert users only.
* For custom entity data flows, change tracking must be enabled within Dynamics 365 for synchronized custom entities.
* If a parent and linked child record are created close to the same time in Dynamics 365, due to the parallel processing of the integration, there is a slight chance that a new child record could be written to Campaign before its parent record.

* If the parent and child are linked on the Campaign side using the **1 cardinality simple link** option, the child record will remain hidden and inaccessible (via UI or API) until the parent record arrives in Campaign.

* (Assuming **1 cardinality simple link** in Campaign) If the child record is updated or deleted in Dynamics 365, and that change is written to Campaign before the parent record shows up in Campaign (not likely, but a remote possibility), that update or delete will not be processed in Campaign and an error will be thrown. In the case of update, the record in question will need to be updated in Dynamics 365 again in order to sync the updated record. In the case of delete, the record in question will need to be taken care of separately on the Campaign side since there is no longer a record in Dynamics 365 to delete or update.

* If you run into a situation where you believe you have hidden child records and no way to access them, you can temporarily change the cardinality link type to **0 or 1 cardinality simple link** to access those records.

A more comprehensive overview of Campaign custom resources can be found [in this section](../../developing/using/key-steps-to-add-a-resource.md).

### Email Marketing Event Flow{#email-marketing-event-flow}

Email marketing events are sent from Campaign to Dynamics 365 to appear in the Timeline view.

Supported marketing event types:
* Send – email sent to recipient
* Open – email opened by recipient
* Click – URL within email clicked by recipient
* Bounce – email to recipient experienced a hard bounce

The following event attributes are displayed within Dynamics 365:
* Marketing campaign name
* Email delivery name
* Timestamp
* Email mirror page URL
* URL clicked (click events only)

Email Marketing Events can be enabled/disabled by type (send, open, click, bounce) so that only the event types you select will be passed to Dynamics 365.

### Opt-Out Flow {#opt-out-flow}

Opt-out (e.g., denyList) values are synchronized between systems; you have the following options to choose from when onboarding:
* Dynamics 365 is source of truth for opt-outs: opt-out attributes will be synchronized in one direction from Dynamics 365 to Campaign Standard
* Campaign Standard is the source of truth for opt-outs: opt-out attributes will be synchronized in one direction from Campaign Standard to Dynamics 365
* Dynamics 365 AND Campaign Standard are both sources of truth: opt-out attributes will be synchronized bi-directionally between Campaign Standard and Dynamics 365

Alternatively, if you have a separate process to manage opt-out synchronization between the systems, the integration's opt-out data flow can be disabled.

>[!NOTE]
>
>In the integration application UI, the uni-directional ACS to Dynamics 365 and the bi-directional opt-out use cases are configured in a separate opt-out workflow. The uni-directional Dynamics 365 to ACS opt-out use case is an exception; it is configured within the ingress (Contact to Profile) workflow.

Opt-out flow mapping is to be specified by the customer since business requirements can differ between companies. On the Campaign side, only the OOTB opt-out attributes can be used for opt-out mapping:

* denyList
* denyListEmail
* denyListFax
* denyListMobile
* denyListPhone
* denyListPostalMail
* denyListPushnotification
* ccpaOptOut

In Dynamics 365, most opt-out fields have the "donot" prefix; however, you can also utilize other attributes for opt-out purposes if the data-types are compatible.

### Initial data transfer {#initial-data-transfer}

The initial data transfer may take a while depending on how many records you are ingesting from Dynamics 365. After the initial data transfer, the integration will pick up the incremental updates.

>[!WARNING]
>
>Certain actions on your part (e.g., initial ingest of records, replaying of record data, etc.) could result in a large load of records being ingested from Microsoft Dynamics 365 to your Adobe Campaign Standard (ACS) instance. To reduce the risk of performance issues which may adversely impact your ACS instance, it is recommended you stop all ACS processes (e.g., no marketing activity, no running of workflows, etc.) until after the large load of records has been ingested into ACS.
