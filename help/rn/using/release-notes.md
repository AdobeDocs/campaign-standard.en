---
title: Latest Release
description: This page details content of the latest Campaign Standard release
feature: Overview
role: User
level: Beginner
exl-id: e1f55a9b-be51-4f57-8719-fed7efc89113
---

# Latest Release{#latest-release}

![Control Panel](assets/do-not-localize/cp-icon.png) **New Control Panel release**. [Learn more](https://experienceleague.adobe.com/docs/control-panel/using/release-notes.html){target="_blank"}.



## Release 23.2 - 2023 Fall/Winter Release {#fall-23}

>[!AVAILABILITY]
>
>This release is only available for a set of organizations (Limited Availability). For more information, contact your Adobe representative.

### Improvements {#fall-23-rn-improvements}

* **Integration with Adobe Experience Manager**. While creating a personalized delivery template for transactional messages in Adobe Experience Manager you can now select and use the personalization fields defined in Campaign Standard in a drop down. [Learn more](../../integrating/using/creating-email-experience-manager.md)

* **Cookie expiration** – The default cookie expirations is now set to 6 months, to align with the French Data Protection Agency (CNIL) recommendations.

* **Profile Search Improvement** – Profile search has been optimized so that search timeout scenarios can be reduced

* **Localization** - The translations of the term "audience" when referring to a group of profiles targeted to receive a message were harmonized across all Digital Experience products for the following languages:

    * German: Zielgruppe
    * Brazilian Portuguese: público-alvo
    * Spanish: público destinatario
    
    These changes will be rolled out gradually with the next UI and documentation releases.


## Release 23.1 - 2023 Spring/Summer Release {#apr-23}

### Improvements {#e-rn-improvements}

* The Push messaging service has been modernized to improve support. (CAMP-47959)
* The SMS messaging service has been improved to provide a better stability. (CAMP-52217)
* Adobe has made many accessibility fixes to improve the application's overall ease of use. Here are a few examples of accessibility improvements:
    * The keyboard accessibility of the interface has been optimized in many screens.
    * The application has been enhanced for touchscreen users. 
    * The color of several items across the interface has been changed to improve visibility.

### Other changes {#e-rn-changes}

* The out-of-the-box **Reporting Enrichment Creation Workflow** has been added. After importing a target mapping from one instance to another, simply run the workflow to import the corresponding reporting enrichment entries. (CAMP-52452)

### Issues fixed{#e-rn-patches}

* Fixed an issue which could lead to a timeout error when displaying the **Hot click** report. (CAMP-51582)
* Fixed an issue which could prevent you from using the integration with the **Places** service. (CAMP-51923)
* Fixed an issue which could prevent the workflow scheduler from working correctly. (CAMP-52003)
* Fixed an issue which prevented the breakdown details from displaying when viewing the PDF version of a custom dynamic report with a large volume of data. (CAMP-52178)
* Fixed an issue which could display an error when accessing reports. (CAMP-52500)
* Fixed an issue which wrongly applied the **Limit MTA instances for this account** SMS connector parameter to all channels instead of applying only to SMS. (CAMP-52640)
