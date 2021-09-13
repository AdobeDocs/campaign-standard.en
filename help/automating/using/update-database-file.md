---
title: Updating the database with external data
description: This use case presents how to add or update profiles to the Adobe Campaign database with the data recovered from the file.
audience: automating
content-type: reference
topic-tags: data-management-activities
context-tags: writer,main
feature: Workflows
role: Data Architect
level: Intermediate
exl-id: 2df7fbed-b979-4706-bd56-83f712cc3070
---
# Updating the database with external data {#update-database-file}

The following example shows the configuration of an **[!UICONTROL Update data]** activity following a **[!UICONTROL Load file]** activity. The aim of this workflow is to add or update profiles to the Adobe Campaign database with the data recovered from the file.

In this example, the reconciliation key used is the **email address**. The file loaded in the [Load file](../../automating/using/load-file.md) activity is a **.txt** format file containing the following example data:

```
lastname;firstname;email;birthdate
jackman;megan;megan.jackman@testmail.com;07/08/1975
phillips;edward;phillips@testmail.com;09/03/1986
weaver;justin;justin_w@testmail.com;11/15/1990
martin;babeth;babeth_martin@testmail.net;11/25/1964
reese;richard;rreese@testmail.com;02/08/1987
cage;nathalie;cage.nathalie227@testmail.com;07/03/1989
xiuxiu;andrea;andrea.xiuxiu@testmail.com;09/12/1992
grimes;daryl;daryl_890@testmail.com;12/06/1979
tycoon;tyreese;tyreese_t@testmail.net;10/08/1971
```

The [Update data](../../automating/using/update-data.md) activity is configured as follows:

![](assets/deduplication_example2_writer1.png)

![](assets/deduplication_example2_writer2.png)
