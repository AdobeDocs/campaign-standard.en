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

Adobe Campaign is a powerful tool for collecting and processing extremely large amounts of data, including personal information.

Privacy needs to be managed carefully, therefore we encourage all users of Adobe Campaign to:
* Work within legislation (DPA, CAN-SPAM, European Directive on Privacy and Electronic Communications, European GDPR, CCPA, PDPA, etc.)
* Make responsible and ethical use of personal information.
* Refrain from sending unsolicited email, push notifications and SMS messages ("spam"). We strongly believe in the principles of permission marketing in fostering customer lifetime value and loyalty, and we therefore strictly forbid the use of Adobe Campaign in sending unsolicited messages.
* Always have recipients agree to receive communications. To do this, keep honoring opt-out requests as quickly as possible and verify consent through a double opt-in process. For more on this, see [Managing opt-in and opt-out in Campaign](../../audiences/using/managing-opt-in-and-opt-out-in-campaign.md) and [Setting up a double opt-in process](../../channels/using/setting-up-a-double-opt-in-process.md).
* Do not import fraudulent lists and use traps to check that your client file is not being used fraudulently. For more on this, see [Using traps](../../sending/using/using-traps.md).
* When integrating Campaign with other Experience Cloud solutions such as the [Audience Destinations service](../../audiences/using/aep-about-audience-destinations-service.md), [Adobe Analytics](../../integrating/using/about-campaign-analytics-integration.md), [Audience Manager or People core service](../../integrating/using/sharing-audiences-with-audience-manager-or-people-core-service.md), or other solutions such as [Microsoft Dynamics 365](../../integrating/using/configure-microsoft-dynamics-365-for-campaign-integration.md), where audiences can be transferred from one system to another, you need to pay extra care to your data when it comes to privacy.

## Adobe Experience Cloud privacy {#experience-cloud-privacy}

Adobe Campaign is part of the Adobe Experience Cloud solutions. Therefore, the way privacy is handled in Campaign obeys the Adobe Experience Cloud general principles, such as the following:

* **What information is collected when using Adobe Experience Cloud?**

    When a company uses Adobe Experience Cloud solutions, that company chooses what information to collect and send to its Adobe Experience Cloud account. Examples of the types of information that may be collected include web browsing activity, IP addresses, location information from mobile devices, campaign success rates, items purchased or placed in shopping cart, etc.

* **How is Adobe Experience Cloud used to collect information?**

    * Adobe Experience Cloud solutions use cookies and similar technologies, such as web beacons (also known as tags or pixels), to enable you to collect information. For more on cookies and tracking capabilities with Adobe Campaign see this [section](#cookies-and-tracking-capabilities).
    * You may also use Adobe Experience Cloud technologies within your mobile apps.

* **What are the users' privacy choices about your use of Adobe's Experience Cloud solutions?**
Adobe asks you to provide your customers privacy policies describing:

    * Your privacy practices in connection with Adobe Experience Cloud
    * How users can set their preferences for the collection or use of their information in connection with Adobe Experience Cloud

    For more on the users' privacy choices, see [this page](https://www.adobe.com/privacy/opt-out.html).

For further details, refer to the [Adobe Experience Cloud privacy](https://www.adobe.com/privacy/marketing-cloud.html) page.

## Privacy management in Adobe Campaign {#privacy-management}

This [article](https://helpx.adobe.com/campaign/kb/campaign-privacy-overview.html) presents general information on what Privacy Management is and the features provided by Adobe Campaign to manage:
* Consent management, data retention and user roles
* Right to Access, Right to Delete, Right to be Forgotten

You will also find best best practices to help you with your Privacy compliance when using Adobe Campaign.

### Consent, Retention and roles {#consent}

Adobe Campaign offers important features that are essential to Privacy:

* **Consent management**: subscription functionality for preference management
* **Data retention**: data retention periods on all standard log tables, additional retention periods can be set up with workflows
* **Rights management**: data access managed by roles

For more on these features and the way to implement them in Campaign Standard, see this [page](https://helpx.adobe.com/campaign/kb/campaign-privacy-overview.html#consent).

### Privacy requests {#privacy-requests}

In addition to consent management, data retention settings, and rights management, Adobe Campaign provides additional capabilities to help you facilitate your readiness as Data Controller for certain Privacy requests.

This set of tools is here to help you with your privacy compliance for GDPR, CCPA, and PDPA:

* GDPR (General Data Protection Regulation) is the European Union’s (EU) privacy law that harmonizes and modernizes data protection requirements. GDPR applies to Adobe Campaign customers who hold data for Data Subjects residing in the EU.

* CCPA (California Consumer Privacy Act) provides California residents new rights in regards to their personal information and imposes data protection responsibilities on certain entities whom conduct business in California.

* Thailand's PDPA (Personal Data Protection Act) is the new privacy law that harmonizes and modernizes data protection requirements for Thailand. This regulation applies to Adobe Campaign customers who hold data for Data Subjects residing in this country.

In order to help you facilitate your privacy readiness, Adobe Campaign now allows you to handle **Access** and **Delete** requests.

* The **Right to Access** is the right for the Data Subject to obtain from the Data Controller confirmation as to whether or not personal data concerning them is being processed, where and for what purpose. The controller shall provide a copy of the personal data, free of charge, in an electronic format.

* Also known as **Data Erasure**, the **Right to be Forgotten** (delete request) entitles the Data Subject to have the Data Controller erase his/her personal data, cease further dissemination of the data, and potentially have third parties halt processing of the data.

Privacy **Access** and **Delete** requests are performed via the **Privacy Core Service** integration: privacy requests pushed from the Privacy Core Service to all Experience Cloud solutions are automatically handled by Campaign via a dedicated workflow.

To learn how to create **Access** and **Delete** requests and how Adobe Campaign processes them, see this [page](https://helpx.adobe.com/campaign/kb/acs-privacy.html#righttoaccess). The implementation steps are detailed on this [page](https://helpx.adobe.com/campaign/kb/acs-privacy.html#ManagingPrivacyRequests).

>[!NOTE]
>
>Tutorials on privacy management for Campaign Standard are available [here](https://docs.adobe.com/content/help/en/campaign-standard-learn/tutorials/privacy/privacy-overview.html).

### Opt-out for the Sale of Personal Information (CCPA) {#opt-out-CCPA}

CCPA (California Consumer Privacy Rights) provides California residents new rights in regards to their personal information and imposes data protection responsibilities on certain entities whom conduct business in California.

The configuration and usage of [Access and Delete requests](#privacy-requests) are common to both GDPR and CCPA. This section presents the opt-out for the sale of personal data, which is specific to CCPA.

In addition to [consent management, data retention settings, and rights management](#consent) tools provided by Adobe Campaign, you also have the possibility to track whether a consumer has opted-out for the sale of Personal Information.

The implementation steps are detailed on this [page](https://helpx.adobe.com/campaign/kb/acs-privacy.html#ccpa).

## Cookies and tracking capabilities {#cookies-and-tracking-capabilities}

Thanks to its tracking functionalities, Adobe Campaign enables you to track the behavior of your delivery recipients. To do this, Adobe Campaign uses session cookies and permanent cookies.

Regulations such as the General Data Protection Regulation (GDPR) state that companies require the agreement of website users before installing any cookies. You must inform users that your sites are equipped with web tracking tools via an authorization request.

Adobe Campaign uses two types of cookies:

* **A session cookie**, which contains the identifier of the email sent to the contact and the identifier of the message template. It is added when the contact clicks a URL included in an email sent by Adobe Campaign and enables you to track their behavior on the web.
* **A cookie shared between Adobe Experience Cloud solutions**. This enables you to identify the users who interact with the Experience Cloud solutions when they visit a website.

For more information on tracking with Adobe Campaign Standard, see [this page](../../sending/using/tracking-messages.md).
