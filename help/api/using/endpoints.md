---
title: Endpoints
description: Learn more about the APIs endpoints.
page-status-flag: never-activated
uuid: c7b9c171-0409-4707-9d45-3fa72aee8008
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
discoiquuid: 304e7779-42d2-430a-9704-8c599a4eb1da

internal: n
snippet: y
---

# Endpoints {#endpoints}

The available endpoints for Adobe Campaign REST API:

* **/profileAndServices**: interact with out of the box fields. Extended fields are not accessible with this endpoint.
* **/profileAndServicesExt**: interact with custom fields added during Profile or Services custom resource extension. For more on custom resources, refer to [this section](#custom-resources).
* **/&lt;transactionalAPI&gt;**: interact with the transactional messages API (the name of the transactional messages API endpoint depends on your instance configuration). For more on this, refer to [this section](#managing-transactional-messages).
* **/workflow/execution**: interact with workflows. For more on this, refer to [this section](#managing-workflows).
* **/privacy/privacyTool**: interact with the privacy API to allow the automatic process of privacy requests. For more on this, refer to [this section](#privacy-management).
* **/history**: retrieve the profiles' marketing history. For more on integrated customer profiles in Campaign, refer to the [Campaign documentation](https://helpx.adobe.com/campaign/standard/audiences/using/integrated-customer-profile.html).

By default, the main resources are available for the **profileAndServices** and **profileAndServicesExt** APIs:

* **/profile**: interact with profiles from Campaign database. To add profiles to a service, use the **/service** endpoint. For more on profiles in Campaign, refer to the [Campaign documentation](https://helpx.adobe.com/campaign/standard/audiences/using/about-profiles.html).
* **/service**: manage subscription services. For more on services in Campaign, refer to the [Campaign documentation](https://helpx.adobe.com/campaign/standard/audiences/using/creating-a-service.html).

>[!NOTE]
>
>All other resources that have been extended or created are available via the <b>ProfileAndServicesExt</b> API only. They must be linekd to the <b>Profile</b> resource in order to be accessible.
