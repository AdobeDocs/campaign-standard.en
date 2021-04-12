---
solution: Campaign Standard
product: campaign
title: About data import and export
description: Learn about the different ways to import and export data with Adobe Campaign.
audience: automating
content-type: reference
topic-tags: importing-and-exporting-data

feature: Workflows
role: Data Architect
level: Experienced
exl-id: 208e8629-c3e2-4f36-bae7-46ffc3f56a1b
---
# About data import and export{#about-data-import-and-export}

Depending on your business needs, you have several ways to import and export data with Adobe Campaign:

* **Packages**: packages are XML files that allow you to export and import configurations and sets of data from an Adobe Campaign instance to another one. System updates are also performed through package imports.
* **Lists**: all list screens can be configured and the displayed data exported in a separate file.
* **Workflows**: import data from files and use it to update the database or send emails. You can also select data to export in files. Workflows are the best way to automate regular updates, like profile imports.

    * The **[!UICONTROL Load file]** activity allows you to import data in one structured form to use this data in Adobe Campaign. The data is temporarily imported and another activity is necessary to definitively integrate it in the Adobe Campaign database. For more on how to use this activity, refer to [this section](../../automating/using/load-file.md).
    * The **[!UICONTROL Transfer file]** activity allows you to receive or send files, test whether there are files present, or list files in Adobe Campaign. You can use this activity before a **[!UICONTROL Load file]** in case you need to retrieve the file from an external source. For more on how to use this activity, refer to [this section](../../automating/using/transfer-file.md).

When designing import processes, it is a best practice to use workflow templates that you can adapt to fit your needs. For more on how to set up a workflow template to import data, refer to [this use case](../../automating/using/creating-import-workflow-templates.md).

Adobe Campaign also offers a simplified way to perform regular imports which consists in designing **import templates**. Import templates are specialized workflow templates available through a dedicated screen. Once designed, the user performing the import only has to upload the file to import in a simplified view.

**Related topics**:

* [Importing data with import templates](../../automating/using/importing-data-with-import-templates.md)
* [Defining import templates](../../automating/using/importing-data-with-import-templates.md#setting-up-import-templates)
* [Managing packages](../../automating/using/managing-packages.md)
