---
title: Get started with processes and data management
description: Automate processes with workflows, manage data and audiences, send messages, and more.
audience: automating
content-type: reference
topic-tags: about-workflows-and-data-management
feature: Workflows
old-role: Data Architect
role: Developer
level: Beginner
exl-id: 26be942a-c252-458f-a590-eb235567ca67
TQID: https://experienceleague.adobe.com/iTJyQV-76oRhjJ4vDLKfSMpYTA27UcYt9UmVW-9YVq4
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
feature_v2:
  - id: a075b2c1-7748-4328-b7f6-343aa314616a
    internal-label: Campaigns
  - id: a4671286-a59f-47e3-b97b-90627a1977d5
    internal-label: Communication channels
  - id: a658c786-869b-4194-a780-2594d663adda
    internal-label: Data management
subfeature_v2:
  - id: b5f0aaf4-1e48-400d-95ac-6eb3078cf22f
    internal-label: Execution activities
  - id: f5293531-9312-4099-bfa3-9e67df6a8750
    internal-label: Query Editor
  - id: fcb46c0f-76e1-48bc-9dd0-fcf9d97526cf
    internal-label: Workflows
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
    internal-label: Data management
---
# Get started with processes and data management {#get-started-processes-data-management}

<table>
<tr>
<td><img src="assets/do-not-localize/icon_workflows.svg" width="60px"><p><a href="#workflow-activities">Workflow activities</a></p></td><td><img src="assets/do-not-localize/icon_activities.svg" width="60px"><p><a href="../../automating/using/workflow-created-query-with-complement.md">Use cases</a></p></td><td><img src="assets/do-not-localize/icon_filter.svg" width="60px"><p><a href="#filter-data">Filter data</a></p></td>
<td><img src="assets/do-not-localize/icon_manage.svg" width="60px"><p><a href="#import-export-data">Import/export data</a></p></td></tr>
</table>

Adobe Campaign offers a comprehensive graphical environment that allows you to design complex processes including segmentation, campaign execution, file processing, etc. For example, you can use a workflow to download a file from a server, decompress it, and then import its records into the Adobe Campaign database.

Workflows can be used in different contexts, as for example:

* Targeting to manage audiences or send messages.
* Data management (ETL) to manipulate data.
* Importing data into Campaign database.
* Technical processes such as database cleanup, recovering tracking information, etc.

>[!IMPORTANT]
>
> Adobe recommends customers not to run more than 20 active workflows executions simultaneously, and to prioritize and spread out your workflow execution over time. For more on this, refer to the best practices provided in [this page](../../automating/using/best-practices-workflows.md).

## Workflow activities {#workflow-activities}

Various activities are available to help you design your workflows.
 
[Targeting activities](../../automating/using/about-targeting-activities.md) allow you to build one or more targets by defining sets and splitting or combining these sets using intersection, union, or exclusion operations.

With [Execution activities](../../automating/using/about-execution-activities.md), coordinate your workflow and its activities, while [Channel activities](../../automating/using/about-channel-activities.md) let you combine Campaign Standard communication channels to create cross-channel workflows.

Finally, [Data management activities](../../automating/using/about-data-management-activities.md) allow you to manipulate data from your database.

Read more:

* [Building a workflow](../../automating/using/building-a-workflow.md)
* [Executing a workflow](../../automating/using/about-workflow-execution.md)
* [Workflow best practices](../../automating/using/best-practices-workflows.md)

## Filter data {#filter-data}

Leverage the **query editor** to filter data from your database and build a population to better target your recipients. The query editor is available to perform several actions in Campaign Standard: create Query type audiences, define delivery targets, or populations in workflow activities.

The query editor comes with **predefined filters and rules** for quick and easy filtering. However, you can also use **advanced expression editing** capabilities. This allows you to manually enter conditions and use functions, in order to form your own rules.

Read more:

* [Editing queries](../../automating/using/editing-queries.md)
* [Advanced expression editing](../../automating/using/advanced-expression-editing.md)
* [List of functions](../../automating/using/list-of-functions.md)

## Import/export data {#import-export-data}

Campaign Standard comes with several **data management capabilities** to import and export data.

[Workflows data management activities](../../automating/using/about-data-management-activities.md) allow you to import data, perform mass updates on fields, receive or send file, or link unidentified data to existing resources.

With [Import templates](../../automating/using/importing-data-with-import-templates.md), manage certain types of import defined by administrators through simplified import functions.

[Exporting logs](../../automating/using/exporting-logs.md) let you export log data through a simple workflow, allowing you to analyse the resultats of your marketing campaigns in your own reporting or BI tools.

Leverage [Packages](../../automating/using/managing-packages.md) to exchange resources between different campaign instances, for example, to replicate the configuration of an instance, or to transfer data from a server to another including custom resources.

Finally, [Exporting lists](../../automating/using/exporting-lists.md) allow you to export any list from Campaign Standard like, for example, the list of test profiles, the list of quarantines email addresses, etc.

Read more:

* [Importing and exporting data](../../automating/using/about-data-import-and-export.md)
* [Use case: Exporting / importing custom resources](../../automating/using/exporting-importing-custom-resources.md)

## Additional resources

* [Processes and data management tutorial videos](https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/managing-processes-and-data/creating-a-workflow.html)
* [Technical workflows](../../administration/using/technical-workflows.md)
* [Get started with Campaign Standard data model](../../developing/using/get-started-data-model.md)
