---
title: WHy using Campaign Standard APIs?
description: Learn more on Campaign Standard APIs and why to use them.
page-status-flag: never-activated
uuid: c7b9c171-0409-4707-9d45-3fa72aee8008
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
discoiquuid: 304e7779-42d2-430a-9704-8c599a4eb1da

internal: n
snippet: y
---

# Why using Campaign Standard APIs {#why-using-campaign-standard-apis}

Adobe Campaign Standard provides APIs which allow existing systems to integrate with the ACS platform to solve real-world problems in real-time.

Public websites like the sign-up or opt-out page need to connect to backend systems to store profile information. Backend systems like Adobe Campaign have the flexibility and power to ingest profile data into and to perform custom operations on it.

Here are some examples:

* Prospects online registration.
* Existing customer profile and marketing communication preference management.
* Event based transactional communication triggering – order confirmation, booking Itinerary, password reset, etc.
* Even cart abandonment email communication.

Sign up landing pages provide a way for customers or prospects to register their name and email address. Once ACS captures the profile information and preferences, Campaign Standard can send personalized messages based on the person’s interests. They are built with the elements below:

1. A registration form with campaign API listeners.

    ![alt text](assets/apis_uc1.png)

1. Custom actions to be taken based on checkboxes. A customer selecting “Email Special Offers” would be sent a different custom mail with a gift coupon compared to normal registration process.

    ![alt text](assets/apis_uc2.png)

1. A profile may change their details after clicking the “Update Details” link in the email. This brings the profile to the “Update your Profile and Preference Details” page. To perform the operation, the profile details (Pkey) are passed to the Campaign server and the profile is retrieved and represented. Once the profile clicks the “Update” button, the information is updated into the system (via a PATCH command).

    ![alt text](assets/apis_uc3.png)

For more on the operations you can carry out using Campaign Standard APIs, refer to the use cases presented in [this section](../../apis/using/about-apis-use-cases).
