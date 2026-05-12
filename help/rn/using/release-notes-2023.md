---
title: Release Notes 2023
description: This page lists all 2023 releases of Adobe Campaign Standard
feature: Overview
role: User
level: Beginner
exl-id: 5817c4d2-4788-4695-bf9a-ec04cc042190
TQID: https://experienceleague.adobe.com/YpZ3cQVh6CeVyCkOChGYLBUo1dMueoWh1AkFj3ycRwk
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
    internal-label: Accessibility
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
---
# Release Notes 2023 {#release-notes-2023}

## Release 23.2 - 2023 Fall/Winter Release {#fall-23}

>[!AVAILABILITY]
>
>This release is only available for a set of organizations (Limited Availability). For more information, contact your Adobe representative.

### Improvements {#fall-23-rn-improvements}

* **Integration with Adobe Experience Manager**. While creating a personalized delivery template for transactional messages in Adobe Experience Manager you can now select and use the personalization fields defined in Campaign Standard in a drop down. [Learn more](../../integrating/using/creating-email-experience-manager.md)

* **Cookie expiration** – The default cookie expiration is now set to 6 months, to align with the French Data Protection Agency (CNIL) recommendations.

* **Profile Search Improvement** – Profile search has been optimized so that search timeout scenarios can be reduced

* **Localization** - The translations of the term "audience" when referring to a group of profiles targeted to receive a message were harmonized across all Digital Experience products for the following languages:

    * German: Zielgruppe
    * Brazilian Portuguese: público-alvo
    * Spanish: público destinatario
    
    These changes will be rolled out gradually with the next UI and documentation releases.


### Other changes {#fall-23-rn-other-changes}

* Transactional Messaging now supports the use of multiple comma-separated affinities. [Learn more](../../sending/using/managing-typologies.md)

### Fixes {#fall-23-rn-fixes}

* Fixed a regression which could cause performance issues when using large workflows. (CAMP-53369)
* Fixed an issue which prevented the link in a workflow email alert or notification from working. (CAMP-51874)

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
