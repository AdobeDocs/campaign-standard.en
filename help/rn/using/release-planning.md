---
title: Campaign Standard Release Planning
description: This page lists upcoming releases of Adobe Campaign Standard.
page-status-flag: never-activated
uuid: 
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: rn
content-type: reference
topic-tags: campaign-standard-release-planning
discoiquuid: 

internal: n
snippet: y
---

# Release Planning {#release-planning}

Adobe continuously improves its solutions by adding new capabilities, enhancements and fixes.

All Adobe Campaign Standard instances are upgraded with every new release. No action is required to upgrade.

Upgrades are deployed in two phases. First, Stage instances are upgraded to allow our customers to test new capabilities and adapt their configuration if needed. Production instances are then subsequently upgraded.

All release dates are subject to change: we recommend you visit this page on a regular basis to check for updates.

Please subscribe to [receive release notifications](https://www.adobe.com/subscription/priority-product-update.html) to get details about latest Adobe Experience Cloud releases straight in your inbox.

## Release 20.2.1 - April Release {#release-20-2-april-release}

Environment updates happen in waves, during the indicated timeframes below. Detailed information about this release are available in the [Release Notes](../../rn/using/release-notes.md). If you have any further questions, please contact [Adobe Client Care](https://support.neolane.net/webApp/extranetLogin).

<table> 
 <thead> 
  <tr> 
   <th> Environment<br /> </th> 
   <th> Dates<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Stage<br /> </td> 
   <td> April 1 - 2, 2020<br /> </td> 
  </tr> 
  <tr> 
   <td> Production<br /> </td> 
   <td> April 6 - 9, 2020<br /> </td> 
  </tr> 
 </tbody> 
</table>



## Questions & Answers {#questions-and-answers}

**Q: What is the impact?**

A: Changes are listed in the [Release Notes](../../rn/using/release-notes.md), including links to related documentation. Adobe also recommends to consult the [Deprecated and Removed Features page](https://helpx.adobe.com/campaign/kb/acs-deprecated-and-removed-features.html). These pages are available for the new release at the Stage environment upgrade date.

**Q: What is the validation process?**

A: As your staging instance is upgraded, Adobe recommends to validate your processes and use cases are working properly with this new version, and report any problem to [Adobe Client Care](https://support.neolane.net/webApp/extranetLogin).

**Q: Will there be access to the instance during the upgrade process?**

A: No. During instance upgrade the database may not be accessible during a few minutes. All processes restart automatically.

**Q: Will the messages continue to be sent?**

A: No. Messages will no be sent during a few minutes. As soon as upgrade is completed, processes are automatically restarted.

**Q: Will the workflows continue to run and send the deliveries?**

A: No. During build upgrade, workflow server and MTA are both stopped. This means workflows will not run and deliveries are not sent during a few minutes. No action is required: workflows will start again as soon as the instance is upgraded.

**Q: Will tracking links in messages still work during the upgrade?**

A: Yes, they will work. New emails cannot be sent during the upgrade but tracking links included in already sent emails will be operational.

**Q: How do I know the upgrade is completed?**

A: When logging on to Campaign, a release notification popup will be displayed, with the latest version.

For any other questions, contact [Adobe Client Care](https://support.neolane.net/webApp/extranetLogin).