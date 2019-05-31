---
title: Profile data ingestion from Dynamics to Campaign
seo-title: Profile data ingestion from Dynamics to Campaign
description: Profile data ingestion from Dynamics to Campaign
seo-description: 
page-status-flag: never-activated
uuid: 20eab9cd-8fe6-4bcd-8365-3435cf001531
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-microsoft-dynamics
discoiquuid: 6f811ef5-f630-4ca1-bf3d-eb1fecb4e072
index: y
internal: n
snippet: y
---

# Profile data ingestion from Dynamics to Campaign{#profile-data-ingestion-from-dynamics-to-campaign}

 As a marketer, I want to batch inject CRM data from my CRM system into ACS in order to utilize this data for marketing campaigns.

Mapping from nmsrecipient to MSD::Contacts. This is to give to Unifi for them to do data translation before sending the data to ACS.

OOTB mapping

the marketer has to work inside Unifi to do the mapping.

15minutes is the default value for sync

1) Unifi read new data from Dynamics every 15Min

2) Unifi sends data to ACS instance with a REST call (new endpoint in ACS)

Unifi is able to perform delta, just new/modify/delete info are sync every 15mn

Unifi u need to delcare data source : Dynamics and Data Stores: Campaign then a job in 7 steps that allow you to define the mapping and all the custom conf.

If we had an ACS cusR for mapping ? is this MvP ?

Define the cusR in ACS (new column in Profile resource), then map a DYnamics field to the new cusR field inside Unify
