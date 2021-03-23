---
solution: Campaign Standard
product campaign
title: Ingest Adobe Experience Platform data into Campaign
description: Learn how to ingest Adobe Experience Platform data into Campaign Standard.
audience: integrating
content-type: reference

feature: Triggers
role: Data Architect
level: Intermediate
---

# Ingest Adobe Experience Platform data into Campaign {#destinations}

Fetching AEP segments to use them into ACC/ACS workflows

Profile-based - you are exporting all members of a segment, together with the desired schema fields (for example: email address, phone number, last name), as chosen in the Select attributes step of the destination activation workflow.

defines attributes to export

Platform creates a tab-delimited .txt or .csv file in the storage location that you provided


Can have at least 5 destinations per contract.

- In AEP, destinations menu
- Authenticate
- Select segments to export
- configure: create a unique name for each segment
- Scheduling: for now 24hours, will have more options
- Select attributes to export
- Review
- Go back to campaign: create workflow to import using load file. Workflow must be created manually, can use blueprints to get some help
