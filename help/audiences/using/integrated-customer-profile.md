---
solution: Campaign Standard
product: campaign
title: Integrated customer profile
description: "Track every customer interaction in a single view: Adobe Campaign integrated customer profile is updated throughout the customer life cycle."
audience: audiences
content-type: reference
topic-tags: managing-profiles
context-tags: marketingHistory,main
---

# Integrated customer profile{#integrated-customer-profile}

An integrated customer profile is available for each contact of your database. This marketing history combines all relevant marketing information concerning contact with a client into one single view. You can then access all digital behaviors, online and offline transactions in a central location: contact information, emails received, tracking logs, subscriptions and unsubscriptions, etc.

To access the integrated customer profile, steps are as follows:

1. From the Adobe Campaign home page, click the **[!UICONTROL Customer profiles]** card or the **Profiles** tab.

1. The list of all profiles display. Campaign Standard allows you to search a profile based on a specific field. To do this, follow these steps:

   1. Open the Search pane, then select the field on which you want to perform your search.

      Search can be performed on all out-of-the-box fields as well as custom fields that have been added to the Profile resource list configuration (see [Defining the default list configuration](./..lp/developing/using/configuring-the-screen-definition.md#defining-the-default-list-configuration).

   1. A search box or drop-down list displays below the selected option. Fill in the value that you want to search.

      >[!NOTE]
      >
      >Note searches are case-sensitive and performed on prefixes only. For example, you will not be able to look up for a profile using his last name's last letters.

   1. Press Enter to launch the search and display the results.

1. Select a contact to open its profile.

   ![](assets/mkt_hist_access.png)

You can then access the **Marketing history** of this contact.

Key information about the profile is gathered in this page, as well as the list of events.
   
Click an event in the list to open it: you can access the messages which have been sent or the services which the profile has subscribed to.

![](assets/mkt_hist_view.png)

>[!NOTE]
>
>Marketing history is also accessible using the Adobe Campaign Standard API. For more on this, refer to the [dedicated documentation](../../api/using/interacting-with-marketing-history.md) .
