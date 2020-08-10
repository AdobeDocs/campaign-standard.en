---
title: Data update using reconciliation
description: The following example demonstrates a workflow that creates an audience of profiles directly from an imported file containing new clients.
page-status-flag: never-activated
uuid: 7884db8c-1717-4724-be15-3b0b32ccc071
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: data-management-activities
discoiquuid: cb8c43f4-9cdd-4e85-99a4-004b36b336aa
context-tags: reconciliation,main
internal: n
snippet: y
---

# Data update using reconciliation {#data-update-reconciliation}

The following example demonstrates a workflow that creates an audience of profiles directly from an imported file containing new clients. It is made up of the following activities:

![](assets/identification_example2.png)

* A [Load file](../../automating/using/load-file.md) activity, which loads and detects tshe data of the file to import. The imported file contains the following data:

  ```
  lastname;firstname;email;dateofbirth
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

* A [Reconciliation](../../automating/using/reconciliation.md) activity, which links each column of the loaded file to a profile dimension column. The file records that cannot be identified (missing data, incompatible data type, etc.) are ignored to preserve the integrity of the final audience data.

  ![](assets/identification_example1.png)

* A [Save audience](../../automating/using/save-audience.md) activity, which saves the audience of profiles.

  ![](assets/identification_example3.png)
