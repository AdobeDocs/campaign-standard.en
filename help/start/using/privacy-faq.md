---
title: Privacy FAQ
description: Learn about privacy, personal data and consent management in Adobe Campaign Standard
page-status-flag: never-activated
uuid: ed9e631c-5ad1-49f1-be1e-b710bc64dc91
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: start
content-type: reference
topic-tags: discovering-the-interface
discoiquuid: 5227ca05-3856-4e54-aec6-14444d6534e3

---

# Privacy FAQ {#privacy-afaq}

## Questions on GDPR {#gdpr}

This article mainly focuses on GPDR. The configuration and usage of Access and Delete requests are common to both GDPR and CCPA. 

### What is GDPR?

Follow the links below to find general information on GDPR:

https://www.adobe.com/privacy/general-data-protection-regulation.html
https://www.adobe.com/marketing-cloud/campaign/general-data-protection-regulation.html

### Is Adobe Campaign GDPR ready?

While there are many new or enhanced requirements in GDPR, the core underlying principles of the current EU data protection requirements remain the same. Many of the data processor responsibilities in GDPR required of Adobe Campaign are already being met by the product functionality available in Adobe Campaign today. We have taken the GDPR opportunity to add additional functionality to help facilitate your GDPR readiness, where possible. Ultimately, we are here to work with our customers and do our part in helping them, the Data Controllers, achieve GDPR readiness.

### What is Adobe Campaign's suggestion for customers?

Adobe does not provide legal advice. All customers should work with their own legal counsel to ensure they are taking all steps necessary towards GDPR readiness.

**Prepare for data access and delete requests**

Identify a process to receive/respond to Data Subject requests, including appointing a privacy point of contact.

Review the various customer data stored in Adobe Campaign and determine unique identifiers (there will likely be more than one).

Determine a validation/authentication policy & process for Data Subject identity confirmation.

Make sure that the Data Subject response is easy to understand.

**Consider consent**

Inventory and update as necessary all touchpoints for data capture for GDPR (e.g.: consider language, mechanism for consent, and consent logs).

Make sure all marketing emails include the unsubscribe links.

Assess global strategy for email marketing to determine geo-specific implementations.

**Understand your data**

Review all data import and capture sources where data is flowing into Adobe Campaign and document which fields are being used for your marketing efforts.

Remove any unused data attributes from your Adobe Campaign database.

Use data available in Adobe Campaign for the intent it was captured and give your recipients better personalized experiences.

Review and update data access permissions to help ensure users of Adobe Campaign can fully leverage only the data needed to run their campaigns, but not access any data beyond this.

Ensure each user of Adobe Campaign has the appropriate access rights to perform their required his/her tasks, but does not have any other rights to perform additional tasks.

### How could Data Controllers obtain consent with minimal impact on user engagement?

In those instances where consent will be needed for certain marketing activities, consumer consent will need to be active (e.g., no silence as assent or pre-checked boxes), unbundled, and it may not be conditional upon offering the services. There may even be instances where certain consents need to be refreshed to be able to continue using data going forward. Rather than thinking of these enhanced GDPR consent requirements as a risk to the marketable universe, marketers could embrace the new consent requirements as a true indicator of brand engagement and loyalty, as well as customer satisfaction and trust.

### How could Data Controllers manage consent in Adobe Campaign going forward?

Adobe Campaign already provides capabilities to manage consent at more levels than most marketers leverage via customized data fields or through one or more Services. Marketers should check with their legal counsel for guidance on how to proceed, and then take advantage of capabilities already built-in to Adobe Campaign. For example, extending the data model in Adobe Campaign to track not only if people have opted-in, but also the timestamp of the opt-in, and some type of indicator that captures the precise scope of consent.

**What data can Data Controllers delete in Adobe Campaign in response to a consumer request by their consumers (data subjects)?**

All data associated to the Data Subject will be deleted including out of the box and custom tables. In technical terms, all data linked to the Data Subject with integrity="own" will be deleted. As the Data Controller, you have the option of customizing this by changing the integrity of links defined in the data schemas (for example, in case you have a business justification to not delete certain data).

**How are reports affected when delivery and tracking logs are deleted?**

Reports in Adobe Campaign are based on indicators computed on aggregated data from delivery and tracking logs. As a result, removing the individual logs should not impact the metrics displayed on the reports.

**Often times, Adobe Campaign is not the system of record, but is uploaded from an external data source. Do I need to be mindful of possibly re-importing data at a later date?**

As the Data Controller you will need to ensure that when you receive a deletion request, you delete all necessary data about the Data Subject from all of your systems.

**Can a Data Subject, whose data has been erased from Adobe Campaign, opt-in again later?**

It is possible for a Data Subject to opt-in again or to be added as a new recipient after his/her data has been erased from Adobe Campaign. You can use the audit trail which details when the previous deletion was performed and when the new recipient has been created.