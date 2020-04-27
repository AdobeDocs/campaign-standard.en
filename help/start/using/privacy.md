---
title: About privacy and recommendations in Adobe Campaign Standard
description: This section is about privacy management in Adobe Campaign Standard.
page-status-flag: never-activated
uuid: ed9e631c-5ad1-49f1-be1e-b710bc64dc91
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: start
content-type: reference
topic-tags: discovering-the-interface
discoiquuid: 5227ca05-3856-4e54-aec6-14444d6534e3

internal: n
snippet: y
---

# Privacy and Consent{#privacy-and-consent}

## Recommendations {#privacy-recommendations}

Adobe Campaign is a powerful tool for collecting and processing extremely large amounts of data, including personal information and sensitive data. This is why privacy needs to be managed carefully.

Therefore, we encourage all users of Adobe Campaign to:
* Work within legislation: [GDPR](https://ec.europa.eu/info/law/law-topic/data-protection/reform/what-does-general-data-protection-regulation-gdpr-govern_en) (European General Data Protection Regulation), [DPA](https://www.gov.uk/data-protection) (UK’s implementation of GDPR), [European Directive on privacy and electronic communications](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:02002L0058-20091219), [CAN-SPAM Act](https://www.ftc.gov/tips-advice/business-center/guidance/can-spam-act-compliance-guide-business) (US law setting the rules and requirements for commercial email), [CCPA](http://leginfo.legislature.ca.gov/faces/codes_displayText.xhtml?lawCode=CIV&division=3.&title=1.81.5.&part=4.&chapter=&article=) (California Consumer Privacy Act), [PDPA](https://secureprivacy.ai/thailand-pdpa-summary-what-businesses-need-to-know/) (Thailand Personal Data Protection Act), etc.
* Make responsible and ethical use of personal information.
* Refrain from sending unsolicited email, push notifications and SMS messages ("spam"). We strongly believe in the principles of permission marketing in fostering customer lifetime value and loyalty, and we therefore strictly forbid the use of Adobe Campaign in sending unsolicited messages.
* Always have recipients agree to receive communications. To do this, keep honoring opt-out requests as quickly as possible and verify consent through a double opt-in process. For more on this, see [Managing opt-in and opt-out in Campaign](../../audiences/using/managing-opt-in-and-opt-out-in-campaign.md) and [Setting up a double opt-in process](../../channels/using/setting-up-a-double-opt-in-process.md).
* Do not import fraudulent lists and use traps to check that your client file is not being used fraudulently. For more on this, see [Using traps](../../sending/using/using-traps.md).
* When integrating Campaign with other Experience Cloud solutions where audiences can be transferred from one system to another, such as the [Audience Destinations service](../../audiences/using/aep-about-audience-destinations-service.md), [Adobe Analytics](../../integrating/using/about-campaign-analytics-integration.md), [Audience Manager or People core service](../../integrating/using/sharing-audiences-with-audience-manager-or-people-core-service.md), or with other solutions such as [Microsoft Dynamics 365](../../integrating/using/configure-microsoft-dynamics-365-for-campaign-integration.md), you need to pay extra care to protect personal data.

## Adobe Experience Cloud privacy {#experience-cloud-privacy}

Adobe Campaign is part of the Adobe Experience Cloud solutions. The way privacy is handled in Campaign obeys the Adobe Experience Cloud general principles, such as the following:

* **What information is collected when using Adobe Experience Cloud?**

    When a company uses Adobe Experience Cloud solutions, that company chooses what information to collect and send to its Adobe Experience Cloud account. Examples of the types of information that may be collected include web browsing activity, IP addresses, location information from mobile devices, campaign success rates, items purchased or placed in shopping cart, etc.

* **How is Adobe Experience Cloud used to collect information?**

    * Adobe Experience Cloud solutions use cookies and similar technologies, such as web beacons (also known as tags or pixels), to enable you to collect information. For more on cookies and tracking capabilities with Adobe Campaign, see this [section](#cookies-and-tracking-capabilities).
    * You may also use Adobe Experience Cloud technologies within your mobile apps.

* **What are the users' privacy choices about your use of Adobe's Experience Cloud solutions?**
Adobe asks you to provide your customers privacy policies describing:

    * Your privacy practices in connection with Adobe Experience Cloud
    * How users can set their preferences for the collection or use of their information in connection with Adobe Experience Cloud

    For more on the users' privacy choices, see [this page](https://www.adobe.com/privacy/opt-out.html).

For further details, refer to the [Adobe Experience Cloud privacy](https://www.adobe.com/privacy/marketing-cloud.html) page.

## Privacy management in Adobe Campaign {#privacy-management}

First, when it comes to Privacy, it is important to define what the data at stake are:
* **Personal Data** is information that can directly or indirectly identify a living individual.
* **Sensitive Personal Data** is information related to a Data Subject’s race, political views, religious beliefs, criminal background, genetic information, health data, sexual preference, biometric information, as well as trade union membership.

It is also essential to understand who the stakeholders are regarding Privacy. The main legislations refer to the different entities that manage data as follows:
* A **Data Controller** is the authority that determines the means and purpose of collecting, using, and sharing personal data.
* A **Data Processor** is any individual or party that collects, uses, or shares personal data as directed by the Data Controller.
* A **Data Subject** is any living individual whose personal data is being collected, used or shared, and who can be identified, directly or indirectly, by reference to that personal data.

Therefore, as a company collecting and sharing personal data, you are the Data Controller, your clients are the Data Subjects and Adobe Campaign acts as a Data Processor when handling their personal data as directed by you. Note that it is your responsibility as a Data Controller to handle the relationship with the Data Subjects when managing [privacy requests](#privacy-requests) for example (via email, customer care or a web portal).

Adobe Campaign provides you with various sets of features dedicated to Privacy Management:
* Consent management, data Retention and user Roles. See [this section](#consent).
* Privacy requests (Right to Access and Right to be Forgotten). See [this section](#privacy-requests).
* Opt-out for the Sale of Personal Information (CCPA-specific). See [this section](#opt-out-CCPA).

<!--[This article](https://helpx.adobe.com/campaign/kb/campaign-privacy-overview.html) presents general information on what Privacy Management is.-->

### Consent, Retention and Roles {#consent}

Originally, Adobe Campaign offers important features that are essential to Privacy:

* **Consent management**: Through the subscription management process, you can manage your recipients' preferences and track which recipients have opted-in to which type of subscriptions.
* **Data retention**: All built-in standard log tables have pre-set retention periods, generally limiting their data storage to 6 months or less. Additional retention periods can be set up with workflows.
* **Rights management**: Adobe Campaign provides you with the ability to manage the rights assigned to the various Campaign operators via different pre-built or custom roles. This allows you to manage who within your company can access, modify or export different types of data.

For more on these features and how to manage them in Adobe Campaign, see [this page](https://helpx.adobe.com/campaign/kb/campaign-privacy-overview.html#consent).

### Privacy requests {#privacy-requests}

In addition to [consent, retention and rights management](#consent), Adobe Campaign provides additional capabilities to help you facilitate your readiness as a Data Controller for certain Privacy requests.

This set of tools is here to help you with your privacy compliance for GDPR, CCPA, and PDPA. For more on these different regulations, see [this page](https://helpx.adobe.com/campaign/kb/campaign-privacy-overview.html#whatisgdpr).

<!--* **GDPR** (General Data Protection Regulation) is the European Union’s (EU) privacy law that harmonizes and modernizes data protection requirements. GDPR applies to Adobe Campaign customers who hold data for Data Subjects residing in the EU.

* **CCPA** (California Consumer Privacy Act) provides California residents new rights in regards to their personal information and imposes data protection responsibilities on certain entities whom conduct business in California.

* **Thailand's PDPA** (Personal Data Protection Act) is the new privacy law that harmonizes and modernizes data protection requirements for Thailand. This regulation applies to Adobe Campaign customers who hold data for Data Subjects residing in this country.-->

In order to help you facilitate your privacy readiness, Adobe Campaign allows you to handle **Access** and **Delete** requests:

* The **Right to Access** is the right for the Data Subject to obtain from the Data Controller confirmation as to whether or not personal data concerning them is being processed, where and for what purpose.

* The **Right to be Forgotten** (delete request) entitles the Data Subject to have the Data Controller erase his/her personal data.

The **Access** and **Delete** requests are presented on [this page](https://helpx.adobe.com/campaign/kb/acs-privacy.html#righttoaccess).

Privacy **Access** and **Delete** requests are now only performed via the Adobe Experience Platform **Privacy Core Service** integration. Privacy requests pushed from the Privacy Core Service to all Experience Cloud solutions are automatically handled by Campaign via a dedicated workflow.

The implementation steps to create **Access** and **Delete** requests are detailed on [this page](https://helpx.adobe.com/campaign/kb/acs-privacy.html#ManagingPrivacyRequests).

>[!NOTE]
>
>Tutorials on privacy management for Campaign Standard are also available [here](https://docs.adobe.com/content/help/en/campaign-standard-learn/tutorials/privacy/privacy-overview.html).

### Opt-out for the Sale of Personal Information (CCPA) {#opt-out-CCPA}

<!--The configuration and usage of [Access and Delete requests](#privacy-requests) are common to both GDPR and CCPA, however the opt-out for the sale of personal information is specific to CCPA.-->

The opt-out for the sale of personal information enables you to track whether a consumer has opted-out for the sale of Personal Data.

>[!NOTE]
>
>This feature is specific to CCPA.

The full description and the implementation steps are detailed on this [page](https://helpx.adobe.com/campaign/kb/acs-privacy.html#ccpa).

For more on GDPR and CCPA, see [this page](https://helpx.adobe.com/campaign/kb/campaign-privacy-overview.html#whatisgdpr).

## Cookies and tracking capabilities {#cookies-and-tracking-capabilities}

Thanks to its tracking functionalities, Adobe Campaign enables you to track the behavior of your delivery recipients using session cookies and permanent cookies.

Regulations such as the General Data Protection Regulation (GDPR) state that companies require the agreement of website users before installing any cookies. You must inform users that your sites are equipped with web tracking tools via an authorization request.

<!--Adobe Campaign uses two types of cookies:

* **A session cookie**, which contains the identifier of the email sent to the contact and the identifier of the message template. It is added when the contact clicks a URL included in an email sent by Adobe Campaign and enables you to track their behavior on the web.
* **A cookie shared between Adobe Experience Cloud solutions**. This enables you to identify the users who interact with the Experience Cloud solutions when they visit a website.-->

For more information on tracking with Adobe Campaign Standard, see [this page](../../sending/using/tracking-messages.md).
