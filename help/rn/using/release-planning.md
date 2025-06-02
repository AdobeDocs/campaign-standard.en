---
title: Campaign Standard Release Planning
description: This page lists upcoming releases of Adobe Campaign Standard.
audience: rn
content-type: reference
topic-tags: campaign-standard-release-planning

feature: Overview
role: User
level: Beginner
exl-id: 1f48d4da-5622-4fab-af87-fcce0e40ade1
---
# Release Planning {#release-planning}

Adobe continuously improves its solutions by adding new capabilities, enhancements, and fixes.

All Adobe Campaign Standard instances are upgraded with every new release. No action is required to upgrade.

Upgrades are deployed in two phases. First, Stage instances are upgraded to allow you to test new capabilities and adapt your configuration if needed. Production instances are then upgraded.

All release dates are subject to change: visit this page regularly to check for updates. Environment updates happen in waves, during the indicated timeframes below. Exact dates are communicated by email to each customer. 

## Release 25.2 - 2025 Summer Release {#release-25-2-release}

Detailed information about this release are available in the [Release Notes](release-notes.md) when Stage environment updgrades start. 

<table>
 <thead>
  <tr>
   <th> Environments </th>
   <th> Dates</th>
   <!--th> General Availability </th-->
  </tr>
 </thead>
 <tbody>
  <tr>
   <td>Stage </td>
   <td>July 8 - Aug 19, 2025 </td>
   <!--td>2025 - Dates to be confirmed</td-->
  </tr>
  <tr>
   <td>Production </td>
   <td>July 15 - Aug 27, 2025 </td>
   <!--td>2025 - Dates to be confirmed</td-->
  </tr>
 </tbody>
</table>

## Questions & Answers {#questions-and-answers}

**Q: What is the impact?**

A: Changes are listed in the [Release Notes](../../rn/using/release-notes.md), including links to related documentation. Adobe also recommends to consult the [Deprecated and Removed Features page](../../rn/using/deprecated-features.md). These pages are available for the new release at the Stage environment upgrade date.

**Q: What is the validation process?**

A: As your staging instance is upgraded, Adobe recommends to validate your processes and use cases are working properly with this new version, and report any problem to [Adobe Client Care](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html).

**Q: Will there be access to the instance during the upgrade process?**

A: No. During instance upgrade the database may not be accessible during a few minutes. All processes restart automatically.

**Q: Will the messages continue to be sent?**

A: No. Messages will no be sent during a few minutes. When upgrade is completed, processes are automatically restarted.

**Q: Will the workflows continue to run and send the deliveries?**

A: No. During build upgrade, workflow server and MTA are both stopped. As a consequence, workflows will not run and deliveries are not sent during a few minutes. No action is required: workflows will start again as soon as the instance is upgraded.

**Q: Will tracking links in messages still work during the upgrade?**

A: Yes, they will work. New emails cannot be sent during the upgrade but tracking links included in already sent emails will be operational.

**Q: How do I know that the upgrade is completed?**

A: When logging on to Campaign, a release notification popup will be displayed, with the latest version.

For any other questions, contact [Adobe Client Care](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html).
