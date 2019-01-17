---
title: About data import and export
seo-title: About data import and export
description: About data import and export
seo-description: Learn about the different ways to import and export data with Adobe Campaign.
uuid: ecc0b455-177b-4b2e-af81-86490321a9d8
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: importing-and-exporting-data
discoiquuid: 0f21ed8d-1bbd-44a5-aa21-bf4d5caa3e82
isreadyforlocalization: false
index: y
internal: n
snippet: y
---

# About data import and export{#about-data-import-and-export}

About data import and export

Depending on your business needs, you have several ways to import and export data with Adobe Campaign:

* **Packages**: packages are XML files that allow you to export and import configurations and sets of data from an Adobe Campaign instance to another one. System updates are also performed through package imports.
* **Lists**: all list screens can be configured and the displayed data exported in a separate file.
* **Workflows**: import data from files and use it to update the database or send emails. You can also select data to export in files. Workflows are the best way to automate regular updates, like profile imports.

When designing import processes, it is a best practice to use workflow templates that you can adapt to fit your needs. For more on how to set up a workflow template to import data, refer to [this use case](../../automating/using/importing-data.md#example--import-workflow-template).

Adobe Campaign also offers a simplified way to perform regular imports which consists in designing **import templates**. Import templates are specialized workflow templates available through a dedicated screen. Once designed, the user performing the import only has to upload the file to import in a simplified view.

**Related topics**:

* [Importing data with import templates](../../automating/using/importing-data-with-import-templates.md)
* [Defining import templates](../../automating/using/defining-import-templates.md)
* [Managing packages](../../automating/using/managing-packages.md)
* [Importing data](../../automating/using/importing-data.md)

