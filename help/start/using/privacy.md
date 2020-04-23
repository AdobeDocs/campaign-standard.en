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

# Privacy and consent{#privacy-and-consent}

## About privacy and consent {#about-privacy-and-consent}

Adobe Campaign is a powerful tool for collecting and processing extremely large amounts of data, including personal information. We encourage all users of Adobe Campaign to:
* Work within legislation (DPA, CAN-SPAM, European Directive on Privacy and Electronic Communications, European GDPR, CCPA, etc.)
* Make responsible and ethical use of personal information.
* Refrain from sending unsolicited email, push notifications and SMS messages ("spam"). We strongly believe in the principles of permission marketing in fostering customer lifetime value and loyalty, and we therefore strictly forbid the use of Adobe Campaign in sending unsolicited messages.
* Always have recipients agree to receive communications.
* Do not import fraudulent lists.
* Use traps to check audiences.

Audiences can come and go from an environment to another (Audience Destinations, MS Dynamics Integration, ACS-AA interaction, Audience Sharing, etc) so it needs additional care when it comes to privacy.

For more on this, refer to [Adobe Experience Cloud privacy](https://www.adobe.com/privacy/marketing-cloud.html).

## Privacy management {#privacy-management}

GDPR (General Data Protection Regulation) is the European Union’s (EU) privacy law that harmonizes and modernizes data protection requirements. GDPR applies to Adobe Campaign customers who hold data for Data Subjects residing in the EU.

CCPA (California Consumer Privacy Act) provides California residents new rights in regards to their personal information and imposes data protection responsibilities on certain entities whom conduct business in California.

In addition to consent management, data retention settings, and rights management, we provide, in our role as Data Processor, additional capabilities, to help facilitate your readiness as Data Controller for certain Privacy requests.

Adobe Campaign offers a set of tools to help you with your Privacy Compliance for GDPR and CCPA:

* This [article](https://helpx.adobe.com/campaign/kb/campaign-privacy-overview.html) presents general information on what Privacy Management is and the features we provide to manage Right to Access, Right to be Forgotten, consent, data retention and user roles. You will also find best best practices, to help you with your Privacy compliance when using our service.

* The implementation steps for Campaign Standard are detailed in this [page](https://helpx.adobe.com/campaign/kb/acs-privacy.html).

* Turorials on privacy management for Campaign Standard are available [here](https://docs.adobe.com/content/help/en/campaign-standard-learn/tutorials/privacy/privacy-overview.html).

## Cookies and tracking capabilities {#cookies-and-tracking-capabilities}

Thanks to its tracking functionalities, Adobe Campaign enables you to track the behavior of your delivery recipients. To do this, Adobe Campaign uses session cookies and permanent cookies.

European directive 2009/136/CE on "Privacy and Electronic Communications" and European General Data Protection Regulation (GDPR) state that companies require the agreement of website users before installing any cookies. You must inform users that your sites are equipped with web tracking tools via an authorization request (that comes up over the page, for example) with a checkbox to authorize the installation of cookies, or add a banner at the top of the first page they land on, etc. Pop-up windows should be avoided as they are often blocked by browsers.

Adobe Campaign uses two types of cookies:

* **A session cookie**, which contains the identifier of the email sent to the contact and the identifier of the message template. It is added when the contact clicks a URL included in an email sent by Adobe Campaign and enables you to track their behavior on the web.
* **A cookie shared between Adobe Experience Cloud solutions**. This enables you to identify the users who interact with the Experience Cloud solutions when they visit a website.

For more information on tracking with Adobe Campaign Standard, see [this page](../../sending/using/tracking-messages.md).
