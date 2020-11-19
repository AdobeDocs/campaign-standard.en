---
title: User process and personas
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

# User process and personas {#privacy-personas}

Adobe Campaign includes the following capabilities, to help with your GDPR readiness: Right to Access, Right to Delete, Consent management, Data retention and Rights management.

In this section, we will introduce those capabilities and present to you an example of a GDPR use case scenario to help you understand the general flow as well as the different personas involved: Data subject, Data Controller and Data Processor.

## Main capabilities

Here are five main capabilities offered by Adobe Campaign for GDPR:

![](assets/privacy-xxx.png)

Right to Access: allows the Data Subject to receive a copy of his/her personal data captured by Data Controllers, potentially including data stored in Adobe Campaign.

Right to Delete: entitles the Data Subject to have his/her personal data captured by Data Controllers erased, potentially including data stored in Adobe Campaign.

Consent management: allows the Data Subject to agree (or not) to the processing of his personal data.

Data retention: each table in Adobe Campaign is set with a specific retention period thus limiting data storage.

Rights management: Adobe Campaign provides access rights to allow you to manage which user can access different types of data.

Example of a use case scenario

Here is an example of a high-level GDPR customer experience use case:

![](assets/privacy-xxx.png)

In this example, we are considering an airline company as Adobe Campaign customer. This company is the Data Controller and all the consumers of the airline company are Data Subjects. Laura in this particular case is a consumer of the airline company.

Here are the different personas used in this example:

* Laura is the Data subject. She’s the recipient who receives messages from the airline company. Laura may be a frequent flyer, but may decide at some point that she doesn’t want any personalized advertising or marketing messages from the airline company. She will ask the airline company (based on their process) to delete her frequent flier number.

* Ann is the Data Controller. She receives Laura’s request, retrieves useful IDs requested to identify the Data Subject and submits the request in Adobe Campaign.

* Then Adobe is the Data Processor.

Here is the general flow for this use case:

1. The Data Subject sends a GDPR request to the Data Controller, via email, customer care or a web portal.

1. The Data Controller pushes the GDPR request to Campaign via the interface or using an API.

1. Once Campaign receives the information, it takes action on the GDPR request and sends a response or acknowledgement to the Data Controller.

1. The Data Controller then reviews the information and sends it back to the Data Subject.