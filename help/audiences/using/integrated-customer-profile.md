---
title: Integrated customer profile
description: "Track every customer interaction in a single view: Adobe Campaign integrated customer profile is updated throughout the customer life cycle."
audience: audiences
content-type: reference
topic-tags: managing-profiles
context-tags: marketingHistory,main
feature: Profiles
role: User
level: Beginner
exl-id: cf3c6408-7fa0-423a-b34b-f4fee771fb47
TQID: https://experienceleague.adobe.com/a-v47cX0DxN6dzLQs-r4e2yMajLD6GHIVXXEX9Ol-lY
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
feature_v2:
  - id: b12f6872-9271-4369-85e5-86969a0b99a2
    internal-label: APIs
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
    internal-label: Customer profiles
---
# Integrated customer profile{#integrated-customer-profile}

An integrated customer profile is available for each contact of your database. This marketing history combines all relevant marketing information concerning contact with a client into one single view. You can then access all digital behaviors, online and offline transactions in a central location: contact information, emails received, tracking logs, subscriptions and unsubscriptions, etc.

To access the integrated customer profile, steps are as follows:

1. From the Adobe Campaign home page, click the **[!UICONTROL Customer profiles]** card or the **Profiles** tab to display the profiles list.

1. To search a profile based on a specific field, open the search pane, then select the field on which you want to perform your search.


   ![](assets/profile-search.png)

1. Specify the value that you want to search, then press Enter.

      >[!NOTE]
      >
      >Note that searches can be performed based on the email, first name and last name fields as well as custom fields that have been added when extending the resource.
      >
      >Searches are case-sensitive and performed on prefixes only. For example, you will not be able to look up for a profile using their last name's last letters.

1. Select a contact to open its profile.

   ![](assets/mkt_hist_access.png)

You can then access the **Marketing history** of this contact.

Key information about the profile is gathered in this page, as well as the list of events.
   
Click an event in the list to open it: you can access the messages which have been sent or the services which the profile has subscribed to.

![](assets/mkt_hist_view.png)

>[!NOTE]
>
>Marketing history is also accessible using the Adobe Campaign Standard API. For more on this, refer to the [dedicated documentation](../../api/using/interacting-with-marketing-history.md) .
